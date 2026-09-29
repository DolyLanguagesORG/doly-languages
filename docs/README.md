# Dolynglish — Documentación

Dolynglish es una aplicación móvil de práctica de inglés que genera ejercicios
de lectura con IA y evalúa las respuestas del usuario. Este repositorio
contiene el backend activo (NestJS), el cliente móvil (Expo / React Native,
actualmente deshabilitado) y la infraestructura dockerizada.

## Estructura del repositorio

| Carpeta             | Contenido                                                    | Estado              |
| ------------------- | ------------------------------------------------------------ | ------------------- |
| `backend/`          | API REST en NestJS 11 + Drizzle ORM + PostgreSQL             | Activo              |
| `mobile/`           | Cliente Expo SDK 54 / React Native                           | Deshabilitado       |
| `infrastructure/`   | Docker Compose para Postgres + backend en producción         | Activo              |
| `docs/`             | Esta documentación                                           | Activo              |
| `.github/`          | Workflows de CI, plantillas de PR, CODEOWNERS                | Activo              |

## Índice de la documentación

- **Cronograma**: [cronograma.md](./cronograma.md) — plan de 5 sprints y 33
  tareas, del 05/Oct/2026 al 10/Dic/2026.
- **Entrada rápida**: [CONTRIBUTING.md](./CONTRIBUTING.md) — clonar,
  instalar, contribuir, abrir un PR.
- **Convenciones** (cómo escribir código, commits, PRs): [conventions/](./conventions/README.md)
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