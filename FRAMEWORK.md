# Framework

How we go from "lots of ideas" to a working demo in about 9 hours of coding. Nothing here is invented for this hackathon: these are well-known methods, cut down to fit two days.

| Phase | When | Method | Output |
| --- | --- | --- | --- |
| Explore | Before the event | Problem canvas, "How might we" | One canvas per idea |
| Decide | Before the event (Discord call) | Scoring matrix, Design Sprint "Decide" | One problem, at most two |
| Scope | Friday 10:30 | MoSCoW | Must / Should / Could / Won't list |
| Build | Friday–Saturday | Walking skeleton, checkpoints | Working payment, then polish |
| Present | Saturday | [PITCH.md](PITCH.md) | 5-minute pitch and demo video |

---

## 1. Explore: problem canvas

A cut-down Lean Canvas. Fill one per idea from the idea bank in the [README](README.md). Keep each answer to one or two sentences.

```markdown
### Idea: <name>

- **How might we…?** <the problem as a question>
- **Problem:** <what hurts, in the user's words>
- **User:** <one specific person, not "everyone">
- **Today they…:** <how they solve it now, and why that's bad>
- **Our solution:** <one sentence>
- **Where Open Payments fits:** <incoming payment, quote, grant, outgoing payment…>
- **Why it matters:** <who else has this problem, how big it is>
- **Evidence:** <article, statistic, conversation with a real person>
```

### "How might we…?" questions

Turn each idea into a question that starts with "How might we…". It makes ideas easier to compare and keeps the focus on the user instead of on the technology.

| Instead of | Write |
| --- | --- |
| "An app to avoid the 4x1000" | How might we move money between our own accounts without paying 4x1000? |
| "Remittances with Interledger" | How might we let a family in Colombia receive money from abroad the same day, with clear fees? |
| "Tap to Pay without NFC" | How might we let a street vendor take a payment from any phone? |

---

## 2. Decide: scoring matrix

Each person scores each idea from 1 to 5 on its own, before discussing. Then add up the scores. Scoring alone first stops the loudest opinion from winning.

The columns are the official judging criteria, plus feasibility.

| Idea | Problem | Open Payments use | UX | Tech quality | Inclusion | Innovation | Impact | Feasible in ~9 h | **Total** |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| | | | | | | | | | |
| | | | | | | | | | |
| | | | | | | | | | |

**Feasibility is a veto.** If we can't picture a working Open Payments payment by Friday evening, drop the idea, whatever its total.

### Decision call (Design Sprint "Decide", ~60 min)

| Time | Activity |
| --- | --- |
| 10 min | Each person presents their canvas, without interruptions |
| 10 min | Silent reading: everyone reviews all canvases and writes questions |
| 10 min | Questions and answers |
| 10 min | Everyone scores the matrix on their own |
| 10 min | Reveal scores, discuss the top two |
| 10 min | Decide. If tied, the Product and pitch owner breaks the tie |

---

## 3. Scope: MoSCoW

On Friday at 10:30, before writing code, sort every feature into four groups. Fifteen minutes, no more.

| Must have | Should have | Could have | Won't have |
| --- | --- | --- | --- |
| A full Open Payments payment: request, authorization, execution, completion | | | |
| | | | |

- **Must have** is the smallest thing we can demo. If it isn't done, nothing else matters.
- **Won't have** is as important as Must have. Write it down so nobody builds it by accident. It is the same list as the Constraints section of the [README](README.md).

---

## 4. Build: walking skeleton

Build the thinnest version that works from start to finish first, even if it's ugly. Then make it better.

1. **Skeleton (Friday):** buttons and plain text that run one real payment through the Test Wallet, from request to confirmation.
2. **Muscle (Saturday morning):** the real screens, clear payment states, error handling.
3. **Skin (only if there's time):** visuals, animations, extras from "Could have".

Why: a polished screen with a broken payment loses to an ugly screen with a working one. "Use of Open Payments" is a judging criterion, and the organizers require a recording of the full payment flow.

### Checkpoints

Event-day checkpoints and owners are in [ROLES.md](ROLES.md#event-day-checkpoints). At each checkpoint, ask:

- Are we on time? If not, what moves from Should to Won't?
- Is anyone blocked for more than 20 minutes? Ask a teammate or a mentor.
- Is everything pushed to `main`? Are prompts saved to [`prompts/`](prompts/)?

---

## 5. Present

See [PITCH.md](PITCH.md).
