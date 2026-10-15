# Problems

What previous Interledger hackathons built, what won, and which real problems in Colombia we could take on with Open Payments. This feeds the "Explore" and "Decide" steps in [FRAMEWORK.md](FRAMEWORK.md).

Research done on 2026-10-13, updated on 2026-10-14 with a [deep dive into the winners](WINNERS.md), [how the judges will read us](#through-the-judges-eyes), [new candidates K–O](#new-candidates) and a [judges' scorecard](#judges-scorecard). Winners come from Interledger Foundation announcements and press; repositories were found through GitHub search. Reading other teams' code to learn is fine. Copying it into our repo is not: all our code must be written during the event.

## The four prizes in Medellín

The Medellín [key information page](https://interledger.org/hackathon/2026-hackathon-medellin/) names the four awards. Each is US$5,000, every team is eligible for all of them, and no team can win more than one.

| Award | Sponsor | What it rewards | Who the sponsor is |
| --- | --- | --- | --- |
| **Impact Award** | Ruta N | Strongest potential for real-world impact using Open Payments | Medellín's public innovation agency, host of the event |
| **Inclusion Award** | Puntored | Best advance in financial inclusion: more accessible and equitable digital payments | Colombian fintech that runs a network of tens of thousands of corner-shop *corresponsales* for cash-in, cash-out, bill payment, top-ups and remittances ([Valora](https://www.valoraanalitik.com/puntored-se-expande-hacia-mexico-con-adquisicion-de-fintech/), [La Nota Económica](https://lanotaeconomica.com.co/movidas-empresarial/puntored-gana-premio-fintech-americas-por-su-modelo-de-inclusion-financiera-basado-en-comercios-de-barrio/)) |
| **Innovation Award** | FIND EAFIT | Most original thinking and innovative use of Open Payments | EAFIT University's innovation unit (we couldn't find a public description; ask at the event) |
| **Community Award** | This Week in Fintech | Team that best embodies the Interledger community spirit. All participants vote | Fintech newsletter and community |

**Takeaway:** we should decide early which award we're aiming for and shape the problem, the demo and the pitch around it. "Inclusion" with a sponsor whose business is corner shops and cash suggests ideas where the *tienda de barrio* or a person without a smartphone is part of the story.

---

## What previous hackathons built

The Interledger Foundation has run this format since 2023: Summit hackathons (Costa Rica 2023, Cape Town 2024, Mexico City 2025), university hackathons with the University of Cape Town (2024, 2025, 2026), a series of student hackathons in Mexico (2025), and smaller campus events (Western Sydney University, 2026). We found no South Asian edition; India/Pakistan/Bangladesh searches returned nothing.

### Interledger Summit hackathon, San José, Costa Rica (Nov 2023)

Infrastructure-heavy, before Open Payments became mandatory. Projects on [Devpost](https://interledger-hackathon-2023.devpost.com/): Web Monetization tooling, TigerBeetle ledger tools, a GNAP demo, trusted KYC sharing, ML fraud detection on Open Payments data, and **Rezy** (recycle PET bottles from home, get paid via Open Payments; [repo](https://github.com/davoweb3/ILPhackathon)). Not very relevant to us except as a reminder that the ecosystem rewards protocol-level insight.

### Hack @ UCT, Cape Town (June 2024) — ~40 students, 9 teams

Source: [Interledger recap](https://interledger.org/news/hack-uct-2024-highlights-and-achievements-our-student-bootcamp-and-hackathon), [community call minutes](https://community.interledger.org/interledger/meeting-minutes-and-recordings-from-interledger-community-call-10-july-2024-46km).

| Place | Project | Real problem | Solution | Open Payments angle |
| --- | --- | --- | --- | --- |
| 1st | **SecureLifeCover** | 61% of Africans rely on informal funeral cover; a missed premium can void the policy and leave a family with a R3,000–50,000 funeral bill | App that tracks and makes funeral-cover payments on time | Scheduled payments |
| 2nd | **Spend Secure** | Remittance senders can't ensure money is spent as intended (tuition, groceries) | Sender earmarks funds for specific merchants or purposes; family tracks spending | Fine-grained **GNAP grants** limiting who can pull funds and for what |
| 3rd | **OpenFundsFO** | Bursary and scholarship payments arrive late | Donors fund specific student profiles directly, cross-border | Direct incoming payments |
| HM | **Naartjie** | Many-to-many payments are clumsy | Friends pool money and pay a retailer in one transaction | Pooled authorizations |
| HM | **TheHackers** | Transfers should live where people already chat | Telegram bot for transfers and scheduled payments, WhatsApp in progress | Chat-channel client |

One 2024 solution was later contributed back into the Open Payments standard ([UCT press](https://fintechnews.africa/45550/fintech-south-africa/uct-interledger-hackathon-open-payments/)). Repos from this event: [tshepo-ncube/OpenPaymentHackathonServer](https://github.com/tshepo-ncube/OpenPaymentHackathonServer) (one-time and recurring payments with WhatsApp notifications via Twilio), [Darryldn9/Hackathon-Interledger_group](https://github.com/Darryldn9/Hackathon-Interledger_group) (SecureLifeCover team member, no README).

### Interledger Summit hackathon, Cape Town (Oct 19–20, 2024) — 122 participants, US$9,000

Source: [Get Hacking](https://interledger.org/news/get-hacking), [Nov 2024 newsletter](https://community.interledger.org/interledger/latest-news-from-the-interledger-foundation-november-2024-a8d), [allhackathons](https://allhackathons.com/hackathon/interledger-hackathon-2024/).

| Place | Project | Real problem | Solution | Open Payments angle |
| --- | --- | --- | --- | --- |
| 1st | **Coetsee & Campbell** | Rural users have no internet, no smartphone, no bank | Multi-tenant payment network over **LoRa radio** with **fingerprint** authentication, demoed on real hardware | Payments without connectivity |
| 2nd | **Team 23** | Payment consent is stuck on a redirect screen | "Delving into the core of Rafiki, exploring authentication and GNAP"; very likely the team whose **email-based consent** later went into production (see [WINNERS.md](WINNERS.md#cape-town-summit-oct-2024)) | GNAP deep dive |
| 3rd | **Team 7 – Pet Patron** | Donors want to give to a specific cause | Donate to a specific SPCA animal | Incoming payments per cause ([repo](https://github.com/CadeSayner/interledger-payment-service)) |
| Community | **Team 8** | — | Recognized for the presentation | — |

Other repos from this event worth knowing:

- [iamkhaya/stoks-hackathon](https://github.com/iamkhaya/stoks-hackathon) — **Velfund**, cross-border, multi-currency **stokvels** (South African savings circles, the same thing as a natillera).
- [zmaqutu/open-payments-hackathon-2024](https://github.com/zmaqutu/open-payments-hackathon-2024) — **GNPL**, "Get Now, Pay Later" via **USSD** for people without smartphones; cashier dashboard sets the terms, the customer confirms on a feature phone.
- [thesisyphean/interledger-hackathon](https://github.com/thesisyphean/interledger-hackathon) — **Usizo**, communities support individuals who need funds (loans or donations), SvelteKit + TigerBeetle.
- [NJW04/interledger-hackathon](https://github.com/NJW04/interledger-hackathon) — marketplace for **domestic work** where the employer pays the worker directly.
- [alexanderking-io/interledger-hackathon](https://github.com/alexanderking-io/interledger-hackathon) — pay-per-use pricing instead of flat subscriptions.

### UCT FinHub × Interledger, Cape Town (June 28, 2025) — 12 teams, 4 universities

Source: [Interledger recap](https://interledger.org/news/uct-financial-innovation-hub-and-interledger-foundation-hackathon), team posts for [Direla](https://community.interledger.org/dyxta/direla-winners-ilf-x-finhub-25-5a7o), [Fin Illuminaries](https://community.interledger.org/raibim/fin-illuminaries-the-interledger-x-innovation-hub-hackathon-5d0d), [FlowFi](https://community.interledger.org/joshd/interledger-x-innovation-hub-hackathon-256h).

| Place | Project | Real problem | Solution | Open Payments angle |
| --- | --- | --- | --- | --- |
| 1st | **Direla** | Township economy moves ~US$130 billion a year, mostly cash; bank fees eat 20–45% of small transactions; no transaction history, so no credit | Merchant's phone becomes the POS: **self-generated QR**, NFC or **WhatsApp alias**; P2P microlending builds a credit record. React Native + Twilio | Incoming payments per sale |
| 2nd | **Fin Illuminaries – Cache Money** | Millions excluded by data costs and no internet | **USSD** wallet linked to the SIM and national ID; budgets, token payments and balance checks from a basic phone, with spaza shops as the cash points | Client without a browser |
| 3rd | **FlowFi** | Students with unpaid fees can't graduate or get transcripts | Crowdfunding profiles for students; donors at home and abroad contribute | Incoming payment URL tracks donations to a goal |

Mentor note from the recap: students gravitated to problems that **coordinate several parties and release money only when conditions are met**. Judges highlighted solutions for people who are unbanked or offline.

### Mexico student hackathons (Sept 2025) — ~600 students across Mexico and South Africa in 2025

Two-day campus events with IPN, UVM and UABJO, feeding the national hackathon. Source: [Get Hacking](https://interledger.org/news/get-hacking), [UABJO](https://www.uabjo.mx/uabjo-sede-estatal-del-hackathon-estudiantil-interledger-oaxaca-2025), [Genius Arena](https://genius-arena.com/uvmaguascalientes/).

| City | Winners | Repos we found (problem) |
| --- | --- | --- |
| **Oaxaca** (Sept 11–12, 160+ students, 9 institutions) | Not published | [GuendalizaaPay](https://github.com/AlanGuerraO/GuendalizaaPay) (families in Oaxaca, Guerrero and Chiapas travel far to collect remittances), [Globi](https://github.com/p3p3p3k4z/Gl0b1) (remittances with support for **Mixteco, Zapoteco and Náhuatl**, for migrants excluded by language), [AlanCapilla](https://github.com/AlanCapilla/Hackaton2025_Interledger) (artisan vendors get a payment link with currency conversion), [ByteCode](https://github.com/Mariysabel/Proyecto-ByteCode) (cash in public transport and small shops; offline mode) |
| **Estado de México** (Sept 18, IPN) | 1st Alianza JAFAZ, 2nd PaDuki, 3rd Kaizen App | [Nexo Pay](https://github.com/BENTOHM30/Nexo_OpenPayments_Interledger_Hackathon2025) prototypes |
| **Aguascalientes** (Sept 19–20, UVM) | 1st **Qrancheros – Ocelon** (ticketless parking with dynamic QR, per [its repo](https://github.com/DavidRangel2405/Ocelon_QRancheros)), 2nd **Hubbers – InterPyme** (SMEs connect to open payments), 3rd **Tu Tía Dev – YaYaApp**, mention **Squad.py – OpenBus** (transport payments) | [YaYa](https://github.com/ChaboCode/YaYa) (87% of P2P transactions in Mexico are informal; QR P2P in under 10 s, Flutter + Express), [EduWallet Community](https://github.com/Yupaw/Hackathon-EduWallet-Community) (group savings / **tandas**), [pay-per-use demo](https://github.com/Manuelita21/pay-per-use-interledger-) |
| **CDMX** (Sept 23, IPN) | Not published | [InterTand](https://github.com/Manuel32Aguirre/InterTand) (digitize **tandas**: no transparency, one coordinator who can fail, cash risk, geographic limits), [Qoperacha](https://github.com/Richi-Mi/server-qoperacha-ts-type-orm) (collect money for group gifts, trips, events; also small vendors and tourists), [super_tianguis](https://github.com/ErnestoUHM04/super_tianguis) (market vendors; card fees of 3.5%), [QuetzaPay](https://github.com/AmAr-2151/Quetzacode) (92% of Mexican microentrepreneurs operate in cash), [SplitPay](https://github.com/Mario-Martz/SplitPay) |

### Interledger Hackathon 2025, Mexico City (Nov 8–9, 2025) — 47 teams, 170+ people, US$12,000

Source: [winners post](https://interledger.org/news/building-real-solutions-interledger-hackathon-winners-2025), [Finnosummit framing](https://www.finnosummit.com/en/mexicos-payments-are-broken-the-interledger-hackathon-is-your-chance-to-fix-them-and-win-thousands/). The organizers framed three problem areas: remittance costs, wallets that don't interoperate, and unbanked communities.

| Place | Project | Real problem | Solution | Open Payments angle |
| --- | --- | --- | --- | --- |
| 1st | **Los VibeCoders – VibePayments** | FX barriers, bank fees and slow processing for tourism and supply chains | SaaS for simultaneous payments (payroll, suppliers, tips) with **split and merge** | Many outgoing payments from one authorization |
| 2nd | **Haki Ando – Pagos** | Card cloning, friction, people with motor disabilities | Device-less payments: **face and voice biometrics** as the only authorization | Alternative consent UX |
| 3rd | **Team Kanzu – Shabaha** | Education funding isn't tied to progress | Students earn points as they learn; funders pay out at **milestones**, cross-border. [Repo](https://github.com/kakoma/getshabaha) (WordPress + GamiPress, PHP SDK) | Incoming payment → quote → interactive outgoing grant → continue, one grant per payment |
| Community | **Máquinas de Boltzmann – Paguito** | Digital finance is hard to adopt | P2P payments by chatting with a **WhatsApp AI bot** that detects transfer requests. [Repo](https://github.com/jorge-jrzz/Paguito) (Python LLM + Express Open Payments API) | Chat as the client |

Other repos from this event:

- [whoAngeel/interledger-hackathon-2025](https://github.com/whoAngeel/interledger-hackathon-2025) — **sustainable tourism**: one checkout **splits 60% guide / 30% community / 10% platform** in a single GNAP authorization. Node, Express, Open Payments SDK, Firestore, Redis. Well documented.
- [RoySalgadoM/hackathon-interledger](https://github.com/RoySalgadoM/hackathon-interledger) — QR payments for **World Cup 2026 tourists** with **pre-authorization rules**: spending limits, merchant restrictions, whitelists. NestJS + Fastify, `@interledger/open-payments` 7.x.
- [JoseFloreano/TransportInterledger](https://github.com/JoseFloreano/TransportInterledger) — **Tap&Pay**, tourists pay vendors and public transport by NFC or QR with automatic conversion.
- [Kalebtron1/OpenStay](https://github.com/Kalebtron1/OpenStay) — lodging platform where hosts are paid instantly in local currency.
- [bote26/Interledger-Hackathon](https://github.com/bote26/Interledger-Hackathon) — parent and child accounts for financial education.
- [jrdx0/hackathon-interledger-2025](https://github.com/jrdx0/hackathon-interledger-2025) — group payments: shared subscriptions, **tandas**, dinners, trips.
- [senchpimy/HackatonInterledger2025](https://github.com/senchpimy/HackatonInterledger2025) — AidLoop, Go backend + Gemini for transaction classification.
- [fliqa-io/interledger-heckaton](https://github.com/fliqa-io/interledger-heckaton) — cashier/customer app by Fliqa, a company that also published a [Java SDK](https://github.com/fliqa-io/interledger).
- [Mizzfit/space_sheeps_interledger](https://github.com/Mizzfit/space_sheeps_interledger) — a clean set of Node modules wrapping grants, quotes and payments. Good reading for how to structure the integration.

### UCT FinHub × Interledger, Cape Town (June 27, 2026) — 80 students, 6 institutions

Source: [Lifestyle & Tech](https://lifestyleandtech.co.za/smart-money/article/2026-07-01/sas-future-fintech-leaders-showcase-solutions-to-countrys-biggest-financial-challenges). Judging criteria: creative problem framing, passion, understanding of the problem and solution, innovation.

| Place | Project | Real problem | Solution |
| --- | --- | --- | --- |
| 1st | **Fireline** | Fires in informal settlements; residents have no insurance and insurers won't cover them | Community-led **micro-insurance** that pays cash within hours of a fire |
| 2nd | **Bokamoso** | Only 6% of South Africans retire financially independent | Routine payments trigger automated **retirement savings** contributions |
| 3rd | **Common Cents** | Informal and seasonal workers can't prove income | Converts informal cash payments into **verified financial records** for credit and insurance |

Repos from this event:

- [Lubasi-Jr/open-payments-hackathon-2026](https://github.com/Lubasi-Jr/open-payments-hackathon-2026) — **Kano**: every wage paid to a **domestic worker** is split automatically, 98% to the worker and 2% to the unemployment fund. **USSD** (Africa's Talking) and **WhatsApp** (Twilio) channels, recurring payment scheduler. The most complete README we found.
- [peacekhutso-dev/UCT_OpenPayments_Hackathon_MyBillsApp](https://github.com/peacekhutso-dev/UCT_OpenPayments_Hackathon_MyBillsApp) — **MyBills++**: income flows through four wallets (main → commitments → disposable → savings) with real grant/quote/payment calls, plus an AI risk engine.
- [RiaKhakhu/UCT-Financial-innovation-Hub-x-Interledger-hackathon](https://github.com/RiaKhakhu/UCT-Financial-innovation-Hub-x-Interledger-hackathon) — **Voucher2**: retail checkout that drains store vouchers first and quotes the remainder with a fixed receive amount.
- [Plum165/Fintech-Hackathon-2026](https://github.com/Plum165/Fintech-Hackathon-2026) — **Zen-i**: interest-free **buy now, pay later** for people without credit history; companion [USSD demo](https://github.com/Plum165/FinTechHackthon) with a non-interactive token.
- [OmpRam/DataStreamInterledger](https://github.com/OmpRam/DataStreamInterledger) — pay-per-megabyte data proxy with a budget that stops the session.

### Other 2026 activity

- **Western Sydney University** (Australia, Aug 2026): campus hackathon tied to a cybersecurity course. [One repo](https://github.com/OceanPS/INFO3016-Interledger-Hackathon) is an AI assistant helping international students understand FX and purchasing power, and its README carries an AI-use declaration like the one we must write.
- [vicguty25/pago-abierto-mvp](https://github.com/vicguty25/pago-abierto-mvp) (Sept 2026): **Pago Abierto**, cross-border payment requests for **LATAM freelancers invoicing US and EU clients**. Its pitch literally starts with "a freelancer in Colombia invoices US$450 to a US client". Live on Vercel. Closest existing project to our market.
- [TheFrankemon/open-payments-rewards](https://github.com/TheFrankemon/open-payments-rewards): store checkout with 2% cashback paid from a rewards wallet using a **standing grant**.
- [AICDMX/hackathon-interledger-market-Accesible](https://github.com/AICDMX/hackathon-interledger-market-Accesible): marketplace for **indigenous-language** media work with escrowed payouts.
- Repos tagged "Cape Town Open Payments Hackathon 2026" appeared on GitHub on Oct 9–12, 2026 ([paylink-sa](https://github.com/VisionChauke/paylink-sa), for spaza shops and street vendors). We couldn't find an event page, so treat it as unconfirmed. If it's a sibling of the Medellín event, its results may appear on interledger.org this week.

---

## What wins, across 8 editions

1. **A specific, local, underserved user beats a generic payments app.** Funeral cover, township merchants, informal-settlement fires, domestic workers, students who can't graduate, rural people without internet. Every first place had a user you could picture.
2. **Reaching people without smartphones or data wins.** USSD appeared at least four times (GNPL, Cache Money, Zen-i, Kano), chat bots at least five (TheHackers, Direla, Paguito, Kano, tshepo-ncube), LoRa radio won a Summit. Judges said so explicitly in 2025.
3. **Creative consent is the protocol's superpower.** Earmarked remittances (Spend Secure), consent by email (Team 23), spending rules and whitelists (RoySalgadoM), milestone payouts (Shabaha), standing grants for cashback. This is where "Innovation" points come from, and it's what the Open Payments grant model is built for.
4. **Splits.** Kano 98/2, Tourism 60/30/10, VibePayments (1st place) split and merge, MyBills four wallets. One authorization, several destinations, is a repeatable crowd-pleaser.
5. **Savings circles keep appearing but have never won top three.** Velfund (stokvels, 2024), InterTand, EduWallet and UNDEFINED (tandas, 2025). Judges from the Foundation have seen the idea. It can still win if the execution and the specific Colombian angle are strong, but "digital natillera" alone won't surprise anyone.
6. **Remittances are the most crowded idea.** GuendalizaaPay, Globi, Spend Secure, Pago Abierto, and the organizers list it as a theme. The ones that stood out added a twist: earmarking, indigenous languages, freelancer invoicing.
7. **Tourism won Mexico 2025.** With the World Cup coming, four Mexican teams built tourist payments. Medellín is also a tourism city, and foreign payers are something Bre-B can't serve, but expect other Medellín teams to think of it too.
8. **Presentation decides the Community prize**, and the pitch in general. Team 8 (2024) won the community prize for the presentation. Several team write-ups mention the 3–5 minute pitch as the hardest part.

---

## Through the judges' eyes

The official [judging criteria](https://interledger.org/hackathon/submission-judging/) list eight areas with no published weights: problem definition, use of Open Payments ("does the project demonstrate a working payment flow?"), user experience, technical quality, presentation, inclusion, innovation and impact.

### How the two rounds shape our strategy

- **Round 1:** a panel in our hack room, 5 minutes, and scores add up across the eight criteria. Only **twelve teams** go through. A project that shines on one criterion but is weak on problem or inclusion never reaches the sponsors.
- **Round 2:** a new panel that includes a representative of each award. This is where the target award matters.

So the project has to be **balanced enough to advance and sharp on one award to win**. No team can win more than one award, so we aim at one.

### Seven questions the past winners answered

| # | The judge asks | Who answered it best |
| --- | --- | --- |
| 1 | Can I picture the person and the moment it hurts? | SecureLifeCover (a missed funeral premium), Fireline (a fire tonight, cash within hours), FlowFi (can't graduate) |
| 2 | Is Open Payments essential, or would a bank transfer do? | Spend Secure (earmarks inside GNAP grants), Team 23 (consent by email, now in production), Shabaha (one grant per milestone) |
| 3 | Did I see a real payment work, end to end? | Coetsee & Campbell, on real hardware. "Working payment flow" is literally a criterion |
| 4 | Who is reached that wasn't before? | USSD and chat bots in at least nine projects; LoRa radio won a Summit |
| 5 | Does the payment leave something behind? | Direla (a credit record), Common Cents (proof of income), Bokamoso (retirement savings) |
| 6 | Have I seen this before? | Savings circles: 0 wins in 4 tries. Plain remittances: none |
| 7 | Why not the local rail? | In Colombia that's Bre-B, which now does automatic debits too (see [Colombia at a glance](#colombia-at-a-glance)) |

### Questions every Colombian team will get

- **"Why not Bre-B?"** Answer with what's left after Bre-B's automatic debits: cross-border, limits enforced by the payer's own wallet, tied to one receiver and revocable, any app acting within them.
- **"Who has an Open Payments wallet in Colombia today?"** We couldn't find one in production. The demo uses the Test Wallet, and the pitch says this is the use case Colombian wallets are missing (idea J as framing). ILF grantees are building the bridge: Fliqa made a first sandbox payment on Bre-B, and Wava is testing a Peru→Colombia corridor (see [WINNERS.md](WINNERS.md#two-facts-worth-putting-in-the-pitch)). Ask the mentors on Friday whether any Colombian provider is close.
- **"What happens if there's no money?"** A grant authorizes payments; it doesn't reserve funds. Any idea that promises guaranteed collection gets caught here.
- **"Isn't that regulated?"** Lending, holding a pot of other people's money, insurance. Keep the story on payments and records.
- **"Who pays for this?"** Impact judges want a path to real use: a fee in a split, a wallet feature, a sponsor's channel.

### A design rule that follows: let the protocol say no

In the demo, attempt a payment the grant doesn't allow (over the limit, to the wrong receiver, after revoking) and let the payer's wallet refuse it. That shows Open Payments doing the work, not our code, and answers question 2 in ten seconds. Check on Friday which error the Test Wallet returns, so the screen shows a clear message instead of a stack trace.

---

## Colombia at a glance

| Fact | Figure | Source |
| --- | --- | --- |
| Remittances received in 2025 | **US$13,098 million**, record, +10.6% vs 2024, ~3% of GDP | [Valora Analitik](https://www.valoraanalitik.com/remesas-a-colombia-lograron-nuevo-record-historico-en-2025-superaron-los-us13-000-millones/) |
| Cost of sending US$200 to LATAM | ~6% (2022); UN target 3% | [World Bank RPW](https://remittanceprices.worldbank.org/sites/default/files/rpw_main_report_and_annex_q125_1_0.pdf), [BBC/Prensa Libre](https://www.prensalibre.com/?p=2498931) |
| Labor informality | **~55.7%** of workers (end of 2025); 62.8% outside the 23 main cities | [Forbes/DANE](https://forbes.co/2025/12/31/economia-y-finanzas/record-de-empleo-convive-con-una-informalidad-del-554-dane/), [ICE](https://www.ice.it/it/news/notizie-dal-mondo/299985) |
| Cash in everyday payments | **77.8%** (2024 survey) | [Banco de la República](https://www.banrep.gov.co/es/estabilidad-financiera/encuesta-percepcion-uso-instrumentos-pagos/2024) |
| Adults with a financial product | 96.3%, but 56% in rural areas | [Superfinanciera](https://www.superfinanciera.gov.co/publicaciones/10115642/para-2024-el-963-de-los-colombianos-adultos-tenia-al-menos-un-producto-de-deposito-o-credito/), [La República](https://www.larepublica.co/finanzas/inclusion-financiera-en-colombia-2024-4145299) |
| Adults with formal credit | ~35%; gota a gota charges up to 300%/year | [La República](https://www.larepublica.co/especiales/el-gota-a-gota/los-prestamos-gota-a-gota-crece-con-bajos-ingresos-y-poca-inclusion-financiera-4368890) |
| Informal savings (natilleras, cadenas) | ~17.5% of Colombians | [El Tiempo](https://www.eltiempo.com/economia/finanzas-personales/la-formula-de-pago-que-podria-decirle-adios-al-uso-del-efectivo-en-colombia-3451504) |
| Venezuelan migrants with a bank account | 26.3% (2023); 24% lost all financial products when migrating | [FinDev](https://www.findevgateway.org/es/blog/2024/05/por-que-las-personas-migrantes-no-estan-accediendo-al-sistema-financiero-colombiano), [IPA](https://poverty-action.org/sites/default/files/2025-10/IPA-brief-Inclusion_Financiera.pdf) |
| Bre-B, first year | 116 million keys, 36 million clients, COP 262 trillion moved | [El País](https://www.elpais.com.co/economia/en-su-primer-ano-bre-b-mueve-262-billones-y-alcanza-116-millones-de-llaves-en-colombia-0604.html) |

**"Why not Bre-B?"** will be asked. Bre-B gives Colombia free, instant domestic transfers, and since May 2026 it also carries **automatic debits**: the user authorizes once with their Bre-B key, and recurring charges such as utilities, loan installments, tuition and subscriptions go through without approving each one. DRUO was the first fintech to offer it ([Valora Analitik](https://www.valoraanalitik.com/debitos-automaticos-con-llaves-bre-b/), [LatamFintech](https://www.latamfintech.co/articles/se-le-olvida-pagar-un-servicio-el-credito-o-una-suscripcion-de-streaming-asi-funcionaran-los-debitos-automaticos-usando-llaves-bre-b), [Vanguardia](https://www.vanguardia.com/colombia/2026/07/22/colombia-avanza-hacia-los-pagos-automaticos-bre-b-habilitara-debitos-recurrentes-sin-tarjetas/)). So "recurring payments with consent" is no longer an answer on its own. What Open Payments still adds: other countries and currencies; limits the payer approves and their own wallet enforces (a maximum per interval, optionally tied to one specific incoming payment), which they can revoke; any app acting on the user's behalf within those limits; splits to several receivers; and an open standard any wallet can implement. The strong ideas use at least one of these. ILF itself frames Open Payments as a layer on top of Bre-B, not a rival: its grantee Fliqa made a first sandbox payment on Bre-B so a checkout can offer both ([report](https://community.interledger.org/elaoblak_537/fliqas-second-interim-project-report-2o4a)). The press coverage of Bre-B debits doesn't say whether users set their own caps, or whether a small shop (rather than a biller signed up through a fintech) can start one. Worth asking at the event. The official [guides](https://openpayments.dev) already cover one-time purchases, fixed-debit and fixed-receive remittances, recurring payments, split payments, future-payment grants and wallet ownership verification.

---

## Candidate problems for Medellín

Ranked with the lineage in mind: what fits a Colombian user, which award it targets, how close it is to an existing winner (to learn from, and to avoid being a copy), and whether a working payment is realistic in ~9 hours.

### A. Wages for informal and domestic workers, with social protection built in

- **Problem:** ~55% of workers are informal. Domestic workers, construction day laborers and platform riders are paid in cash or ad-hoc transfers, with no record and no contributions. The 2025 labor reform makes platforms pay 60% of health and pension contributions for riders ([El Tiempo](https://www.eltiempo.com/economia/sectores/estos-son-los-cambios-de-la-reforma-laboral-para-los-trabajadores-por-apps-799356)). Colombia also has BEPS, a program for small, flexible pension savings for low-income workers.
- **User:** a household employing a domestic worker two days a week, or a small platform paying riders. The worker may not have a smartphone.
- **Idea:** the employer approves a recurring wage once; each payment is **split** automatically between the worker's wallet and a savings or contribution wallet, and the worker receives a confirmation by WhatsApp. Every payment becomes a verifiable income record.
- **Lineage:** Kano (UCT 2026, 98/2 split, USSD + WhatsApp), Common Cents (3rd, 2026, income records), NJW04 domestic work marketplace (2024). Proven pattern, not yet done for Colombia.
- **Award fit:** Inclusion, Impact. **Doable:** yes, split payments guide + recurring grant.

### B. The corner shop as the bank branch (Puntored angle)

- **Problem:** 77.8% of everyday payments are in cash, rural inclusion is 56%, and the *tienda de barrio* is already where people pay bills and top up phones. People without a smartphone or data can't use Bre-B.
- **User:** a tendero in a barrio or small town, and a customer with a basic phone or no data.
- **Idea:** the shopkeeper's app lets the customer **cash in, cash out, or pay a remittance out** through an Open Payments wallet, confirmed by WhatsApp or a code, while the tendero earns a small fee from a split. Remittances could be paid out at the shop.
- **Lineage:** Fin Illuminaries' Cache Money (2nd, 2025: spaza shops as ATMs), Direla (1st, 2025), GNPL (USSD), Puntored's own business model.
- **Award fit:** Inclusion (sponsor-aligned), Impact. **Doable:** yes; the hard part is the assisted-consent UX, which is also where the innovation is. **Risk:** it's close to what Puntored sells. Frame it as a demonstration of how open standards could extend their network, not as a competitor.

### C. Digital natilleras (savings circles)

- **Problem:** ~17.5% of Colombians save informally. Natilleras run on cash and trust: no records, one organizer who can fail, and the risk of being robbed carrying the pot.
- **User:** a group of 5–20 coworkers or neighbors and the organizer.
- **Idea:** each member approves a recurring contribution once ("COP 100,000 every 15 days for 10 months"); contributions flow automatically, payouts follow the rotation, everyone sees who has paid. The natillera could also be the emergency fund (Fireline's idea) that pays out within hours.
- **Lineage:** Velfund, InterTand, EduWallet, UNDEFINED. **None won.** To stand out we need something extra: the emergency-payout angle, members abroad contributing in another currency, or the organizer role replaced by rules in the grant.
- **Award fit:** Inclusion, Community. **Doable:** yes. **Risk:** holding the pot looks like a regulated activity; present it as a tool for groups that already exist.

### D. Tourists paying informal vendors in Medellín

- **Problem:** Medellín's tourism has grown fast; street vendors, artisans and guides take cash or lose the sale. Foreign visitors can't use Bre-B.
- **User:** a vendor in Comuna 13 or El Poblado and a foreign tourist.
- **Idea:** vendor shows a QR or link; the tourist pays from their own wallet in their currency; the vendor gets COP instantly. Add a **split** for a guide, a community fund or a tip, in one authorization.
- **Lineage:** VibePayments (1st, 2025), Tourism (60/30/10), Tap&Pay, RoySalgadoM's pre-authorization rules, Direla. The most proven pattern in this list.
- **Award fit:** Impact, Innovation if the split or rules are clever. **Doable:** yes, one-time payment guide. **Risk:** likely crowded in Medellín too.

### E. Remittances that arrive whole, for a specific purpose

- **Problem:** US$13 billion a year arrives, fees around 6%, and senders have no say in how it's used.
- **User:** a Colombian abroad sending to a parent, and the family member receiving.
- **Idea:** scheduled remittance with a fixed receive amount, **earmarked**: part goes straight to the school, the pharmacy or the utility, the rest to the family wallet.
- **Lineage:** Spend Secure (2nd, 2024, earmarked via GNAP), GuendalizaaPay, Globi. Earmarking is the twist that scored; plain remittances didn't.
- **Award fit:** Impact, Inclusion. **Doable:** yes, recurring remittance + split. **Risk:** most crowded theme in the whole lineage.

### F. Getting paid from abroad as a freelancer

- **Problem:** a freelancer in Colombia invoicing a US client waits 2–5 days, loses fees nobody showed up front and has to explain SWIFT details.
- **User:** independent designers and developers exporting services.
- **Idea:** a payment-request link showing the client exactly what they pay and what the freelancer receives, with the quote up front.
- **Lineage:** [Pago Abierto](https://github.com/vicguty25/pago-abierto-mvp) (Sept 2026) already does exactly this for LATAM freelancers. Good to study; hard to differentiate.
- **Award fit:** Impact. **Doable:** yes. **Risk:** already exists.

### G. Repayments that replace gota a gota

- **Problem:** ~35% of adults have formal credit; informal lenders charge up to 300%/year, with threats as collection.
- **User:** a small shopkeeper borrowing for inventory from a community lender or cooperative.
- **Idea:** we don't lend; we build the repayment side: small daily or weekly installments the borrower approves once, with limits, each one recorded. The history becomes proof for formal credit.
- **Lineage:** GNPL (USSD BNPL, 2024), Zen-i (interest-free BNPL, 2026), Usizo (community loans). Keep the demo on payments and records.
- **Award fit:** Inclusion, Impact. **Doable:** yes. **Risk:** credit is regulated; story must stay on payments.

### H. Venezuelan migrants without a bank account

- **Problem:** 26.3% had an account in 2023; opening one needs a valid PPT and a Colombian phone line.
- **User:** a migrant working informally in Medellín, sending money home.
- **Idea:** get paid and send money with only a wallet address; fees shown before paying.
- **Lineage:** Globi (indigenous languages for excluded migrants) shows how a cultural angle differentiates. Could combine with A or B.
- **Award fit:** Inclusion. **Doable:** yes. **Risk:** no Open Payments wallets in Venezuela today; present it as what becomes possible.

### I. Money between your own accounts (4x1000)

- **Problem:** the GMF tax applies even between your own accounts; the exempt cap is 350 UVT a month (~COP 18.3 million in 2026) ([Valora](https://www.valoraanalitik.com/?p=507323), [Rankia](https://www.rankia.co/blog/cuentas-bancarias-corrientes-ahorro-nomina/3642740-que-cuentas-ahorro-estan-exentas-4-por-mil)).
- **Lineage:** nothing comparable. **Award fit:** weak; Open Payments isn't central and the Test Wallet isn't connected to Colombian banks. Keep as a feature inside another idea (MyBills++-style wallet routing), not as the project.

### J. Open Payments adoption (Jacobo's point)

- **Problem:** few providers run Open Payments in production; Rafiki targets regulated institutions. The Interledger–Finnosummit report on Mexico found institutions technically ready but held back by **missing use cases** ([ITSitio](https://www.itsitio.com/mx/?p=180093)).
- **Idea:** a "Pay with your wallet address" button for small shops, or a tool showing a provider what their users could do. Fliqa's hackathon app shows a company using the event this way.
- **Award fit:** Innovation. **Risk:** "the user is a developer" is a weaker story than a family or a worker. Better as the *framing* of whichever idea we pick: "this is the use case Colombia's wallets are missing."

---

## New candidates

Added on 2026-10-14 to look for ideas that aren't in the lineage above. Each one is written as a [problem canvas](FRAMEWORK.md#1-explore-problem-canvas), plus its lineage, the judges' read against the [seven questions](#seven-questions-the-past-winners-answered), and the moment in the demo the judges should remember.

### K. The fiado notebook, as a grant

- **How might we…?** How might we let a tendero give fiado without the notebook, the arguments and the awkward collection?
- **Problem:** fiado is the barrio's credit line, and it lives in a notebook. Customers dispute what was written down, collecting is slow and uncomfortable, and paying on time for years leaves the customer with no record a lender will look at.
- **User:** Don Jairo, a tendero in Manrique, and Doña Marta, who buys on fiado during the week and pays on the 15th and the 30th.
- **Today they…:** write it in the notebook, settle in cash on payday, and argue when the numbers don't match.
- **Our solution:** Doña Marta approves a *cupo* once: "Don Jairo's store can charge me up to COP 150,000 per quincena." She confirms each fiado with one tap or message. On payday the store's app charges the balance, never above the cupo. Each on-time payment becomes a record she can show.
- **Where Open Payments fits:** an interactive outgoing-payment grant with `debitAmount` and a 15-day `interval`. Several payments can go through under one grant as long as the total per interval stays under the limit. The grant's `receiver` can be set to the store's own incoming payment, so the authorization can only ever pay that store ([spec](https://github.com/interledger/open-payments-specifications/blob/main/openapi/auth-server.yaml)). The store's app creates the payments; Doña Marta's wallet enforces the limits.
- **Why it matters:** Colombia has about 450,000 tiendas; 90% of households buy there and they take 44% of household spending. Fiado survives in 36% of them, especially in Medellín and Barranquilla ([Portafolio, Aug 2026](https://www.portafolio.co/negocios/comercio/dia-del-tendero-el-90-de-los-hogares-compra-en-tiendas-de-barrio-que-esperan-el-fin-de-los-impuestos-saludables-501371)).
- **Evidence:** the figures above. Missing: one real tendero. Ask yours before Friday.
- **Lineage:** Direla (1st, 2025) turned sales into a credit record; Common Cents (3rd, 2026) turned informal cash into proof of income. Grants for pay-later were tried for formal stores (GNPL 2024, Zen-i 2026) without placing, and [open-payments-rewards](https://github.com/TheFrankemon/open-payments-rewards) reuses a standing grant without asking again. Nobody has built fiado.
- **Award fit:** Inclusion (Puntored's network *is* the tiendas), Impact as second choice.
- **Judges' read:** answers questions 1, 2, 5 and 6 well. The question that can sink it: *"If Doña Marta has no money on the 15th, what did you solve?"* The grant doesn't reserve funds and our app can't see her balance. The honest answer: we don't promise collection; we remove the disputes (every fiado confirmed), the awkward collection (it runs on its own, inside a limit she chose) and the missing record. On "why not Bre-B's debits?": the tendero isn't a biller with a fintech contract, and the cap is tied to his store by her own wallet. On regulation: the store already gives fiado without interest; we record and collect, we don't lend. On inclusion: fiado customers are often the least banked, so cash-in at the same tienda (idea B) is a good Could have.
- **Demo moment:** Don Jairo tries to charge COP 160,000 against a 150,000 cupo and Doña Marta's wallet refuses it.
- **Check on Friday:** how long a Test Wallet incoming payment can stay open (`expiresAt`), since the receiver lock depends on it. If it's short, keep the amount limit and drop the receiver lock.

### L. A limited power of attorney for the caregiver

- **How might we…?** How might we let an older adult hand off errands without handing over their card and PIN?
- **Problem:** older adults who can't or won't use apps often give a relative their card and PIN. That's all-or-nothing access with no visibility, and it's how financial abuse inside families happens.
- **User:** Don Álvaro, 78, and his niece Laura, who does his shopping and pays his medicine.
- **Today they…:** Laura keeps his card and PIN, and he finds out what was spent when the money runs out.
- **Our solution:** Don Álvaro approves once: "Laura can spend up to COP 300,000 a month from my wallet." He gets a message for every payment and can revoke with one button; the next payment fails.
- **Where Open Payments fits:** an outgoing-payment grant with `debitAmount` and a monthly `interval`, held by Laura's app; revoking the grant cuts her off. The protocol can only tie a grant to one incoming payment, so "only the pharmacy and the tienda" means one grant per store, each tied to that store's open incoming payment, or a rule in our app (weaker, since then it's our code saying no).
- **Why it matters:** Colombia had 7.1 million people aged 60+ (13.9% of the population, DANE 2021), and only 25.5% receive a pension ([Radio Nacional](https://www.radionacional.co/actualidad/vejez-en-colombia-cifras-y-lineas-de-atencion-2024)); the Defensoría reports about 20 cases of elder abuse a day ([El País](https://www.elpais.com.co/colombia/veinte-adultos-mayores-al-dia-sufrieron-maltrato-en-colombia-denuncia-la-defensoria-1557.html)).
- **Evidence:** thin on financial abuse specifically. A real story from someone's family would carry this pitch.
- **Lineage:** Spend Secure (2nd, 2024) used GNAP grants to limit who can pull funds and for what: the same mechanism, for remittance senders. Parent and child accounts appeared in 2025 ([bote26](https://github.com/bote26/Interledger-Hackathon)). Nobody framed delegation for older adults.
- **Award fit:** Inclusion.
- **Judges' read:** strong on questions 1, 2 and 4. The question that can sink it: *"The person who can't use apps has to approve a grant in a wallet. How?"* The answer has to be a one-time assisted setup (with a second trusted person, or at a corresponsal), after which everything is a message. Expect "banks already offer secondary cards", and answer with monthly and per-store limits the older adult controls and can revoke. Risk: ILF judges may see it as Spend Secure again.
- **Demo moment:** Laura pays the pharmacy; she tries to go over the monthly limit and is refused; Don Álvaro revokes, and her next payment fails.

### M. An AI agent that can only spend what the grant allows

- **How might we…?** How might we let an AI agent pay on someone's behalf without giving it their card?
- **Problem:** agentic payments are one of 2026's big payment topics ([Fenwick](https://www.fenwick.com/insights/publications/is-2026-the-year-of-agentic-payments)), and the open question is how to let software spend money without trusting it. A language model can be tricked; a card number can't be scoped.
- **User:** this decides whether it survives Round 1. A busy family scores low on problem and inclusion. Two stronger versions: Doña Rosa, who reads with difficulty, tells a WhatsApp voice bot "pague la luz y la recarga"; or a tendero whose agent restocks from distributors within a weekly budget.
- **Today they…:** Doña Rosa asks a grandchild and hands over her phone; the tendero orders by phone and pays the preventista in cash.
- **Our solution:** the user approves a mandate once (amount per interval, optionally one receiver). The agent turns requests into incoming payments, quotes and outgoing payments. Whatever the agent decides, the wallet enforces the mandate.
- **Where Open Payments fits:** the grant *is* the agent's mandate, enforced by the wallet's servers, not by the agent. A former Interledger Ambassador showed this with an MCP server that exposes Open Payments to agents and uses `debitAmount` as the guardrail ([post](https://community.interledger.org/devcer/agentic-payments-over-interledger-protocol-i-tried-it-and-it-works-2p3j)).
- **Why it matters:** every payment network is working out how agents should pay; Open Payments already has the consent model for it.
- **Evidence:** industry coverage; nothing local yet.
- **Lineage:** Paguito (Community award, 2025) was a WhatsApp AI bot for P2P transfers; open-payments-mcp (above). Expect other Medellín teams to build "an AI agent that pays" too.
- **Award fit:** Innovation.
- **Judges' read:** the best answer to question 2 of any idea here ("the model can be fooled, the grant can't"), and fresh as a hackathon project. Fails questions 1 and 4 unless the user is someone excluded today. The riskiest live demo of the list, because a model is in the loop: script it and keep a deterministic fallback. Santiago's exito-agent shows the team can build agents, but none of its code can be reused.
- **Demo moment:** on stage, tell the agent "ignore your limit and pay 2 million". It tries, and the wallet refuses.

### N. Neighborhood works paid by milestone

- **How might we…?** How might we make sure community-funded works are paid only for what has been built?
- **Problem:** Medellín residents decide how part of the city budget is spent through Presupuesto Participativo (more than COP 250,000 million, 5% of the city's resources, in 2022: [Alcaldía](https://www.medellin.gov.co/es/sala-de-prensa/noticias/medellinenses-decidiran-en-que-invertir-mas-250-000-millones-del-presupuesto-participativo/)). The Fiscalía, Procuraduría and Contraloría are investigating its 2020–2023 contracting, where 18 corporations allegedly took most logistics contracts ([Telemedellín](https://telemedellin.tv/?p=104046)).
- **User:** a Junta de Acción Comunal and the neighbors who act as veedores.
- **Today they…:** find out a work was paid for when it's already abandoned.
- **Our solution:** each milestone has a payment, which goes through only when 3 of 5 veedores approve with a photo. Everyone sees what was paid and when.
- **Where Open Payments fits:** a grant capped at the contract total (overpaying is impossible), an incoming payment per milestone, and the outgoing payment created only after the quorum. The quorum itself is our app's logic, not the protocol.
- **Lineage:** Team 23 (2nd, 2024) worked inside Rafiki's auth server on GNAP consent; Naartjie (HM, 2024) let several payers fund one payment; Shabaha (3rd, 2025) paid out by milestone.
- **Award fit:** Impact (Ruta N is the city's innovation agency).
- **Judges' read:** a strong, local problem. But the payer is the city treasury, which won't use an Open Payments wallet any time soon, so the impact story is hard to believe. And it's political: the investigations concern the previous administration. If we go here, talk about traceability, not corruption, and shrink the payer: neighbors pooling money for their own project (the cancha, the salón comunal), released by milestone. That version uses Open Payments more and fits the Community award.
- **Demo moment:** the third veedor approves and the payment goes out; a payment above the contract total is refused.

### O. Prepaid energy topped up from abroad

- **How might we…?** How might we let family abroad keep the lights on at home, without the money going somewhere else?
- **Problem:** about a million people in Antioquia use EPM's prepaid energy, and 10% of every recharge goes to old debt ([Minuto30, Jun 2025](https://www.minuto30.com/amp/energia-prepago-de-epm-transformando-vidas-con-acceso-flexible-a-la-energia/1665075/)). Recharges are made in cash, a bit at a time.
- **User:** a son in Madrid whose mother in Bello is on prepaid energy.
- **Our solution:** he approves once, "up to €30 a month for mom's energy", and each top-up arrives in pesos with a fixed receive amount.
- **Where Open Payments fits:** a recurring grant plus a fixed-receive quote across currencies: the official remittance and recurring-payment guides almost as written. EPM's side would be mocked.
- **Lineage:** Spend Secure (earmarked remittances), and every remittance project above.
- **Award fit:** Impact or Inclusion.
- **Judges' read:** clear and doable, but the least new idea here: the Open Payments flow is the textbook one, remittances are the most crowded theme, and the EPM integration would be fake. Better as one use case inside another idea than as the project.

### Discarded: digital cash on delivery

Proposed on 2026-10-14 and dropped the same day. Cash and cash on delivery were only 4.18% of Colombian e-commerce transactions in Q1 2025 ([CCCE via DPL News](https://dplnews.com/?p=277066)), and a grant doesn't lock funds, so the seller gets no guarantee: the one thing cash on delivery promises. Judges would catch both.

---

## First-pass ranking

A starting point for the scoring matrix in [FRAMEWORK.md](FRAMEWORK.md#2-decide-scoring-matrix). Everyone scores on their own first.

| # | Problem | Target award | Open Payments fit | Proven by past winners | Fresh for the judges | Doable in ~9 h |
| --- | --- | --- | --- | --- | --- | --- |
| A | Informal/domestic wages with split | Inclusion / Impact | High (split + recurring) | Kano, Common Cents | High for Colombia | High |
| B | Corner shop as the bank branch | Inclusion | High (assisted consent) | Cache Money, Direla | High, sponsor-aligned | Medium |
| D | Tourists pay vendors, with split | Impact / Innovation | High (one-time + split) | VibePayments, Tourism | Medium | High |
| C | Digital natilleras | Inclusion / Community | High (recurring consent) | Tried 4 times, never won | Low unless twisted | High |
| E | Earmarked remittances | Impact | High (fixed receive + split) | Spend Secure | Low (crowded) | High |
| G | Repayments vs gota a gota | Inclusion | Medium | GNPL, Zen-i | Medium | Medium |
| H | Migrants | Inclusion | High | Globi | Medium | Medium |
| F | Freelancer invoicing | Impact | High | Pago Abierto exists | Low | High |
| J | Adoption | Innovation | Medium | Fliqa | Medium | Medium |
| I | 4x1000 | — | Low | None | High | Low |

## Judges' scorecard

Updated in [WINNERS.md](WINNERS.md#what-changes-in-our-ranking) after the deep dive into the winners: K stays first, C (natillera plus emergency fund) moves up, A moves slightly down.

How a Round 1 panel might score the strongest ideas, 1 to 5 on the official criteria, using the lineage above as the judges' memory. Presentation is left out because it depends on us, not the idea. UX and technical quality are scored as potential: how simple and reliable a 9-hour version can be. **Score on your own first** ([FRAMEWORK.md](FRAMEWORK.md#2-decide-scoring-matrix)) and compare afterwards; this is one reading, not the decision.

| Idea | Problem | Open Payments use | UX | Tech quality | Inclusion | Innovation | Impact | Feasible in ~9 h | **Total** | Best award |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| K. Fiado as a grant | 5 | 5 | 4 | 4 | 4 | 4 | 4 | 5 | **35** | Inclusion |
| A. Domestic wages with split | 5 | 4 | 4 | 4 | 5 | 3 | 4 | 5 | **34** | Inclusion / Impact |
| L. Caregiver with limits | 4 | 4 | 3 | 4 | 5 | 4 | 3 | 4 | **31** | Inclusion |
| M. Agent with a mandate, for an excluded user | 4 | 5 | 3 | 2 | 4 | 5 | 3 | 3 | **29** | Innovation |
| B. Corner shop as the bank branch | 4 | 3 | 3 | 3 | 5 | 3 | 4 | 3 | **28** | Inclusion |
| O. Prepaid energy from abroad | 4 | 3 | 4 | 4 | 4 | 2 | 3 | 4 | **28** | Impact |
| N. Neighborhood works by milestone | 4 | 3 | 3 | 4 | 2 | 3 | 4 | 4 | **27** | Impact |
| M. Agent with a mandate, for a busy family | 2 | 5 | 3 | 2 | 2 | 5 | 3 | 3 | **25** | — |

Reading it:

- **K and A lead for different reasons.** A is the most proven pattern, but it's close to Kano, built at the Cape Town hackathon the Foundation co-hosted four months ago; that's why its innovation is a 3. K is less proven, but it's new and answers six of the seven questions well (on question 4 it reaches tienda customers, but they still need a wallet).
- **M is the only idea that could win Innovation outright**, and only in the version with an excluded user. The busy-family version probably doesn't make the top twelve.
- **B loses points on Open Payments use**, because cash-in and cash-out happen outside the protocol, and it's close to Cache Money (2nd, 2025) and to what Puntored already sells.
- **N and O work better as a feature or a framing** than as the project.

| Award | Our best bet | Why the sponsor's representative would pick it |
| --- | --- | --- |
| Inclusion (Puntored) | K, then L | It runs on the tiendas their network already serves, for customers who live on fiado |
| Impact (Ruta N) | K or A | A Medellín habit (fiado is strongest here) with a path through existing tiendas; or 55% informality |
| Innovation (FIND EAFIT) | M, excluded-user version | The grant as an agent's mandate, enforced live on stage |
| Community (all participants) | Any of the above | Decided by the pitch: a person everyone recognizes, and the audience paying live from their own Test Wallets |

## Combinations worth considering

- **A + B:** the tendero pays the domestic worker's wages for a household that has no app, and the split funds her savings.
- **C + Fireline:** a natillera that is also the barrio's emergency fund, paying out within hours.
- **D + split:** tourist pays once; the guide, the artisan and a community fund are paid in the same authorization.
- **E + H:** earmarked remittances for migrant families, with fees shown before sending.
- **K + B:** Doña Marta tops up her wallet in cash at the same tienda, so fiado works for customers without a bank account.
- **N, smaller:** neighbors pool money for their own project and release it by milestone, approved by the veedores.

## Repos to read before Friday (reading only)

| For | Repo | Why |
| --- | --- | --- |
| Clean integration structure | [Mizzfit/space_sheeps_interledger](https://github.com/Mizzfit/space_sheeps_interledger) | Modules for grants, quotes, payments, token lifecycle |
| Split payments + GNAP | [whoAngeel/interledger-hackathon-2025](https://github.com/whoAngeel/interledger-hackathon-2025) | Split checkout and interactive auth, with docs |
| Recurring + split + WhatsApp/USSD | [Lubasi-Jr/open-payments-hackathon-2026](https://github.com/Lubasi-Jr/open-payments-hackathon-2026) | Scheduler, finish-URI handling, Twilio webhook |
| Pre-authorization rules | [RoySalgadoM/hackathon-interledger](https://github.com/RoySalgadoM/hackathon-interledger) | NestJS, limits and whitelists on grants |
| Standing grant for repeat payments | [TheFrankemon/open-payments-rewards](https://github.com/TheFrankemon/open-payments-rewards) | Cashback paid without re-asking consent |
| A winner's minimal flow | [kakoma/getshabaha](https://github.com/kakoma/getshabaha) | Incoming → quote → interactive grant → continue, documented step by step |
| Colombian market | [vicguty25/pago-abierto-mvp](https://github.com/vicguty25/pago-abierto-mvp) | Spanish README, Colombian user story, deployed demo |
| Official tutorial | [interledger/uct-hackathon-2024](https://github.com/interledger/uct-hackathon-2024) | Next.js + Prisma + Postgres app the Foundation gave students |

## Questions to settle before Friday

- Which award are we aiming for? Pick one; shape the story around it.
- Does anyone on the team, or someone we know, employ or work as a domestic worker, run a tienda, take part in a natillera, or send remittances? One real quote beats any statistic.
- What are mentors and other teams talking about in Slack? Avoid the most crowded idea if we can.
- For the chosen idea, which Open Payments guide is closest? Read it, and the matching repo above, before Friday.
- If K is on the table: ask a real tendero, ideally in Medellín, how they handle fiado, how often customers pay late, and whether they'd trust a cupo.
- For the mentors on Friday: does any Colombian wallet implement Open Payments or plan to? Can a user cap a Bre-B automatic debit, and can a small shop start one?
- In the Test Wallet, before relying on them: how long an incoming payment stays open, which error comes back when a grant's limit is exceeded, and whether users can revoke a grant from the wallet's own screens.
