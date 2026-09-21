# Story Bank — Master STAR+R Stories

This file accumulates your best interview stories over time. Each evaluation (Block F) adds new stories here. Instead of memorizing 100 answers, maintain 5-10 deep stories that you can bend to answer almost any behavioral question.

## How it works

1. Every time `/career-ops oferta` generates Block F (Interview Plan), new STAR+R stories get appended here
2. Before your next interview, review this file — your stories are already organized by theme
3. The "Big Three" questions can be answered with stories from this bank:
   - "Tell me about yourself" → combine 2-3 stories into a narrative
   - "Tell me about your most impactful project" → pick your highest-impact story
   - "Tell me about a conflict you resolved" → find a story with a Reflection

## Stories

<!-- Format:
### [Theme] Story Title
**Source:** Report #NNN — Company — Role
**S (Situation):** ...
**T (Task):** ...
**A (Action):** ...
**R (Result):** ...
**Reflection:** What I learned / what I'd do differently
**Best for questions about:** [list of question types this story answers]
-->

### [Quality / Ownership] Building a testing foundation from zero at STC Bank
**Source:** Report #003 — Speechify — Software Engineer, iOS Core Product
**S (Situation):** Joined STC Bank's digital banking app (4M+ users) which had no test architecture in place.
**T (Task):** Raise quality and reliability in a fintech environment without freezing feature delivery.
**A (Action):** Introduced an XCTest-based testing architecture from scratch, drove initial team adoption, and ran systematic refactoring backed by code review discipline.
**R (Result):** Bug rate down 30%; App Store rating raised to 4.8.
**Reflection:** Starting from zero coverage, the ROI is entirely in *which* code you cover first. The percentage is a vanity number — the selection criteria are the engineering judgment. Be ready to explain how you chose.
**Best for questions about:** code quality, technical debt, testing strategy, working in a legacy/complex codebase, influencing without authority
**⚠️ Prep note:** Coverage reached ~5%. Always frame as "inherited zero, built the foundation" *before* an interviewer surfaces the number.

### [Speed / Trade-offs] Backend-driven UI at Grinta (Arena 3.0)
**Source:** Report #003 — Speechify — Software Engineer, iOS Core Product
**S (Situation):** Built the Arena 3.0 fan engagement platform from inception at a startup; every UI change required a full App Store release cycle.
**T (Task):** Ship product changes faster without waiting on App Store review.
**A (Action):** Introduced backend-driven UI for dynamic rendering, plus a reusable UI component library.
**R (Result):** Feature development time cut 20%; UI changes shippable without a release.
**Reflection:** The trade-off is client control vs. delivery velocity — you give up compile-time safety and some native polish. Know what you gave up, not just what you gained.
**Best for questions about:** shipping fast, architecture trade-offs, "ship now vs. needs time", building from scratch, startup environments

### [Scale] Performance and engagement at Vodafone (30M+ users)
**Source:** Report #003 — Speechify — Software Engineer, iOS Core Product
**S (Situation):** Consumer telecom app on a platform serving 30M+ users, with secure billing and usage tracking.
**T (Task):** Improve responsiveness and user engagement at scale.
**A (Action):** Optimized API performance and reworked the push notification and engagement flows.
**R (Result):** Daily active users up 25%.
**Reflection:** At this scale, problems are rarely one bug — they're a class of bug. Name the class you found, not just the fix.
**Best for questions about:** working at scale, performance optimization, growth metrics, consumer products
**⚠️ Prep note:** Needs specific technical detail — which bottleneck, which fix, what you measured. Currently too thin for a "hardest technical problem" answer.

### [Delivery] Cutting release cycle time at Vodafone
**Source:** Report #003 — Speechify — Software Engineer, iOS Core Product
**S (Situation):** Large-scale telecom app with a slow release cadence.
**T (Task):** Shorten time from merge to production.
**A (Action):** CI/CD implementation and release process improvements.
**R (Result):** Release cycle time cut 15%.
**Reflection:** Worth knowing where the remaining 85% of cycle time sat and why it wasn't worth cutting — that answer shows judgment about diminishing returns.
**Best for questions about:** CI/CD, release engineering, developer productivity, process improvement
**⚠️ Prep note:** Needs specifics — which tooling, which bottleneck was removed.

