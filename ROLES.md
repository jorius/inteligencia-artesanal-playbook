# Roles

Everyone writes code and helps wherever it's needed, but each person owns one area. Owning means you make sure it gets done, not that you do it alone. Every role has a backup in case someone gets stuck or overloaded.

Not everyone enjoys public speaking. The pitch goes to whoever is comfortable presenting, and nobody is forced on stage.

## Assignments

| Role | Owner | Backup |
| --- | --- | --- |
| Open Payments integration | _TBD_ | _TBD_ |
| Frontend / UX | Jose | Manuel |
| Backend / infrastructure | Victor | Manuel · Jose (hosting) · Santiago (DevOps) |
| Product and pitch | Santiago, Manuel, Jacobo | |
| Demo and deliverables | _TBD_ | _TBD_ |

## Team

| Member | Specialty | Presents the pitch |
| --- | --- | --- |
| Jose Ríos | Frontend / Full Stack | |
| Santiago Gómez | Full Stack / Data Scientist / DevOps | Yes |
| Victor Villadiego | Backend | |
| Jacobo Zuluaga | Full Stack / AI Agentic Developer | Yes |
| Manuel Gil | Backend / Frontend | Yes |

The three presenters also write code. On Saturday they step away from coding by 10:30 to rehearse, so the code freeze is mostly handled by Jose and Victor. Plan Saturday-morning tasks with that in mind.

## Role descriptions

### Open Payments integration

Gets the payment flow working end to end. This is the part judges check most closely.

- Sets up the Test Wallet accounts, wallet addresses and developer keys for the app.
- Implements the flow: wallet address lookup, incoming payment, quote, interactive grant, continue, outgoing payment, confirmation.
- Handles the redirect back from the wallet (the finish URI) and the grant continuation.
- **Done when:** one real test payment goes from request to completion. Target: end of Friday.

### Frontend / UX

Makes the solution understandable and pleasant to use in a 5-minute demo.

- Designs and builds the screens of the user flow.
- Makes payment states clear: waiting for approval, processing, completed, failed.
- Keeps accessibility and inclusion in mind, since inclusion is a judging criterion.
- **Done when:** the full flow can be shown without explaining what's on screen.

### Backend / infrastructure

Keeps the app running and reachable.

- Sets up the repo, project structure, environment variables and secrets (keys never go in git).
- Builds the API routes the frontend needs and keeps state for payments in progress.
- Deploys the app on the Netlify and Railway setup Jose provides ([TECH_STACK.md](TECH_STACK.md#infrastructure)) and owns the demo link.
- **Done when:** the demo link works from a phone that isn't on our laptop's network.

### Product and pitch

Owns the story: what problem we solve, for whom, and why it matters.

- Leads the problem research and the choice of idea before the event.
- Writes the slides with the required structure: challenge, user, solution, how Open Payments was used, key takeaways.
- Presents the 5-minute pitch, or coaches whoever presents.
- **Done when:** the pitch has been rehearsed at least twice within 5 minutes.

### Demo and deliverables

Makes sure nothing is missing at the deadline. Good fit for someone who prefers to stay off stage.

- Records the demo video of the payment flow: request, authorization, execution, completion.
- Keeps [AI_USAGE.md](AI_USAGE.md) and [`prompts/`](prompts/) up to date during the event.
- Checks the repo is public and everything is on `main`, then submits the Google Form and uploads slides and video to the shared Drive folder.
- **Done when:** everything is submitted before Saturday 11:00 (code) and 12:00 (videos and slides).

## Event-day checkpoints

| When | Checkpoint | Owner |
| --- | --- | --- |
| Fri 10:30 | Repo created, stack running locally for everyone | Backend |
| Fri 14:00 | Incoming payment and quote working | Open Payments |
| Fri 17:30 | Full test payment working end to end | Open Payments |
| Fri 17:30 | First draft of the slides | Product and pitch |
| Sat 09:30 | Frontend flow complete, app deployed | Frontend, Backend |
| Sat 10:30 | Demo video recorded, AI_USAGE.md complete | Demo and deliverables |
| Sat 11:00 | **Code freeze.** Everything on `main` | Everyone |
| Sat 12:00 | Slides and video uploaded, pitch rehearsed | Product and pitch, Demo and deliverables |
