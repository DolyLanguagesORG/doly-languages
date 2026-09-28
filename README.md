# Dolynglish

Aplicación móvil de práctica de inglés que genera ejercicios de lectura con
IA y evalúa las respuestas del usuario en tiempo real.

## Estructura del repositorio

| Carpeta             | Contenido                                                  | Estado              |
| ------------------- | ---------------------------------------------------------- | ------------------- |
| [`backend/`](./backend/README.md)         | API REST NestJS 11 + Drizzle ORM + PostgreSQL 15   | Activo              |
| [`mobile/`](./mobile/README.md)           | Cliente Expo SDK 54 / React Native                 | Deshabilitado       |
| [`infrastructure/`](./infrastructure/README.md) | Docker Compose (Postgres + backend en prod) | Activo              |
| [`docs/`](./docs/README.md)               | Convenciones, arquitectura, onboarding             | Activo              |
| [`.github/`](./.github)                  | CI workflows, plantillas, CODEOWNERS              | Activo              |

## Empezar

- **Cronograma del proyecto**: [`docs/cronograma.md`](./docs/cronograma.md) — 5 sprints,
  33 tareas, del 05/Oct/2026 al 10/Dic/2026
- **Setup del backend**: [`docs/onboarding/setup.md`](./docs/onboarding/setup.md)
- **Cómo contribuir**: [`docs/CONTRIBUTING.md`](./docs/CONTRIBUTING.md)
- **Convenciones**: [`docs/conventions/`](./docs/conventions/README.md)
- **Arquitectura**: [`docs/architecture/`](./docs/architecture/overview.md)

## Estado actual

- Release vigente: `v0.1.0`. La entrega de cierre del proyecto está prevista para
  `v1.0.0`.
- Backend: activo. La integración diaria ocurre en `develop`; `main` es la rama
  estable de producción.
- Cliente móvil: pausado hasta nuevo aviso.
- El backend histórico en AdonisJS fue eliminado; ahora todo está en NestJS.

## Próximos pasos

| Qué | Dónde |
| --- | --- |
| Plan del proyecto | [`docs/cronograma.md`](./docs/cronograma.md) |
| Tablero Kanban y Timeline | [Project de GitHub](https://github.com/users/XxjesusalbertoxX/projects/3) |
| Tareas (33 entregables) | [Issues del repositorio](https://github.com/DolyLanguagesORG/doly-languages/issues) |
| Cierre de cada sprint | [Milestones](https://github.com/DolyLanguagesORG/doly-languages/milestones) |
| Reporte diario | [Hilo de standup](https://github.com/DolyLanguagesORG/doly-languages/discussions/39) |

## Licencia

`UNLICENSED`. El repositorio es público, pero no se ha definido una licencia
abierta, así que todos los derechos quedan reservados.