### [Leadership] Establishing engineering standards at Grinta
**Source:** Report #003 — Speechify — Software Engineer, iOS Core Product
**S (Situation):** Startup with no established engineering standards or review practice.
**T (Task):** Raise the quality floor without slowing a small team down.
**A (Action):** Established engineering standards and code review practices; added crash monitoring and testing.
**R (Result):** Improved app stability and faster onboarding for new engineers.
**Reflection:** Standards that are imposed get worked around; standards that are adopted stick. The hard part was buy-in, not authorship.
**Best for questions about:** technical leadership, mentoring, influencing peers, process change, conflict over code review

**Extension (added #004, Vinted):** This doubles as the "healthy conflict" story. When pushback came on review overhead, the move was to argue from defect data rather than preference — conceding on process weight while holding on coverage of critical paths. Disagreement is cheap when you argue from shared data and expensive when you argue from taste.

### [Systemic Risk / Coupling] Refactoring for bug reduction at STC Bank
**Source:** Report #004 — Vinted — Senior iOS Engineer, Order
**S (Situation):** Defect rate on a 4M-user digital banking app where failures are financial, not cosmetic.
**T (Task):** Cut the bug rate without a feature freeze.
**A (Action):** Targeted refactoring of tightly coupled modules rather than spreading effort evenly; used code review as the enforcement mechanism rather than a rubber stamp.
**R (Result):** 30% reduction in bug rate.
**Reflection:** Defects clustered in a few coupled areas instead of spreading uniformly. Naming the *class* of bug beats fixing instances of it — and knowing when to stop is the same skill as knowing where to start.
**Best for questions about:** spotting hidden coupling, systemic risk, technical debt prioritisation, "under-fixing vs over-engineering", refactoring under delivery pressure

### [Design Systems] Reusable component library at Grinta
**Source:** Report #004 — Vinted — Senior iOS Engineer, Order
**S (Situation):** Inconsistent UI and duplicated work across a startup product built from inception.
**T (Task):** Establish reusable foundations a small team could actually keep using.
**A (Action):** Built a shared UI component library and paired it with the engineering standards and review practice that governed its adoption.
**R (Result):** Feature development time cut by 20%; consistency held as the product grew.
**Reflection:** A design system only pays off if adoption is enforced socially, not just technically. Building the library was the easy half.
**Best for questions about:** design systems, DSKit-style shared layers, reusable architecture, consistency at scale, platform work

### [AI Tooling] Running an AI-driven engineering pipeline
**Source:** Report #004 — Vinted — Senior iOS Engineer, Order
**S (Situation):** Wanted rigour and speed in a high-volume, judgment-heavy workflow that manual effort could not sustain.
**T (Task):** Automate the mechanical parts without outsourcing the judgment.
**A (Action):** Built and operates an AI pipeline that extracts, evaluates, scores, and tracks — with explicit rules about which decisions belong to the model and which stay with him.
**R (Result):** Consistent, auditable output at a volume manual work could not reach.
**Reflection:** The value is in knowing which parts *shouldn't* be automated. AI tooling that removes judgment from the loop produces confident garbage — the skill is drawing that boundary deliberately.
**Best for questions about:** evaluating and adopting AI developer tools, automation judgment, building internal tooling, "how do you use AI in your work"

### [Platform / Delivery] Release cycle automation at Vodafone Egypt
**Source:** Report #006 — Koinz — Staff Software Engineer (iOS)
**S (Situation):** Manual, slow release process on a consumer platform serving 30M+ users.
**T (Task):** Shorten the release cycle without adding risk to a system that size.
**A (Action):** Introduced CI/CD automation across build, test and distribution.
**R (Result):** 15% reduction in release cycle time.
**Reflection:** The win was not speed. It was that shipping stopped being an event — once releases were cheap, smaller and safer changes became the default, which is where the real risk reduction came from.
**Best for questions about:** CI/CD ownership, developer productivity, reducing release risk, "tell me about a process you improved", platform vs feature work

### [Reliability] Instrumenting stability before scale at Grinta
**Source:** Report #006 — Koinz — Staff Software Engineer (iOS)
**S (Situation):** Arena 3.0 was a new platform with unproven reliability heading into launch.
**T (Task):** Establish what "healthy" meant before scaling users onto it.
**A (Action):** Set up testing plus crash monitoring instrumentation, feeding the signal into release decisions.
**R (Result):** Improved reliability and performance ahead of scale.
**Reflection:** I set up monitoring before I set up budgets. Instrumentation without a threshold is a dashboard nobody opens — define the number that means "stop the release" first, then wire the tooling to it.
**Best for questions about:** reliability metrics, crash-free rate, performance budgets, pre-launch quality, "how do you know your app is healthy?"
