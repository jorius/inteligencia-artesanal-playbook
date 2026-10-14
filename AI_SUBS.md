# AI Subscriptions

What AI plans the team has and how we split work across them. The goal is to use the biggest plan for the heaviest agent work, and to stop anyone from running out of usage in the middle of the event.

Everything used here must be declared in [AI_USAGE.md](AI_USAGE.md), with prompts saved to [`prompts/`](prompts/).

## Plans

| Member | Plan | Cost / month | Main tool | Capacity |
| --- | --- | --- | --- | --- |
| Jose Ríos | Claude Max | 200 USD | Claude Code | High: the team's heavy agent work |
| Santiago Gómez | Claude Pro | 20 USD | Claude Code | Standard |
| Victor Villadiego | Claude Pro | 20 USD | Claude Code | Standard |
| Manuel Gil | Claude Pro | 20 USD | Claude Code | Standard |
| Jacobo Zuluaga | ChatGPT Plus | 20 USD | Codex | Standard, different vendor |

Pro and Plus plans have usage limits that reset every few hours. A long agent session with big files can use up a window quickly, and the hackathon only has about 9 hours of coding, so limits matter.

## Strategy

### Jose (Claude Max): heavy lifting

- Scaffolds the project on Friday at 10:30 so everyone can start from the same base.
- Takes multi-file features, long debugging sessions and refactors.
- Runs parallel subagents when several independent pieces can be built at once.
- Picks up tasks from teammates who hit their usage limit.

### Santiago, Victor, Manuel (Claude Pro): focused tasks

- One task per session: one component, one route, one bug.
- Start a fresh session for each new task instead of continuing a long one.
- Point the agent at specific files instead of the whole repo. Don't paste huge logs, only the relevant lines.
- Use a lighter, faster model for simple tasks and save the strongest one for hard problems.

### Jacobo (Codex): second opinion and parallel work

- Reviews critical code written with Claude, especially the Open Payments integration. A model from a different vendor tends to catch different mistakes.
- Takes tasks that can run in parallel without touching the same files as the others.
- Brings his agentic development experience to set up how agents get context (see below).

## Who does what

| Task | Who / tool |
| --- | --- |
| Project scaffold and base structure | Jose · Claude Code |
| Open Payments flow (grants, quotes, payments) | Owner of the integration + Jose for heavy sessions |
| Backend routes and storage | Victor, Manuel · Claude Code |
| Frontend screens and components | Jose, Manuel · Claude Code |
| Deployment and environment setup | Santiago · Claude Code |
| Review of critical files | Jacobo · Codex |
| Slides and pitch text | Santiago, Manuel, Jacobo · any chat assistant |
| `AI_USAGE.md` draft from the saved prompts | Jose · Claude Code |

## Context for agents

On Friday, add a short context file to the project repo so every agent starts with the same information. Claude Code reads `CLAUDE.md`. Codex reads `AGENTS.md`. Keep one as the main file and have the other point to it.

What to put in it (decide the content before the event, write the file on Friday):

- What the project does, in two sentences.
- The agreed stack from [TECH_STACK.md](TECH_STACK.md) and the folder structure.
- How to run the app locally.
- The Open Payments flow we use and where its code lives.
- Rules: no secrets in code, amounts are strings with an `assetScale`, check Open Payments calls against the official docs.

## Rules for working with agents

- **One agent per area.** Two agents editing the same files at the same time create conflicts. Say in the chat what you're about to work on.
- **Pull before you start a session, push when you finish.** Small commits, straight to `main` or through short-lived branches.
- **Read and test what the agent wrote before committing.** Everyone is responsible for what goes into the repo, whoever or whatever wrote it.
- **Save prompts as you go.** Claude Code: `/export`. Codex: copy the prompts from the conversation. Use the format in [prompts/README.md](prompts/README.md).
- **Out of usage?** Hand the task to Jose or Jacobo, and switch to testing, reviewing or helping with the pitch until your limit resets.
