# Interview Intel: Koinz — Staff Software Engineer (iOS)

**Report:** [006](../reports/006-koinz-2026-09-10.md) — scored 2.9/5 (structural blockers: Cairo on-site, comp)
**Researched:** 2026-09-10
**Sources:** ~10 Glassdoor interview reviews + ~34 Glassdoor company reviews (all roles, not iOS-specific), koinz.app product site, App Store metadata, company LinkedIn feed. **No Blind, LeetCode, or engineering-blog data exists for this company.**

> **Read this first.** Prep is worth doing, but the location question is still unresolved. As posted this role is Cairo on-site, which costs the IQAMA and ~75% of take-home. Prep so you can have a *strong* conversation — and use that conversation to ask whether a Riyadh seat exists. Do not walk into it having already decided to accept Cairo.

---

## The single most useful thing found

Their own product site advertises:

> **"Perfect Pickup Experience** — Streamline your drive-thru pickup process, **Siri integration**, **Apple CarPlay** compatibility, seamless ordering."

**This is the iOS-platform work at Koinz.** Siri/App Intents and CarPlay for a drive-thru pickup flow is genuinely hard, genuinely iOS-specific, and exactly what a Staff iOS engineer would own. It is also nowhere in the job description — which means almost none of the 200+ applicants will bring it up.

If you say one prepared thing in this interview, make it this. It proves you looked at the product, not the req.

---

## Process Overview

- **Rounds:** 3 reported — HR/recruiter screen → **take-home assignment (build an app)** → technical interview with a senior developer. A Staff req may add a hiring-manager or founder round; unconfirmed.
- **Timeline:** ~1–2 weeks end-to-end (one candidate reported 2 weeks applying online; another reported 1 week, on-site at the **Maadi Corniche office**, and described it as organized and professionally handled).
- **Difficulty:** **2.8/5** (Glassdoor average). ⚠️ Small sample across all roles — almost certainly *not* Staff-level reviews. Assume the real bar for this req is higher.
- **Positive experience rate:** **60%**
- **Known quirks:**
  - Take-home described as "easy" but explicitly graded on **code quality and edge-case handling**, not on getting it working.
  - Technical round reported as **heavily OOP-focused** — SOLID, design patterns, inheritance/polymorphism. Not algorithm-heavy.
  - **The recurring complaint is silence after the technical round.** Multiple candidates reported promised feedback within a week that never came, and unanswered follow-up emails. One said a rejection email would have been preferable to being ignored.

**Company ratings (Glassdoor, ~34 reviews):** 3.8/5 overall · **79%** would recommend · **75%** positive business outlook · **+9% over the last 12 months**.

| Category | Rating |
|---|---|
| Career opportunities | 3.7 |
| Culture & values | 3.5 |
| Work-life balance | 3.4 |
| Compensation & benefits | 3.4 |
| Diversity & inclusion | 3.4 |
| **Senior management** | **3.2** ← lowest |

**Engineering-specific reviews — read these carefully, they describe the job you'd be taking:**

- A **mobile team lead (5+ yrs, Cairo)** rated it **5.0**, citing a good learning environment — but flagged *"Process not best practice at all."*
- A former **senior product manager** listed pros as niche food-aggregation experience; cons as *"low salaries and **no process for dev teams**."*
- General culture notes: collaborative teams, opinions expressed openly, flexible hours and some remote options; offset by startup stress, tight deadlines, and stretched resources.

**Two independent reviewers say the same thing: engineering process is weak.** That is not a warning here — that is the job. Their JD asks you to "introduce new technologies and engineering practices that improve developer productivity" and "improve release quality through automation testing and continuous integration." The reviews confirm the gap is real. **Your entire pitch is that you have closed exactly this gap twice** (XCTest from zero at STC Bank → 30% bug reduction; standards from nothing at Grinta that outlasted you).

