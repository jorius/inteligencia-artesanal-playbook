# Competition

How crowded each kind of idea is, based on the public repositories from past Interledger hackathons, and which Medellín teams have already shown their hand. It complements [WINNERS.md](WINNERS.md) (what wins) and [PROBLEMS.md](PROBLEMS.md) (our candidates).

Research done on 2026-10-15.

## In short

- **Medellín is the first edition with themed awards.** Past events gave a podium (1st to 3rd) plus, at the summits, a community prize, so nobody has measured how teams split across Impact, Inclusion and Innovation. We estimate it from what teams built.
- **Payments for local merchants (QR, small vendors) is the most crowded theme by far:** 26% of all repos, 30% in Latin America. It has won at student events (Direla, Cache Money, Ocelon, YaYa, InterPyme), never at a summit.
- **Emergencies and insurance is the least crowded theme with the best record:** 4% of repos, two first places (SecureLifeCover 2024, Fireline 2026). Biometrics and accessibility is similar: 5% of repos, a first and a second place.
- **Inclusion will be the most contested award.** Inclusion-type themes appear in 43% of repos, Puntored's sponsorship pulls more teams in, and at least one well-prepared Medellín team (Tatú) targets it directly.

## Award formats over time

| Edition | Format |
| --- | --- |
| Costa Rica 2023 | Four challenge tracks (design, Open Payments, Web Monetization, TigerBeetle), 12 winners |
| UCT student hackathons 2024–2026 | 1st, 2nd, 3rd (plus honourable mentions) |
| Cape Town Summit 2024 | 1st, 2nd, 3rd and a community prize; criterion "fit between the use case and the APIs" |
| Mexico student hackathons 2025 | 1st, 2nd, 3rd, sometimes a special mention |
| Mexico City Summit 2025 | 1st, 2nd, 3rd and a community prize; three suggested themes: cross-border, financial inclusion, automating payments |
| **Medellín 2026** | **Four sponsor awards (Impact, Inclusion, Innovation, Community), no suggested themes** |

## How crowded each theme is

**Method.** We searched GitHub for repositories created during each hackathon window (UCT 2024, Cape Town 2024, UCT 2025, the Mexico student events, Mexico City 2025, UCT 2026, and other 2026 events up to Oct 15) that mention Interledger or Open Payments. We read their READMEs and kept the 280 that are actual Open Payments projects. Each was tagged with every theme its README mentions, so the shares add up to more than 100%. Keyword tagging is approximate, and many teams never publish a repo (Fireline, for example), so treat the figures as orders of magnitude.

| Theme | Share of 280 repos | Past winners in this theme |
| --- | --- | --- |
| Local merchants, QR, small vendors | 26% | Direla, Cache Money, Ocelon, YaYa, InterPyme (all student events) |
| Subscriptions, recurring payments, bills | 14% | SecureLifeCover, Bokamoso |
| Remittances, cross-border | 13% | Spend Secure; VibePayments in part |
| E-commerce, checkout, marketplace | 13% | PaDuki |
| No internet: USSD, SMS, offline | 11% | Coetsee & Campbell, Cache Money |
| Chatbots, WhatsApp, AI | 11% | Paguito (community prize), Direla |
| Transport, parking | 10% | Ocelon |
| P2P between people | 10% | YaYa, Paguito |
| Donations, crowdfunding | 9% | OpenFundsFO, Pet Patron, FlowFi (all 3rd places) |
| Credit, loans, BNPL | 9% | Direla (microlending) |
| Split and group payments | 7% | VibePayments |
| Education, students | 7% | OpenFundsFO, FlowFi, Shabaha |
| Tourism | 7% | VibePayments |
| Payroll, workers, freelancers | 6% | none |
| Credit history, income records | 5% | Direla, Common Cents |
| Tips, creators, Web Monetization | 5% | none |
| **Biometrics, accessibility** | **5%** | **Coetsee & Campbell (1st), Haki Ando (2nd)** |
| Micropayments, pay-per-use | 5% | none |
| **Emergencies, insurance, disasters** | **4%** | **SecureLifeCover (1st), Fireline (1st)** |
| Group savings (tandas, natilleras) | 3% | none, in at least four attempts |

Grouping the themes by the award they most naturally fit:

| Award | Themes counted | Share of repos |
| --- | --- | --- |
| Inclusion | Merchants and QR, USSD and offline, credit, credit history, group savings, accessibility | 43% |
| Impact | Remittances, payroll, education, transport, emergencies, donations | 39% |
| Innovation | Split payments, biometrics, micropayments, chatbots and agents | 24% |

## Medellín teams with public repositories

Reading public repos is fair; copying them is not.

| Team or repo | Idea | What it tells us |
| --- | --- | --- |
| **Tatú** ([repo](https://github.com/mauromaecha921-ship-it/test-openpayment)) | Government subsidies paid on demand: the agency approves a capped grant once, each beneficiary collects to their wallet or a Bre-B key, or in cash at an Efecty or Punto Red point that is reimbursed in seconds | A strong, well-prepared Inclusion contender aimed squarely at the sponsor (Punto Red). It ran a disposable pilot with real Test Wallet payments (Oct 10–14, 185 automated tests) and says the event code will be rewritten from scratch. It uses the same mechanism as our fiado idea: consent once with a cap, payments later. Pitch line: "Bre-B es la carretera; Tatú decide quién pasa, cuándo y cuánto." |
| VaquitaMuh ([repo](https://github.com/Luisr26/VaquitaMuhFront)) | Group money pots ("vaquitas") in COP with real Open Payments payments and a conversational assistant | Someone in Colombia is already on group savings (Aug 2026) |
| Pago Abierto ([repo](https://github.com/vicguty25/pago-abierto-mvp)) | Cross-border payment requests for LATAM freelancers | Already known (see PROBLEMS.md, idea F) |

One technical lesson from Tatú's notes: on the Test Wallet the access token for a grant lasts **10 minutes**, so an app that pays later (fiado, subsidies, recurring payments) must rotate the token. The SDK has a rotate call.

## What it means for us

- **If we stay with fiado (K), we share Tatú's mechanism and award.** Differentiate on who pays and why: the customer (not the government) sets her own cupo, the grant is locked to the tienda's incoming payment, and every on-time payment becomes her record. Or aim fiado at Impact instead of Inclusion.
- **Emergencies are the open lane.** Least crowded theme, two first places, and ILF chose it for its own 2026 challenge. The risk is looking like Fireline to Alex Lakatos, so the Colombian version has to be clearly different.
- **Merchant payments plus credit history is the most crowded corner.** It accounts for 26% of repos plus 14 repos that combine it with credit or records, Direla (1st 2025) and Common Cents (3rd 2026) already won with it, and Bre-B's interoperable QR already lets any merchant get paid from hundreds of entities.
