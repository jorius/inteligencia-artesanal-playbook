# Problems

What previous Interledger hackathons built, what won, and which real problems in Colombia we could take on with Open Payments. This feeds the "Explore" and "Decide" steps in [FRAMEWORK.md](FRAMEWORK.md).

Research done on 2026-10-13. Winners come from Interledger Foundation announcements and press; repositories were found through GitHub search. Reading other teams' code to learn is fine. Copying it into our repo is not: all our code must be written during the event.

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
| 2nd | **Team 23** | Payments that need more than one approver | Extended Rafiki's auth server for **multi-party approvals** | GNAP deep dive |
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
| **Aguascalientes** (Sept 19–20, UVM) | 1st **Qrancheros – Ocelon** (interoperable payments for local markets), 2nd **Hubbers – InterPyme** (SMEs connect to open payments), 3rd **Tu Tía Dev – YaYaApp**, mention **Squad.py – OpenBus** (transport payments) | [YaYa](https://github.com/ChaboCode/YaYa) (87% of P2P transactions in Mexico are informal; QR P2P in under 10 s, Flutter + Express), [EduWallet Community](https://github.com/Yupaw/Hackathon-EduWallet-Community) (group savings / **tandas**), [pay-per-use demo](https://github.com/Manuelita21/pay-per-use-interledger-) |
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
3. **Creative consent is the protocol's superpower.** Earmarked remittances (Spend Secure), multi-party approvals (Team 23), spending rules and whitelists (RoySalgadoM), milestone payouts (Shabaha), standing grants for cashback. This is where "Innovation" points come from, and it's what the Open Payments grant model is built for.
4. **Splits.** Kano 98/2, Tourism 60/30/10, VibePayments (1st place) split and merge, MyBills four wallets. One authorization, several destinations, is a repeatable crowd-pleaser.
5. **Savings circles keep appearing but have never won top three.** Velfund (stokvels, 2024), InterTand, EduWallet and UNDEFINED (tandas, 2025). Judges from the Foundation have seen the idea. It can still win if the execution and the specific Colombian angle are strong, but "digital natillera" alone won't surprise anyone.
6. **Remittances are the most crowded idea.** GuendalizaaPay, Globi, Spend Secure, Pago Abierto, and the organizers list it as a theme. The ones that stood out added a twist: earmarking, indigenous languages, freelancer invoicing.
7. **Tourism won Mexico 2025.** With the World Cup coming, four Mexican teams built tourist payments. Medellín is also a tourism city, and foreign payers are something Bre-B can't serve, but expect other Medellín teams to think of it too.
8. **Presentation decides the Community prize**, and the pitch in general. Team 8 (2024) won the community prize for the presentation. Several team write-ups mention the 3–5 minute pitch as the hardest part.

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

**"Why not Bre-B?"** will be asked. Bre-B gives Colombia free, instant domestic transfers. Open Payments adds what Bre-B lacks: other countries and currencies, an app paying on the user's behalf within approved limits, recurring payments with built-in consent, splits to several receivers, and any wallet that implements the open standard. The strong ideas use at least one of these. The official [guides](https://openpayments.dev) already cover one-time purchases, fixed-debit and fixed-receive remittances, recurring payments, split payments, future-payment grants and wallet ownership verification.

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

## Combinations worth considering

- **A + B:** the tendero pays the domestic worker's wages for a household that has no app, and the split funds her savings.
- **C + Fireline:** a natillera that is also the barrio's emergency fund, paying out within hours.
- **D + split:** tourist pays once; the guide, the artisan and a community fund are paid in the same authorization.
- **E + H:** earmarked remittances for migrant families, with fees shown before sending.

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