*Sources: [Glassdoor interviews](https://www.glassdoor.com/Interview/Koinz-Interview-Questions-E3294585.htm) · [Glassdoor reviews](https://www.glassdoor.com/Reviews/Koinz-Reviews-E3294585.htm). Direct fetch returns 403; figures are from search-surfaced summaries. Sample is small — individual reviews carry heavy weight.*

---

## Know the product cold

Interviewers at a 140-person consumer startup notice immediately whether you have used the app. **Download it before any call** (App Store: *Koinz — Order, collect, redeem*).

**What they are:** Saudi Arabia's social food-ordering and pickup platform. Not a delivery aggregator — that is the whole thesis. Aggregators take 25–30% commission; Koinz charges a subscription plus a cut on app orders, and claims ~60% lower customer acquisition cost. They compete with Jahez, HungerStation and The Chefz by **not** fighting on delivery — they own **pickup and drive-thru**.

**Numbers to have ready** (all company-published):

| Metric | Value | Source |
|---|---|---|
| Signups | 2.7M+ | The JD itself |
| Orders in 2025 | **25M** | LinkedIn year-in-review, 2025-12-30 |
| Coffee orders 2025 | 2.5M | same |
| Drive-thru orders 2025 | 500K | same |
| Saved for users 2025 | 7M SAR | same |
| Saudi restaurants/cafés | 500+ | App Store listing |
| iOS rating (Saudi) | **4.64★ / 15,085 ratings** | App Store, 2026-09-10 |

**Product surface:** loyalty points → free meals, cashback, direct weekday/weekend discounts, following restaurants with **stories** (Instagram-style), point-sharing with friends, gamified monthly competitions and leaderboards, drive-thru/pickup with order tracking, **Siri + CarPlay**, and an **AR Treasure Hunt** (Pokémon Go-style mechanics) shipped for Ramadan 2026.

**Merchant side:** real-time merchant dashboard with analytics and order management, plus **POS integrations — Foodics and Marn**. These integrations are the actual moat in Saudi F&B; know the names.

**Named customers** (from their site and year-in-review): Al-Ennabi Grill (claims 300K customers via Koinz), Hamburgini (200K ratings/reviews in one year), Go-Ya ("top three online ordering channels"), plus Hazel, Umq Coffee, Olden, Modern Supply.

**Offices:** HQ **Office 10, Destination Building, Abu Bakr Al Sidik, Al Yasmin, Riyadh**. Engineering at **Maadi, Cairo** (interviews reported at the Maadi Corniche office).

**People:** Hussein Momtaz (co-founder/CEO, computer engineer, Al Azhar — ran the GPlanet software house before Koinz), Ahmed Said (co-founder/CTO), Abdullah Al Khaldi (co-founder/CRO).

---

## What you can infer about their codebase (and why it matters)

This is your edge. Nobody else applying will have looked.

| Observation | Source | What it means |
|---|---|---|
| Consumer app bundle ID is **`tech.gplanet.shopx`**, first released **2017-03-31** | App Store metadata | The app predates Koinz — it is the founders' **GPlanet software-house app ("ShopX") rebranded**. ~9 years of sediment. |
| Version **10.13.36**, shipped **2026-09-06** | App Store | Mature versioning, active release cadence. They ship constantly. |
| Minimum iOS **15.6**, **213 MB** binary | App Store | Large, asset-heavy. A 213MB binary is a real app-size/startup-time conversation. |
| **Koinz Partner** (merchant app, `com.koinz.partner`) last updated **2024-09-18**, 0 ratings | App Store | Merchant mobile abandoned ~2 years while consumer ships weekly. |
| JD says *"build from scratch"* | The req | Contradicts a live v10 app. Probe what they actually mean. |
| JD names Flutter and Android breadth | The req | Either they have cross-platform surfaces, or they want one lead across both native teams. Ask. |
| Marketing site is a **Lovable-generated React SPA** using **Supabase** for restaurant sign-up | `/lovable-uploads/` paths + Supabase auth strings in the JS bundle | Marketing site only — says nothing about the product stack, but tells you the culture ships AI-built tooling without ceremony. |
| **No engineering blog, no talks, no OSS.** GitHub org `Koinz-App` created 2026-07-13 with **0 public repos** | GitHub API | Nothing public to study. Everything you know about their engineering, you inferred — say so, it lands well. |

**Last public stack signal** (a ~6-year-old Koinz req): native **Swift** iOS + native **Java** Android, **Realm**, Git, CI/CD, unit and UI tests, design patterns, UML, Jira. Six years stale — treat as a starting hypothesis to verify, not fact.

---

## Likely Questions

### Technical

| Question | Source | Your angle |
|---|---|---|
| OOP fundamentals — SOLID, design patterns, inheritance vs. composition, polymorphism | **Reported** — multiple candidates say the technical round was heavily OOP | Do not wing this because you are Staff. Be ready to explain protocol-oriented Swift *as a deliberate alternative* to class inheritance. Ground each principle in a real refactor: your "systematic refactoring of coupled modules" at STC Bank is an SOLID story with a number attached (30% bug reduction). |
| Take-home: build a small app, graded on **code quality and edge-case handling** | **Reported** | Assume architecture is the grade. Ship MVVM with a clean separation, dependency injection via protocols, and — critically — **tests plus explicit error/empty/offline states**. Reviewers said the task is easy; the differentiator is what you do beyond "it works." Include a short README stating your trade-offs and what you deliberately left out. |
| Mobile system design: design the Koinz order/pickup flow | `[inferred JD]` — "architectural decisions that support long-term product growth", "work closely with Backend on API design" | Two-layer framing: on-device vs. server, and be explicit about which lives where. Push on offline/intermittent connectivity, local caching, order-state consistency, and the POS integration boundary (Foodics/Marn are third-party — what happens when they are slow or down?). At Staff level the differentiator is trade-off reasoning, not the diagram. |
| Performance: crashes, startup time, memory, reliability metrics | `[inferred JD]` — two full bullets on this | **Your thinnest documented area — prepare real numbers from STC Bank before the call.** Crash-free session rate, cold-start time, memory ceiling. Then use the Grinta reflection: instrumentation without a threshold is a dashboard nobody opens; define the number that stops a release first. |
| Mobile CI/CD pipeline design | `[inferred JD]` — named ownership bullet | Vodafone: 15% shorter release cycle. Name the tooling honestly (Fastlane / Jenkins / Xcode Cloud — whichever is true). Land the reflection: the win was that shipping stopped being an event, so smaller, safer changes became the default. |
| UIKit → SwiftUI migration strategy on a legacy app | `[inferred]` — their app has a 2017 lineage and an iOS 15.6 floor | **This is your unfair advantage.** Production experience on both sides — UIKit at Vodafone 2017-22, SwiftUI at STC Bank 2023-now. Talk incremental adoption at a module boundary, not a rewrite. |
| App size / binary bloat | `[inferred]` — their binary is 213 MB | Optional. If it comes up, asset catalogs, on-demand resources, dead-code stripping, dependency audit. |
| Siri / App Intents and CarPlay for pickup and drive-thru | `[inferred]` — advertised on koinz.app, absent from the JD | Be honest if you have not shipped App Intents. Say what you would need to learn and how you would approach it. Raising it at all puts you ahead of the field. |

### Behavioral

| Question | Source | Best story from `story-bank.md` |
|---|---|---|
| Tell me about yourself | **Reported** — standard HR round | The 10-year arc: Vodafone → Grinta → STC Bank, each step higher stakes. Land on: *"I inherit systems that work and leave them measurably better."* |
| Tell me about a process you introduced | `[inferred JD]` + reviews say dev process is weak | **Testing foundation from zero at STC Bank** — strongest available. Reflection: adoption came from making tests the cheapest path to merging, not from mandating them. |
| How do you mentor engineers? | `[inferred JD]` — "mentor and coach iOS, Android and cross-functional engineers" | **Standards that outlasted me at Grinta.** Reflection: standards written down are ignored; standards enforced in review become culture. |
| Tell me about building something from scratch | `[inferred JD]` — explicit requirement | **Arena 3.0 from inception at Grinta** — component library, backend-driven UI, 20% faster delivery. |
| A time you improved reliability | `[inferred JD]` | **Instrumenting stability before scale at Grinta.** |
| Why do you want to work at Koinz? | **Reported** — "questions about the company" | Product-specific, never generic. Pickup/drive-thru as a deliberate anti-aggregator thesis + a v10 codebase that needs a modernization owner. |

### Role-Specific

- **"What would you do in your first 90 days?"** `[inferred]` — Their JD lists 13 ownership areas with no sequencing. Answer with sequencing, because that *is* the Staff signal: measure first (crash-free rate, cold start, build and release times), pick the one metric with the worst ratio of pain to effort, fix it visibly, then use that credibility to change process. Do not open with a rewrite.
- **"How do you decide what to refactor versus leave alone?"** `[inferred]` — 9-year-old codebase. Your STC Bank answer: you refactored *coupled modules* specifically, on the critical transaction paths, not everything.
- **"How do you work with Product and Design?"** `[inferred JD]` — explicitly requires a "Product Engineer mindset." Use the analytics work at STC Bank: you instrumented to *measure release impact*, which is a product habit, not an engineering one. The 25% DAU lift at Vodafone is the outcome-shaped proof.

### Background & Red Flags

| Likely question | Why it comes up | Recommended framing |
|---|---|---|
| **"You haven't done Flutter or Android."** | The JD asks for cross-platform breadth; your CV is iOS-only | Concede immediately and precisely — never claim breadth in a Staff loop, it collapses in ten minutes. Then redirect to the **platform layer**: CI/CD, release automation, crash and performance budgets, API contract design are all platform-agnostic and you have owned all four. |
| **"Do you have direct reports?"** | Staff/lead title, no management history on the CV | Honest no. The req names mentoring and technical direction, not headcount. Pivot to standards adoption and review leadership at two companies. |
| **"Why leave STC Bank?"** | Standard | Ladder, not escape: you lead iOS at a bank and want technical direction across a whole mobile platform. **Never mention comp first.** |
| **"You're in Riyadh — are you relocating to Cairo?"** | The req is Maadi on-site; you are in Saudi | Do not answer yes reflexively, and do not answer no. Turn it into the question you actually need answered — see below. |
| **"Your background is banking and telecom, not consumer food."** | Domain jump | Consumer scale is consumer scale: 4M+ banking users, 30M+ telecom platform, 25% DAU lift. And in banking a bug moves money — their app moves money too (points, cashback, order payments, POS reconciliation), just with lower regulatory weight. |

---

## Story Bank Mapping

| # | Likely question/topic | Best story | Fit | Gap? |
|---|---|---|---|---|
| 1 | Introducing engineering process where none exists | Testing foundation from zero at STC Bank | **strong** | — |
| 2 | Building from scratch / architecture for growth | Arena 3.0 from inception at Grinta | **strong** | — |
| 3 | Mentoring, standards, review culture | Standards that outlasted me at Grinta | **strong** | — |
| 4 | Shipping at large scale | 25% DAU lift at Vodafone Egypt | **strong** | — |
| 5 | CI/CD and release velocity | Release cycle automation at Vodafone | **strong** | — |
| 6 | Reliability metrics and monitoring | Instrumenting stability before scale at Grinta | **partial** | Needs real numbers attached — see below |
| 7 | Legacy modernization / UIKit→SwiftUI migration | — | **none** | ⚠️ **Missing** |
| 8 | Disagreement or conflict with a peer/manager | — | **none** | ⚠️ **Missing** |
| 9 | A decision you got wrong | — | **none** | ⚠️ **Missing** |

**Three gaps worth closing before any interview:**

1. **A migration story.** You have lived UIKit→SwiftUI on both sides — the most reusable asset in your background for this role — and it is not a STAR+R story yet. Source it from the STC Bank migration ("supporting the ongoing migration from UIKit").
2. **A conflict story.** Staff loops always ask. Likely source: driving code review adoption at STC Bank or standards adoption at Grinta — introducing process into a team that had none creates friction by definition.
3. **A failure story.** Currently every story lands on a win. Senior candidates volunteer the miss and what changed after. The Grinta reflection (monitoring before budgets) is close — it could be developed into a real one.

Story 6 also needs hardening: pull the actual crash-free rate, startup time and memory figures from STC Bank.

Say the word and I'll draft all three and append them to `story-bank.md`.

---

## Technical Prep Checklist

- [ ] **SOLID, design patterns, inheritance vs. composition** — reported as the technical round's main focus across multiple candidate reviews
- [ ] **Protocol-oriented Swift as an answer to OOP questions** — lets you engage their OOP framing without pretending Swift is Java
- [ ] **Real reliability numbers from STC Bank** (crash-free sessions, cold start, memory) — the JD dedicates two bullets to it and your CV cannot currently answer
- [ ] **Take-home plan decided in advance**: MVVM + protocol-based DI + tests + explicit error/empty/offline states + a README of trade-offs — reviews say quality and edge cases are the grade
- [ ] **Mobile system design for offline-tolerant ordering** — order state, caching, retry, and the third-party POS boundary (Foodics/Marn)
- [ ] **Incremental UIKit→SwiftUI migration strategy** on a 9-year-old codebase — their app's actual situation
- [ ] **Your CI/CD tooling named accurately** — it is a named ownership bullet and "I set up CI/CD" without specifics reads thin at Staff
- [ ] **Install and use the Koinz app** — place a pickup order if you can; consumer-startup interviewers ask
- [ ] **Skim App Intents / SiriKit and CarPlay basics** — enough to discuss the pickup use case intelligently, not to claim expertise
- [ ] **Their numbers memorized**: 2.7M signups, 25M orders in 2025, 500K drive-thru, 500+ Saudi restaurants, 4.64★

---

## Company Signals

**Vocabulary they use** — mirror it:
- **"social commerce"** and **"social food ordering"**, not "food delivery app" (they are explicitly not a delivery aggregator)
- **"pickup"** and **"drive-thru"**, not "takeaway"
- **"brands"** for restaurants; **"loyalty"**, **"rewards"**, **"cashback"**, **"points"**
- Their positioning line: *"where Gen Z and young consumers discover brands, earn rewards, share experiences, and make food social"*

**What they appear to screen for:** pragmatism over ceremony (their marketing site is AI-generated and their process is admittedly loose), shipping speed, and — for this req specifically — someone who can bring order without stalling delivery. Their internal Automation Hackathon (Dec 2025, 3 days, 6 themes, cash prizes) says they reward building over proposing.

**Things to avoid:**
- **Do not lead with process for its own sake.** Two reviewers say there is "no process for dev teams" — that is your opening, but if you present as the person who arrives and adds ceremony, a startup hears "slower." Frame every process change by the delivery metric it improved: 30% fewer bugs, 20% faster features, 15% shorter release cycle.
- **Do not claim Flutter or Android depth.**
- **Do not accept "build from scratch" at face value** — it contradicts their live v10 app, and probing it shows you did the work.
- **Do not raise comp before you have raised location.**

**Questions to ask them — in priority order:**

1. **"Koinz is headquartered in Riyadh and hires in Saudi Arabia — I saw the Dammam business development role. Is there any path to this role being Riyadh-based, or is engineering deliberately consolidated in Maadi?"** *Ask this first, in the recruiter screen. Everything else is contingent on the answer.*
2. **"Your site advertises Siri integration and CarPlay for drive-thru pickup, but neither is in the job description. How much of this role is deep-platform iOS work versus feature delivery?"** — the question that separates you from 200 other applicants.
3. **"The consumer app is at v10 with a 2017 lineage. When you say 'build from scratch,' do you mean a rewrite, a new surface, or incremental modernization?"**
4. **"The partner app hasn't shipped since September 2024 — is the merchant experience moving to web, and would it be in this role's scope?"**
5. **"What's your current crash-free session rate and cold-start time — and do you have budgets for them, or just monitoring?"**
6. **"Last announced round was 2021. How is the company funded today, and how do you think about runway?"** — ask late, ask plainly. At ~140 people with no priced round in five years it is fair, and *how* they answer is the signal.

**One process request to make explicitly:** the most consistent complaint in candidate reviews is silence after the technical round — promised feedback that never arrived and unanswered follow-ups. **At the end of the technical interview, ask for a decision date and a named point of contact, and confirm it by email.** You are not being difficult; you are pre-empting the single most reported failure mode of their process.

---

## Reality Check

Everything above assumes the location question resolves. It might not.

The honest read: role content is an excellent match (4.6/5 CV match, best evaluated to date), the engineering-process gap in their reviews is precisely the gap you have closed twice, and their public numbers show a real business with real momentum. Against that: Cairo on-site means giving up the IQAMA and roughly 71–82% of take-home, equity is near-worthless at ~$7M raised with five years of funding silence, and 200+ applicants are ahead of you in a queue for a job you could not accept as written.

**Prepare for the conversation, not the offer.** Ask about Riyadh in the first five minutes of the recruiter screen. If the answer is Cairo-only, you have lost an hour and learned something about the Saudi market. If it is Riyadh, you walk into the rest of this loop better prepared than anyone else in it.
