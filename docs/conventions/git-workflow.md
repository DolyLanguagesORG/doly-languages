# Git workflow

Este documento define cómo se mueve el código entre ramas. Es la fuente de
verdad para PRs, merges y hotfixes.

## Diagrama de flujo

```
                     ┌──────────────────┐
                     │   feat/issue-12-* │
                     │   fix/issue-45-*  │
                     │   chore/*         │
                     │   docs/*          │
                     └────────┬─────────┘
                              │  PR + checks en verde
                              ▼
                     ┌──────────────────┐
                     │     develop      │  ← integración diaria
                     └────────┬─────────┘
                              │  PR + 1 aprobación + checks
                              ▼
                     ┌──────────────────┐
                     │      main        │  ← producción / release
                     └──────────────────┘

                     ┌──────────────────┐
                     │   hotfix/*       │  ← sale de main, vuelve a develop
                     └──────────────────┘
```

## Convenciones de nombres

El prefijo de la rama coincide con el **tipo de commit** que llevará
(ver [commits.md](./commits.md)), para evitar confusiones alinear
`feat/issue-12-login` con `feat(auth): ...`.

- `feat/issue-<n>-<kebab>` — nuevas funcionalidades
- `fix/issue-<n>-<kebab>` — correcciones
- `chore/<kebab>` — refactors, limpieza, tooling
- `docs/<kebab>` — solo documentación
- `hotfix/<kebab>` — corrección urgente sobre producción

El número de issue es obligatorio en `feat/` y `fix/` para poder trazar la
tarea en el tablero de Projects.

Ejemplos:

- `feat/issue-12-login-page`
- `fix/issue-45-header-bug`
- `chore/remove-archived-backend`
- `docs/git-workflow`

Máximo 50 caracteres en total.

## Reglas por rama

### `develop` (integración diaria)

- Recibe PRs de `feat/*`, `fix/*`, `chore/*`, `docs/*`.
- Requiere **status checks** verdes antes de mergear (CI de GitHub Actions).
- Requiere **1 aprobación** de un CODEOWNER.
- **Prohibido el push directo**: siempre por PR.
- Solo **squash-merge**, para mantener historia lineal.
- No se permiten force-pushes ni deleciones.

### `main` (producción / release)

- Recibe PRs **únicamente** desde `develop` (excepto hotfixes).
- Requiere status checks verdes **más** 1 aprobación de CODEOWNER.
- **Prohibido el push directo**: siempre por PR.
- Solo **squash-merge**.
- No se permiten force-pushes ni deleciones.

`main` permanece estable entre releases. Durante el desarrollo activo solo
recibe merge en los hitos acordados.

## Procedimiento de hotfix

Para un fix urgente en producción:

1. Crea rama desde `main`:
   ```bash
   git checkout main
   git checkout -b hotfix/<nombre-descriptivo>
   ```
2. Commitea el fix mínimo (ver [commits.md](./commits.md)).
3. Abre PR con título `fix(scope): <descripción>` directo contra `main`.
4. Después de mergearlo en `main`, **cherry-pick** el commit a `develop`:
   ```bash
   git checkout develop
   git cherry-pick <sha-del-hotfix>
   git push origin develop
   ```

## Cómo trabajar en el día a día

```bash
# 1. Traer lo último de develop
git checkout develop
git pull

# 2. Crear la rama de la tarea
git checkout -b feat/issue-12-login-page

# 3. Verificar antes de commitear
cd backend && npm run verify

# 4. Commitear (husky + commitlint validan el mensaje)
git add -A
git commit -m "feat(auth): register endpoint with argon2 hashing"

# 5. Publicar la rama y abrir el PR hacia develop
git push -u origin feat/issue-12-login-page
gh pr create --base develop --title "feat(auth): register endpoint" --body "Closes #12"
```

## Política de merges

- **Solo squash-merge**, en `develop` y en `main`, para mantener historia lineal.
- Commits locales en la rama de trabajo pueden ser múltiples; el squash
  los colapsa en uno al mergear.
- Títulos de PR siguen Conventional Commits y los valida el check
  `pr-title` de CI (ver [commits.md](./commits.md)).

## Versionado

El título del commit de squash determina el bump automático de versión
(ver [versioning.md](./versioning.md)):

| Prefijo del título del PR | Bump  | Ejemplo           |
| ------------------------- | ----- | ----------------- |
| `fix:` / `refactor:` / …  | patch | `v0.1.0` → `v0.1.1` |
| `feat:`                   | minor | `v0.1.0` → `v0.2.0` |
| `!` (breaking)            | major | `v0.1.0` → `v1.0.0` |

## Pull requests

Usa la plantilla en [`.github/PULL_REQUEST_TEMPLATE.md`](../../.github/PULL_REQUEST_TEMPLATE.md).
Cada PR debe tener su checklist marcado antes de pedir review:
`npm run verify` pasa, tests añadidos, envelope respetado, etc.

Los archivos que considero requeridos por un PR:

- `.github/workflows/ci-backend.yml` — `unit-and-static`, `e2e`, `build`
- `.github/workflows/openapi-guard.yml` — `openapi-guard`
- `.github/workflows/docs-link-check.yml` — `link-check`
- `.github/workflows/pr-title.yml` — `pr-title`
