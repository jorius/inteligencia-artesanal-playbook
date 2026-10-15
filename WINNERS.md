# Winners

A deep dive into the projects that won past Interledger hackathons, and into what the judges themselves say they reward. It builds on the lineage in [PROBLEMS.md](PROBLEMS.md) and goes one level down: the winners' repositories, their recorded pitches, the judges' interviews and the official scoring guide for Medellín.

Research done on 2026-10-14. We cloned every winner repository we could find, read transcripts of 20 Interledger Foundation (ILF) videos (pitches, recaps, info sessions, podcasts) and read the source of the ILF website, which holds the hackathon pages and FAQ. Reading other teams' code to learn is fine; copying it is not. All our code must be written during the event.

## In short

1. **The gate is one real Open Payments payment, end to end.** "The first thing we will look at is a complete Open Payments payment" (Medellín info session). Technical mentors review every repository between 11:00 and 12:00 on Saturday. In Oaxaca 2025 two teams were disqualified because their AI-generated code called Open Payments APIs that don't exist.
2. **Spend everything on the payment, nothing on the scaffolding.** Alex Lakatos, ILF's CTO and the most frequent judge: "99% of them have a login screen and a forgot-your-password screen. Nobody cares. Don't even build the user authentication flow. Just fake it."
3. **Creativity means bending the standard flow.** Tímea Nagy, ILF engineering manager and judge: "think creatively about where to tweak, pause, or extend this flow to strengthen your use case. That would surely impress the judges."
4. **A local, relatable problem that improves something people already do.** The official participant guide: "Many of the best hackathon projects improve an existing experience rather than inventing something completely new."
5. **Soul wins the deliberation.** Tímea on judging three Mexican hackathons: the judges rarely disagreed, and the winners "had a soul in the presentation. They were animated. They were enthusiastic. You could feel their appreciation for Open Payments."
6. **A 5 out of 5 needs a path beyond the hackathon.** The official scoring guide reserves its top score for a "viable pathway for deployment supported by a well considered go-to-market strategy".
7. **ILF runs hackathons to learn.** They watch where teams stumble so they can fix docs and tools, and at least one hackathon idea is now in production. "Key learnings" is a required part of the presentation; a sharp learning about the protocol earns goodwill.
8. **Experience compounds.** Darryl Nyamayaro won first place in 2024 and again in 2025. Los VibeCoders won a student hackathon in September 2025 and then first place at the Mexico City Summit two months later.

---

## Who judges

The same ILF people appear again and again, so their stated preferences matter more than any generic hackathon advice.

| Person | Role | Judged or ran |
| --- | --- | --- |
| Alex Lakatos | CTO, ILF | Costa Rica 2023, Cape Town Summit 2024, Mexico student hackathons 2025, Mexico City 2025, UCT 2026 |
| Tímea Nagy | Engineering manager, ILF (Test Wallet, integrations) | UCT 2025, three Mexico student hackathons 2025, HackOMania 2026; presented Open Payments at the Medellín info session |
| Ioana Chiorean | Engineering manager, ILF | Costa Rica 2023; hosted the Medellín info session |
| Sabine Schaller | Engineering manager, ILF | Costa Rica 2023, Mexico City 2025 |
| Roberto Valdovinos | People's Clearinghouse (Mexico) | Mexico student hackathons and Mexico City 2025 |
| Matthew de Haast | CTO, Fynbos | UCT 2024, UCT 2026 |
| Allan Davids | Director, UCT Financial Innovation Hub | Cape Town Summit 2024, UCT 2026 |
| Marian Villa | Developer advocate, ILF (Colombian) | Ran the Mexico student hackathons and the Platzi course; Medellín organizer |

For Medellín, the info session said judges are "a mix of industry experts from Colombia's financial systems and our developers and software engineers". Round 2 adds a representative from each sponsor. The organizers also said Medellín judges won't know past hackathon projects, but the mentors will.

---

## The official scoring guide

