---
title: "Chapter 4: Adoption & Implementation of AI"
subtitle: "From Pilot to Enterprise — The GES Roadmap"
short_title: "Adoption & Implementation"
description: "The strategic, structural view. Where AI fits in the exhibitions and experiential marketing business, how to plan its rollout responsibly across 4,000+ events a year, and how Microsoft Copilot — including the new Copilot Cowork — becomes the platform that ties it all together at GES."
label: ch-04-adoption-implementation
tags: [AI adoption, implementation, exhibitions, trade shows, Microsoft Copilot, Copilot Cowork, governance, compliance, union labor, OSHA, GDPR, ESG, ROI, Center of Excellence, GES]
---

```{admonition} Download this Chapter as PDF
:class: tip

[Download PDF](https://github.com/liquid-books/ges-learns-ai/raw/main/pdfs/ch04-adoption-implementation.pdf)
```

# Chapter 4: Adoption & Implementation of AI

:::{figure} ../images/ch04-adoption-infographic.png
:label: fig-ch04-infographic
:alt: Illustrated roadmap infographic showing the journey from AI pilot to enterprise deployment at a global exhibitions company — a winding road moving from a small pilot light on the left through stages of proof of concept, workflow integration, governance, and full enterprise deployment on the right, with show floor, freight, and booth build imagery and GES branding elements
:width: 80%
:align: center

The path from pilot to enterprise is not a straight line. But it has a known shape — and the organizations that navigate it successfully share specific structural choices in common.
:::

> *"The measure of intelligence is the ability to change."*
> — Albert Einstein

Most AI programs inside large operating companies die at the same place.

They run a pilot. The pilot succeeds. People are impressed. Leadership is encouraged. And then — almost universally — the pilot sits in a deck for six months while IT, legal, operations, and the show teams work through their respective concerns, and the momentum built by the pilot slowly evaporates under the weight of the next move-in.

That last part matters more at GES than it does almost anywhere else. Our calendar does not pause for a technology rollout. There is always another show. There is always another marshaling yard filling up at 5:00 a.m., another exhibitor calling about a crate that has not hit the booth yet, another organizer who needs the floor plan reissued before sales close. A pilot that requires a quiet quarter to mature will never get one here.

The technology worked. The people believed in it. The ROI was there to be captured.

And still — nothing scaled.

This is the most important implementation problem in event-services AI today. Not the technical problem. Not the model selection problem. Not even the compliance problem, which is more navigable than most people believe. The scaling problem: **how do you take a thing that works in one pocket of the organization and make it the way everyone works — across 24 facilities, 75+ countries, and 4,000+ events a year?**

This chapter is the strategic answer to that question. It covers the state of AI in the exhibitions and experiential marketing industry right now — where our peers and our competitors actually are — the known shape of the curve from pilot to enterprise, the compliance environment that genuinely governs AI at GES (which is *not* the one you read about in generic AI articles), the Microsoft platform architecture that makes Copilot the right implementation choice for us, the economics of the new usage-based Copilot Cowork model, the risk framework we need, the organizational structure that makes adoption sustainable, and the business case that stands up to a CFO's scrutiny.

By the end of this chapter, you will have a complete strategic picture. And you will have built your personal "AI Adoption One-Pager" — the single-page document that names your workflow, your metrics, your risks, and your timeline. That document is the seed of your Showcase Project. And it starts here.

---

## 1. The State of AI in Exhibitions & Experiential Marketing — 2026

Let's establish the baseline. Where is our industry actually, right now, in its AI journey? Not the trade-press version — the operational reality.

:::{figure} ../images/ch04-finserv-landscape.png
:label: fig-ch04-landscape
:alt: Visual landscape of AI adoption in the events and exhibitions industry in 2026 — a tiered diagram showing early adopters at the top (large organizers, global logistics providers, event technology platforms) through mid-adopters to late movers — with GES positioned in the strategic early-majority tier with arrows showing the opportunity ahead, including onPeak AI Smart Suite as an existing production deployment
:width: 80%
:align: center

The AI adoption curve in exhibitions and experiential marketing — 2026. The early movers have 18–24 months of operational learning that late movers cannot buy. The question is which tier GES is determined to occupy.
:::

**The early movers have established durable advantages — and some of them are inside our own building.**

Start with the good news, because it is easy to miss when you are heads-down on a show. **GES is already running production AI.** The **onPeak AI Smart Suite**, launched in 2026 under Lisa Baez (EVP, Tech-Enabled Services) with Tayler Gilmartin's product team, is a live, revenue-touching AI deployment: AI-assisted hotel search for attendees, an AI contract reader that ingests hotel agreements and pulls out the terms that matter, and AI email categorization that routes housing inquiries to the right human faster. Alongside it, **onPeak Compass** applies AI to accommodation management, and **Visit by GES** — Visit Create, Visit Connect, Visit Discover, and the next-generation NFC Touchpoints released in June 2026 — is generating structured event data at a scale that simply did not exist five years ago.

That is not a slide. That is shipped software with customers on it. Which means the question for the rest of GES is not *"can we do AI?"* It is *"how fast can we spread what one part of the company has already proven?"*

**Around us, the landscape is moving.**

The large organizers we serve — Informa, Clarion, Emerald and their peers — are deploying AI in audience acquisition, matchmaking, and content programming. Our competitors in general service contracting are investing in the same automation targets we are: labor forecasting, freight and drayage optimization, order-to-invoice accuracy, and exhibitor self-service. Global logistics providers have been applying machine learning to freight routing and customs classification for years. Venue operators are piloting AI for crowd flow, energy management, and security.

Meanwhile the agencies we compete with — and sometimes partner with — on the experiential side are using generative AI in concept ideation, rendering, and pitch production. If a competitor can turn a client brief into three credible stand concepts overnight and we take a week, the RFP is decided before the design review even happens.

**The mid-tier is where the strategic opportunity lives.**

Here is what the early movers' experience has established: **first-mover advantage in event-services AI is real, but it is not permanent.** The tools are available to everyone. The primary differentiator is no longer access to AI — it is **organizational capability**: the learned ability to deploy it effectively inside a business that runs on deadlines, union rules, venue constraints, and a thousand small operational judgments a day.

For GES, this is the moment — and the timing is not accidental.

**December 31, 2024 changed our position.** When the Truelink Capital transaction closed and GES separated from Viad Corp after 55 years, we stopped being a segment inside somebody else's portfolio and became a company that controls its own roadmap, its own capital allocation, and its own technology agenda. Under Derek P. Linde as CEO & President, with Neal Parsons as CFO, decisions about what GES invests in are made by GES. For the first time in decades, an AI program at this company does not have to survive a parent-company prioritization exercise before it can start.

That independence is an asset with a shelf life. Windows for building organizational capability before it becomes table stakes are measured in months, not years.

**And the compliance environment is clarifying — it just isn't the one people expect.**

If you read general-purpose AI adoption material, you will find page after page about financial regulators and model risk management frameworks. None of that is our world. GES has a real, demanding, and specific compliance environment — union jurisdiction, venue safety and OSHA, international customs and carnets, GDPR and attendee data privacy, organizer and venue contract terms, ESG and emissions reporting, and client confidentiality that is arguably as sensitive as anything in finance. Section 3 covers it properly, because getting this right is what makes fast adoption *safe* adoption.

---

## 2. The Pilot-to-Enterprise Curve — Why Pilots Stall

Before we go into the compliance environment, let's name the structural reason most AI pilots fail to scale. Understanding this pattern is the prerequisite to avoiding it.

:::{figure} ../images/ch04-pilot-curve.png
:label: fig-ch04-curve
:alt: Graph showing the typical AI pilot-to-enterprise curve at an events company — initial excitement and results in the pilot phase, followed by a valley of death where IT review, show-season workload, and fading momentum combine, then either a recovery to enterprise scale or a flatline where the pilot is quietly abandoned between move-in and move-out cycles
:width: 80%
:align: center

The Valley of Death is not inevitable. But it is the default. Every organization that has successfully scaled past it made specific structural choices that others did not.
:::

The curve has a known shape:

**Phase 1 — The Pilot Peak:** Enthusiasm is high. A small team runs a focused experiment — maybe the Chicago office automates its post-show labor reconciliation, or a Spiro account team uses Copilot to turn a client brief into a first-pass creative narrative. Results are real and visible. Champions are energized. Leadership is encouraged.

**Phase 2 — The Valley of Death:** The pilot moves from the experiment phase to the "what do we do with this now?" phase. IT needs to assess security. Legal needs to weigh in on client-confidential data. Someone needs to know whether the output can be shared with an organizer under our contract terms. Meanwhile — and this is the GES-specific killer — **show season arrives.** The team that ran the pilot goes back to running shows, because there is no structure for sustaining momentum through a move-in. Three months and eleven events pass. The pilot deck sits on a SharePoint page. Nobody mentions it at the next leadership call.

