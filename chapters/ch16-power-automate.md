---
title: "Chapter 16: Microsoft Power Automate — From Assistance to Automation"
subtitle: "The Third Gear — Where Work Happens Without You"
short_title: "Power Automate"
description: "Power Automate is where the progression completes: from asking Copilot (one question, one answer) to delegating to Cowork (multi-step, run once) to automating permanently (the work happens every time the trigger fires, forever, without a human in the loop). This capstone chapter covers cloud flows versus desktop flows, triggers, Copilot inside Power Automate, AI Builder for document processing, the Cowork-to-flow progression, ten GES automation scenarios, governance that prevents automation from becoming machine-speed error production, honest limitations, and a build-your-first-flow walkthrough."
label: ch-16-power-automate
tags: [Power Automate, automation, RPA, cloud flows, desktop flows, triggers, AI Builder, Copilot, document processing, GES, drayage, material handling, exhibitor services, onPeak, governance, T.R.U.E., connectors, approval flows]
---

```{admonition} Download this Chapter as PDF
:class: tip

[Download PDF](https://github.com/liquid-books/ges-learns-ai/raw/main/pdfs/ch16-power-automate.pdf)
```

# Chapter 16: Microsoft Power Automate — From Assistance to Automation

:::{figure} ../images/ch16-power-automate-infographic.png
:label: fig-ch16-infographic
:alt: Illustrated explainer infographic showing the progression from Copilot (conversation) to Cowork (delegation) to Power Automate (permanent automation), with trigger types, cloud and desktop flows, and GES automation scenarios arranged in a connected system diagram. Blue and orange color scheme with exhibition industry examples.
:width: 80%
:align: center

The three gears of Microsoft 365 intelligence — Copilot for asking, Cowork for delegating, Power Automate for automating. This chapter completes the arc: from human-in-the-loop to human-at-the-start, from one-off assistance to permanent operational infrastructure.
:::

> *"The first rule of any technology used in a business is that automation applied to an efficient operation will magnify the efficiency. The second is that automation applied to an inefficient operation will magnify the inefficiency."*
> — Bill Gates

It is 6:47 a.m. on a Monday. Nobody is in the office yet. In a SharePoint library, a file appears: the final labor actuals for a show that closed over the weekend. That file's appearance triggers a flow.

Within seconds, the flow opens the labor data, cross-references it against the forecast, computes the variance by crew and by phase, flags anything over eight percent, generates a reconciliation workbook, drafts a summary narrative, and posts a notification to the show team's channel with a link to the finished package — all before the first coffee is poured.

The show manager reviews it on the train. The account director sees it before their 9 a.m. call with the organizer. What used to be a four-hour task that waited until someone had a free afternoon is done, documented, and waiting for human judgment on the parts that require it.

That is Power Automate. And it is where everything in this book converges.

---

## 1. The Three Gears — And Why This Is the Third

Every chapter before this one taught you to work with AI. Chapter 14 taught you to delegate to it. This chapter teaches you to **step out of the loop entirely** — to build automation that runs without you, every time the trigger fires, forever.

:::{figure} ../images/ch16-three-gears.png
:label: fig-ch16-three-gears
:alt: Three interconnected gears diagram showing the progression from Copilot (you ask, human in the loop every turn) to Cowork (you delegate, human approves at checkpoints) to Power Automate (you automate, work happens without you). Each gear is labeled with its mode, human involvement level, and a GES example.
:width: 80%
:align: center

The three gears of Microsoft 365 intelligence. Each gear serves a different purpose, and knowing when to use which is the professional skill this chapter builds.
:::

The distinction is structural, not just a matter of degree.

```{list-table} The three gears compared
:header-rows: 1
:name: table-ch16-three-gears

* - 
  - **Copilot**
  - **Cowork**
  - **Power Automate**
* - **Mode**
  - You ASK
  - You DELEGATE
  - You AUTOMATE
* - **Interaction**
  - Conversation — one prompt, one response
  - Assignment — describe the outcome, review at checkpoints
  - Trigger — set it once, it runs forever
* - **Human role**
  - In the loop every turn
  - Approves at designed checkpoints
  - At the start (design) and the end (review outputs)
* - **Runs when**
  - You ask
  - You assign (or schedule)
  - The trigger fires — a file appears, a form is submitted, a date arrives
* - **Best for**
  - One-off questions, drafting, ideation
  - Multi-step projects, finished artifacts
  - Repetitive tasks that should never require a human again
* - **GES example**
  - "Summarize the venue's dock restrictions"
  - "Produce the post-show reconciliation package"
  - "Every time a labor file posts, generate and distribute the reconciliation"
```

:::{important}
**The key insight: Cowork is how you discover what is worth automating.**

You delegate a task to Cowork a few times. You see it work. You understand its shape, its edge cases, and where it needs human judgment versus where it is purely mechanical. Then — and only then — you build a Power Automate flow so the mechanical part never needs a human again.

Cowork is the prototype. Power Automate is production.
:::

This progression matters because it prevents the most common automation failure: building a flow for a process you do not fully understand. Delegating first, manually, teaches you the process. Then automation codifies what you learned.

---

## 2. What Power Automate Actually Is

Power Automate is Microsoft's automation platform within the Power Platform family. It connects systems, moves data, and executes logic — either through APIs in the cloud or through UI automation on a desktop.