The ILF hackathon FAQ scores each criterion from 0 to 5 ([FAQ](https://interledger.org/hackathon/faq/)). The jump from 3 to 5 is what separates a working project from a winner.

| Score | What it takes |
| --- | --- |
| 0 Not met | Problem or solution unclear, no working prototype |
| 1 Minimal | Little evidence that Open Payments was used or that the solution works |
| 2 Partial | Some features work; core features incomplete or unstable |
| 3 Meets expectations | Functional demo, stable core features, clear problem and approach |
| 4 Strong | Polished demo, well-scoped with **measurable impact**, **clear scope for expansion beyond the initial context**, technical depth |
| 5 Exemplary | Exceptional demo, **novel and technically impressive**, **multiple technologies** stand out, thinking beyond the initial problem, a **viable deployment path with a go-to-market strategy** |

The FAQ also lists what makes a strong project: it solves one problem well, demonstrates a working payment flow, focuses on user value, is easy to explain and shows thoughtful use of Open Payments.

---

## What the judges say, in their own words

| Who, where | What they said | What it means for us |
| --- | --- | --- |
| Medellín info session, Sept 23, 2026 ([video](https://www.youtube.com/watch?v=i6zC-FUGq6s)) | "Lo que nosotros vamos a mirar, el primer paso, es un pago completo de Open Payments." | One real payment before anything else |
| Same session | They gave no suggested themes this time "because when we say remittances or donations, everyone builds that", and cited the 2024 fingerprint-hardware winner as the kind of creativity they want | Originality is explicitly asked for |
| Marian Villa, same session | "Encuentra en tu contexto local qué es lo que quieres solucionar... cómo nos conectamos con la región y con el mundo" | Local problem, with interoperability in the story |
| Tímea Nagy, "Tips and Tricks" ([video](https://www.youtube.com/watch?v=35BVQPCLTSk)) | Judges value originality but also "creativity in applying the standard Open Payments flow to a real, meaningful problem... local and relatable, like an issue faced by your family, your neighborhood". "Imagine the judges see 10 donation platforms. What will make yours different?" "Tweak, pause, or extend this flow." | Our twist on the flow is the innovation point |
| Alex Lakatos, Mexico webinar ([video](https://www.youtube.com/watch?v=ATO1d9PfD0g)) | Don't build login or account screens. "Your application should focus on the payments part." Example of innovation he likes: "multiple people paying into the same payment that is split into four parts" | VibePayments built exactly that and won |
| Alex Lakatos, same webinar | Hackathons exist so ILF can see "where they stumble, where the user experience or the documentation isn't what we want it to be". A 2024 hackathon team moved the payment consent from the wallet screen to email; it is now in production | Learnings about the protocol are valued |
| Ioana Chiorean, "Of the Ledger" podcast ([video](https://www.youtube.com/watch?v=vNgSuIxtI2M)) | "Don't waste time presenting the team... demo the Open Payments, that was the must thing." "If you just present a nice UI of an app, this is not our purpose." Explaining "why Open Payments is the best solution for that is definitely winning you points" | No team slide, no stack slide |
| Tímea Nagy, same podcast | Mentors review the code and "filter out by code" who goes through, so judges already know the stack. Winners "had a soul in the presentation". From ~15 teams the judges usually agreed on ~5 quickly | Enthusiasm and a working demo decide it |
| Ioana Chiorean, same podcast | Impressed by teams whose presentations were "connected identity-wise, each project had identity, some had logos". AI use was fine | A name, a logo, one visual identity |
| Marian Villa, same podcast | "Choose the best speaker... a storyteller, and practice", so you can answer questions | One presenter, rehearsed Q&A |
| UCT 2025 judge, recap ([video](https://www.youtube.com/watch?v=drZfYz7Eafc)) | "You judge equally between the pitch and the technical implementation." "You're mostly looking for a solution that can be widely used, especially locally." | Pitch and code weigh the same |
| Raul Ranete, ILF, UCT 2025 ([ITWeb](https://www.itweb.co.za/article/students-find-solutions-to-real-world-payment-challenges/KA3Ww7dzApyqrydZ)) | "You get to be surprised by the fact that Open Payments could potentially be used in these left-field ways." | Surprise is a goal |
| Direla's mentors, 2025 ([post](https://community.interledger.org/dyxta/direla-winners-ilf-x-finhub-25-5a7o)) | "Tell the story. Make people feel the problem you're solving." | Open with a person |
| Fireline, UCT 2026 winners ([ILF blog](https://interledger.org/news/beyond-hackathon-building-future-open-payments-through-collaboration)) | "The more time you spend genuinely understanding the people you're building for, the more likely your solution is to meet their needs." | Talk to a real user before Friday |

---

## Winners, edition by edition

### Costa Rica Summit, Nov 2023

A contribution-style hackathon ([Devpost](https://interledger-hackathon-2023.devpost.com/)), judged by Alex Lakatos, Sabine Schaller, Ioana Chiorean and others. The four winners were infrastructure work: Helm charts, deploying TigerBeetle to fly.io, migrating the Web Monetization tools, and a TigerBeetle schema wizard. Not our format, but it shows the ILF's instinct: they reward things that improve the ecosystem itself.

### Hack @ UCT, June 2024

Judges: Matt (CTO, Fynbos), Anda (UCT Fintech Hub), Aretha (MakeDev), Max and Sid (ILF). ILF gave students a starter app. Winners re-pitched on the [July 2024 community call](https://www.youtube.com/watch?v=96665lZTu3E).

| Place | Project | What we found |
| --- | --- | --- |
| 1st | **SecureLifeCover** | The pitch opens with an emotional story and a quote from a woman in a township: "we are poor in life, let's not be poor in death". Then come the numbers (61% rely on informal funeral cover, a R10 billion market), the solution ("a digital guardian angel") and a call to funeral parlours to join. In the repo we found ([Darryldn9/Hackathon-Interledger_group](https://github.com/Darryldn9/Hackathon-Interledger_group)), the "pay" button only marks the policy as paid in a local database, and a commit message says "API doesn't seem to be connecting". Asked why they won, the team said: "We were giving people dignity in their time of despair." |
| 2nd | **Spend Secure** | Remittance senders pay into a merchant's wallet (a grocery store, a utility) that dependents redeem, so the money can't be misused. Public "communities" such as orphanages show where donations go. They added a Web Monetization game as a donation booster. Marc Levin came back in 2026 as a mentor. |
| 3rd | **OpenFundsFO** | Donors fund student profiles directly, cross-border. The team included a professor from Bowie State, who judged Mexico City in 2025. |
| HM | **Naartjie** | Changed the protocol's one-to-one model: several payers fund one purchase, and one authorization pays two receivers. Technically the deepest project, but no podium at a student event. |
| HM | **TheHackers** | Telegram bot for transfers and scheduled payments ([repo](https://github.com/tshepo-ncube/OpenPaymentHackathonServer)). |

**Lesson:** at the 2024 student event, story and dignity beat technical depth. The rules have since tightened: "working payment flow" is now a criterion with a code review gate, so we can't win the way SecureLifeCover did.

### Cape Town Summit, Oct 2024

Judges listed on [Devpost](https://interledger-hackathon-2024.devpost.com/): Alex Lakatos and Allan Davids. Their only published criterion: **"the fit between the use case and the APIs used in the project."** About 40 teams; 20 reached the main stage ([highlights](https://www.youtube.com/watch?v=Pz6t4TGzaf4)).

| Place | Project | What we found |
| --- | --- | --- |
| 1st | **Byron Coetsee & Lex Campbell** | A multi-tenant payment network over LoRa radio with tokenized fingerprints, shown on real hardware. ILF's newsletter praised "blending technology and hardware to elevate the presentation". The Medellín organizers still cite it as their example of creativity. No public repo. |
| 2nd | **Team 23** | "Delving into the core of Rafiki, exploring authentication and GNAP" ([newsletter](https://community.interledger.org/interledger/latest-news-from-the-interledger-foundation-november-2024-a8d)). Alex Lakatos later described a four-person local fintech team at this hackathon that moved the consent step from the wallet's redirect screen to email, an idea that went into production. That is very likely Team 23. |
| 3rd | **Pet Patron** | Donate to a specific SPCA animal ([repo](https://github.com/CadeSayner/interledger-payment-service)). Its developer then wrote a Java Open Payments client library. |
| Community | **Team 8** | Recognized for the presentation. |

**Lesson:** at professional events judged by the CTO, the protocol itself is the star: hardware, new consent channels, auth-server internals.

### UCT FinHub, June 2025

Judges: Tímea Nagy and Raul Ranete (ILF), Si-Jia Wu, Takunda Chirema. Around 60 students in 20 teams.

| Place | Project | What we found |
| --- | --- | --- |
| 1st | **Direla** | Township merchants (~US$130 billion a year, mostly cash) turn their phone into the POS. The repo ([Darryldn9/Direla-Interledger](https://github.com/Darryldn9/Direla-Interledger), created on hackathon day) has one real flow (QR → incoming payment → quote → interactive grant → outgoing payment, ZAR, Test Wallet) wrapped in a broad app: dashboard with a demo balance, merchant analytics, WhatsApp, NFC and a lending tab. Its implementation notes read like an AI assistant's output. Same lead developer as SecureLifeCover. |
| 2nd | **Fin Illuminaries – Cache Money** | USSD wallet using spaza shops as cash points. The repo ([Plum165/FinTechHackthon](https://github.com/Plum165/FinTechHackthon)) asks for the interactive grant **once**, keeps the token, then sends payments from a USSD menu (Africa's Talking simulator) without any redirect. Consent once, pay later. |
| 3rd | **FlowFi** | Student crowdfunding with the frontend built in Softr, a no-code tool. The team didn't plan to continue it. |

**Lesson:** one real flow plus a credible product around it wins; a no-code frontend can still place. Pausing the flow (grant now, payments later) worked here and fits a USSD or no-smartphone channel.

### Mexico student hackathons, Sept 2025

Four events (Oaxaca, Estado de México, Aguascalientes, CDMX), ~15 finalists each, judged by Alex Lakatos, Tímea Nagy, Roberto Valdovinos and university staff. Demos were pre-recorded ([podcast](https://www.youtube.com/watch?v=vNgSuIxtI2M)).

| Event and place | Project | What we found |
| --- | --- | --- |
| Aguascalientes 1st | **Qrancheros – Ocelon** | Parking without tickets: dynamic QR and mobile payment ([repo](https://github.com/DavidRangel2405/Ocelon_QRancheros)). Four people with named roles, including a UX/UI designer and QA. Real Open Payments code. |
| Aguascalientes 2nd | **Hubbers – InterPyme** | Payments for small businesses ([repo](https://github.com/yosoyemi/interpyme-app)), Open Payments in an Express backend. |
| Aguascalientes 3rd | **Tu Tía Dev – YaYa** | P2P QR in under 10 seconds ([repo](https://github.com/ChaboCode/YaYa)). The README states the problem with a number, then the solution, benefits, architecture, essential features, and who builds what, including a person for "pitch and documentation". |
| Edomex 2nd | **PaDuki** | Artisan e-commerce: a store, a cart, and payment authorization opened in a new tab while the cart polls for approval ([repo](https://github.com/gcDiego/PaDuki-Cliente)). |
| One of the four (likely Oaxaca) | **Los VibeCoders** | Won a student event according to the [Nov 2025 community call](https://community.interledger.org/interledger/interledger-community-call-summary-12-november-2025-16kg). A member's repo from Sept 12 is a crowdfunding app called FoundUP ([repo](https://github.com/RonaldoAO/Interledger_Crowfunding)). |

**Lesson:** ordinary use cases win student events when the payment is real and the team is organized: a designer, a presenter, a clear README, a pre-recorded demo.

### Mexico City Summit, Nov 2025

47 teams, 24 hours. Judges: Alex Lakatos, Roberto Valdovinos, Andrew Mangle, Afua Bruce, Sabine Schaller. Criteria: idea quality, strategic impact, implementation ([winners](https://interledger.org/news/building-real-solutions-interledger-hackathon-winners-2025)).

| Place | Project | What we found |
| --- | --- | --- |
| 1st | **Los VibeCoders – VibePayments** | Tourism and supply-chain payments. The backend ([RonaldoAO/Interledger_back](https://github.com/RonaldoAO/Interledger_back)) has three Open Payments features: **split checkout** (merchant plus platform commission, one consent), **group checkout** (several payers cover one bill) and an **FX comparator** showing the ILP rate against the market rate. It also has Swagger docs. The Flutter client ([repo](https://github.com/RonaldoAO/Interledger_turismo)) was designed through the night. Two months earlier, Alex Lakatos had publicly praised multiple payers funding one payment that is split. |
| 2nd | **Haki Ando – Pagos** | Face and voice biometrics as the only authorization, for people with motor disabilities. No public repo found. |
| 3rd | **Team Kanzu – Shabaha** | An existing ILF grantee built on its own WordPress, LearnDash and GamiPress stack, plus a small Node service: incoming payment → quote → interactive grant → continue, one grant per milestone payout ([repo](https://github.com/kakoma/getshabaha), [service](https://github.com/kakoma/getshabaha-openpayments-service)). |
| Community | **Máquinas de Boltzmann – Paguito** | WhatsApp bot with an LLM that understands text, audio and photos of receipts, replies with voice, and triggers the Open Payments flow ([repo](https://github.com/jorge-jrzz/Paguito)). |

**Lesson:** at the professional event the winner showed several Open Payments capabilities at once (split, multi-payer, quotes as a transparency tool) for a concrete industry, and matched what the CTO had said he wanted to see.

### UCT FinHub, June 2026

80 students. Judges: Alex Lakatos, Matthew de Haast (Fynbos), Allan Davids. Criteria: creative problem framing, passion, understanding of the problem and solution, innovation ([ITWeb](https://www.itweb.co.za/article/student-fintech-innovators-tackle-financial-challenges-at-uct-hackathon/KBpdgvpmGb67LEew), [ILF blog](https://interledger.org/news/beyond-hackathon-building-future-open-payments-through-collaboration)).

| Place | Project | What it did |
| --- | --- | --- |
| 1st | **Fireline** | Community-led micro-insurance that pays cash within hours of a fire in an informal settlement |
| 2nd | **Bokamoso** | Everyday purchases trigger automatic pension contributions, including for informal workers |
| 3rd | **Common Cents** | Turns informal cash income into authenticated payment records for credit and insurance |

No public repos found. A few months earlier, ILF set its own challenge at HackOMania 2026 in Singapore: **"community-powered emergency funds with instant money payouts"** ([community call](https://www.youtube.com/watch?v=3LUgUHOWfvI)). Emergency payouts are a theme ILF itself chose, and Fireline won with it.

---

## Patterns across the winners

| Pattern | Winners that used it |
| --- | --- |
| **Consent once, pay later** (a grant used for later payments) | Cache Money, SecureLifeCover, Bokamoso, Shabaha (per milestone) |
| **One payment, several parties** | VibePayments (split and group checkout), Spend Secure (earmarked merchants), Naartjie (HM) |
| **A new way to say yes** | Fingerprints (Coetsee & Campbell), face and voice (Haki Ando), email (Team 23), USSD (Cache Money), WhatsApp with voice (Paguito) |
| **The payment leaves a record** | Direla (credit history), Common Cents (proof of income) |
| **A safety net in the worst moment** | SecureLifeCover (funerals), Fireline (fires) |
| **Hardware or a physical demo** | Coetsee & Campbell |

What none of the winners did: start with a login screen, spend the pitch on the team or the stack, or present a generic payments app.

---

## What this means for us

### Building

- [ ] First milestone, Friday morning: one real payment through the Test Wallet, from request to completion. Use only the official SDK and docs; check anything AI writes against [openpayments.dev](https://openpayments.dev).
- [ ] No login, sign-up or password screens. Hard-code the demo users.
- [ ] Show where we bend the flow: for fiado, the pause between the grant and the payments, and the limit the wallet enforces.
- [ ] Give the project a name, a logo and one visual identity.
- [ ] Coding time is longer than ~9 hours: Ruta N closes at 18:00, but the official guide says "Sleep is for Sunday" and a virtual mentor team supports overnight hacking from home.

### Pitching

- [ ] Open with a person and a moment, not with the team or the stack.
- [ ] Show the four payment moments (request, authorization, execution, completion), live and as a recording.
- [ ] Say in one sentence why Open Payments is the right tool, and name what Bre-B can't do.
- [ ] One slide on what happens after the hackathon: who deploys it, how many people, which partner. That's what turns a 4 into a 5.
- [ ] One "key learning" about Open Payments itself, something we discovered building it. It's required content, and it's what ILF runs these events for.
- [ ] One storyteller, rehearsed until the five minutes feel easy, plus prepared answers to the questions in [PROBLEMS.md](PROBLEMS.md#questions-every-colombian-team-will-get).
- [ ] Use the official presentation template linked on the [Medellín page](https://interledger.org/hackathon/2026-hackathon-medellin/).

### Submitting (Saturday 11:00, changed on Oct 14)

- [ ] Code pushed to `main` on a public repo, **plus the demo video and slides uploaded to the team's Drive folder by 11:00** (it used to be 12:00).
- [ ] `AI_USAGE.md` and `/prompts` complete ([AI policy](https://interledger.org/hackathon/ai-policy/)).
- [ ] Every team member has finished the Platzi course or the Open Payments guide; the AI policy makes it mandatory.

---

## What changes in our ranking

Updates to the [judges' scorecard](PROBLEMS.md#judges-scorecard) in light of the above.

| Idea | Change | Why |
| --- | --- | --- |
| **K. Fiado as a grant** | Stays first, with a stronger case | It improves an existing practice (the participant guide's advice), pauses the flow the way Cache Money did, leaves a record like Direla and Common Cents, and is local and relatable. The new framing comes from ILF's own Colombia campaign: 66% of payments are still cash, and **95% of digital transfers stay inside the same institution** ([Beyond Access](https://interledger.org/blog/beyond-access-building-the-future-in-colombia/)). With Open Payments the tienda collects the cupo from whatever wallet the customer uses. Path beyond the hackathon: Puntored's tienda network, and savings-and-credit cooperatives (next row). |
| **C. Natillera + emergency fund** | Moves up, close to A | ILF chose "community-powered emergency funds with instant payouts" as its own 2026 challenge, and Fireline won with it. A Colombian version (the barrio fund that pays within hours after a landslide or a fire) uses recurring grants for contributions and a quorum before the payout. Risk: Alex Lakatos judged Fireline four months ago, so ours must clearly differ. |
| **A. Domestic wages with split** | Slightly down | Besides Kano, ILF grantee miPlata builds payroll plus remittances for unbanked Latinos and presents at the Oct 15 event in Medellín. Judges will compare. |
| **M. Agent with a mandate** | Unchanged | Fits "tweak, pause, extend", but nothing in ILF's materials asks for agents, and Round 1 still needs an excluded user. |
| **L. Caregiver with limits** | Slightly up | Haki Ando (2nd, 2025) shows that accessible ways to authorize payments win. |

### Two facts worth putting in the pitch

- **Open Payments complements Bre-B, it doesn't compete with it.** ILF grantee Fliqa made its first sandbox payment on Bre-B so a checkout can offer both, Bre-B for domestic and Interledger for cross-border ([report](https://community.interledger.org/elaoblak_537/fliqas-second-interim-project-report-2o4a)). Wava is testing a corridor where a Peruvian customer pays with a local QR and a Colombian merchant receives pesos ([intro](https://community.interledger.org/wava/wava-exploring-how-open-payments-could-connect-latin-americas-domestic-payment-rails-4nek)). Both are listed in the [Oct 13 grant roundup](https://interledger.org/blog/quarterly-grant-reports-and-updates-roundup/).
- **Cooperatives are an underserved group ILF is looking at.** Fliqa counts about 171 savings-and-credit cooperatives with over 4 million members in 23 departments. In roughly 40 municipalities a cooperative is the only financial intermediary, and most sit outside the Open Finance mandate without the technical capacity to interoperate. Fliqa is asking for contacts in that sector, and Antioquia has one of the strongest cooperative traditions in Colombia.

---

## What we couldn't find

- Repositories for Coetsee & Campbell, Team 23, Haki Ando, Fireline, Bokamoso and Common Cents, and the winners of the Oaxaca and CDMX student events.
- Slides from any winner. No decks were committed to the repos we cloned, and the 2024 and 2025 Devpost galleries are empty.
- A transcript of the second Medellín info session (Sept 29, 2026): captions are disabled on that video.
- Who exactly judges in Medellín. Alex Lakatos, Tímea Nagy and Ioana Chiorean are likely, given the pattern, but not confirmed.

## Sources

Official pages: [submission and judging](https://interledger.org/hackathon/submission-judging/), [FAQ with the scoring guide](https://interledger.org/hackathon/faq/), [AI policy](https://interledger.org/hackathon/ai-policy/), [Medellín page](https://interledger.org/hackathon/2026-hackathon-medellin/), [participant guide (PDF)](https://interledger.org/uploads/img/original/Hackathon_Survival_Guide_EN_Letter_7512f45ccb.pdf).

Videos (transcripts read): [Medellín info session, Sept 23, 2026](https://www.youtube.com/watch?v=i6zC-FUGq6s) · [Tips and Tricks, Tímea Nagy](https://www.youtube.com/watch?v=35BVQPCLTSk) · [Of the Ledger: Mexico student hackathons](https://www.youtube.com/watch?v=vNgSuIxtI2M) · [Mexico webinar with Alex Lakatos](https://www.youtube.com/watch?v=ATO1d9PfD0g) · [Community call, July 2024 (UCT 2024 winners pitch)](https://www.youtube.com/watch?v=96665lZTu3E) · [Community call, July 2025](https://www.youtube.com/watch?v=XuQZ7e0e9ho) · [Community call, April 2026 (HackOMania)](https://www.youtube.com/watch?v=3LUgUHOWfvI) · [Interledger on Campus](https://www.youtube.com/watch?v=W2zYiqAcU3I) · recaps: [UCT 2024](https://www.youtube.com/watch?v=_0SUbZMhrWA), [Cape Town 2024](https://www.youtube.com/watch?v=Pz6t4TGzaf4), [UCT 2025](https://www.youtube.com/watch?v=drZfYz7Eafc), [Mexico City 2025](https://www.youtube.com/watch?v=gj4uXQ1MmG4), [Oaxaca](https://www.youtube.com/watch?v=dePClpFEGpI), [Edomex](https://www.youtube.com/watch?v=cJvlMqHuCac), [CDMX](https://www.youtube.com/watch?v=yj4ASbd_cGM).

Posts and press: [Hack @ UCT 2024](https://interledger.org/news/hack-uct-2024-highlights-and-achievements-our-student-bootcamp-and-hackathon) · [Nov 2024 newsletter](https://community.interledger.org/interledger/latest-news-from-the-interledger-foundation-november-2024-a8d) · [UCT 2025](https://interledger.org/news/uct-financial-innovation-hub-and-interledger-foundation-hackathon) · [Direla](https://community.interledger.org/dyxta/direla-winners-ilf-x-finhub-25-5a7o) · [Fin Illuminaries](https://community.interledger.org/raibim/fin-illuminaries-the-interledger-x-innovation-hub-hackathon-5d0d) · [FlowFi](https://community.interledger.org/joshd/interledger-x-innovation-hub-hackathon-256h) · [Mexico City 2025 winners](https://interledger.org/news/building-real-solutions-interledger-hackathon-winners-2025) · [Finnosummit](https://www.finnosummit.com/en/global-talent-gathers-in-mexico-to-hack-the-future-of-payments/) · [UCT 2026, ILF blog](https://interledger.org/news/beyond-hackathon-building-future-open-payments-through-collaboration) · [EWN](https://www.ewn.co.za/2026/06/28/uct-master-s-students-win-financial-innovation-hub-hackathon) · [Beyond Access](https://interledger.org/blog/beyond-access-building-the-future-in-colombia/) · [Interledger comes to Colombia](https://interledger.org/news/interledger-comes-colombia-help-build-internet-opportunity) · [Grant roundup, Oct 13, 2026](https://interledger.org/blog/quarterly-grant-reports-and-updates-roundup/).