**Phase 3 — Enterprise or Flatline:** Organizations that built the right structures — a governance framework that was ready for the pilot results, a Champion network that could absorb the learnings, a funding decision made before the first phase ended — scale through the Valley. Organizations that didn't flatline. The AI program gets quietly deprioritized, and eighteen months later someone proposes the same pilot again, not knowing it already happened.

**The structural choices that separate scalers from flatliners:**

1. **Governance framework exists before the pilot launches**, not after. The pilot findings slot into a pre-built review process rather than triggering a governance conversation from scratch. At GES this means knowing *in advance* the answer to "can this touch exhibitor data?" and "can this touch a client's unreleased product information?"

2. **The next phase is funded before the current phase ends.** Momentum is the most fragile resource in any change program. Gaps in commitment are where momentum dies — and in an events business, a gap does not stay a gap. It gets filled by the next show cycle.

3. **The pilot is designed to produce a workflow template**, not just a result. The goal is not "show it works" — it is "build the repeatable pattern that Toronto, London, Dubai, and Las Vegas can each adopt without redesigning it." A pilot that produces a one-off win in one office has produced entertainment. A pilot that produces a template has produced leverage.

4. **Champions are organized into a named community** before the pilot ends. The learning does not live in the pilot team. It lives in a structured network that spans functions and geographies — because a labor coordinator in Chicago and a project manager in Amsterdam are solving more of the same problem than either of them realizes.

5. **The pilot is scheduled against the show calendar, not against the fiscal calendar.** This one is ours alone. Plan pilot checkpoints for the gaps between major move-ins for the teams involved, not for the last week of a quarter when half the participants are on a show floor in another time zone.

These are not complicated. They are not expensive. They are, however, decisions that have to be made deliberately — because the default path leads straight into the Valley.

---

## 3. The Compliance Environment — What Every GES Professional Needs to Know

Let us be specific about the compliance landscape, because this is the area where the most confusion — and the most unnecessary fear — lives inside operating companies running AI programs.

GES is not a lightly regulated business. We are a *differently* regulated business. Our obligations do not come from a single federal supervisor; they come from union agreements, venue rules, national safety regulators, customs authorities, privacy law across 75+ countries, and — critically — the contracts we sign with organizers, exhibitors, and agencies. Every one of those touches how we can use AI.

::::{admonition} ⚠️ Compliance Guidance Disclaimer
:class: warning

The compliance information in this section reflects the general landscape as of 2026 and is written for educational context. Union agreements, venue rules, customs regimes, and privacy law vary by jurisdiction, by venue, and by contract — sometimes between two halls in the same city. Always consult GES Legal (Detra Page, SVP General Counsel and her team), your Labor Relations lead, and your regional operations leadership before designing AI workflows that touch labor jurisdiction, safety documentation, customs filings, or personal data. This chapter is educational context, not legal advice.
::::

:::{figure} ../images/ch04-regulatory-landscape.png
:label: fig-ch04-regulatory
:alt: Clean infographic showing the seven compliance domains that govern GES operations — union labor jurisdiction, venue safety and OSHA, international customs and carnets, GDPR and attendee data privacy, organizer and venue contract compliance, ESG and emissions reporting, and client confidentiality — with Microsoft Copilot's enterprise architecture controls mapped to each domain
:width: 80%
:align: center

Seven compliance domains, one direction: AI use at GES must be safe, accurate, confidential, and auditable. Microsoft Copilot's enterprise architecture was designed with exactly these kinds of requirements in mind.
:::

### 3.1 Union Labor Rules and Jurisdiction

This is the compliance domain most likely to bite an enthusiastic AI user first, and the one least understood by anyone who has not worked a show floor.

Union jurisdiction determines **who is allowed to perform which task, in which venue, under which agreement.** Who unloads the truck at the marshaling yard. Who operates the forklift. Who hangs the sign. Who runs the electrical. Who can touch a crate on the show floor and who cannot. These rules vary by city, by venue, by local, and by contract term — and they are not advisory. Getting them wrong creates grievances, cost overruns, delays, and damaged relationships with partners we depend on show after show.

**Where AI helps:** summarizing a long collective bargaining agreement so a new coordinator can find the relevant clause faster; drafting a plain-language labor briefing for an exhibitor who does not understand why they cannot plug in their own booth; building labor hour forecast models in Excel; comparing our planned crew build against historical actuals for the same venue; preparing questions for a labor call.

**Where AI must not be trusted alone:** any determination of what work falls under which jurisdiction. **Copilot does not know your local's agreement, and it will produce a confident, fluent, wrong answer if you ask it to arbitrate jurisdiction.** Jurisdiction calls are made by people with the agreement in front of them and the relationship on the line. Use AI to prepare for that conversation. Never to replace it.

**The rule:** AI drafts the summary. A human who owns the labor relationship confirms the call.

### 3.2 Venue Safety and OSHA Compliance

Safety is a core operational value at GES, and our **low global reportable incident rate is a stated KPI** — not a poster in the break room. Install and dismantle is genuinely hazardous work: rigging, forklifts, aerial lifts, heavy freight, compressed schedules, unfamiliar venues, and crews working overnight.

The compliance surface includes OSHA (and its international equivalents), venue-specific safety rules, rigging and structural certification requirements, and our own internal standards, which in many cases exceed the local minimum.

**Where AI helps:** generating first-draft toolbox talks and pre-shift safety briefings tailored to the day's scope; summarizing a venue's safety manual into a one-page crew brief; drafting incident report narratives from field notes (OneNote is excellent for this — see Chapter 10); analyzing incident and near-miss data in Excel to find patterns across venues, shifts, and show types; preparing safety sections of exhibitor service kits; turning a long standard into a checklist a crew will actually read at 6:00 a.m.

**Where AI must not be trusted alone:** safety determinations, structural or rigging calculations, incident classification and reportability decisions, and anything that becomes a regulatory filing. A hallucinated load rating is not a productivity problem. It is a person getting hurt.

**The rule:** AI can help a safety professional communicate faster and analyze deeper. It never replaces the qualified person who signs.

### 3.3 International Customs, Carnets, and Cross-Border Freight

GES moves freight into and out of 75+ countries. That means ATA Carnets, temporary import regimes, HS classification, country-specific documentation, restricted materials, and customs brokers in dozens of jurisdictions. A carnet error can strand a client's entire stand in a bonded warehouse while their show opens without them.

**Where AI helps:** drafting and proofreading shipping instructions for exhibitors; summarizing country-specific documentation requirements for an account team; comparing a packing list against a manifest to flag discrepancies; producing multilingual freight instructions (genuinely valuable across a 75-country footprint); building freight cost and material handling weight analyses; drafting the customs sections of an exhibitor service kit; preparing a client-facing explainer on why their advance warehouse deadline matters.

**Where AI must not be trusted alone:** the actual classification, valuation, and declaration content of a customs filing. Tariff classification is a legal determination with financial and criminal exposure. Carnet documentation must be verified by a qualified logistics professional or licensed broker, every time.

**The rule:** AI prepares and checks. Licensed and qualified professionals file.

### 3.4 GDPR and Attendee/Exhibitor Data Privacy

This is the domain where GES's exposure is broadest, because of the sheer volume of personal data flowing through our platforms.

**Visit by GES** captures attendee and lead data — badge scans, NFC touchpoint taps, lead qualification notes — on behalf of organizers and exhibitors. **onPeak** holds guest data: names, contact details, travel dates, payment information, sometimes accessibility needs. Our registration and housing operations touch personal data belonging to hundreds of thousands of individuals every year, across GDPR in Europe, UK GDPR, an expanding patchwork of US state privacy laws, PIPEDA in Canada, and privacy regimes across the Middle East and India.

Two concepts matter enormously here and are frequently confused:

- **Controller vs. processor.** For much of the attendee data we handle, GES is a **processor** acting on an organizer's instructions — not the controller. That means we may only process that data for the purposes the contract specifies. "We fed the attendee list into an AI tool to see what it could find" is not a specified purpose. It is a breach.
- **Purpose limitation.** Data collected for badge access or hotel booking cannot be repurposed for analysis, model input, or a new product idea without a lawful basis.

**Where AI helps:** analyzing *aggregated and anonymized* event metrics — booth traffic patterns, dwell time, hotel block pickup rates, session attendance; drafting privacy notices and consent language for legal review; summarizing a data processing agreement; building reporting that never touches an individual record; drafting responses to exhibitor questions about how lead data works.

**Where AI must not be used:** pasting attendee lists, guest rosters, lead capture exports, or any personal data into any AI tool that has not been explicitly cleared for that data category. This applies to consumer AI tools absolutely and unconditionally. It applies to enterprise Copilot only within the boundaries GES IT and Legal have approved.

**The rule:** if it identifies a human being, it does not go into a prompt until someone with authority has said it can.

### 3.5 Contract Compliance with Organizers and Venues

