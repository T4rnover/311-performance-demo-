# 211 Arizona: Using AI to Escape the Annual Funding Fight
*A funding-resilience thesis*

**The problem isn't cost. It's fragility.** 211 Arizona needs about **$3.5M per year**, has **no permanent state line**, and gets rescued season to season from a single volatile payer: the general fund. It is easy to cut because its value is diffuse and unmeasured, so every budget cycle it competes as a "nice lifeline" against universities and public safety, and loses.

**AI's job is to attack the two root causes, single-source funding and unmeasured value, not just to make the call center cheaper.** Two levers:

**1. Lower and stabilize the cost of delivery.** AI handles high-volume, low-complexity contacts (food, utility assistance, cooling-center hours) through multilingual chat, voice, and SMS grounded in the verified resource directory, and keeps that directory current automatically. This deflects routine load, extends specialist reach, and makes the automated fallback tier genuinely usable. It turns a funding *cliff* into a *slope*, where access degrades gracefully instead of going dark. It does **not** replace the human core; the hardest, highest-value calls still need people.

**2. Make the value measurable, then diversify who pays.** 211 touches Medicaid/AHCCCS, housing, utilities, public health, and heat response, each a distinct funding stream with its own self-interest. AI-driven outcome tracking quantifies what 211 *prevents* (utility shutoffs, ER and heat costs, Medicaid and shelter spend), converting a discretionary line into an **attributable cost-avoidance investment** that AHCCCS, DES, counties, hospitals, and utilities each have reason to co-fund. Closed-loop data and multi-payer reporting, both AI-enabled, make braided, non-general-fund revenue administratively feasible. APS already funds 211 on exactly this logic; the goal is to generalize it.

**Honest guardrails.** AI is cheaper but not free (you trade a labor line for a smaller technology-plus-oversight line). The ROI story must **protect specialists, not justify cutting them**. Equity is a hard constraint: automation must not abandon the hardest-to-serve. And the AI itself must be funded sustainably, not by another one-time grant. *Confirm current AHCCCS/Medicaid social-needs reimbursement specifics before relying on them.*

---

## Five hackathon tracks that attack funding dependence

*Each maps to a lever above. Ground rules: use the **public 211 resource directory** as the sandbox; use **synthetic** call scenarios only, never real transcripts. Judge on safety, equity/language access, groundedness, and feasibility, not novelty.*

**1. Directory Autopilot** *(cost).* AI that keeps the resource directory verified and current: extracting structured records from agency websites, checking freshness (hours, eligibility, closures), and deduplicating. Cuts the largest recurring back-office cost and makes every downstream tool trustworthy.

**2. Grounded Self-Service Navigator** *(cost + continuity).* A multilingual chat/voice assistant answering routine needs from the verified directory, with **hard escalation** to a human or 988 for anything crisis-adjacent. Makes the automated tier usable, so a funding lapse degrades gracefully instead of leaving residents with a dead phone tree.

**3. Cost-Avoidance Ledger** *(measure value, the flagship).* Turn contacts and outcomes into attributable dollar savings by domain: utility shutoffs prevented, ER and heat costs avoided, Medicaid and shelter spend reduced. Produces the ROI evidence that justifies co-funding. The heat-illness-prevention number is the sharpest in Arizona.

**4. Closed-Loop Reimbursement Pipeline** *(new recurring revenue).* Capture referral, connection, and outcome in the format a Medicaid social-needs (HRSN / 1115) or utility / health-plan payer requires, unlocking recurring, non-general-fund revenue tied to a federal match.

**5. Multi-Payer Reporting and Shared Directory API** *(braided funding).* One interaction generates the documentation many funders each need, and exposes the directory as shared infrastructure that counties, health plans, 988, and hospitals co-fund, reframing 211 from "a call center the state pays for" into Arizona's canonical health-and-human-services resource layer.

---

## Appendix A: How we will measure it (MOEs)

