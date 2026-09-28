# Cronograma del MVP — DolyNation

Este documento es la fuente de verdad escrita del cronograma. La vista
interactiva (Kanban y Timeline) vive en el [Project de GitHub](
https://github.com/users/XxjesusalbertoxX/projects/3), y el detalle de cada
tarea en los issues del repositorio.

| Dato | Valor |
| --- | --- |
| Inicio del proyecto | 05/Oct/2026 |
| Entrega final | 10/Dic/2026 |
| Límite diario por tarea | 23:59 CST |
| Sprints | 5 |
| Tareas | 33 |
| Release actual | `v0.1.0` |
| Release de cierre | `v1.0.0` |

## Dónde ver el avance

- **Kanban y Timeline**: [Project — DolyNation Roadmap MVP (2026)](https://github.com/users/XxjesusalbertoxX/projects/3)
  - Vista *Tablero Kanban*: agrupada por `Status` (Todo / In Progress / In Review / Done)
  - Vista *Timeline del MVP*: eje de tiempo con `Start Date` → `Target Date`
  - Vista *Todos los entregables*: tabla con las 33 tareas
- **Issues**: los 33 entregables, uno por tarea
- **Milestones**: un milestone por sprint, con su fecha de cierre
- **Standup diario**: [hilo de registro de avances](https://github.com/DolyLanguagesORG/doly-languages/discussions/39)

## Cómo leer los números

En este documento las tareas se numeran del **1 al 33**, como en el
cronograma original. En GitHub los issues van del **6 al 38**, porque los
cincos pull request de configuración de la infraestructura consumieron los
números 1 a 5 antes de que se creara el backlog.

La correspondencia es fija y lineal:

```
número de GitHub = número de cronograma + 5
```

Cada issue indica su número de cronograma en la primera línea del cuerpo,
y este documento indica el número de GitHub. La tabla de abajo es la
referencia para pasar de uno a otro.

---

## Sprint 1 — Infraestructura, Autenticación y Perfil

**Periodo:** 05/Oct – 18/Oct/2026  
**Objetivo:** Configuración inicial del repositorio con reglas CI/CD, modelo de base de datos y módulo funcional de autenticación y perfil.  
**Cierre (milestone):** [Sprint 1: Infraestructura, Autenticación y Perfil](https://github.com/DolyLanguagesORG/doly-languages/milestone/1)  
**Tareas:** 9

| # | Issue | Tarea | Responsable | Inicio | Entrega |
| --: | :---: | --- | --- | :---: | :---: |
| 1 | [#6](https://github.com/DolyLanguagesORG/doly-languages/issues/6) | chore(repo): configurar main/develop, branch protection, plantillas y CI | Jesús (SM) | 05 Oct 2026 | 06 Oct 2026 |
| 2 | [#7](https://github.com/DolyLanguagesORG/doly-languages/issues/7) | feat(setup): arquitectura NestJS y conexión a base de datos con entidad User | Azael | 05 Oct 2026 | 08 Oct 2026 |
| 3 | [#8](https://github.com/DolyLanguagesORG/doly-languages/issues/8) | feat(setup): proyecto Next.js con Tailwind, layout base y temas | Juan | 05 Oct 2026 | 07 Oct 2026 |
| 4 | [#9](https://github.com/DolyLanguagesORG/doly-languages/issues/9) | feat(auth): hashing con Argon2 y estrategia JWT en NestJS | Azael | 09 Oct 2026 | 12 Oct 2026 |
| 5 | [#10](https://github.com/DolyLanguagesORG/doly-languages/issues/10) | feat(auth): DTOs de validación y endpoints /auth/register y /auth/login | Elías | 09 Oct 2026 | 12 Oct 2026 |
| 6 | [#11](https://github.com/DolyLanguagesORG/doly-languages/issues/11) | feat(auth): vistas de Login y Registro en Next.js | Juan | 08 Oct 2026 | 12 Oct 2026 |
| 7 | [#12](https://github.com/DolyLanguagesORG/doly-languages/issues/12) | feat(user): endpoints de consulta y actualización de /user/profile | Elías | 13 Oct 2026 | 15 Oct 2026 |
| 8 | [#13](https://github.com/DolyLanguagesORG/doly-languages/issues/13) | feat(user): vista de perfil e integración con el estado de sesión | Juan | 13 Oct 2026 | 16 Oct 2026 |
| 9 | [#14](https://github.com/DolyLanguagesORG/doly-languages/issues/14) | test(auth): pruebas de integración del Sprint 1 y revisión de PRs | Jesús (SM) | 16 Oct 2026 | 18 Oct 2026 |

---

## Sprint 2 — Configuración de Estudio y Lecturas con IA

**Periodo:** 19/Oct – 01/Nov/2026  
**Objetivo:** Conectar el backend con la API de IA (OpenAI/Gemini) para generar lecturas según la configuración del estudiante.  
**Cierre (milestone):** [Sprint 2: Configuración de Estudio y Lecturas con IA](https://github.com/DolyLanguagesORG/doly-languages/milestone/2)  
**Tareas:** 7

| # | Issue | Tarea | Responsable | Inicio | Entrega |
| --: | :---: | --- | --- | :---: | :---: |
| 10 | [#15](https://github.com/DolyLanguagesORG/doly-languages/issues/15) | feat(ai): módulo de servicios para OpenAI/Gemini y arquitectura de prompts | Azael | 19 Oct 2026 | 23 Oct 2026 |
| 11 | [#16](https://github.com/DolyLanguagesORG/doly-languages/issues/16) | feat(settings): endpoints de /settings/categories y /settings/languages | Elías | 19 Oct 2026 | 22 Oct 2026 |
| 12 | [#17](https://github.com/DolyLanguagesORG/doly-languages/issues/17) | feat(settings): formulario de parámetros de estudio en Next.js | Juan | 19 Oct 2026 | 23 Oct 2026 |
| 13 | [#18](https://github.com/DolyLanguagesORG/doly-languages/issues/18) | feat(cache): caché de lecturas para parámetros equivalentes (RNF-05) | Jesús (SM) | 22 Oct 2026 | 26 Oct 2026 |
| 14 | [#19](https://github.com/DolyLanguagesORG/doly-languages/issues/19) | feat(reader): visor inmersivo de lectura | Juan | 24 Oct 2026 | 28 Oct 2026 |
| 15 | [#20](https://github.com/DolyLanguagesORG/doly-languages/issues/20) | feat(content): endpoint /content/generate | Azael + Elías | 24 Oct 2026 | 28 Oct 2026 |
| 16 | [#21](https://github.com/DolyLanguagesORG/doly-languages/issues/21) | feat(study): flujo completo parámetros → IA → visor | Jesús (SM) + Juan | 29 Oct 2026 | 01 Nov 2026 |

---

## Sprint 3 — Vocabulario Contextual y Evaluación por PNL

**Periodo:** 02/Nov – 15/Nov/2026  
**Objetivo:** Implementar la interacción flotante de diccionario por palabra/oración (con audio) y la calificación automática de resúmenes redactados.  
**Cierre (milestone):** [Sprint 3: Vocabulario Contextual y Evaluación por PNL](https://github.com/DolyLanguagesORG/doly-languages/milestone/3)  
**Tareas:** 7

| # | Issue | Tarea | Responsable | Inicio | Entrega |
| --: | :---: | --- | --- | :---: | :---: |
| 17 | [#22](https://github.com/DolyLanguagesORG/doly-languages/issues/22) | feat(reader): captura de selección de texto en el visor | Juan | 02 Nov 2026 | 05 Nov 2026 |
| 18 | [#23](https://github.com/DolyLanguagesORG/doly-languages/issues/23) | feat(dictionary): endpoint de consulta contextual de vocabulario a la IA | Azael | 02 Nov 2026 | 06 Nov 2026 |
| 19 | [#24](https://github.com/DolyLanguagesORG/doly-languages/issues/24) | feat(dictionary): pop-up de diccionario contextual con TTS | Juan | 06 Nov 2026 | 09 Nov 2026 |
| 20 | [#25](https://github.com/DolyLanguagesORG/doly-languages/issues/25) | feat(summary): área de redacción libre de resumen y envío de evaluación | Juan + Elías | 07 Nov 2026 | 10 Nov 2026 |
| 21 | [#26](https://github.com/DolyLanguagesORG/doly-languages/issues/26) | feat(nlp): servicio de evaluación de resúmenes por PNL con feedback | Jesús (SM) + Azael | 06 Nov 2026 | 11 Nov 2026 |
| 22 | [#27](https://github.com/DolyLanguagesORG/doly-languages/issues/27) | feat(evaluation): endpoint /evaluation/submit con persistencia del resultado | Elías | 10 Nov 2026 | 13 Nov 2026 |
| 23 | [#28](https://github.com/DolyLanguagesORG/doly-languages/issues/28) | test(sprint3): pruebas de vocabulario y evaluación de resúmenes por PNL | Jesús (SM) | 13 Nov 2026 | 15 Nov 2026 |

---

## Sprint 4 — Historial, Rachas y Panel Administrativo

**Periodo:** 16/Nov – 29/Nov/2026  
**Objetivo:** Desarrollar el módulo de trazabilidad (historial y progreso), contador de racha diaria y el panel básico de administración.  
**Cierre (milestone):** [Sprint 4: Historial, Rachas y Panel Administrativo](https://github.com/DolyLanguagesORG/doly-languages/milestone/4)  
**Tareas:** 6

| # | Issue | Tarea | Responsable | Inicio | Entrega |
| --: | :---: | --- | --- | :---: | :---: |
| 24 | [#29](https://github.com/DolyLanguagesORG/doly-languages/issues/29) | feat(streak): cálculo de racha diaria y asignación de puntos | Azael | 16 Nov 2026 | 19 Nov 2026 |
| 25 | [#30](https://github.com/DolyLanguagesORG/doly-languages/issues/30) | feat(history): endpoints de consulta de historial de actividades | Elías | 16 Nov 2026 | 20 Nov 2026 |
| 26 | [#31](https://github.com/DolyLanguagesORG/doly-languages/issues/31) | feat(dashboard): dashboard de usuario con métricas, racha y gráfica de puntos | Juan | 19 Nov 2026 | 24 Nov 2026 |
| 27 | [#32](https://github.com/DolyLanguagesORG/doly-languages/issues/32) | feat(admin): endpoints /admin/categories y supervisión de usuarios | Elías | 21 Nov 2026 | 25 Nov 2026 |
| 28 | [#33](https://github.com/DolyLanguagesORG/doly-languages/issues/33) | feat(admin): vista del panel administrativo básico | Juan + Jesús (SM) | 24 Nov 2026 | 27 Nov 2026 |
| 29 | [#34](https://github.com/DolyLanguagesORG/doly-languages/issues/34) | refactor(review): revisión general de código y limpieza de endpoints | Jesús (SM) | 27 Nov 2026 | 29 Nov 2026 |

---

## Sprint 5 — Pruebas, Tagging v1.0.0 y Cierre del MVP

**Periodo:** 30/Nov – 10/Dic/2026  
**Objetivo:** Congelamiento de código, ejecución de pruebas E2E, tagging de versión estable v1.0.0 y entrega académica del anteproyecto.  
**Cierre (milestone):** [Sprint 5: Pruebas, Tagging v1.0.0 y Cierre del MVP](https://github.com/DolyLanguagesORG/doly-languages/milestone/5)  
**Tareas:** 4

| # | Issue | Tarea | Responsable | Inicio | Entrega |
| --: | :---: | --- | --- | :---: | :---: |
| 30 | [#35](https://github.com/DolyLanguagesORG/doly-languages/issues/35) | test(usability): pruebas de usabilidad y diseño responsivo | Juan | 30 Nov 2026 | 03 Dic 2026 |
| 31 | [#36](https://github.com/DolyLanguagesORG/doly-languages/issues/36) | test(hardening): rendimiento, modo degradado de la IA y validación de seguridad | Azael + Elías | 30 Nov 2026 | 04 Dic 2026 |
| 32 | [#37](https://github.com/DolyLanguagesORG/doly-languages/issues/37) | chore(release): PR final develop→main, tag v1.0.0 y verificación de CI/CD | Jesús (SM) | 04 Dic 2026 | 06 Dic 2026 |
| 33 | [#38](https://github.com/DolyLanguagesORG/doly-languages/issues/38) | docs(release): documentación final, capturas del sistema y presentación | Todo el equipo | 06 Dic 2026 | 10 Dic 2026 |

---

## Correspondencia completa

| Cronograma | GitHub | Tarea | Sprint |
| --: | :---: | --- | --: |
| 1 | [#6](https://github.com/DolyLanguagesORG/doly-languages/issues/6) | chore(repo): configurar main/develop, branch protection, plantillas y CI | 1 |
| 2 | [#7](https://github.com/DolyLanguagesORG/doly-languages/issues/7) | feat(setup): arquitectura NestJS y conexión a base de datos con entidad User | 1 |
| 3 | [#8](https://github.com/DolyLanguagesORG/doly-languages/issues/8) | feat(setup): proyecto Next.js con Tailwind, layout base y temas | 1 |
| 4 | [#9](https://github.com/DolyLanguagesORG/doly-languages/issues/9) | feat(auth): hashing con Argon2 y estrategia JWT en NestJS | 1 |
| 5 | [#10](https://github.com/DolyLanguagesORG/doly-languages/issues/10) | feat(auth): DTOs de validación y endpoints /auth/register y /auth/login | 1 |
| 6 | [#11](https://github.com/DolyLanguagesORG/doly-languages/issues/11) | feat(auth): vistas de Login y Registro en Next.js | 1 |
| 7 | [#12](https://github.com/DolyLanguagesORG/doly-languages/issues/12) | feat(user): endpoints de consulta y actualización de /user/profile | 1 |
| 8 | [#13](https://github.com/DolyLanguagesORG/doly-languages/issues/13) | feat(user): vista de perfil e integración con el estado de sesión | 1 |
| 9 | [#14](https://github.com/DolyLanguagesORG/doly-languages/issues/14) | test(auth): pruebas de integración del Sprint 1 y revisión de PRs | 1 |
| 10 | [#15](https://github.com/DolyLanguagesORG/doly-languages/issues/15) | feat(ai): módulo de servicios para OpenAI/Gemini y arquitectura de prompts | 2 |
| 11 | [#16](https://github.com/DolyLanguagesORG/doly-languages/issues/16) | feat(settings): endpoints de /settings/categories y /settings/languages | 2 |
| 12 | [#17](https://github.com/DolyLanguagesORG/doly-languages/issues/17) | feat(settings): formulario de parámetros de estudio en Next.js | 2 |
| 13 | [#18](https://github.com/DolyLanguagesORG/doly-languages/issues/18) | feat(cache): caché de lecturas para parámetros equivalentes (RNF-05) | 2 |
| 14 | [#19](https://github.com/DolyLanguagesORG/doly-languages/issues/19) | feat(reader): visor inmersivo de lectura | 2 |
| 15 | [#20](https://github.com/DolyLanguagesORG/doly-languages/issues/20) | feat(content): endpoint /content/generate | 2 |
| 16 | [#21](https://github.com/DolyLanguagesORG/doly-languages/issues/21) | feat(study): flujo completo parámetros → IA → visor | 2 |
| 17 | [#22](https://github.com/DolyLanguagesORG/doly-languages/issues/22) | feat(reader): captura de selección de texto en el visor | 3 |
| 18 | [#23](https://github.com/DolyLanguagesORG/doly-languages/issues/23) | feat(dictionary): endpoint de consulta contextual de vocabulario a la IA | 3 |
| 19 | [#24](https://github.com/DolyLanguagesORG/doly-languages/issues/24) | feat(dictionary): pop-up de diccionario contextual con TTS | 3 |
| 20 | [#25](https://github.com/DolyLanguagesORG/doly-languages/issues/25) | feat(summary): área de redacción libre de resumen y envío de evaluación | 3 |
| 21 | [#26](https://github.com/DolyLanguagesORG/doly-languages/issues/26) | feat(nlp): servicio de evaluación de resúmenes por PNL con feedback | 3 |
| 22 | [#27](https://github.com/DolyLanguagesORG/doly-languages/issues/27) | feat(evaluation): endpoint /evaluation/submit con persistencia del resultado | 3 |
| 23 | [#28](https://github.com/DolyLanguagesORG/doly-languages/issues/28) | test(sprint3): pruebas de vocabulario y evaluación de resúmenes por PNL | 3 |
| 24 | [#29](https://github.com/DolyLanguagesORG/doly-languages/issues/29) | feat(streak): cálculo de racha diaria y asignación de puntos | 4 |
| 25 | [#30](https://github.com/DolyLanguagesORG/doly-languages/issues/30) | feat(history): endpoints de consulta de historial de actividades | 4 |
| 26 | [#31](https://github.com/DolyLanguagesORG/doly-languages/issues/31) | feat(dashboard): dashboard de usuario con métricas, racha y gráfica de puntos | 4 |
| 27 | [#32](https://github.com/DolyLanguagesORG/doly-languages/issues/32) | feat(admin): endpoints /admin/categories y supervisión de usuarios | 4 |
| 28 | [#33](https://github.com/DolyLanguagesORG/doly-languages/issues/33) | feat(admin): vista del panel administrativo básico | 4 |
| 29 | [#34](https://github.com/DolyLanguagesORG/doly-languages/issues/34) | refactor(review): revisión general de código y limpieza de endpoints | 4 |
| 30 | [#35](https://github.com/DolyLanguagesORG/doly-languages/issues/35) | test(usability): pruebas de usabilidad y diseño responsivo | 5 |
| 31 | [#36](https://github.com/DolyLanguagesORG/doly-languages/issues/36) | test(hardening): rendimiento, modo degradado de la IA y validación de seguridad | 5 |
| 32 | [#37](https://github.com/DolyLanguagesORG/doly-languages/issues/37) | chore(release): PR final develop→main, tag v1.0.0 y verificación de CI/CD | 5 |
| 33 | [#38](https://github.com/DolyLanguagesORG/doly-languages/issues/38) | docs(release): documentación final, capturas del sistema y presentación | 5 |

## Reglas de trabajo

Cada tarea del cronograma se entrega con un pull request:

1. La rama sigue la convención `feat/issue-<n>-<kebab>`, donde `<n>` es el
   **número de GitHub** del issue (no el número de cronograma).
2. El PR va hacia `develop`, salvo el PR de release, que va hacia `main`.
3. El título del PR es un Conventional Commit en inglés; el check
   `pr-title` lo valida.
4. Se requieren 7 checks en verde y una aprobación antes de fusionar.
5. Al fusionar a `main`, el workflow `release` crea el tag y la release
   automáticamente.

El detalle completo está en [git-workflow.md](./conventions/git-workflow.md)
y [versioning.md](./conventions/versioning.md).

## Reporte diario

Cada desarrollador publica su avance al cierre de su jornada en el
[hilo de standup](https://github.com/DolyLanguagesORG/doly-languages/discussions/39),
usando la plantilla del hilo. El límite es 23:59 CST.