:::{figure} ../images/ch16-cloud-vs-desktop-flows.png
:label: fig-ch16-cloud-desktop
:alt: Split comparison diagram showing cloud flows on the left (API-to-API, runs in Microsoft's cloud, connects modern systems via connectors) and desktop flows on the right (UI automation, runs on a Windows machine, clicks and types in legacy applications). Center shows how the two can be combined.
:width: 80%
:align: center

Cloud flows connect modern systems through APIs. Desktop flows automate legacy applications by recording and replaying user actions. The combination handles everything from modern SaaS platforms to green-screen terminals.
:::

### Cloud Flows — The Modern Path

Cloud flows run in Microsoft's cloud. They connect systems through **connectors** — pre-built integrations with over 1,000 services including SharePoint, Outlook, Teams, Excel, Dataverse, Dynamics 365, Salesforce, ServiceNow, SAP, and hundreds more.

When a cloud flow runs, it calls APIs. No human clicks anything. No browser opens. The work happens in the background, at machine speed, and you receive the output.

**At GES:** An exhibitor submits an order through the exhibitor portal. A cloud flow captures the submission, extracts the order data, routes it to the appropriate show operations team, logs it in the tracking workbook, and sends the exhibitor a confirmation — all within seconds of the submit button being clicked.

### Desktop Flows — The RPA Path

Not every system has a modern API. Freight management systems, legacy show operations platforms, venue-specific terminals, and older ERP systems often have no programmatic interface at all. The only way to get data in or out is through the same screens a human uses.

**Desktop flows** solve this through Robotic Process Automation (RPA). Power Automate Desktop records a user's actions — clicks, keystrokes, screen navigation — and replays them. It literally operates the application the way a human would, just faster and more reliably.

**Why RPA exists:** Not because it is elegant, but because the alternative is manual data entry in perpetuity. When the only interface is a 1990s terminal, RPA is the bridge.

**At GES:** A legacy freight system has no API. Every weight and piece count must be keyed manually from the manifest. A desktop flow reads the manifest workbook, opens the legacy terminal, navigates the screens, and enters the data — forty shipments in the time it takes a human to do three.

### The Combination

The real power appears when cloud and desktop flows work together. A cloud flow triggers on an event (a file appears, a form is submitted), calls a desktop flow to interact with a legacy system, and then continues in the cloud to update SharePoint, send notifications, or feed the data downstream.

**At GES:** A reconciliation file arrives in SharePoint (cloud trigger). The flow calls a desktop flow to extract data from a legacy show operations system that has no API. The desktop flow returns the data. The cloud flow computes the variance, generates the report, and posts to the show team's channel.

---

## 3. Triggers — The Conceptual Heart of Automation

A flow without a trigger is just a process waiting to be manual again. The trigger is what makes automation automatic.

:::{figure} ../images/ch16-trigger-types.png
:label: fig-ch16-triggers
:alt: Four-quadrant diagram showing trigger types for Power Automate flows. Top left: Scheduled (runs on a cadence — daily, weekly, monthly). Top right: Event-Driven (runs when something happens — file created, email received, form submitted). Bottom left: Manual (instant — runs when a user clicks a button). Bottom right: Approval-Based (runs when an approval is granted or rejected).
:width: 80%
:align: center

The four trigger types determine when automation fires. Choosing the right trigger is half the design decision.
:::

```{list-table} Trigger types and GES applications
:header-rows: 1
:name: table-ch16-triggers

* - Trigger Type
  - When It Fires
  - GES Example
* - **Scheduled**
  - On a defined cadence — hourly, daily, weekly, at a specific time
  - Every Monday at 6 a.m., generate the cross-show freight variance report for shows in move-in this week
* - **Event-driven**
  - When something happens — a file appears, an email arrives, a form is submitted, a record is created
  - When a final labor file posts to SharePoint, generate the reconciliation package
* - **Manual (Instant)**
  - When a user clicks a button or invokes the flow
  - An account director clicks "Generate QBR Package" and receives the assembled deck and data in five minutes
* - **Approval-based**
  - When an approval is granted, rejected, or times out
  - When a show manager approves the exhibitor order change, update the tracking workbook and notify the exhibitor
```

### Event-Driven Is Where the Magic Lives

Scheduled flows are useful — the Monday morning report, the Friday compliance sweep, the monthly cost analysis. But **event-driven flows** are what make automation feel like infrastructure rather than a scheduled chore.

The pattern: something happens in the real world, and the system responds without waiting for a human to notice.

- An exhibitor service kit question arrives via email → extract the question, classify it, route it to the right inbox, and post to the show channel
- A venue's updated rules document is uploaded → notify every show team working at that venue this season
- A safety walk checklist is submitted with a failed item → escalate immediately to the facility safety lead
- A hotel block pickup report shows a threshold breach → alert the onPeak team and draft a recommendation

The discipline: **design the trigger before you design the actions.** The trigger is the business logic. The actions are just execution.

---

## 4. Copilot Inside Power Automate — Describing Flows in Plain English

The single biggest barrier to Power Automate adoption has always been the learning curve. Building flows required understanding connectors, actions, conditions, and loops — skills that took time to develop.

**Copilot changes that equation.** You can now describe what you want a flow to do in natural language, and Copilot builds it.

:::{figure} ../images/ch16-copilot-builds-flow.png
:label: fig-ch16-copilot-flow
:alt: Screenshot-style diagram showing the Copilot flow creation experience. Left panel shows a natural language prompt describing the desired automation. Right panel shows the flow structure Copilot generated, with connectors, triggers, and actions visible in the designer.
:width: 80%
:align: center

Copilot in Power Automate translates natural language descriptions into working flow structures. The barrier to entry drops dramatically — but the responsibility to review what was built does not.
:::

**The prompt:** *"When an email arrives from any address ending in @ges.com with 'Urgent' in the subject, extract the sender's name and the subject, post a message to the Show Operations channel in Teams, and send me a mobile notification."*

**Copilot's response:** A complete flow structure with the email trigger, condition logic, Teams posting action, and push notification — ready to review, refine, and deploy.

### What This Means for GES

The operational teams who know the process best are no longer dependent on a developer to translate that knowledge into automation. A show manager who has run the same show four years in a row understands exactly when escalations should fire and what information needs to reach whom. With Copilot, they can describe that directly and see a working draft.

That said: **Copilot lowers the barrier to building. It does not lower the barrier to building well.** A flow built in five minutes from a vague prompt is still a vague flow. The professional skill is in the specificity of the description and the rigor of the review.

:::{tip}
**The good prompt pattern for Copilot flow creation**

1. **State the trigger explicitly.** "When a file is created in the Show 5108 Post-Show folder..."
2. **Name the specific actions.** "...extract the labor hours from column C, compare them to the forecast in the Labor Forecast workbook..."
3. **Specify the outputs.** "...create a variance summary in a new row of the Reconciliation Tracker, and post to the Show 5108 channel with a link to the file."
4. **Include constraints.** "Do not run on files that contain 'DRAFT' in the filename."

Vague in, vague out. Specific in, specific out.
:::

---

## 5. AI Builder — Intelligence Inside the Flow

AI Builder is Microsoft's embedded AI capability for Power Platform. It brings document processing, text classification, object detection, and prediction directly into Power Automate flows.

:::{figure} ../images/ch16-ai-builder-extraction.png
:label: fig-ch16-ai-builder
:alt: Process diagram showing AI Builder document processing within a Power Automate flow. A PDF form enters the flow, AI Builder extracts structured fields (exhibitor name, booth number, order items, quantities), and the extracted data flows into downstream actions (database update, confirmation email, tracking workbook).
:width: 80%
:align: center

AI Builder extracts structured data from unstructured documents — forms, invoices, letters — and feeds it into the flow as usable fields. No manual data entry required.
:::

### Document Processing at GES Scale

Consider the volume: 150,000+ exhibitors, many submitting paper or PDF order forms. Each form contains exhibitor name, booth number, show code, order items, quantities, and special instructions. Historically, that is manual data entry — slow, error-prone, and scaling linearly with show size.

AI Builder's document processing models extract those fields automatically. The flow receives a PDF, AI Builder reads it, and the structured data flows downstream — into the order tracking system, the confirmation email, the billing workbook.

**Pre-built models** handle common document types: invoices, receipts, business cards, identity documents. **Custom models** can be trained on GES-specific forms — exhibitor service kit order forms, freight authorization forms, badge request forms — with training requiring only a handful of labeled examples.

### Other AI Builder Capabilities

- **Text classification:** Automatically categorize incoming exhibitor questions by topic (freight, labor, electrical, deadlines) and route accordingly
- **Sentiment analysis:** Flag exhibitor communications showing frustration before they escalate
- **Object detection:** Identify and count items in site survey photos
- **Prediction:** Forecast labor hours based on historical show characteristics

The pattern is consistent: intelligence that used to require a human to interpret now happens inside the flow, at machine speed.

---

## 6. The Handoff Pattern — Cowork → Power Automate

:::{figure} ../images/ch16-cowork-to-flow-progression.png
:label: fig-ch16-progression
:alt: Three-stage progression diagram showing the journey from manual process to automated flow. Stage 1: Cowork Prototype (delegate the task 2-3 times, learn its shape). Stage 2: Refinement (adjust the prompt, understand edge cases). Stage 3: Power Automate Production (build the flow, deploy, monitor).
:width: 80%
:align: center

The Cowork-to-flow progression: prototype with delegation, refine through iteration, then automate for production. This sequence prevents the most common automation failure — building a flow for a process you do not fully understand.
:::

Never build a flow for a process you have only done once. The failure mode is obvious in hindsight: you automate the wrong thing, or you automate it incompletely, and then the flow runs hundreds of times before anyone notices.

The discipline is a progression:

**Stage 1 — Cowork prototype.** Delegate the task to Cowork two or three times. Use the five-part structure from Chapter 14 (Outcome, Inputs, Definition of done, Constraints, Approval scope). Observe what works and what does not. Note the edge cases.

**Stage 2 — Refinement.** Adjust the assignment based on what you learned. Where did Cowork need clarification? Where did the output require manual correction? Those are the places your flow will break if you do not account for them.

**Stage 3 — Power Automate production.** Only now — after you understand the process, its variations, and its exceptions — build the flow. The Cowork prompt becomes the flow's specification. The edge cases become condition logic. The manual corrections become error handling.

```{list-table} Decision framework — which gear to use
:header-rows: 1
:name: table-ch16-decision-framework

* - If...
  - Then use...
  - Because...
* - One question, one answer, right now
  - **Copilot Chat**
  - You need the response in conversation, not as a finished artifact
* - Multi-step work producing a finished artifact, run once or on request
  - **Cowork**
  - You need a deliverable, not a conversation, and it is not yet routine
* - The same task, every time the trigger fires, without human initiation
  - **Power Automate**
  - You have delegated it enough times to understand its shape, and now you want it to run forever
* - You have done the task manually only once
  - **Not Power Automate yet**
  - Automating a process you do not understand multiplies the uncertainty
```

::::{admonition} 🧭 T.R.U.E. Check — Trust
:class: note

**Trust each other to always be honest and do what's right.**

Trust in automation is earned, not assumed. A flow you built after prototyping with Cowork carries the credibility of tested logic. A flow you built from a guess carries the risk of guessed logic running at machine speed. Prototype first. Automate second. Trust third.
::::

---

## 7. GES Automation Scenarios — Ten Flows That Compound

At 4,000+ events a year, GES work is overwhelmingly **repetitive**. The same show returns to the same venue. The same exhibitor submits the same kind of order. The same reconciliation happens after every move-out. That repetition is exactly what automation compounds against.

A flow that saves 20 minutes and runs 4,000 times a year is not a convenience. It is over 1,300 hours.

:::{figure} ../images/ch16-ges-automation-map.png
:label: fig-ch16-automation-map
:alt: Visual map showing ten GES automation scenarios arranged by function (Show Operations, Exhibitor Services, Logistics, Safety, Housing, Sales) and trigger type (event-driven vs scheduled). Lines connect related flows to show how automation compounds across the show lifecycle.
:width: 80%
:align: center

Ten automation scenarios mapped across GES functions. Each flow represents time recovered — time that compounds across thousands of shows.
:::

### Scenario 1 — Exhibitor Order Form Intake

**Trigger:** An exhibitor submits an order form (PDF or web form)

**The flow:**
1. AI Builder extracts: exhibitor name, booth number, show code, order items, quantities, special instructions
2. Validate against the show's exhibitor list — is this a registered exhibitor?
3. Route to the appropriate show operations team based on show code
4. Log the order in the tracking workbook
5. Send the exhibitor a confirmation email with order summary and deadlines
6. If rush order (move-in < 7 days), post an alert to the show channel

**Time saved per instance:** 12 minutes of manual processing

**Annual impact at GES scale:** With tens of thousands of exhibitor orders annually, even conservative estimates yield thousands of hours recovered.

### Scenario 2 — Post-Show Reconciliation on Labor File

**Trigger:** Final labor actuals file posted to the show's SharePoint library

**The flow:**
1. Open the labor file and the original forecast
2. Compute variance by crew, by phase, by jurisdiction
3. Flag any variance over 8%
4. Generate the reconciliation workbook on the standard template
5. Draft the summary narrative
6. Save both to the Post-Show folder
7. Post to the show channel with links

**Time saved per show:** 3-4 hours

**Annual impact:** At 4,000+ shows, even if half have automated reconciliation, the compounding is substantial.

### Scenario 3 — Freight Target Variance Alert

**Trigger:** Daily at 6 a.m. during move-in week, or when a weight file updates

**The flow:**
1. Pull current inbound weights from the advance warehouse receiving log
2. Compare against agreed freight targets
3. If variance exceeds threshold (e.g., 15% over target with 3+ days remaining):
   - Alert the logistics team
   - Draft talking points for the organizer conversation
4. Log the variance to the tracking workbook

**Value:** Catches freight surprises before they become show-floor surprises.

### Scenario 4 — Site Survey Photo and Report Filing

**Trigger:** A site survey report or photo batch is uploaded to the staging folder

**The flow:**
1. Identify the venue from the file name or metadata
2. Move to the correct folder in the Venue Knowledge Library
3. Apply the standard naming convention
4. Update the venue profile with "Last Survey" date
5. Notify the regional operations director

**Value:** Institutional knowledge lands in the right place automatically instead of sitting in someone's OneDrive.

### Scenario 5 — Move-In Daily Log Distribution

**Trigger:** Daily at 6 p.m. during move-in, or when the daily log file is created

**The flow:**
1. Compile the day's activity: exhibitors checked in, freight received, issues logged
2. Format as a summary email
3. Send to the show team distribution list
4. Post to the show channel with any flagged items highlighted

**Value:** The show team starts the next day knowing what happened while they were off the floor.

### Scenario 6 — Organizer RFP Intake and Acknowledgement

**Trigger:** An email arrives at the RFP inbox with an attachment

**The flow:**
1. Extract the RFP document
2. Save to the RFP Library with the sender's organization name and date
3. Send an automated acknowledgement to the sender
4. Post to the Sales channel with sender info and a link
5. Create a follow-up task due in 48 hours

**Value:** No RFP sits unacknowledged, and the paper trail starts immediately.

### Scenario 7 — onPeak Hotel Block Pickup Monitoring

**Trigger:** Weekly (or when a pickup report uploads)

**The flow:**
1. Pull current pickup data by property
2. Compare against the historical curve for this show at equivalent weeks-to-cutoff
3. Calculate attrition exposure at current pace
4. If exposure exceeds threshold, alert the onPeak team with:
   - The properties driving the shortfall
   - The dollar exposure by property
   - Draft recommendation (release rooms, extend deadline, or hold)
5. Log to the pickup tracking workbook

**Value:** Attrition risk is surfaced while there is still time to act.

### Scenario 8 — Safety Walk Checklist Escalation

**Trigger:** A safety walk checklist is submitted via Microsoft Forms

**The flow:**
1. Parse the responses
2. If any critical item is marked "Fail":
   - Immediately notify the facility safety lead
   - Post to the Safety channel with the failed item and location
   - Create a corrective action task
3. If all items pass, log to the safety record and confirm to the submitter

**Value:** Safety failures escalate in seconds, not hours.

### Scenario 9 — Access Review Triggered at Move-Out

**Trigger:** The show's move-out date passes

**The flow:**
1. Pull the current access list for the show's SharePoint site
2. Generate a review report: who has access, when it was granted, last activity
3. Send to the show manager for review
4. Flag any external sharing or organization-wide links for immediate attention
5. Schedule a follow-up in 14 days if review not completed

**Value:** This is Chapter 12's cross-client contamination control, automated. Access does not outlive the show.

### Scenario 10 — Recurring Cross-Show Drayage Variance Report

**Trigger:** Monthly on the third business day

**The flow:**
1. Pull all reconciliation files for shows that closed in the prior month
2. Compute drayage and material handling variance for each
3. Normalize by net square footage for comparability
4. Generate the variance workbook with tabs by venue and by account
5. Generate the summary narrative
6. Post to the Logistics Analytics channel

**Value:** The analysis Chapter 13 described — cross-show cost patterns — runs without anyone initiating it.

---

## 8. Governance — The Discipline That Makes Automation Safe

:::{figure} ../images/ch16-approval-checkpoint.png
:label: fig-ch16-approval
:alt: Flowchart showing an approval step embedded within a Power Automate flow. The flow pauses, sends an approval request to a designated approver, waits for response, and branches based on approved/rejected outcome. Labels indicate where human judgment re-enters the automated process.
:width: 80%
:align: center

Approval steps are designed control points, not friction. They embed human judgment exactly where it belongs — at moments of consequence.
:::

Automation is not inherently good. **An automated bad process is a bad process running at machine speed, forever.**

This section is not optional. It is the difference between automation as operational infrastructure and automation as risk multiplication.

### The Cardinal Rule: Never Automate an Unverified Process

:::{warning}
**Before you build a flow, ask: have I done this manually at least twice?**

If the answer is no, you are automating a guess. Guesses at machine speed, repeated thousands of times, produce outcomes nobody anticipated — and they produce them confidently, without error messages, because the flow is doing exactly what you told it to.

Cowork exists precisely so you can prototype before you automate. Use it.
:::

### Flow Ownership and Orphaned Flows

Every flow runs under the identity of its **owner** — the person who created it or was assigned ownership. The flow sees what the owner can see. It acts with the owner's permissions.

When someone leaves the company, their flows do not stop running. They become **orphaned** — still executing, still using connections that may become stale, still producing outputs nobody is reviewing.

**The governance requirement:**
- Every flow has a named owner, visible and accountable
- Flow ownership transfers explicitly when someone changes roles or leaves
- Quarterly sweeps identify orphaned flows and decommission or reassign them
- Flows touching client data or external communications require a secondary reviewer

:::{figure} ../images/ch16-flow-ownership-risk.png
:label: fig-ch16-ownership
:alt: Risk diagram showing flow ownership and the orphaned flow problem. Left: Active flow with owner, monitored and maintained. Center: Owner leaves without transfer. Right: Orphaned flow continues running, connections fail silently, outputs go unreviewed.
:width: 80%
:align: center

The orphaned flow problem: when an owner leaves without transferring ownership, flows continue running without oversight — a silent failure waiting to become a visible one.
:::

:::{danger}
**A flow runs with its owner's permissions.**

If an account director who has broad access to multiple client sites builds a flow, that flow inherits that access. A poorly scoped flow can read from one client's library and write to another's — not through malice, but through overly broad design.

This is Chapter 12's cross-client contamination risk, expressed in automation. The mitigation is the same: **scope narrowly, name what the flow must not touch, review outputs.**
:::

### Error Handling and Silent Failure

:::{figure} ../images/ch16-error-handling.png
:label: fig-ch16-error
:alt: Two flow diagrams side by side. Left: Flow with no error handling — errors cause silent failure, nobody notified. Right: Flow with proper error handling — try-catch pattern, notifications on failure, logging for audit.
:width: 80%
:align: center

Flows without error handling fail silently. Flows with error handling fail visibly — which is the only kind of failure you can fix.
:::

The most dangerous failure is not a flow that crashes spectacularly. It is a flow that **stopped working and nobody noticed**.

A connector authorization expires. A file path changes. A column header is renamed. The flow encounters an error, logs it to a run history nobody checks, and moves on — or stops entirely. The Monday report does not arrive. Nobody realizes until Wednesday, when someone asks where it went.

**The governance requirement:**
- Every flow sends a failure notification to a monitored channel or inbox
- Flows with scheduled triggers include a "heartbeat" — a success notification that confirms the run completed
- Run history is reviewed at least weekly for flows processing client or financial data
- Error rates above threshold trigger an automatic pause for human review

### Approval Steps as Designed Control Points

Approval actions in Power Automate pause the flow and route a decision to a human. The flow waits until approved, rejected, or timed out.

This is not friction. It is **designed human judgment** embedded at the moments that require it.

**GES examples where approval steps belong:**
- Before sending any communication to an exhibitor or organizer
- Before posting variances or reconciliation figures to a client-visible channel
- Before releasing information that involves competitive or embargo-sensitive content
- Before any action that modifies a rate, a deadline, or a contractual term

The discipline: **decide at design time where humans must re-enter the loop.** Do not leave it to chance.

### Environments and Connections

Power Automate flows run in **environments** — organizational containers that determine what data the flow can access and what connections are available.

Connections are the credentials that link Power Automate to external services. They include OAuth tokens, service accounts, and API keys. Connections are **per-user** by default — which means the flow uses the connection owner's identity and permissions.

**The governance implications:**
- Flows accessing sensitive systems should use service accounts with scoped permissions, not personal accounts
- Connections should be reviewed quarterly to ensure they still belong to active employees
- Premium connectors (which require additional licensing) should be governed centrally to manage costs

### The Cross-Client Contamination Risk in Automation

Chapter 12 established the principle: GES serves direct competitors at the same show. A permission gap that exposes one client's material to another is a business-critical failure.

Automation raises the stakes. A flow that runs nightly, processing data from every show site its owner can access, can systematically traverse content it should not touch — and produce outputs that blend client data in ways no human ever would.

**The mitigation:**
- Flows are scoped to specific sites, libraries, or data sources — never "all sites the owner can access"
- Constraints are explicit in the flow design: "Only process files in Show 5108 library"
- Outputs are reviewed before distribution, especially on cross-show or cross-account flows
- Flows that touch multiple client workspaces require explicit approval from legal or compliance

::::{admonition} 🧭 T.R.U.E. Check — Responsibility
:class: note

**Be responsible for our actions and deliver on our commitments.**

A flow runs under your name. Its outputs carry your implicit endorsement. If a reconciliation report goes to an organizer from a flow you built, that report is yours — whether you assembled it at your desk or it ran at 6 a.m. while you were asleep.

The discipline that makes automation safe is non-negotiable: **you review every artifact before anyone else does.** If you do not have time to review it, you do not have time to schedule it.
::::

---

## 9. Honest Limitations — What Automation Cannot Do

Power Automate is powerful. It is not omnipotent. Understanding its limits prevents the expensive discovery of those limits in production.

### Desktop RPA Is Brittle

Desktop flows automate by interacting with user interfaces — clicking buttons, typing in fields, navigating menus. When the UI changes, the flow breaks.

A software update that moves a button, renames a menu item, or changes a screen layout can turn a working desktop flow into a series of failed clicks. The flow does not adapt. It follows the recording.

**The implication:** Desktop flows require maintenance. Every update to the underlying application is a potential breaking change. Budget for ongoing adjustments, and do not assume a desktop flow will run unchanged for years.

### Premium Connectors Cost Money

Power Automate offers hundreds of connectors. Some are included with Microsoft 365. Others require the **Power Automate Premium** license (approximately $15/user/month) or specific add-ons.

Connectors to Salesforce, ServiceNow, SAP, SQL Server databases, and many third-party services fall in the premium category. Unattended RPA — desktop flows that run without a logged-in user — requires approximately $150/bot/month.

**The implication:** Before designing a flow that relies on premium connectors, confirm the licensing is in place. A brilliant flow that requires a connector nobody has licensed is a blueprint, not a solution.

### Not Everything Should Be Automated

Some processes are too variable. Some decisions require too much judgment. Some situations demand a human presence.

- **Exception-heavy processes** where the "edge case" is actually most cases
- **High-stakes communications** where tone and relationship matter more than speed
- **Situations requiring emotional intelligence** — an exhibitor who is frustrated, an organizer who is concerned, a crew member who needs support
- **Novel situations** where the process does not exist yet

Automation amplifies consistency. It does not replace judgment. If a process requires significant human judgment at every step, automating the steps between those judgments may add complexity without adding value.

### The Maintenance Burden Is Real and Underestimated

Flows are not fire-and-forget. They require:
- **Monitoring** — checking run history, reviewing error rates, confirming outputs
- **Updates** — adjusting when source systems change, when requirements evolve, when edge cases emerge
- **Ownership transfer** — ensuring continuity when the original builder moves on
- **Retirement** — decommissioning flows that are no longer needed

A portfolio of fifty flows without a maintenance discipline is not automation infrastructure. It is technical debt that compounds monthly.

::::{admonition} 🧭 T.R.U.E. Check — Understanding
:class: note

**People come first. Be understanding and compassionate.**

Automation can process an exhibitor's order in seconds. It cannot understand why they submitted it late. It cannot hear the stress in their voice when they call asking if it is too late. It cannot exercise the judgment to make an exception for a client relationship that matters.

When the right answer requires understanding a person, not processing a form, the right tool is a human.
::::

---

## 10. Build Your First Flow — A Walkthrough

This section is designed for someone who has never built a Power Automate flow. If you are experienced with the platform, skip to the Try This section.

### The Scenario

You want a flow that notifies the show team whenever a new file is added to the show's "Critical Updates" folder — a simple event-driven notification.

### Step by Step

**Step 1 — Access Power Automate**

Navigate to [make.powerautomate.com](https://make.powerautomate.com) and sign in with your Microsoft 365 account.

**Step 2 — Create a New Flow**

Click **Create** in the left navigation, then select **Automated cloud flow**. This type fires on an event rather than a schedule.

**Step 3 — Name and Choose Trigger**

Name your flow: "Critical Updates Notification — Show 5108"

Search for the trigger: "When a file is created (properties only)" from the SharePoint connector.

**Step 4 — Configure the Trigger**

- **Site Address:** Select the SharePoint site for Show 5108
- **Library Name:** Select or enter "Critical Updates"

The flow will now fire every time a new file appears in that folder.

**Step 5 — Add the Notification Action**

Click **+ New step**. Search for "Post message in a chat or channel" from the Microsoft Teams connector.

Configure:
- **Post as:** Flow bot
- **Post in:** Channel
- **Team:** Select the Show 5108 team
- **Channel:** Select the appropriate channel (e.g., "General" or "Critical Alerts")
- **Message:** Compose using dynamic content:

```
🚨 New Critical Update Posted

File: [File name with extension]
Added: [Created]
Link: [Link to item]
```

Use the dynamic content picker to insert the actual file properties.

**Step 6 — Save and Test**

Click **Save**. Then click **Test** in the upper right. Choose "Manually" and trigger the test.

Upload a test file to the Critical Updates folder. Within seconds, you should see the notification appear in the Teams channel.

**Step 7 — Review Run History**

Return to the flow and click the flow name to see run history. Each run shows status (succeeded, failed), duration, and details. This is where you will monitor for errors.

### What You Built

A complete event-driven automation: file appears → notification posts. No human had to notice the file, open Teams, compose a message, and post it. The flow handles the mechanical part; the team handles the response.

---

## 11. The Compounding Math

:::{figure} ../images/ch16-automation-roi-compounding.png
:label: fig-ch16-roi
:alt: Line graph showing cumulative time savings from automation over one year. X-axis shows months 1-12. Y-axis shows hours saved. Multiple lines represent different flow frequencies (daily, weekly, per-show). The compounding effect is visible as lines curve upward. A callout shows: 20 minutes saved per run × 4,000 runs per year = 1,333 hours.
:width: 80%
:align: center

Automation ROI compounds with repetition. A 20-minute task automated across 4,000 annual shows recovers over 1,300 hours — the equivalent of more than half a full-time position.
:::

At GES, the math is not subtle.

- **4,000+ live experiences per year**
- **150,000+ exhibitors**
- **24 global production and warehouse facilities**
- **75+ countries**

A flow that saves 20 minutes and runs once per show: 1,333 hours annually.

A flow that saves 5 minutes and runs for every exhibitor order: tens of thousands of hours annually.

A flow that saves 2 minutes and runs daily at every facility: 17,520 minutes — 292 hours — annually.

The question is not whether automation is worth the investment. The question is which automations deliver the most value, and that answer is usually: **the ones that fire most frequently on the most repetitive, least judgment-requiring tasks.**

---

## 12. Try This: Your First Automated Notification

::::{admonition} 🧪 Try This: Build a File-Arrival Notification
:class: tip

**Time required:** 20 minutes

**Goal:** Build a flow that notifies you when a file arrives in a SharePoint folder you monitor.

**Steps:**

1. Navigate to [make.powerautomate.com](https://make.powerautomate.com)
2. Create an **Automated cloud flow**
3. Name it: "My Folder Monitor"
4. Trigger: "When a file is created (properties only)" — SharePoint
5. Configure with a folder you have access to
6. Add action: "Send me an email notification" (or Teams notification if you prefer)
7. Compose the notification with the file name and link
8. Save, test by uploading a file, confirm the notification arrives

**Then answer:**

1. How long did it take from file upload to notification arrival?
2. What happens if the flow encounters an error? (Check your flow's settings for failure notifications)
3. What would you add to make this production-ready for a show team?
::::

---

## 13. Productive Struggle Problem

You are the GES operations director for a major venue. Three recurring problems consume your team's time:

1. **Exhibitor service questions** arrive by email at a rate of 40-60 per day during the pre-show period. They currently sit in a shared inbox until someone triages them — often several hours later. Questions about deadlines and freight targets need faster response.

2. **Site survey reports** are submitted by show managers after venue walks, but they end up scattered across OneDrive folders instead of in the Venue Knowledge Library where other teams can find them.

3. **Labor forecast variance reviews** should happen daily during move-in, but nobody has time to pull the numbers, compare them to forecast, and flag issues until the show is over — by which point the information is historical rather than actionable.

**Your challenge:**

For each of the three problems:
- Decide whether to use Copilot Chat, Cowork, or Power Automate — and justify your choice using the decision framework
- If Power Automate: specify the trigger type, the key actions, and where human approval should re-enter the loop
- Identify one governance control that must be in place before deploying each flow
- Estimate the time saved per instance and the annual compounding effect

For at least one of the three, sketch the Cowork assignment you would use to prototype before building the flow. Include the five-part structure: Outcome, Inputs, Definition of done, Constraints, Approval scope.

There is no single right answer. The quality of your reasoning — especially your justification for what you chose *not* to automate — matters more than the flow designs themselves.

---

## Glossary

```{glossary}
Power Automate
  Microsoft's automation platform within the Power Platform family. Enables cloud flows (API-based automation), desktop flows (RPA), and combinations of both.

Cloud Flow
  An automation that runs in Microsoft's cloud, connecting systems through API-based connectors. Triggers include scheduled, event-driven, instant (manual), and approval-based.

Desktop Flow
  An automation that runs on a Windows machine, interacting with applications through recorded UI actions (clicks, keystrokes, screen navigation). The RPA component of Power Automate.

RPA (Robotic Process Automation)
  Technology that automates tasks by mimicking human interactions with software interfaces. Used when systems lack modern APIs.

Trigger
  The event that starts a flow. Types include scheduled (time-based), event-driven (something happens), instant (user-initiated), and approval-based.

Connector
  A pre-built integration between Power Automate and another service (SharePoint, Outlook, Teams, Salesforce, SAP, etc.). Standard connectors are included with Microsoft 365; premium connectors require additional licensing.

AI Builder
  Microsoft's embedded AI capability for Power Platform. Provides document processing, text classification, object detection, and prediction within Power Automate flows.

Approval Action
  A Power Automate action that pauses the flow, routes a decision to one or more approvers, and branches based on the response. Embeds human judgment at designed control points.

Flow Owner
  The user whose identity and permissions a flow uses when executing. Flow ownership determines what data the flow can access and what actions it can perform.

Orphaned Flow
  A flow whose owner has left the organization or changed roles without transferring ownership. Orphaned flows continue running without oversight until they fail or are discovered.

Premium License
  The Power Automate Premium license (approximately $15/user/month) required for premium connectors, attended desktop flows, and process mining. Unattended RPA requires approximately $150/bot/month.

Environment
  An organizational container in Power Platform that determines what data flows can access and what connections are available. Environments provide isolation between development, test, and production.

Connection
  The credential (OAuth token, service account, API key) that links Power Automate to an external service. Connections are typically per-user and inherit the user's permissions.

Cowork-to-Flow Progression
  The recommended practice of prototyping with Copilot Cowork before building a Power Automate flow. Delegation teaches the process; automation codifies what was learned.

Silent Failure
  A flow failure that produces no notification and goes unnoticed until someone asks where the expected output went. Prevented through error handling and failure notifications.

Drayage
  The movement of exhibitor freight from the dock or advance warehouse to the booth space, and back at move-out. A core material handling service automated through reconciliation and variance flows.

Freight Target
  An agreed target for exhibitor freight — weight, arrival window, or cost. Variance against freight targets is a key metric tracked through automated monitoring flows.
```

---

## Discussion

Power Automate completes the arc from asking to delegating to automating. The capability is real: work that used to require human initiation now runs on triggers, processing data, generating outputs, and notifying teams without anyone clicking "start."

But capability is not strategy. The question facing GES is not "can we automate this?" The question is "should we, and under what governance?"

Consider your own role. Where does repetition live in your work? What tasks fire the same way, with the same inputs, producing the same outputs, show after show? And critically: which of those are genuinely mechanical, and which only look mechanical until an edge case arrives?

::::{admonition} 📝 Discussion Guidelines
:class: note

Post your reflection in the course discussion forum before the next session. Your response should:

- Identify one process in your role that is a strong automation candidate, and one that should remain human-driven — justify both choices
- Address the governance question: what would have to be true about a flow's design and oversight before you would trust it to run without you reviewing every output?
- Describe the progression you would use to move from Cowork prototype to Power Automate production for your automation candidate
- Respond to at least **two peers** with substantive engagement — challenge their automation/human-driven distinction, suggest governance controls they missed, or push back on a flow design
- Reference at least one credible source — Microsoft Power Automate documentation, GES operational guidance, or automation governance research

Minimum 300 words for your main post.
::::

---

## Leader's Takeaway

Power Automate is where the capability gains from Copilot and Cowork become permanent operational infrastructure. The progression is complete: from AI that answers questions, to AI that executes assignments, to automation that runs without human initiation.

For GES leaders deploying this:

**1. Govern before you scale.** The first flow is an experiment. The fiftieth is a portfolio. Before you reach that scale, establish ownership standards, orphan flow processes, error handling requirements, and approval checkpoint rules. Automation without governance is risk multiplication.

**2. Prototype with Cowork, then automate.** The Cowork-to-flow progression prevents the most common failure: automating a process you do not understand. Require that any flow processing client data or producing client-facing outputs was first delegated manually at least twice.

**3. Budget for maintenance.** Flows are not fire-and-forget. Connectors expire. Source systems change. Edge cases emerge. Build maintenance into the operational model from day one, or watch your automation portfolio degrade into a collection of broken flows nobody owns.

**4. Measure the compounding, and prioritize accordingly.** A 20-minute task automated across 4,000 shows is 1,333 hours. That is the math that justifies investment. Prioritize flows by frequency × time saved, not by complexity or novelty.

**5. Never automate what requires judgment.** Automation amplifies consistency. It does not replace wisdom. The exhibitor who needs an exception, the organizer who needs reassurance, the crew member who needs support — those moments require humans, and protecting space for them is part of the automation strategy.

GES runs 4,000+ live experiences a year with ~2,600 people across 75+ countries. The repetition in that scale is exactly what automation was built for. The discipline in deploying it — prototype, govern, maintain, review — is what makes the difference between automation as operational advantage and automation as expensive, machine-speed error production.

---

## Closing: The Arc Complete

This book has traveled a path.

It began with a question: *what does it mean to work with AI?* The early chapters taught the fundamentals — prompting, context, the permission model, the boundaries of what Copilot knows and does not know. You learned to ask well.

The middle chapters went deeper into the applications: Word, Excel, PowerPoint, Outlook, Teams, SharePoint. You learned where Copilot fits into the work you already do, and where it does not. You developed the verification discipline that turns AI outputs into trustworthy artifacts.

Chapter 14 introduced a shift. Copilot Cowork was not about asking better questions. It was about delegating real work — multi-step, multi-app, finished artifacts returned while you focused on what only you could do. The skill changed from prompting to briefing, from consuming outputs to managing a capable collaborator.

This chapter completes the arc. Power Automate is where delegation becomes permanent. The work that used to require you to initiate it now runs when the trigger fires — forever, without you, until you decide otherwise.

**The three gears are not a ladder to climb. They are tools to choose.**

Some work will always be conversation — one question, one answer, right now. Copilot Chat is not obsolete because Cowork exists. Some work will always be delegation — a project, a deliverable, run once or on request. Cowork is not obsolete because Power Automate exists. And some work should become automation — the same mechanical task, fired by the same trigger, producing the same output, thousands of times a year.

The professional skill is knowing which gear fits which work.

::::{admonition} 🧭 T.R.U.E. Check — Excellence
:class: note

**Provide excellent service and execution.**

Excellence in 1939, when GES was a small sign and exhibit company in Kansas City, meant a craftsman standing over their work until it was right. Excellence in 2026, with 4,000+ live experiences across 75+ countries, means something more: it means **systems that deliver excellence at scale**, reliably, repeatedly, without depending on one person being awake at 6 a.m. to run a report.

Automation is not a replacement for the craftsman's care. It is how that care scales to serve 150,000+ exhibitors across shows the craftsman will never see.
::::

**What this means for a GES professional's career:**

The skills that mattered before this book still matter. Operational judgment. Client relationships. The ability to walk a floor and see what is wrong before it becomes a crisis. The institutional knowledge that says *"last time we did this at that venue, here is what went wrong."*

What changes is the leverage available to apply those skills.

A show manager who knows exactly which variance signals a real problem no longer has to pull the data to find it. The flow delivers the flagged lines; the manager applies the judgment. An account director who understands a client's priorities no longer has to assemble the QBR package to communicate them. Cowork produces the deck; the director shapes the conversation.

The mechanical work — the assembly, the formatting, the routine processing that ate hours every week — recedes. What remains is the work that is genuinely yours: the judgment, the relationships, the decisions that shape outcomes.

That is not a threat to professional value. It is an amplification of it.

The question facing every GES professional reading this book is not *"will AI take my job?"* The question is *"how will I use these tools to do work that would have been impossible before?"*

The cross-show cost analysis that nobody had time for. The exhibitor question that got answered in minutes instead of hours. The reconciliation that was done before you landed. The pattern across six years of shows at one venue that revealed why costs kept drifting — a pattern nobody could see because nobody had time to assemble the data.

**That is the work that opens up.** The mechanical work contracts; the meaningful work expands.

GES became independent on December 31, 2024, for the first time in 55 years. The company is setting its own course, making its own technology decisions, defining its own standards. onPeak shipped an AI Smart Suite. Visit by GES ships intelligent hardware. The organization has proven it can build AI into products.

This book has been about building AI into operations — into the daily work of delivering 4,000+ live experiences with ~2,600 people who are more often on show floors than at desks.

The capability is real. The governance is defined. The path from asking to delegating to automating is mapped.

What happens next is up to you.
