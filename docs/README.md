# Dolynglish — Documentación

Dolynglish es una aplicación web de práctica de inglés que genera ejercicios
de lectura con IA y evalúa las respuestas del usuario. Este repositorio
contiene el backend activo (NestJS), la infraestructura dockerizada y el
cliente Expo heredado (`mobile/`, deshabilitado y fuera del alcance de
`v1.0.0`; el diseño de `v1.0.0` es web responsivo, ver issue #35).

## Estructura del repositorio

| Carpeta             | Contenido                                                    | Estado              |
| ------------------- | ------------------------------------------------------------ | ------------------- |
| `backend/`          | API REST en NestJS 11 + Drizzle ORM + PostgreSQL             | Activo              |
| `mobile/`           | Cliente Expo SDK 54 / React Native (heredado)              | Deshabilitado       |
| `infrastructure/`   | Docker Compose para Postgres + backend en producción         | Activo              |
| `docs/`             | Esta documentación                                           | Activo              |
| `.github/`          | Workflows de CI, plantillas de PR, CODEOWNERS                | Activo              |

## Índice de la documentación

**Empieza por aquí:**

- **[Cómo hacer un Pull Request](./COMO-HACER-UN-PR.md)** — flujo paso a paso:
  ramas, checks, `Closes #N`, troubleshooting. **Léelo si vas a abrir tu
  primer PR.**
- **[Flujo de trabajo del repositorio](./FLUJO-DE-TRABAJO.md)** — el panorama
  completo: ramas, tablero, CODEOWNERS, dependencias, releases, y qué reglas
  **sí** te bloquean y cuáles no.
- [Cronograma](./cronograma.md) — plan de 5 sprints y 33 tareas, del
  05/Oct/2026 al 10/Dic/2026.
- [Entrada rápida](./CONTRIBUTING.md) — clonar, instalar, contribuir.

**Detalle:**

- **Convenciones** (cómo escribir código, commits, PRs):
  [conventions/](./conventions/README.md)
- **Arquitectura**: [architecture/](./architecture/README.md)
- **Onboarding**: [onboarding/](./onboarding/README.md)

## Documentación adicional

- `backend/README.md` — quick start, scripts, arquitectura del backend.
- `backend/TYPESCRIPT_STANDARDS.md` — reglas no negociables de TypeScript.
- `backend/.env.example` — variables de entorno requeridas.
- `infrastructure/README.md` — servicios dockerizados.

## Estado del repositorio

- Backend: activo y desplegado.
- Mobile: pausado hasta nuevo aviso.
- Release vigente: `v0.1.0`; la entrega de cierre del proyecto está prevista
  para `v1.0.0`.
- La planificación vive en GitHub: [Project con Kanban y Timeline](https://github.com/orgs/DolyLanguagesORG/projects/1),
  [issues](https://github.com/DolyLanguagesORG/doly-languages/issues),
  [milestones](https://github.com/DolyLanguagesORG/doly-languages/milestones) y el
  [hilo de standup diario](https://github.com/DolyLanguagesORG/doly-languages/discussions/39).

## Licencia

`UNLICENSED`. El repositorio es público, pero no se ha definido una licencia
abierta, así que todos los derechos quedan reservados.