**The measurement gap is the funding gap.** 211's own field concedes that efforts to report service outcomes in support of funding requests have been held back by the lack of common definitions for basic measures. What 211 reports today is mostly performance and output: speed-of-answer, abandonment, referrals provided, satisfaction, and self-reported improvement. "Referral provided" is an output. "Reported improvement" at end of call is a weak proxy. Neither answers the effectiveness question: *did the need get met, and what downstream public cost did that prevent?* Instrumenting the true Measures of Effectiveness (MOEs) and diversifying the funding are the same project.

**Capability statement (what effectiveness is measured against):** *reliably connect any Arizonan with an unmet health or human-services need to an appropriate, currently-available resource, especially in crisis and surge events (heat, disaster), equitably across language, geography, and ability, such that the need is actually met, downstream public cost is reduced, and the capability is sustainable.*

| Measure | Type | What it tells us | Baseline today | Target |
|---|---|---|---|---|
| Successful-connection rate | MOE | Did the person actually reach the resource, not just get a referral | Not captured | Establish via follow-up, then grow |
| Needs-met rate | MOE | Did the presented need resolve | ~78% self-reported improvement (proxy only) | Validated follow-up measure |
| Unmet-need / service-gap rate | MOE | Where the system of care has no resource; also intelligence | Partial (AIRS construct) | Full taxonomy coverage, trended |
| Time-to-resolution | MOE | Latency for crisis and heat, a life-safety factor | Not captured | Thresholds by need type |
| Public cost avoided per connection | MOE | The ROI that underwrites multi-payer funding | Not captured | Model, then validate on a pilot |
| Downstream events prevented | MOE | Shutoffs, evictions, ER and heat cases avoided | Not captured | Attribution pilot by domain |
| Equity parity (language, geography, ability) | MOE / KPP | Connection and outcome rates across groups | Not measured as parity | Gap within a set threshold |
| Directory accuracy / currency | MOE (enabler) | Share of referrals that were actually open and eligible | Site visits and DB adds tracked; freshness partial | % verified within N days |
| Speed-of-answer | MOP | Responsiveness of the live tier | ~80% in 60 sec | Maintain |
| Abandonment rate | MOP | Access lost before contact | <10% | <5% |
| Automated-tier containment | MOP | Routine needs resolved without a human | New | Target band once live |
| Escalation accuracy | MOP / KPP | Crisis-adjacent contacts routed correctly to a human or 988 | New | Above threshold, no missed crisis |
| Grounding / traceability | MOP / KPP | Referrals traceable to a verified record; no fabrication | New | ~100% traceable |
| Cost per successful connection | MOS / KPP | Affordability, the number that makes the funding case | ~$3.5M/yr total; per-outcome not computed | Defined ceiling |
| Funding-diversification ratio | MOS | Share of budget from non-general-fund payers | Effectively single-source | Grow non-GF share year over year |
| Continuity / graceful-degradation | MOS / KPP | Fraction of capability that survives a funding lapse | Binary (live service on or off) | Defined 24/7 floor in lapse mode |

**Key Performance Parameters (the threshold few).** Safety: crisis mis-routing below a hard threshold, with no missed handoff. Groundedness: zero fabricated referrals. Equity: language-group connection-rate gap within a set number of points. Continuity: a defined capability available 24/7 even in lapse mode. Affordability: a ceiling on cost per successful connection.

**The honest part.** The MOEs that matter most (successful connection, needs met, cost avoided) are exactly the ones 211 cannot measure today, because they require closed-loop follow-up data it has never captured at scale. That is not a knock on 211; it is the opportunity. The instrument that closes the loop (AI-assisted follow-up plus cost-avoidance attribution) is the same instrument that produces the multi-payer ROI evidence in the thesis above. Measuring effectiveness properly belongs at the top of the hackathon, not in the evaluation afterthought.

---
*Prepared as a discussion starter. Figures and program details reflect public reporting as of August 2026 and should be verified before external use.*
