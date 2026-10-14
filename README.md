# Inteligencia Artesanal — Hackathon Playbook

**English** · [Español](README.es.md)

Team **Inteligencia Artesanal** at the Open Payments Hackathon by the Interledger Foundation: **October 16–17, 2026**, Ruta N, Medellín.
We build a working prototype on **Open Payments** that solves a real financial problem.

> This repo is for planning and getting organized before the event. All project code must be written during the two days of the hackathon. Writing code before the event is grounds for disqualification.

## Team docs

- [TEAM.md](TEAM.md): members, skills, AI tools, prerequisites, working agreements
- [ROLES.md](ROLES.md): role descriptions, assignments, event-day checkpoints
- [AI_SUBS.md](AI_SUBS.md): AI plans per member and how we split agent work
- [TECH_STACK.md](TECH_STACK.md): constraints, options, how we decide, setup before Friday
- [PROBLEMS.md](PROBLEMS.md): what past Interledger hackathons built (with repos), what wins, and candidate problems for Colombia
- [FRAMEWORK.md](FRAMEWORK.md): how we choose the problem, scope it and build it
- [PITCH.md](PITCH.md): 5-minute structure, demo script, rehearsal checklist
- [AI_USAGE.md](AI_USAGE.md) and [prompts/](prompts/): AI disclosure required by the organizers

## Key event facts

| What | Details |
| --- | --- |
| Team | 4 to 5 people, in person, both days |
| Technical requirement | The project must integrate the Open Payments API; any language or stack |
| Actual coding time | ~9 h: Fri 10:30–14:00 and 15:00–17:30, Sat 08:00–11:00 |
| Code freeze | **Saturday 11:00** |
| Submission | Slides, demo link, public GitHub repo (everything on `main`), video of the payment flow |
| Pitch | 5 minutes per team (Round 1, and Round 2 if we advance) |
| Prizes | Four awards of US$5,000 each: **Impact** (Ruta N), **Inclusion** (Puntored), **Innovation** (FIND EAFIT), **Community** (This Week in Fintech, voted by participants). A team can win only one |
| Judging criteria | Problem definition, use of Open Payments, UX, technical quality, presentation, inclusion, innovation, impact |
| AI policy | `AI_USAGE.md` at the repo root and a `/prompts` folder with the actual prompts |
| Prerequisite | Platzi course **or** the Open Payments guide, for every team member |

## Next steps

1. **Meet on Discord** to get to know each other and talk about what each of us knows, both technical and non-technical.
2. **Define clear roles.** The idea is that everyone can get hands-on with the code, but each person has one main responsibility.
3. **Research problems:**
   - Current problems with the Open Payments protocol, such as the one Jacobo mentioned about mass adoption.
   - Real problems people and businesses have when moving money, even between their own accounts.
4. **Pick one, or at most two, of those problems** and arrive at the hackathon with it defined.

## What we need to agree on

### 1. Tech stack

We want to reach consensus on a stack everyone feels comfortable enough to work with. Skills, options and the final decision are in [TECH_STACK.md](TECH_STACK.md).

**Agreed stack:** TypeScript + PostgreSQL. Architecture still open: Next.js monolith, React + Express, or React + NestJS.

### 2. AI subscriptions

The idea is to split agent and subagent work based on the plan each person pays for. Jose has Claude Max and takes the heavier agent tasks. Santiago, Victor and Manuel have Claude Pro, and Jacobo has ChatGPT Plus with Codex. The full split is in [AI_SUBS.md](AI_SUBS.md).

Reminder: every coding prompt we use must be saved to `/prompts` during the event, not at the end.

### 3. Roles

Clear, well-defined roles. Not everyone is comfortable speaking in public, so the pitch goes to whoever enjoys it, and the rest contribute elsewhere.

| Role | Responsibility | Member |
| --- | --- | --- |
| Open Payments integration | Grants, quotes, incoming and outgoing payments, test wallet | _TBD_ |
| Frontend / UX | Interface and user flow in the demo | Jose |
| Backend / infrastructure | API, deployment, demo link | Victor |
| Product and pitch | Problem definition, slides, 5-minute presentation | Santiago, Manuel, Jacobo |
| Demo and deliverables | Payment flow video, `AI_USAGE.md`, `/prompts`, submission form | _TBD_ |

Backups, specialties and event-day checkpoints are in [ROLES.md](ROLES.md).

### 4. Constraints

Where, how and why we will **NOT** do certain things.

| We won't | Why |
| --- | --- |
| | |
| | |
| | |

## Idea bank

Loose ideas to explore, thinking out loud. Researched versions of these and more are in [PROBLEMS.md](PROBLEMS.md).

- **4x1000 between personal accounts:** Colombia's tax on moving money, even between your own accounts.
- **Apple Tap to Pay on Android without NFC.**
- **Remittances.**
- **Money availability:** how long money takes to arrive or become usable.

| Idea | Problem | User | How it uses Open Payments | Doable in ~9 h |
| --- | --- | --- | --- | --- |
| | | | | |

## Resources

- [Hackathon page](https://interledger.org/es/hackathon/overview/)
- [Open Payments docs](https://openpayments.dev)
- [Interledger Test Wallet](https://wallet.interledger-test.dev)
- [Node SDK](https://github.com/interledger/open-payments-node)
- [Platzi course](https://platzi.com/cursos/interledger-openpayments/) (Spanish)
- [Submission & judging](https://interledger.org/es/hackathon/submission-judging/)
- [AI policy](https://interledger.org/es/hackathon/ai-policy/)