Every show GES runs sits inside a stack of contracts: the organizer agreement, the venue agreement, union agreements, EAC (Exhibitor Appointed Contractor) rules, exclusive services designations, and the exhibitor service kit terms themselves. Those contracts govern exclusivity, service levels, insurance and indemnity, data ownership, branding, and confidentiality.

A surprising number of them now include AI-specific language: restrictions on using client data in AI systems, requirements for disclosure of AI-generated deliverables, and provisions about who owns AI-assisted work product.

**Where AI helps:** summarizing contract terms so a show manager can find the SLA without reading forty pages; comparing this year's organizer agreement against last year's to spot changed terms; drafting RFP responses (Chapter 6 goes deep on this); preparing post-show reconciliation narratives against contracted scope; building compliance checklists per show.

**Where AI must not be trusted alone:** interpreting contract obligations, determining whether a specific use is permitted, or generating any binding commitment. Contract interpretation runs through GES Legal, full stop.

**The rule:** AI helps you *understand* the contract faster. It does not tell you what the contract *means*.

### 3.6 ESG and Emissions Reporting

GES made real, public commitments here. We published the **2024 ESG Report**, and GES EMEA published the **Impact Report & Roadmap to Net Zero** in 2025 with data-led event emissions reporting. The **Better Stands** initiative in the UK and Europe drives the shift from disposable to reusable stands, and **Show Ready – The Edit** (launched October 2025, Gold certified) is a premium sustainable modular exhibit product line.

Public commitments create reporting obligations, and increasingly those obligations come with assurance requirements. Under CSRD in Europe and a growing set of disclosure regimes elsewhere, sustainability data is moving toward the same standard of rigor as financial data. Organizers are also asking for show-level emissions reporting as a condition of the contract.

**Where AI helps:** aggregating and analyzing emissions data across shows in Excel; drafting narrative sections of ESG reports from underlying data; tracking Better Stands reuse rates and modeling waste diversion; summarizing evolving disclosure standards for the sustainability team; building client-facing sustainability summaries per event; identifying data gaps in an emissions dataset.

**Where AI must not be trusted alone:** any published emissions figure, any assured disclosure, any claim made to a client or regulator about environmental performance. Greenwashing exposure is real, and a hallucinated number in a public ESG report is a serious problem that outlives the show.

**The rule:** AI accelerates the analysis and the drafting. Humans verify every number that gets published.

### 3.7 Client Confidentiality — The GES-Specific Obligation

This one deserves its own heading because it is the domain where GES's exposure is genuinely unusual, and where a well-meaning employee is most likely to cause harm without realizing it.

**GES sees things before the world does.** We see booth plans for products that have not launched. We handle crates containing prototypes under embargo. We build stands whose entire design is the reveal. We know which competitors are exhibiting next to each other, at what size, with what budget, months before the floor plan goes public. In some verticals we serve — healthcare and medical, aerospace and defense, automotive, technology — that information is commercially explosive and sometimes export-controlled.

And here is the part that makes it sharp: **we frequently serve direct competitors at the same show.** Two rival manufacturers, two rival device companies, two rival software vendors — all GES clients, all on the same floor, all trusting us with their plans.

That trust is the foundation of the business. It is literally the **T** in T.R.U.E.

**What this means for AI use:**

- Do not put unreleased product information, embargoed launch details, or confidential design files into any AI tool not cleared for that data.
- Be deliberate about cross-client contamination. Copilot respects Microsoft 365 permissions, which is exactly why **permissions must be correct at the source.** If Client A's design files sit in a SharePoint site that the Client B account team can open, Copilot will happily surface them — because from the system's point of view, that access was authorized. Copilot does not create the leak. It reveals the misconfiguration, at speed.
- Never use one client's confidential material as an example, template, or reference when generating work for another client — even indirectly, even paraphrased.
- Treat anything under NDA as if it will be read aloud at the client's board meeting. Because if it leaks, it will be.

**The rule:** the same discretion you apply on the show floor applies in the prompt window. If you would not say it in the aisle with a competitor standing there, do not type it.

### 3.8 What This Means for Your Day-to-Day Copilot Use

Here is the practical translation, and it is more permissive than most people expect.

For the vast majority of Copilot use cases in this master class — drafting documents, summarizing meetings, researching an industry vertical, preparing organizer briefs, building Excel analyses of labor hours and drayage costs, producing recap decks, cleaning up site survey notes — the compliance considerations above do not create a blocker. Those activities are professional productivity work on data you already have legitimate access to.

The compliance framework becomes directly relevant when AI touches:

- Union jurisdiction determinations or labor agreement interpretation
- Safety determinations, incident classification, or structural/rigging calculations
- Customs classification, valuation, or carnet documentation content
- Any personal data belonging to attendees, guests, exhibitor staff, or employees
- Contract interpretation or any binding commitment to an organizer, venue, or exhibitor
- Published ESG figures or client-facing sustainability claims
- Any client-confidential design, product, or launch information

For those workflows, GES Legal, your Labor Relations lead, your safety lead, or your regional operations leadership should be the first call — before implementation, not after.

::::{admonition} 💡 The Proportional Governance Principle
:class: tip

Governance intensity should match the risk of the use case — not the anxiety level of the room.

**Fast lane (just go):** Drafting internal documents. Summarizing meetings you attended. Analyzing your own operational data. Cleaning up notes. Translating an internal message. Reformatting a deck. Brainstorming approaches.

**Check first:** Anything client-facing that leaves GES. Anything touching personal data. Anything that becomes a number in a report someone relies on.

**Formal review required:** Union jurisdiction, safety determinations, customs filings, published ESG disclosures, contract interpretation, client-confidential product information.

Most of your work is in the fast lane. The discipline is knowing precisely when it isn't.
::::

---

## 4. Microsoft Copilot as the Implementation Platform — Why M365 Is the Right Home

Given the compliance environment just described, the question "which AI platform should GES use?" is not primarily a technology question. It is primarily a **governance and confidentiality question**.

And on that dimension, Microsoft 365 Copilot has specific architectural advantages over generic AI tools that are worth understanding in detail.

:::{figure} ../images/ch04-copilot-architecture.png
:label: fig-ch04-architecture
:alt: Clean technical architecture diagram showing Microsoft 365 Copilot's enterprise security structure — the LLM brain at top connected downward through Microsoft's commercial data protection layer, through the Microsoft 365 permissions and compliance layer, into GES's existing data environment including Exchange, SharePoint, Teams, and OneDrive — with audit logs flowing to the right
:width: 80%
:align: center

Microsoft 365 Copilot's architecture was designed for enterprises with real confidentiality obligations. The compliance infrastructure is not added on — it is foundational.
:::

**Your data does not train the model.**
This is the first and most important architectural point for a company that holds client secrets. When GES professionals use Microsoft 365 Copilot, their prompts, their data, and their outputs are not used to train Microsoft's underlying AI models. The conversations and data stay within the GES Microsoft 365 tenant — protected by the same enterprise data boundary that governs all M365 data. A client's unreleased booth design does not become training data for a model that a competitor might later query.

**Permission inheritance is automatic.**
As established in Chapter 1: Copilot can only access data that the user themselves can access. Restricted SharePoint sites, confidential email threads, protected design files — the AI respects the same access controls that GES IT has configured. A Copilot agent cannot surface information that the requesting user would not be permitted to see manually.

The corollary, stated plainly in Section 3.7 and worth repeating: **this makes source permissions matter more than they used to.** Show document libraries and client design asset folders that were "technically open but nobody browses there" are now instantly searchable in natural language. Cleaning up permissions is not an IT chore that can wait until after AI rollout. It is a *prerequisite* for it.

**Every interaction is logged.**
Microsoft 365 Copilot maintains audit logs of all interactions within the Microsoft Purview compliance infrastructure. This is not a privacy concern — it is a compliance asset. If a client's legal team ever asks *"what AI interactions produced this document?"* — the answer is retrievable. GES IT and Legal can access these logs through Microsoft Purview. For a company that signs confidentiality obligations with 150,000+ exhibitors a year, provable auditability is a commercial advantage, not overhead.

**Sensitive information labels are respected.**
Documents marked as Confidential, Highly Confidential, or otherwise restricted under Microsoft Information Protection (MIP) are handled according to those labels in Copilot interactions. AI does not bypass information protection classifications. Client NDA material that is properly labeled stays properly protected.

**The data never leaves your Microsoft 365 tenant.**
All Copilot processing happens within Microsoft's commercial data processing infrastructure — the same environment Microsoft uses for all enterprise M365 data. Data does not transit to consumer AI services. Prompts and responses do not go to consumer chatbot infrastructure. For GDPR purposes, this means data residency and processing terms are governed by Microsoft's enterprise data protection commitments, which our Legal team can review as part of standard vendor diligence.

