# Inteligencia Artesanal — Hackathon Playbook

[English](README.md) · **Español**

Equipo **Inteligencia Artesanal** en el Open Payments Hackathon de Interledger Foundation: **16 y 17 de octubre de 2026**, Ruta N, Medellín.
Construimos un prototipo funcional sobre **Open Payments** a partir de un problema financiero real.

> Este repo es para planear y organizarnos antes del evento. Todo el código del proyecto debe escribirse durante los dos días del hackathon. Escribir código antes del evento es motivo de descalificación.

## Documentos del equipo

- [TEAM.md](TEAM.md): integrantes, habilidades, herramientas de IA, prerrequisitos, acuerdos de trabajo
- [ROLES.md](ROLES.md): descripción de roles, asignaciones, checkpoints del evento
- [AI_SUBS.md](AI_SUBS.md): planes de IA por integrante y cómo repartimos el trabajo de agentes
- [TECH_STACK.md](TECH_STACK.md): restricciones, opciones, cómo decidimos, setup antes del viernes
- [WINNERS.md](WINNERS.md): los ganadores de cada edición de cerca (repos, pitches, lo que dicen los jurados) y la guía oficial de puntaje de 0 a 5
- [PROBLEMS.md](PROBLEMS.md): qué construyeron los hackathons anteriores de Interledger (con repos), qué gana, cómo nos va a leer el jurado, y problemas candidatos para Colombia con una tabla de puntajes
- [FRAMEWORK.md](FRAMEWORK.md): cómo elegimos el problema, lo acotamos y lo construimos
- [PITCH.md](PITCH.md): estructura de 5 minutos, guion del demo, checklist de ensayo
- [AI_USAGE.md](AI_USAGE.md) y [prompts/](prompts/): declaración de uso de IA que exigen los organizadores

## Datos clave del evento

| Qué | Detalle |
| --- | --- |
| Equipo | 4 a 5 personas, presencial, los dos días |
| Requisito técnico | El proyecto debe integrar la API de Open Payments; cualquier lenguaje o stack |
| Tiempo real de código | ~9 h en Ruta N: vie 10:30–14:00 y 15:00–17:30, sáb 08:00–11:00, más trabajo opcional de noche desde casa con mentores virtuales |
| Code freeze | **Sábado 11:00** |
| Entrega | Slides, link al demo, repo público de GitHub (todo en `main`), video del flujo de pago |
| Pitch | 5 minutos por equipo (Ronda 1, y Ronda 2 si pasamos) |
| Premios | Cuatro premios de US$5.000 cada uno: **Impacto** (Ruta N), **Inclusión** (Puntored), **Innovación** (FIND EAFIT), **Comunidad** (This Week in Fintech, votado por los participantes). Un equipo solo puede ganar uno |
| Criterios | Definición del problema, uso de Open Payments, UX, calidad técnica, presentación, inclusión, innovación, impacto |
| Política de IA | `AI_USAGE.md` en la raíz del repo y carpeta `/prompts` con los prompts reales |
| Prerrequisito | Curso de Platzi **o** la guía de Open Payments, cada integrante |

## Próximos pasos

1. **Reunirnos en Discord** para conocernos y hablar de lo que sabe cada uno, tanto en lo técnico como en lo no técnico.
2. **Definir roles claros.** La idea es que todos podamos meter mano en el código, pero cada uno con una responsabilidad principal.
3. **Investigar problemas:**
   - Problemas actuales del protocolo Open Payments, como el que menciona Jacobo sobre la adopción masiva.
   - Problemas reales de personas y empresas al mover dinero, incluso entre sus propias cuentas.
4. **Elegir uno, o máximo dos, de esos problemas** y llegar al hackathon con eso definido.

## Lo que tenemos que acordar

### 1. Tech stack

Queremos llegar a un consenso sobre un stack con el que todos nos sintamos lo bastante cómodos para meterle mano. Habilidades, opciones y la decisión final están en [TECH_STACK.md](TECH_STACK.md).

**Stack acordado:** TypeScript + PostgreSQL. Arquitectura por definir: monolito con Next.js, React + Express, o React + NestJS.

### 2. Suscripciones de IA

La idea es repartir el trabajo de agentes y subagentes según el plan que paga cada uno. Jose tiene Claude Max y se encarga de las tareas de agentes más pesadas. Santiago, Victor y Manuel tienen Claude Pro, y Jacobo tiene ChatGPT Plus con Codex. El reparto completo está en [AI_SUBS.md](AI_SUBS.md).

Recordatorio: cada prompt de código que usemos debe quedar guardado en `/prompts` durante el evento, no al final.

### 3. Roles

Roles bien claros y definidos. No todos se sienten cómodos hablando en público, así que el pitch lo presenta quien lo disfrute, y el resto aporta en otras partes.

| Rol | Responsabilidad | Integrante |
| --- | --- | --- |
| Integración Open Payments | Grants, quotes, pagos entrantes y salientes, wallet de pruebas | _por definir_ |
| Frontend / UX | Interfaz y flujo del usuario en el demo | Jose |
| Backend / infraestructura | API, despliegue, link del demo | Victor |
| Producto y pitch | Definición del problema, slides, presentación de 5 min | Santiago, Manuel, Jacobo |
| Demo y entregables | Video del flujo de pago, `AI_USAGE.md`, `/prompts`, formulario de entrega | _por definir_ |

Backups, especialidades y checkpoints del evento están en [ROLES.md](ROLES.md).

### 4. Constraints

Dónde, cómo y por qué **NO** haremos ciertas cosas.

| No haremos | Por qué |
| --- | --- |
| | |
| | |
| | |

## Banco de ideas

Ideas sueltas para explorar, pensando en voz alta. Versiones investigadas de estas y otras están en [PROBLEMS.md](PROBLEMS.md).

- **4x1000 entre cuentas personales:** el impuesto al mover dinero entre cuentas propias.
- **Apple Tap to Pay en Android sin NFC.**
- **Remesas.**
- **Disponibilidad del dinero:** cuánto tarda en llegar o en estar disponible.

| Idea | Problema | Usuario | Cómo usa Open Payments | Viable en ~9 h |
| --- | --- | --- | --- | --- |
| | | | | |

## Recursos

- [Página del hackathon](https://interledger.org/es/hackathon/overview/)
- [Documentación de Open Payments](https://openpayments.dev/es)
- [Interledger Test Wallet](https://wallet.interledger-test.dev)
- [SDK de Node](https://github.com/interledger/open-payments-node)
- [Curso de Platzi](https://platzi.com/cursos/interledger-openpayments/)
- [Entrega y evaluación](https://interledger.org/es/hackathon/submission-judging/)
- [Política de IA](https://interledger.org/es/hackathon/ai-policy/)
