# Tech Stack

The goal is a stack everyone feels comfortable enough to work with on day one. A hackathon is not the place to learn a new framework: we pick what most of us already know.

**Decided: the JavaScript / TypeScript ecosystem, with PostgreSQL.** What's still open is which architecture inside it (see [Architecture options](#architecture-options)).

## Constraints from the hackathon

- **Open Payments is mandatory.** Projects that don't integrate the Open Payments API can't be judged or win prizes.
- **Any language or framework is allowed.** We use the official Node.js / TypeScript SDK, [open-payments-node](https://github.com/interledger/open-payments-node), which signs requests for us.
- **Public GitHub repo, everything on `main`, a working demo link.**
- **No project code before Friday 10:30.** Installing tools, creating accounts and studying the docs is fine. Check with the organizers whether project generators (`create-next-app`, `create-t3-app`, `nest new`…) count as pre-written code before relying on one.

## Core technologies

| Layer | Technology | Role |
| --- | --- | --- |
| Language | **TypeScript** | Main language, frontend and backend |
| Frontend | **React** | Isolated frontend (with Vite) |
| Backend | **Express** | Isolated, minimal backend |
| Backend | **NestJS** | More structured backend, if the project needs it |
| Full-stack | **Next.js** | Single monolith: frontend and backend in one app |
| Database | **PostgreSQL** | Relational database, with JSON / JSONB columns when needed |
| Payments | **@interledger/open-payments** | Official Open Payments SDK for Node.js |

## Architecture options

| Option | Stack | Pros | Cons | Best when |
| --- | --- | --- | --- | --- |
| **A. Monolith** | Next.js + PostgreSQL | One repo, one deploy, shared types out of the box | Everyone works in the same app, more merge conflicts | The team wants the fastest path to a deployed demo |
| **B. Split, minimal** | React (Vite) + Express + PostgreSQL | Clear frontend/backend split, easy to divide work, Express is quick to start | Two apps to run and deploy, CORS and shared types to set up | Work is clearly divided between frontend and backend people |
| **C. Split, structured** | React (Vite) + NestJS + PostgreSQL | Modules, dependency injection and validation built in | More boilerplate, slower to start | The backend is large, or most of the team already knows NestJS |

With about 9 hours of coding, A or B will usually be faster than C. Choose NestJS only if the people writing the backend use it daily.

### Speed-up options

Starter stacks that set up a lot of the wiring for us. Useful only if someone on the team has used them before.

| Option | What it is | Fits with |
| --- | --- | --- |
| **T3 Stack** | Next.js + TypeScript + tRPC + Tailwind + Prisma or Drizzle, generated with `create-t3-app` | Option A |
| **Vike** | Vite-based framework that adds server rendering and routing to React, and can run on top of an Express server | Options B or C, when we want one server for both |

## Database: PostgreSQL, kept simple

PostgreSQL for everything. When some data doesn't have a fixed shape, store it in a `JSONB` column instead of adding a second database. Start simple and only add structure when the project needs it.

Good candidates for JSONB in this project:

- Raw Open Payments responses (grants, quotes, incoming and outgoing payments), to debug and show in the demo.
- Metadata that changes from one payment to another.

What stays in normal columns: anything we filter, join or sort by, such as user, wallet address, payment status and dates.

The interactive grant also needs somewhere to keep its continue URI and token between the redirect to the wallet and the return to our app. A row in PostgreSQL works well, and it survives on serverless hosting where memory doesn't.

## Infrastructure

Jose provides the hosting through **Jericho Digital**, which already has Netlify and Railway set up and configured. We don't spend event time creating accounts or configuring hosting.

| Service | Hosts | Notes |
| --- | --- | --- |
| **Netlify** | Frontend: React (Vite) build, or the Next.js app in option A | Builds automatically from GitHub on every push to `main`. Gives us the public demo link. |
| **Railway** | Backend: Express or NestJS API (options B and C) | Builds automatically from GitHub. Runs as a long-lived server, so it can keep state in memory if needed. |
| **Railway** | PostgreSQL | One shared database for the whole team, used locally and by the deployed app. |

### How it fits each option

| Option | Netlify | Railway |
| --- | --- | --- |
| A. Next.js monolith | Next.js app (frontend + API routes) | PostgreSQL |
| B. React + Express | React frontend | Express API + PostgreSQL |
| C. React + NestJS | React frontend | NestJS API + PostgreSQL |

### Access and rules

- **Jose owns the infrastructure.** He connects the hackathon repo to Netlify and Railway on Friday, and sets the environment variables.
- **Teammates get access as needed**, for example to read logs or the database. Ask Jose instead of creating separate hosting accounts.
- **Secrets stay in Netlify and Railway.** The Open Payments private key, key ID and database URL are set as environment variables there, and shared with the team privately, never in the repo or the chat history.
- **Only hackathon resources.** The hackathon project lives in its own Netlify site and Railway project, separate from Jericho Digital's own services.
- **CORS and URLs.** With a split frontend and backend, the API must allow the Netlify domain, and the Open Payments finish URI must point to the deployed frontend URL.

## Who knows what

Fill in your row, 1 = never used, 5 = use it daily.

| Member | TypeScript | React | Next.js | Express | NestJS | PostgreSQL | T3 Stack | Vike | Deploying |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Jose Ríos | | | | | | | | | |
| Santiago Gómez | | | | | | | | | |
| Victor Villadiego | | | | | | | | | |
| Jacobo Zuluaga | | | | | | | | | |
| Manuel Gil | | | | | | | | | |

## How we decide the architecture

1. Add up each column in the table above.
2. Pick the option whose technologies have the highest total.
3. Tie: pick the one the Open Payments integration owner ([ROLES.md](ROLES.md)) is most comfortable with, since that part decides whether we have a demo.
4. Only use a speed-up option (T3, Vike) if at least two people have used it before.

## Decision

| | Choice |
| --- | --- |
| Language | TypeScript |
| Architecture | _A, B or C — TBD_ |
| Frontend | _React (Vite) or Next.js — TBD_ |
| Backend | _Express, NestJS or Next.js — TBD_ |
| Speed-up | _None, T3 or Vike — TBD_ |
| Database | PostgreSQL |
| ORM / query builder | _Prisma, Drizzle or none — TBD_ |
| Open Payments SDK | @interledger/open-payments |
| UI library / styling | _TBD_ |
| Database hosting | Railway (PostgreSQL) · provided by Jose / Jericho Digital |
| App hosting | Netlify (frontend) + Railway (backend) · provided by Jose / Jericho Digital |
| Decided on | _YYYY-MM-DD_ |

## Things to keep in mind

- **The finish URI changes with the environment.** `http://localhost:3000/callback` works locally because the redirect happens in the browser. In the deployed demo it has to be the public URL.
- **Keys never go in git.** The Open Payments private key, key ID and database URL go in environment variables. Add `.env` and `*.key` to `.gitignore` from the first commit, since the repo will be public.
- **One database for the whole team.** Everyone connects to the shared Railway PostgreSQL, which avoids "works on my machine" problems. Keep a local Docker database only as a fallback.
- **Amounts are strings.** Open Payments sends amounts as a string `value` plus an `assetScale`. Store them as text or `NUMERIC`, never as floating point.

## Setup to do before Friday

Each person, on their own laptop:

- [ ] Node.js LTS installed (`node -v`) and a package manager agreed (npm, pnpm or yarn)
- [ ] PostgreSQL client or GUI (psql, TablePlus, DBeaver…) and, optionally, Docker for a local database
- [ ] Git configured, with access to the GitHub account we'll use
- [ ] Editor ready, plus the AI tools from [AI_SUBS.md](AI_SUBS.md) signed in
- [ ] Test Wallet account with KYC done and a wallet address created
- [ ] Jose: Netlify site and Railway project (with PostgreSQL) ready for the hackathon, separate from Jericho Digital's own services
- [ ] Read the Node SDK README and the Open Payments docs on grants