These architectural features map directly to the compliance domains above: the enterprise data boundary supports our GDPR processor obligations and client NDAs. Audit logging supports contract compliance and client assurance. Permission inheritance prevents cross-client contamination. Information protection labels enforce confidentiality classification on the design and launch material we are trusted with.

---

## 5. Microsoft Graph and Work IQ — Your AI Already Knows Your Work

:::{figure} ../images/ch04-microsoft-graph.png
:label: fig-ch04-microsoft-graph
:alt: Microsoft Graph connecting GES's M365 data — show document libraries, exhibitor emails, Teams channels for move-in coordination, design asset folders, and calendars — to Copilot
:width: 80%
:align: center

Microsoft Graph is the connective tissue between Copilot and your entire M365 ecosystem — emails, documents, meetings, and files — making your AI contextually aware of your actual work.
:::

One of the most underappreciated aspects of Microsoft 365 Copilot's architecture is what Microsoft calls the **Microsoft Graph** — the data layer that connects all M365 services and makes your Copilot contextually aware of your actual work.

The Microsoft Graph is the technical infrastructure that answers the question: *"How does Copilot know about my emails and calendar without me having to tell it?"*

The Graph is a vast, continuously updated data model of your work activity across all M365 services: who you email, what documents you work on, what meetings you attend, what topics appear in your Teams conversations, what files you have recently accessed, and the relationships between all of these. It is, in effect, a real-time map of your professional context.

**Work IQ** is the applied intelligence layer built on top of the Graph. When you ask Copilot *"What are the open items from my last three calls with the show team on the MINExpo build?"* — Work IQ is what makes that question answerable. It traverses the Graph to find the relevant meetings, access the transcripts if available, identify the decisions and open items, and present them in a coherent summary — without you having to specify any file paths, dates, or document names.

For a workforce that spans time zones and moves between venues, this matters more than it does in a single-office company. A project manager who lands in Dubai after a red-eye should not have to reconstruct three days of decisions from a scroll-back. That is exactly the problem Work IQ solves.

Work IQ also matters for a reason we will return to in Section 6: **it is the grounding layer that Copilot Cowork uses.** When Cowork executes a multi-step task on your behalf, Work IQ is what keeps it anchored to GES reality rather than to generic internet knowledge.

::::{admonition} 🧪 Try This: Work IQ in Action
:class: tip

**Step-by-step:**

