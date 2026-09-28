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

- **Setup del backend**: [`docs/onboarding/setup.md`](./docs/onboarding/setup.md)
- **Cómo contribuir**: [`docs/CONTRIBUTING.md`](./docs/CONTRIBUTING.md)
- **Convenciones**: [`docs/conventions/`](./docs/conventions/README.md)
- **Arquitectura**: [`docs/architecture/`](./docs/architecture/overview.md)

## Estado actual

- Backend: activo. La integración diaria ocurre en `develop`; `main` es la rama
  estable de producción.
- Cliente móvil: pausado hasta nuevo aviso.
- El backend histórico en AdonisJS fue eliminado; ahora todo está en NestJS.

## Licencia

`UNLICENSED` — proyecto privado.