1. Navigate to [m365.cloud.microsoft](https://m365.cloud.microsoft) → Copilot Chat. Sign in with your GES Microsoft 365 credentials. Confirm the green enterprise shield.
2. Try each of these prompts — one at a time, reviewing what Copilot surfaces:

   - *"What documents have I worked on in the last week related to [a show, client, or venue you're currently working on]?"*
   - *"Who have I communicated with most frequently this month, and what were the main topics?"*
   - *"Are there any emails or Teams messages from this week that I haven't responded to that might need attention before move-in?"*

3. For each response, note: How much of the context did you have to provide? How does the response compare to what you would have produced if you'd searched manually?

**The discovery:** Copilot is not a search engine — it is a context engine. It synthesizes across the breadth of your work environment in a way that no manual search could replicate. This is Work IQ doing its job.
::::

---

## 6. Copilot Cowork — The Economics of Usage-Based AI

Everything up to this point describes Microsoft 365 Copilot as most people have experienced it: a per-user license, a predictable monthly cost, an assistant sitting inside Word, Excel, Outlook, and Teams.

**Copilot Cowork changes the cost model, and GES needs to understand that change before it rolls out — not after the first invoice.**

Cowork reached general availability on **June 16, 2026**. It is not "Copilot with a new coat of paint." It is a different mode of working with AI, and it carries a different commercial structure.

### 6.1 What Cowork Actually Is

Cowork is Microsoft's agentic work surface. Instead of a single prompt-and-response exchange, you hand Cowork a **task** — something with multiple steps, multiple sources, and a deliverable at the end — and it works on it: retrieving context, calling tools, iterating, and producing output.

Four architectural facts matter for our purposes:

- **It is cloud-hosted.** Cowork runs in Microsoft's cloud, not on your laptop. Long-running tasks continue whether or not your machine is awake — genuinely useful when your laptop is in a case in a marshaling yard.
- **It is grounded in Work IQ.** Cowork does not operate on generic knowledge. It operates on *your* GES work context via the Graph — your show files, your emails, your Teams threads, your SharePoint libraries, subject to your permissions.
- **It stays inside the Microsoft 365 trust boundary.** Same enterprise data protection, same permission inheritance, same Purview audit logging as the Copilot you already know. This is not a separate tool with separate risk. That matters enormously for a company with our confidentiality obligations.
- **It is multi-model.** Cowork runs on **Anthropic's Opus 4.8 and Sonnet 4.6** models, routing between them based on task complexity — Sonnet for lighter, faster work; Opus for heavier reasoning. You generally do not select the model; the system routes. But the routing is exactly what drives the cost.

### 6.2 The Billing Model — This Is the Part to Read Twice

**Cowork is billed on a usage basis, in Copilot Credits, *on top of* the Microsoft 365 Copilot user license.**

Read that again, because it inverts an assumption most enterprises have carried for two years. The M365 Copilot seat license is a fixed, predictable per-user cost. Cowork is a **variable** cost that scales with how much work you ask it to do.

Cost per task is driven by four inputs:

```{list-table} What Drives Copilot Cowork Cost per Task
:header-rows: 1
:label: table-ch04-cowork-cost-drivers

* - Cost Driver
  - What It Means
  - GES Example of a High-Cost Pattern
* - **Model use**
  - Which model runs, and how many tokens it processes. Opus 4.8 costs more per unit of work than Sonnet 4.6.
  - Asking for deep reasoning across a full show contract stack when a summary of one section would do.
* - **Context retrieval**
  - How much of your Graph data Cowork pulls in to ground the task.
  - "Look across everything we've ever done with this organizer" instead of scoping to the last two show cycles.
* - **Tool calls**
  - How many actions Cowork takes — searching, opening files, writing documents, querying connected systems.
  - A task that touches forty files when eight would answer the question.
* - **Runtime**
  - How long the task runs end to end.
  - Open-ended research tasks with no defined stopping condition.
```

Microsoft categorizes tasks into three bands — **light, medium, and heavy** — and the credit consumption differs accordingly:

```{list-table} Cowork Task Categories
:header-rows: 1
:label: table-ch04-cowork-task-bands

* - Band
  - Profile
  - GES Examples
* - **Light**
  - Narrow scope, few sources, short runtime, typically routed to the faster model.
  - Summarize one exhibitor service kit section. Reformat a punch list from site survey notes. Draft a move-in reminder email to exhibitors.
* - **Medium**
  - Multiple sources, several tool calls, a real deliverable at the end.
  - Build a post-show recap deck from the show file, labor actuals, and the organizer's feedback survey. Reconcile a labor forecast against actuals and draft the variance narrative.
* - **Heavy**
  - Many sources, extended reasoning, long runtime, deep retrieval.
  - Analyze three years of drayage and material handling data across a venue portfolio to model cost drivers. Produce a full RFP response draft grounded in the last twelve organizer proposals.
```

Heavy tasks are not bad. Heavy tasks are often exactly where the value is — a heavy task that replaces thirty hours of analyst work is a bargain at almost any credit price. The discipline is **knowing which band you're in and choosing it deliberately**, rather than accidentally running a heavy task because you were vague.

### 6.3 The Competitive Cost Picture

Microsoft's own testing claims that **Copilot Cowork is 30–40% cheaper per prompt than Claude Cowork operating through the Microsoft 365 connector.** That is a vendor claim and should be treated as one — but the underlying mechanism is plausible: Copilot Cowork's native grounding in Work IQ means it retrieves GES context more efficiently than an external agent reaching in through a connector, and retrieval efficiency is one of the four cost drivers.

For GES, the more important point is not the percentage. It is that **agentic AI cost is now a line item that behaves like cloud compute, not like software licensing** — and it must be managed the way we manage variable costs everywhere else in this business: with forecasts, budgets, thresholds, and someone accountable.

We already know how to do this. It is not conceptually different from managing material handling cost variance across a show portfolio. Same muscle, new domain.

### 6.4 Governing Variable AI Spend at GES

Here is the practical framework. This is a conversation that involves Neal Parsons's finance organization, GES IT, and the AI Center of Excellence described in Section 7 — and it should happen *before* broad Cowork enablement, not after.

**1. Start with a bounded pilot population.**
Do not enable Cowork tenant-wide on day one. Pick a defined group — say, a show operations team, a Spiro account team, and a corporate function — and enable there first. Bounded populations produce bounded invoices and clean learning.

**2. Establish per-department budgets and thresholds.**
Every department with Cowork access gets a credit budget and an alert threshold. Not to police people — to create the feedback loop that makes usage visible while it is still adjustable. A department that hits 70% of budget at mid-month learns something useful about its own patterns.

**3. Measure cost per outcome, not cost per user.**
The wrong metric is "credits consumed per employee." The right metric is "credits consumed per deliverable, versus the labor hours that deliverable used to consume." A heavy task that eats meaningful credits and saves two days of a senior designer's time is a spectacular trade. A light task run three hundred times a week out of habit, producing nothing anyone reads, is waste — regardless of how cheap each run was.

**4. Teach scoping as a cost control.**
This is the highest-leverage thing in this entire section, and it costs nothing to implement. **A well-scoped prompt is cheaper than a vague one**, because it reduces retrieval breadth, tool calls, and runtime simultaneously. "Analyze our shows" is expensive and unhelpful. "Compare labor hours forecast versus actual for the four shows we ran at this venue in 2025, and identify the two largest variance drivers" is cheap *and* better. Everything Chapter 5 teaches about prompting is now also a cost-management skill.

**5. Right-size the task band.**
Train people to ask: *does this need to be a Cowork task at all?* Many things are better as a single Copilot Chat prompt or a Copilot action inside Word or Excel — cheaper, faster, and included in the seat license. Cowork earns its cost on multi-step, multi-source work with a real deliverable. Use it there.

**6. Build a reusable task library.**
When someone develops a well-scoped Cowork task that produces a reliably good deliverable — a post-show recap builder, an exhibitor service kit updater, a variance narrative generator — capture it in the Champion community's shared library. Reuse of a tuned task is dramatically cheaper than a hundred people each discovering the same workflow badly. This is the single biggest cost lever available to us, and it is entirely an organizational behavior, not a technology setting.

**7. Review monthly, with finance in the room.**
Cowork spend goes on the monthly Executive Review agenda alongside the rest of the AI portfolio. Trend, drivers, outliers, and cost-per-outcome. If a department's consumption spikes, the first question is not "who's overusing it?" It is "what did they produce, and was it worth it?" Sometimes the answer is yes and the budget should go up.

::::{admonition} ⚠️ The Governance Point Nobody Wants to Say Out Loud
:class: warning

Usage-based AI spend fails in one of two directions, and both are expensive.

**Failure Mode A — Uncontrolled burn.** Cowork is enabled broadly with no budgets, no visibility, and no scoping discipline. Consumption grows organically, finance is surprised at quarter close, and the reaction is a hard shutdown. The company loses the capability *and* the trust, and the next AI proposal starts from behind.

**Failure Mode B — Fear-driven underuse.** Cost anxiety leads to such restrictive controls that nobody uses Cowork for anything meaningful. Spend is beautifully low. Value is zero. The seat licenses get paid anyway, and eighteen months later a competitor is doing in two hours what still takes us two days.

The target is neither. The target is **deliberate, measured, visible usage** where the people spending credits understand the cost drivers and can articulate the value of what they produced. That is a training and culture outcome, not a policy outcome — which is precisely why it belongs in a book like this one rather than in a memo from IT.
::::

---

## 7. Risk Frameworks for AI — The Four Dimensions GES Must Manage

With the compliance landscape understood and the platform architecture established, let's get specific about the risk dimensions that GES's AI program needs to manage. These are not hypothetical risks — they are the ones that have actually materialized in enterprise AI deployments.

:::{figure} ../images/ch04-risk-framework.png
:label: fig-ch04-risk
:alt: Clean four-quadrant risk framework diagram for AI at an exhibitions company — showing Data Leakage Risk, Hallucination Risk, Bias Risk, and Model Drift Risk — each quadrant with a risk description, specific trade show and event services examples, and the Copilot control that mitigates it
:width: 80%
:align: center

The four AI risk dimensions — each real, each manageable with the right controls. Understanding them is the prerequisite to deploying AI responsibly.
:::

### Risk 1: Data Leakage

**What it is:** Sensitive information from one context being exposed inappropriately in another context, or being exposed to external parties.

**At GES specifically:** A client's unreleased product or launch strategy surfacing in a Copilot response accessed by a team working for a competitor at the same show. Attendee or guest personal data from Visit by GES or onPeak appearing in outputs shared outside the lawful processing purpose. Confidential organizer contract terms — rates, exclusivity, SLAs — appearing in a document shared with a different organizer. Booth design files from a bespoke Spiro build informing a proposal for a rival brand.

**The Copilot control:** Permission inheritance (only surfaces data the user can access), the enterprise data boundary (data doesn't leave the M365 tenant), and Information Protection label enforcement. But the two decisive controls are organizational, not technical: **correct source permissions** on show document libraries and design asset folders, and **human judgment** about what belongs in a prompt. Professionals must apply the same discretion to AI prompts that they apply to conversations in a venue aisle where a competitor's team is standing ten feet away.

### Risk 2: Hallucination

**What it is:** AI generating factually incorrect information with apparent confidence. The model "hallucinates" — producing text that sounds plausible but is fabricated, citing sources that don't exist, or stating numbers that are wrong.

**At GES specifically:** A labor briefing that states a jurisdiction rule the local agreement does not contain. An exhibitor service kit with a wrong advance warehouse deadline or an invented drayage rate. A customs summary citing a documentation requirement that does not apply in that country. A post-show report with a fabricated attendance or lead-capture figure. An ESG narrative containing an emissions number nobody can trace to source data. A safety briefing citing a standard that does not exist.

Every one of those is a real operational consequence: a grievance, a stranded shipment, a missed deadline, a client escalation, a public disclosure problem, or an injury.

**The Copilot control:** Grounding — Copilot and Cowork source responses from your actual Microsoft 365 data via Work IQ when performing work tasks, which reduces but does not eliminate hallucination. The primary control is human: **every AI-generated factual claim in anything client-facing, safety-related, contractual, or published must be verified by a qualified professional before it leaves their hands.** Chapter 6 builds this verification discipline into a repeatable habit. Treat it as non-negotiable.

### Risk 3: Bias

**What it is:** AI systems producing outputs that reflect biases present in training data, leading to systematically different treatment of different groups.

**At GES specifically:** Recruiting and hiring workflows that screen candidates differentially — a live concern for a company hiring across 75+ countries with an active DEIB commitment and Jenna Trosper's People & Culture organization owning fair process. Performance review language that describes similar performance differently depending on who is being described. Vendor and subcontractor selection analyses that encode historical patterns rather than current capability. Client-facing creative that defaults to narrow cultural assumptions when we are building experiences for global audiences across North America, Europe, the Middle East, and India.

There is also a subtler operational version: AI-assisted resource allocation or labor forecasting that quietly reproduces historical staffing inequities across venues or crews because that is what the historical data contains.

**The Copilot control:** For general productivity use — drafting, summarizing, analyzing operational data — bias risk is low. For anything touching people decisions (hiring, promotion, performance, discipline), human review is mandatory and People & Culture must be involved in workflow design. For client-facing creative aimed at global audiences, cultural review by people from those markets is not a nice-to-have. It is quality control. **Understanding** is a T.R.U.E. value for a reason.

### Risk 4: Model Drift

**What it is:** An AI model's performance degrading over time as the real world changes in ways not reflected in the model's training data — or, in the enterprise context, as the grounding data goes stale.

**At GES specifically:** This is a bigger deal for us than most people assume, because our operating environment changes constantly. Venue rules change. Union agreements get renegotiated. Customs regimes shift. Material handling rates change season to season. A venue reconfigures its docks. An AI grounded on last year's show file will confidently describe a marshaling yard procedure that no longer exists.

Generative model drift is managed by Microsoft through continuous model updates. **Grounding drift is ours to manage.** If SharePoint holds three versions of the exhibitor service kit and the current one is not clearly marked, Copilot may ground on the wrong one — and it will do so with complete confidence.

**The Copilot control:** For the generative models, Microsoft handles it. For grounding, the control is content hygiene: current documents clearly identified, superseded versions archived, show document libraries structured and maintained. Chapter 12 covers this in depth. **Your AI is only as current as your SharePoint.**

---

## 8. Building an AI Center of Excellence at GES

An AI Center of Excellence (CoE) is not a department. It is a **coordination function** — a lightweight organizational structure that prevents the AI program from fragmenting into disconnected initiatives in Las Vegas, Chicago, Toronto, London, Amsterdam, and Dubai, each reinventing the wheel, each creating redundant review work, and none of them sharing the learnings that compound over time.

The CoE does not do AI work. It enables AI work. The distinction matters.

:::{figure} ../images/ch04-coe-structure.png
:label: fig-ch04-coe
:alt: Clean org-chart-style diagram showing GES's AI Center of Excellence structure — a small core team with representatives from IT, Legal, Operations, and the business brands (GES Exhibitions, Spiro, onPeak, Visit by GES, SHOWTECH), connected outward to departmental and regional AI Champions and feeding upward to an executive AI Sponsor — showing information flows in both directions
:width: 80%
:align: center

The AI Center of Excellence is not where AI happens. It is the infrastructure that makes AI happen well — across brands, functions, and regions, at scale, with shared learning and consistent governance.
:::

**Core roles in the GES CoE:**

**Executive AI Sponsor** — A senior leader who provides organizational visibility and accountability for the AI program. Given that Lisa Baez already leads Tech-Enabled Services and shipped the onPeak AI Smart Suite, that organization is the natural center of gravity. The Sponsor's job is not operational. It is to ensure AI adoption remains a strategic priority under Derek Linde's leadership agenda, that resourcing decisions get made, and that the program has the cross-functional authority to unblock things.

**AI Program Lead** — The operational coordinator of the CoE. Manages the Champion network, coordinates reviews, tracks the portfolio of AI initiatives, owns the communication calendar, and serves as connective tissue between IT, Legal, and the operating brands. Critically, this person also owns the **Cowork credit budget dashboard** described in Section 6.

**IT Representative** — Owns the technical infrastructure: Microsoft 365 tenant configuration, Copilot and Cowork licensing and access, SharePoint permission hygiene, security architecture review, and integration with GES's existing stack (including Adobe Workfront for creative and graphics workflow).

**Legal/Compliance Representative** — The governance translator, working with Detra Page's office: maps AI use cases to the seven compliance domains, provides input on acceptable use policy, flags anything touching client confidentiality, personal data, customs, or contract interpretation, and maintains the approved use case library.

**Finance Representative** — New, and specific to the Cowork era. Someone from Neal Parsons's organization owns the variable-spend view: credit budgets by department, trend analysis, cost-per-outcome reporting, and the forecast that goes into the annual plan.

**Operations Representative** — Because a CoE staffed only by corporate functions will design workflows that no one on a show floor can use. This role brings show operations reality into every decision: what works during move-in, what works on mobile, what works when you have four hours of sleep and a hall to turn.

**Brand Representatives** — GES Exhibitions, Spiro, onPeak, Visit by GES, and SHOWTECH each have distinct workflows and distinct clients. Light-touch representation from each prevents the CoE from optimizing for one brand's reality.

**Departmental and Regional Champions** — The existing Champion network from Chapter 3, organized into the CoE's extended team. Each Champion is the CoE's eyes and ears in their function and geography — surfacing what is working, what is stalling, and what new use cases are emerging. Regional coverage matters: North America, EMEA, and the Middle East/India operate under different privacy regimes, different labor structures, and different venue norms.

**The three operating cadences:**

```{list-table} AI CoE Operating Cadences
:header-rows: 1
:label: table-ch04-coe-cadences

* - Cadence
  - Participants
  - Agenda
  - Frequency
* - Executive Review
  - Sponsor + Program Lead + Brand Leaders + Finance
  - AI portfolio review, strategic priorities, Cowork spend and cost-per-outcome, resource decisions
  - Monthly
* - Operational Sync
  - Program Lead + IT + Legal + Finance + Champions
  - Pilot updates, review queue, shared learnings, task library additions, blocker resolution
  - Bi-weekly
* - Champion Community
  - All Champions + Program Lead
  - What's working, what's not, prompt and Cowork task library updates, peer support
  - Weekly (async-first, with optional live session across time zones)
```

::::{admonition} 🌍 A Note on Time Zones
:class: note

A CoE for a company operating in 75+ countries cannot run on synchronous meetings. The Champion Community must be **async-first** — a Teams channel with a weekly rhythm, not a weekly call that Dubai and Amsterdam attend at inconvenient hours while Las Vegas talks. Live sessions should rotate their time slots so the inconvenience is shared rather than assigned. This is a small thing that signals a large one: **Understanding** is one of our four values, and how we schedule is how we practice it.
::::

The CoE does not need to be large to be effective. At GES's scale — roughly 2,600+ employees across 24 facilities — a part-time Program Lead, one IT resource, one Legal resource, one Finance resource, one Operations voice, and an active Champion network is sufficient to run a high-functioning AI program. The leverage is in the coordination and the shared learning — not in headcount.

**And we have a head start.** The onPeak team has already navigated the full arc: concept, build, governance review, launch, and iteration on a live AI product with paying customers. The CoE's first act should be to sit down with Lisa Baez's and Tayler Gilmartin's teams and extract every lesson from that experience. What took longer than expected? What did Legal ask for? What did customers actually value? That debrief is worth more than any external consultant's playbook, because it happened here, under our constraints, with our clients.

---

## 9. The Economics — Making the Case for AI Investment

:::{figure} ../images/ch04-cost-of-inaction.png
:label: fig-ch04-cost-of-inaction
:alt: The diverging performance gap between event services companies that adopt AI and those that don't — showing widening differences in proposal turnaround speed, labor forecast accuracy, exhibitor response time, and talent retention over time
:width: 80%
:align: center

The cost of inaction compounds over time — companies that delay AI adoption fall further behind competitors on speed, productivity, and talent retention with every passing show cycle.
:::

We have covered the technology, the compliance environment, the architecture, the Cowork economics, and the organizational structure. Now let's talk about the business case — because every investment at GES requires a defensible return, and AI is no exception.

:::{figure} ../images/ch04-roi-economics.png
:label: fig-ch04-roi
:alt: Clean financial infographic showing the economics of AI adoption at an exhibitions company — three panels: left showing time-savings ROI for event professionals, center showing revenue and win-rate impact of AI-augmented account management and proposal production, right showing cost-of-inaction analysis — each with specific trade show industry numbers
:width: 80%
:align: center

The economics of AI at GES are compelling on three dimensions: time-savings ROI, revenue impact, and cost of inaction. Each dimension alone justifies investment. Together, they make inaction the riskier choice.
:::

### The Time-Savings ROI

PwC's analysis found that professionals who consistently apply AI to their knowledge work recapture an average of 47% of previously consumed task time. Let's put GES numbers around that.

An account or project manager at GES might spend, in a typical week:

- 2 hours researching and preparing for organizer and exhibitor calls
- 3 hours drafting client communications — emails, service kit updates, move-in instructions, status summaries
- 2 hours compiling and formatting reports: labor actuals, freight summaries, post-show recaps
- 1.5 hours on meeting preparation and follow-up documentation across time zones

That is 8.5 hours per week of work that Copilot can materially accelerate. At a 47% efficiency gain, that is **4 hours per week recovered** — time that goes back into the parts of the job that actually differentiate GES: walking the floor, solving the exhibitor's problem before they escalate it, and building the relationship that renews the contract.

Four hours per week at a conservative loaded rate of $85/hour is $340 per person per week — roughly **$17,000 per person per year.** Multiply across the account management, project management, and operations coordination population, and the number becomes significant quickly. And that is one slice of one function.

Now extend the same logic across our other personas:

- **Creative and design teams** using AI for concept development, copy, and iteration on the way to a client review — with Adobe Workfront still governing the production workflow.
- **Logistics and freight coordinators** drafting shipping instructions, checking manifests against packing lists, and producing multilingual documentation for cross-border moves.
- **Show operations** turning site survey notes into punch lists, generating safety briefings, and reconciling labor forecasts against actuals.
- **Corporate functions** — finance, People & Culture, legal, marketing — doing what every corporate function does, faster.

Across roughly 2,600+ employees, even partial adoption produces a number that gets attention in a CFO review.

### The Revenue Impact

Time savings are the easy half of the case. The revenue half is bigger.

**Proposal and RFP velocity.** GES wins work through proposals to organizers and agencies. If AI takes first-draft RFP response time from five days to two, we can pursue more opportunities with the same team — and give each one more human thinking time, because the drafting time collapsed. In a competitive GSC bid, the difference between a good response and a great one is often just whether anyone had time to make it great.

**Pitch quality in experiential.** On the Spiro side, we compete against experiential agencies on creative. AI-assisted ideation and narrative development means more concepts explored per pitch, not fewer hours spent — the ceiling goes up, not just the floor. Chapter 2 made this point about human superpowers; this is where it shows up on an invoice.

**Exhibitor experience and attach rate.** We serve 150,000+ exhibitors a year. Faster, clearer, more accurate responses to exhibitor questions drive both satisfaction scores that organizers care about at renewal *and* order volume through ordering.ges.com. An exhibitor who gets a clear answer in an hour instead of a day is an exhibitor who orders the extra service.

**Retention and renewal.** Organizer relationships are multi-year and renewal-driven — the extended Clarion Events North America partnership is exactly this kind of relationship. Account teams that are better prepared, faster to respond, and sharper in their post-show analysis defend those renewals better.

**Margin on execution.** Better labor forecasting and better freight and drayage analysis directly improve show-level margin. This is not soft ROI. It is the P&L.

### The Cost of Inaction

This is the analysis that does not appear in most ROI models but should. The question is not just "what is the return on AI investment?" but **"what is the cost of not investing?"**

As competitors continue to build AI capability, two things happen simultaneously. Their costs decrease — because AI-assisted professionals are more efficient, and that efficiency compounds. And their client experience improves — because AI-augmented account teams are better prepared, more responsive, and capable of managing more relationships well.

For a company competing for the same organizer contracts, the same exhibitor spend, and the same agency partnerships, the competitive consequence of a 24-month delay in AI capability is not a missed quarter. It is a compounding disadvantage that gets harder to close every show cycle.

There is a talent dimension too, and it is underrated. The people we want to hire — and the people we want to keep — increasingly expect to work somewhere that gives them modern tools. A company that makes people do manual work a machine could do is a company that loses its best operators to one that doesn't.

The BCG framing is the most useful here: **AI leaders generate 1.7× the revenue growth of AI laggards.** Not as a one-time event — as a sustained divergence. The gap widens over time, not closes.

And there is a specifically GES reason this matters right now. The Truelink independence gives us the ability to move without a parent company's approval cycle. That advantage is temporal. It is worth the most in the first two or three years, when the ability to decide quickly is a genuine differentiator. Spending that window deliberating is the most expensive version of inaction available to us.

Inaction is not a neutral choice. It is a choice to be on the losing side of that divergence.

---

## 🧪 Try This — Build Your AI Adoption One-Pager

This is the exercise that the rest of the program builds toward. The AI Adoption One-Pager is a single page that captures your personal roadmap for applying everything in Part I of this book to one specific, real workflow at GES.

It is the seed of your Showcase Project. It is the document you will bring to your manager in a 1:1. It is the thing that transforms this master class from interesting reading into a professional development commitment.

---

::::{admonition} Exercise 1: Build Your AI Adoption One-Pager in Microsoft Word
:class: tip

**Time required:** 30 minutes

**Step-by-step:**

1. Open **Microsoft Word** at [office.com](https://office.com) → Sign in with your GES Microsoft 365 credentials → New Document.
2. Title the document: *My AI Adoption One-Pager — [Your Name] — [Date]*.
3. Complete each of the following five sections — keep each section to three bullet points or fewer. Brevity forces clarity.

**Section 1: The Workflow**
Name the specific, recurring workflow you will redesign with AI assistance. Be precise: not "exhibitor communications" but *"drafting the move-in instruction packet for the 340 exhibitors at our recurring spring show at this venue."* Not "reporting" but *"building the post-show labor variance narrative from forecast versus actual hours."* Specificity is everything.

**Section 2: The Current State**
How long does this workflow currently take? How many people are involved? What is the quality and consistency of the output today? How often does it get done late or under pressure? Describe it plainly — no selling, just facts.

**Section 3: The AI-Assisted Future State**
With Copilot in the workflow, what changes? What does the new process look like, step by step? How long will it take? What is different about the output? Be specific about which Copilot surfaces are involved — Copilot Chat, Copilot in Word, Copilot in Excel, Copilot in Teams — and whether any step warrants a **Cowork task** rather than a single prompt. If you propose Cowork, say which band you expect it to fall in: light, medium, or heavy.

**Section 4: The Metrics**
How will you know it worked? Name two numbers you will track: one for efficiency (time saved, cycle time reduced, volume increased) and one for quality (error rate, exhibitor or organizer feedback, rework requests, output consistency). You do not need to hit these metrics to start. You need to be able to measure them to learn.

**Section 5: The Risks and Controls**
Name the one or two most significant risks in this workflow, and for each, the human control that mitigates it. Run it against the seven compliance domains from Section 3: does it touch union jurisdiction, safety, customs, personal data, contract terms, published ESG figures, or client-confidential information? If yes to any, note who you will clear it with before proceeding.

4. Add one more line at the bottom: **"I will review this document on [date 90 days from today] and report results to [name of manager or accountability partner]."**

5. Save to your OneDrive (File → Save → OneDrive). Name it clearly.
::::

---

::::{admonition} Exercise 2: The GES Compliance Self-Check
:class: tip

**Time required:** 10 minutes

Before you implement the workflow in your One-Pager, run it through this self-check. Open a new document or simply review mentally:

**Step-by-step:**

1. **Does your workflow touch union jurisdiction or labor agreement interpretation?** *If yes:* your Labor Relations lead reviews before implementation. AI may prepare and summarize; it does not determine jurisdiction.

2. **Does your workflow touch safety determinations, incident classification, or rigging/structural calculations?** *If yes:* your safety lead reviews. AI may draft communications and analyze trends; it does not make safety calls.

3. **Does your workflow touch customs classification, valuation, or carnet documentation?** *If yes:* a qualified logistics professional or licensed broker verifies every filing element.

4. **Does your workflow involve personal data** — attendee records, onPeak guest data, Visit by GES lead capture, exhibitor staff details, or employee data? *If yes:* confirm with GES IT and Legal that the specific workflow and data category are approved before proceeding. Do not substitute your own judgment for organizational clearance on personal data.

5. **Does your workflow involve client-confidential material** — unreleased products, embargoed launches, bespoke design files, competitor-adjacent accounts at the same show? *If yes:* confirm handling with your account lead and Legal. Check that source permissions are correct before you point Copilot at anything.

6. **Does your workflow produce numbers or claims that get published** — ESG and emissions figures, client-facing sustainability claims, contractual reporting? *If yes:* every number gets traced to source and verified by the owning function before publication.

7. **Does your workflow involve contract interpretation or any binding commitment to an organizer, venue, or exhibitor?** *If yes:* Legal reviews. AI summarizes contracts; it does not interpret them.

8. **If you answered "no" to all seven** — your workflow is in the fast lane. Proceed with the verification discipline: human review of every output before it leaves your hands.

**What you are practicing:** applying proportional governance to your own AI use — not excessive caution, but appropriate professional judgment about where human oversight is most critical. This is **Responsibility** in the T.R.U.E. values, made operational.
::::

---

::::{admonition} Exercise 3: Ask Copilot to Pressure-Test Your One-Pager
:class: tip

**Time required:** 15 minutes

**Step-by-step:**

1. Navigate to [m365.cloud.microsoft](https://m365.cloud.microsoft) → Copilot Chat. Sign in with your GES Microsoft 365 credentials. Confirm the green enterprise shield.

2. Paste this prompt — and then share the full text of your One-Pager after the colon:

> *"I work at GES, a global provider of exhibition and experiential marketing services — we act as general service contractor for trade shows, build custom exhibits, manage event housing, and provide event technology. I have written a one-page AI adoption plan for a specific workflow I want to redesign with Microsoft Copilot. I want you to play the role of a skeptical but supportive senior operations leader reviewing this plan before I present it to my manager. Review my plan and do four things: (1) Identify the two most significant gaps or weaknesses in my plan. (2) Ask me the two questions a senior leader would most likely ask that my plan doesn't currently answer. (3) Stress-test whether this workflow holds up during a live move-in, when people are on a show floor and time-constrained. (4) Suggest one specific improvement that would make this plan significantly stronger. Here is my plan: [paste your One-Pager text here]"*

3. Read the response carefully. Update your One-Pager accordingly — not necessarily to add more content, but to strengthen the content you have.

4. When you are satisfied with the strengthened version, save the updated document to OneDrive.

**What you are practicing:** using AI as a quality-control tool for your own strategic thinking — the highest-leverage prompting application for decision-makers and project leaders.
::::

---

::::{admonition} Exercise 4: Estimate Your Cowork Task Band
:class: tip

**Time required:** 10 minutes

This exercise builds the cost intuition that Section 6 argues is a core adoption skill.

**Step-by-step:**

1. Take the workflow from your One-Pager. Write down every distinct step a person currently performs.

2. For each step, mark it:
   - **(P)** — a single Copilot prompt would do it (included in your seat license)
   - **(A)** — a Copilot action inside Word, Excel, PowerPoint, or Teams would do it (included in your seat license)
   - **(C)** — genuinely needs a multi-step Cowork task (usage-based credits)

3. For every step you marked **(C)**, estimate the band using the Section 6 table: light, medium, or heavy. Ask specifically: how many sources does it need to retrieve? How many tool calls? How long will it run?

4. Now do the important part. **Rewrite each (C) step with tighter scope.** Name the exact sources. Set a date range. Define the stopping condition. Specify the output format. Then re-estimate the band.

5. Write one sentence answering: *"For the credits this task consumes, what does GES get?"* If you cannot answer that in one sentence, the task is not scoped well enough yet.

**What you are practicing:** treating AI cost as an operational variable you control through prompt design — the same discipline you already apply to labor hours and freight weight. Scoping is a cost control. It is also, conveniently, how you get better output.
::::

---

## Chapter Summary

Chapters 1 through 4 form a complete foundation.

Chapter 1 gave you the conceptual framework — the LLM, context engineering, the flashlight, the persona, meta-prompting, and agents. Chapter 2 gave you the personal operating system — the mindset that determines whether everything else sticks. Chapter 3 gave you the organizational blueprint — how individual action becomes collective behavior. And this chapter has given you the strategic architecture: where our industry actually is, why pilots stall, what GES's real compliance environment requires, how Microsoft 365 Copilot is built for exactly this environment, how the new Cowork economics work and how to govern them, what risks to manage and how, what organizational structure enables scale, and what the business case looks like.

You now have the complete map.

**Part II of this book — beginning with Chapter 5 — is where you start driving.**

We go application by application, workflow by workflow, through the Microsoft 365 Copilot suite: Word, Excel, PowerPoint, Teams, OneNote, SharePoint. Not conceptually. Hands-on. In your actual Microsoft 365 environment, doing real work on real shows, building real habits.

The strategy in Part I becomes the practice in Part II. And the practice becomes the Showcase Project in Part IV.

GES has been building experiences since 1939. We have been independent since December 31, 2024. We already have production AI running in onPeak. The foundation is solid. The road ahead is clear.

Let's build.

---

:::{note}
**Chapter 4 — Key Takeaways**

1. GES is not starting from zero. The onPeak AI Smart Suite is live production AI, built here, under our constraints. The CoE's first act should be to debrief that team and reuse what they learned.
2. Truelink independence since December 31, 2024 means GES controls its own technology roadmap for the first time in decades. That advantage has a shelf life — it is worth the most right now.
3. Pilots stall in the Valley of Death by default, and at GES the Valley has a specific name: show season. Structural choices that prevent it must be made before the pilot launches, and pilot checkpoints must be scheduled against the show calendar.
4. GES's compliance environment is real and specific: union jurisdiction, venue safety and OSHA, international customs and carnets, GDPR and attendee data privacy, organizer and venue contract compliance, ESG and emissions reporting, and client confidentiality. Proportional governance — not blanket restriction — is the answer.
5. Client confidentiality is our sharpest obligation. We see unreleased products and competitor plans before the world does, often for direct rivals at the same show. That is the **T** in T.R.U.E., and it applies inside the prompt window.
6. Microsoft 365 Copilot's enterprise architecture maps directly to those requirements: enterprise data boundary, permission inheritance, Purview audit logging, and information protection labels. Permission hygiene at the source is a prerequisite, not a follow-up task.
7. Microsoft Graph and Work IQ make Copilot contextually aware of your actual work — and Work IQ is the grounding layer that keeps Cowork anchored to GES reality.
8. **Copilot Cowork (GA June 16, 2026)** runs on Anthropic Opus 4.8 and Sonnet 4.6, is cloud-hosted inside the Microsoft 365 trust boundary, and is billed **usage-based in Copilot Credits on top of the M365 Copilot seat license.** Cost is driven by model use, context retrieval, tool calls, and runtime, across light / medium / heavy task bands. Microsoft's testing claims 30–40% lower cost per prompt than Claude Cowork via the M365 connector.
9. Variable AI spend needs the same discipline we apply to any variable cost: bounded pilots, departmental budgets and thresholds, cost-per-outcome measurement, scoping as a cost control, a reusable task library, and monthly review with finance in the room.
10. Four AI risk dimensions require management — data leakage, hallucination, bias, and model drift. Grounding drift is ours to manage: your AI is only as current as your SharePoint.
11. An AI Center of Excellence is a coordination function, not a department. Lightweight, cross-functional, cross-brand, async-first across time zones, and powered by Champions.
12. The economics are compelling on three dimensions: time-savings ROI, revenue impact (proposal velocity, pitch quality, exhibitor experience, renewal defense, execution margin), and cost of inaction. AI leaders generate 1.7× the revenue growth of laggards, and the gap widens.
:::

---

:::{seealso}
**Resources for Chapter 4**

- 🤖 Microsoft 365 Copilot: [m365.cloud.microsoft](https://m365.cloud.microsoft)
- 🔒 Microsoft 365 Copilot Data Privacy & Security: [learn.microsoft.com/copilot/microsoft-365/microsoft-365-copilot-privacy](https://learn.microsoft.com/en-us/copilot/microsoft-365/microsoft-365-copilot-privacy)
- 📊 Microsoft Purview Compliance: [learn.microsoft.com/microsoft-365/compliance](https://learn.microsoft.com/en-us/microsoft-365/compliance/)
- 💳 Microsoft Copilot Credits & Usage-Based Billing: [learn.microsoft.com/copilot](https://learn.microsoft.com/en-us/copilot/)
- 📖 Microsoft Copilot Adoption Hub: [adoption.microsoft.com/copilot](https://adoption.microsoft.com/en-us/copilot/)
- 🏗️ GES Exhibitor Resources & Ordering Portal: [ordering.ges.com](https://ordering.ges.com)
- 🌱 GES ESG Reporting and Sustainability: [ges.com](https://www.ges.com)
- 🛡️ OSHA Standards and Guidance: [osha.gov](https://www.osha.gov)
- 🌍 ICC ATA Carnet Information: [iccwbo.org](https://iccwbo.org)
- 🔐 GDPR Official Text and Guidance: [gdpr.eu](https://gdpr.eu)
- 📊 BCG AI Adoption Research: [bcg.com](https://www.bcg.com)
- 📊 McKinsey State of AI: [mckinsey.com](https://www.mckinsey.com)
:::

---

```{glossary}
AI Center of Excellence (CoE)
  A lightweight organizational coordination function that prevents AI adoption from fragmenting into disconnected initiatives across brands, functions, and regions — maintaining shared governance, shared learning, and shared standards across GES.

Microsoft Graph
  The technical data layer underlying Microsoft 365 that connects all M365 services into a unified model of a user's work activity — enabling Copilot to synthesize across email, calendar, documents, and Teams conversations contextually.

Work IQ
  Microsoft's applied intelligence layer built on the Microsoft Graph — enabling Copilot and Copilot Cowork to answer contextual questions about a user's actual work environment, and to ground agentic tasks in real GES data, without manual data loading.

Copilot Cowork
  Microsoft's agentic work surface, generally available June 16, 2026. Cloud-hosted, grounded in Work IQ, operating inside the Microsoft 365 trust boundary, and multi-model — running on Anthropic Opus 4.8 and Sonnet 4.6. Billed usage-based in Copilot Credits on top of the M365 Copilot seat license.

Copilot Credits
  The usage-based billing unit for Copilot Cowork. Consumption per task is driven by four inputs — model use, context retrieval, tool calls, and runtime — and tasks are categorized as light, medium, or heavy.

Task Band (Light / Medium / Heavy)
  Microsoft's categorization of Cowork task intensity. Light tasks are narrow-scope and short-running; medium tasks span multiple sources and produce a deliverable; heavy tasks involve extended reasoning across large retrieval sets. Choosing the band deliberately is a core cost-control skill.

Union Jurisdiction
  The set of rules — varying by city, venue, local, and agreement — determining which categories of worker may perform which tasks on a show floor. A determination that must always be made by a qualified human, never by AI.

Carnet (ATA Carnet)
  An international customs document permitting temporary duty-free import of goods, widely used for exhibition materials moving across borders. Errors can strand a client's stand in customs while their show opens without them.

Drayage / Material Handling
  The movement of exhibitor freight from the dock or advance warehouse to the booth space on the show floor and back out again — a core GES service and a significant cost line for exhibitors.

EAC (Exhibitor Appointed Contractor)
  A contractor engaged directly by an exhibitor rather than the show's general service contractor, operating on the show floor under rules set by the organizer and venue. Spiro often serves in this capacity.

GSC (General Service Contractor)
  The official on-site service provider appointed by a show organizer, responsible for the operational delivery of the exhibition — floor plan execution, decorating, labor coordination, material handling, and exhibitor services. GES's core role.

Permission Inheritance
  The architectural principle by which Microsoft 365 Copilot respects existing M365 access controls — ensuring the AI can only surface data the requesting user is already authorized to access. Makes source permission hygiene a prerequisite for safe AI adoption.

Hallucination
  The AI phenomenon in which a model generates factually incorrect information with apparent confidence — requiring human verification of all factual outputs in client-facing, safety, contractual, or published contexts.

Grounding Drift
  The degradation of AI output quality caused not by the model but by stale or ambiguous source content — outdated exhibitor service kits, superseded venue rules, or unarchived prior-year show files sitting alongside current ones.

Valley of Death
  The organizational phase between a successful AI pilot and enterprise scaling — characterized by review queues, fading momentum, and, at GES specifically, the arrival of show season with no structure to sustain the effort through it.

AI Adoption One-Pager
  A single-page personal implementation plan identifying the specific workflow, current state, AI-assisted future state, metrics, and risk controls for a professional's first AI deployment — the seed of the Showcase Project.

Microsoft Purview
  Microsoft's compliance and data governance platform — providing audit logging, data classification, information protection, and compliance management for all Microsoft 365 activity including Copilot and Cowork interactions.

Proportional Governance
  The principle that AI governance intensity should be calibrated to the risk of the specific use case — enabling a fast lane for low-risk productivity work while applying full scrutiny to union jurisdiction, safety, customs, personal data, contracts, published ESG figures, and client-confidential information.
```
