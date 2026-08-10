---
title: "Chapter 16: Microsoft Power Automate — From Assistance to Automation"
subtitle: "The Third Gear: Work That Happens Without You"
short_title: "Power Automate"
description: "The capstone chapter. Copilot answers questions. Cowork completes projects. Power Automate runs processes forever — without a human in the loop — every time a trigger fires. This chapter teaches the progression from asking to delegating to automating, the critical difference between cloud flows and desktop RPA, AI Builder for document extraction, governance risks unique to automation, and ten fully worked GES scenarios from exhibitor order intake to post-show reconciliation to cross-show drayage variance reporting."
label: ch-16-power-automate
tags: [Power Automate, automation, RPA, desktop flows, cloud flows, AI Builder, triggers, Copilot, Cowork, GES, governance, exhibitor services, drayage, material handling, post-show reconciliation, T.R.U.E., flow ownership]
---

```{admonition} Download this Chapter as PDF
:class: tip

[Download PDF](https://github.com/liquid-books/ges-learns-ai/raw/main/pdfs/ch16-power-automate.pdf)
```

# Chapter 16: Microsoft Power Automate — From Assistance to Automation

:::{figure} ../images/ch16-power-automate-infographic.png
:label: fig-ch16-infographic
:alt: Illustrated explainer infographic showing the progression from Copilot (conversational, one answer) to Cowork (delegated multi-step project) to Power Automate (permanent automation, trigger fires forever). Three interconnected gears in blue and orange, with GES exhibition industry scenarios illustrated beneath each gear.
:width: 80%
:align: center

The three gears of Microsoft 365 AI: ask, delegate, automate. Each one changes how you work — and the last one changes whether you need to be there at all.
:::

> *"The first rule of any technology used in a business is that automation applied to an efficient operation will magnify the efficiency. The second is that automation applied to an inefficient operation will magnify the inefficiency."*
> — Bill Gates

There is a moment, usually around the third or fourth time you delegate the same task to Cowork, when a different question surfaces. Not *can I delegate this?* — you have already answered that. The new question is: *why am I delegating this at all?*

It is 6:45 a.m. on the Monday after a show closes. A GES logistics analyst opens Copilot and types the same prompt they have typed for twelve weeks running: run the freight target variance report for the shows that closed this week, compare to the same shows last year, flag any venue with a consistent overage pattern. The analyst waits, reviews the output, approves the Teams post to the logistics channel.

That analyst just spent fifteen minutes on work that is identical every week. Not *similar* — identical. Same prompt. Same libraries. Same output location. Same approval scope.

Here is the question this chapter answers: *why is a human involved at all?*

---

## 1. The Three Gears — Ask, Delegate, Automate

Every chapter before this one taught you to work with AI. Chapter 14 taught you to delegate to it. This chapter teaches you to **remove yourself entirely**.

:::{figure} ../images/ch16-three-gears.png
:label: fig-ch16-three-gears
:alt: Three interconnected gears diagram showing Copilot Chat (Ask — human in the loop every turn), Copilot Cowork (Delegate — human approves at checkpoints), and Power Automate (Automate — trigger fires, work happens, no human required until review). Visual progression from left to right showing decreasing human involvement.
:width: 80%
:align: center

The three gears of Microsoft 365 AI work. As you move from left to right, human involvement decreases — and so does the tolerance for an unverified process.
:::

**Copilot Chat** is a conversation. You ask, Copilot answers, you evaluate, you refine. You are the loop. Every step passes through you. This is the right model for drafting, ideation, and one-off questions where you want to see the answer before deciding what to do with it.

**Copilot Cowork** is delegation. You describe an outcome, Cowork plans and executes the steps, and you review and approve at checkpoints. You are no longer the loop — you are the manager. The work keeps running while your laptop is off. This is the right model for multi-step, multi-file projects you need done rather than watched.

**Power Automate** is automation. You build a flow once. A trigger fires — an email arrives, a file posts, a scheduled time passes — and work happens. No prompt. No approval request. No human at all, unless you designed a checkpoint into the flow. This is the right model for the work that is *exactly the same every time*.

The decision rule is simple enough to memorize: **how much human judgment is required at execution time?**

- A lot → Chat
- Some, at checkpoints → Cowork
- None → Power Automate

:::{important}
**The insight that makes this chapter land**

Cowork is how you discover what is worth automating.

Delegate a task three or four times. Watch how it behaves. See where it succeeds reliably and where it needs correction. Notice the constraints you add because last week's run surfaced an edge case you had not thought of.

That iterated Cowork prompt — tight, tested, edge-case-aware — is your automation prototype. Power Automate is how you promote it to production so it never needs a human again.

Skip the prototype phase and you automate an unverified process. Do that and you learn the hardest lesson in this chapter the hard way.
:::

---

## 2. Why Power Automate Exists at GES

GES runs **4,000+ live experiences a year**, serves **150,000+ exhibitors**, operates across **75+ countries**, and manages **24 global warehouse and production facilities**. The sheer volume of repetitive work is staggering.

Consider just one task: the freight target variance report after a show closes. It takes the logistics analyst twenty minutes to run. It runs once per show. At 4,000 shows a year, that is **1,333 hours** of human time — the equivalent of two-thirds of a full-time employee — on a task that is *identical every time*.

Now multiply that across every repeatable process in show operations, exhibitor services, creative, onPeak, and Visit by GES. The math is not subtle.

Power Automate exists because some work does not need a human present. Not because the human adds no value — they designed the process, they verified it, they built the constraints that make it safe. But once that design work is done, the execution work is pure overhead.

**Automation is how you convert repetitive execution into design work.** Instead of running the freight variance report 4,000 times, you build it once, verify it carefully, set the trigger, and let it run forever. Your time goes to the exceptions it flags, not the routine it handles.

---

## 3. Cloud Flows vs. Desktop Flows — and Why RPA Exists

Power Automate offers two fundamentally different types of automation. Understanding the difference is not optional; it determines which tool you reach for and what risks you accept.

:::{figure} ../images/ch16-cloud-vs-desktop-flows.png
:label: fig-ch16-cloud-vs-desktop
:alt: Side-by-side comparison of cloud flows (left) and desktop flows (right). Cloud flows show API connections between cloud services — Outlook, SharePoint, Teams, Dataverse — running on Microsoft servers. Desktop flows show UI automation on a local Windows machine — clicking buttons, typing into fields, reading screens — running on the user's device or a hosted machine.
:width: 80%
:align: center

Cloud flows talk to APIs. Desktop flows talk to screens. The difference determines reliability, maintenance burden, and when each is the right choice.
:::

### Cloud flows

Cloud flows run on Microsoft's servers. They connect applications through **connectors** — standardized API integrations. When a file lands in a SharePoint library, a cloud flow can read it, extract values, send an email, update a row in Excel, post to Teams, and file the result — all through documented, versioned APIs.

**Microsoft offers over 1,000 connectors.** The Microsoft 365 suite is fully covered: Outlook, SharePoint, Teams, OneDrive, Planner, Forms, Excel. So are major external services: Salesforce, ServiceNow, SAP, DocuSign, and hundreds more.

Cloud flows are **stable** because APIs are versioned and documented. When SharePoint changes its interface, the API remains backward-compatible, and your flow keeps working. Cloud flows are **scalable** because they run in Microsoft's cloud — you do not need a machine running somewhere for the flow to execute.

### Desktop flows (RPA)

Desktop flows run on a Windows machine. They automate applications by **clicking buttons, typing into fields, reading text from screens** — the same actions a human would take. This is Robotic Process Automation (RPA), and Power Automate Desktop is Microsoft's RPA tool.

**Why does RPA exist?** Because not everything has an API.

GES, like most companies with decades of operational history, uses applications that were built before APIs became standard. A freight management system from 2008. A labor reporting tool from a union jurisdiction. A venue's proprietary ordering portal that exists only as a web form. A customs and carnet system that only accepts Excel files in a very specific format uploaded through a browser.

None of these have connectors. None of them expose APIs. The only way to automate them is to simulate what a human does: open the application, navigate to the right screen, paste data, click submit.

That works. It is also **fragile**.

:::{warning}
**RPA is brittle — design for it**

Desktop flows break when the user interface changes. A button moves. A field is renamed. A dialog box appears that was not there before. The flow keeps clicking where the button *used to be*, and either fails or does something unintended.

RPA is maintenance-intensive. Every application update is a potential flow-breaking event. Every vendor UI refresh is a debugging session.

Use cloud flows whenever a connector exists. Use desktop flows only when there is no other path — and budget for maintenance when you do.
:::

### The decision rule

**If every application in your workflow has a connector, use a cloud flow.** It will be more reliable, easier to maintain, and cheaper to run.

**If any application requires UI interaction — clicking, typing, reading from screens — you need a desktop flow.** Understand that you are accepting a maintenance burden for the capability.

For many GES workflows, the answer is both: a cloud flow that triggers on a SharePoint event, calls a desktop flow to interact with a legacy system, and returns to cloud actions for the downstream steps. Hybrid patterns are normal, and they concentrate the fragility in the desktop portion where it can be monitored and maintained.

---

## 4. Triggers — What Starts the Work

Every flow has a trigger. The trigger is what makes automation *automated* — work that starts itself rather than waiting for a human to initiate it.

:::{figure} ../images/ch16-trigger-types.png
:label: fig-ch16-trigger-types
:alt: Four-panel diagram showing the four trigger types in Power Automate. Panel 1: Scheduled (clock icon) — runs at a set time or interval. Panel 2: Event-driven (lightning bolt) — runs when something happens in a connected system. Panel 3: Manual (hand icon) — runs when a user clicks a button. Panel 4: Approval-based (checkmark icon) — runs when an approval is granted or denied. Each panel includes a GES example.
:width: 80%
:align: center

The four trigger types determine *when* your flow runs. The trigger you choose defines what automation means for that workflow.
:::

### Scheduled triggers

The flow runs at a set time or on a recurring schedule. Every Monday at 6 a.m. Every day at midnight. The first business day of each month.

**GES examples:** The weekly freight target variance report. The monthly cross-show drayage analysis. The daily exhibitor order summary during move-in week.

### Event-driven triggers

The flow runs when something happens in a connected system. A file is created in a SharePoint library. An email arrives in a shared mailbox. A row is added to an Excel table. A form is submitted.

**GES examples:** When the final labor file posts to a show's SharePoint library, run the post-show reconciliation. When an email arrives from a venue's exhibitor services desk, extract the request and route it to the show team. When an exhibitor order form is uploaded, extract the data and populate the order system.

### Manual triggers

The flow runs when a user clicks a button — in Power Automate, in Teams, or embedded in a SharePoint page. It is not truly "automated" in the fire-and-forget sense; it is a standardized, repeatable action that a human initiates on demand.

**GES examples:** A button in Teams that runs the hotel block pickup analysis for the show the user selects. A button that generates the organizer QBR deck from the account's current data.

### Approval-based triggers

A special case of event-driven: the flow runs (or branches) based on the outcome of an approval. This is how you build human checkpoints into otherwise automated processes.

**GES examples:** When an exhibitor requests a rate exception, the flow routes the request to the account director. If approved, the flow updates the order system and sends confirmation. If rejected, it sends a different response. The human judgment is the trigger; the downstream work is automated.

---

## 5. Copilot Inside Power Automate — Describing Flows in Plain English

Microsoft has embedded Copilot directly into the Power Automate designer. You can describe what you want in natural language, and Copilot will generate the flow structure for you.

:::{figure} ../images/ch16-copilot-builds-flow.png
:label: fig-ch16-copilot-builds-flow
:alt: Screenshot-style diagram showing the Power Automate designer with a Copilot chat panel. The user has typed "When a new file is added to the Exhibitor Orders folder in SharePoint, extract the company name and order total, and email me a summary." Copilot has generated a three-step flow: SharePoint trigger, Parse JSON action, Send Email action.
:width: 80%
:align: center

Copilot in Power Automate lets you describe what you want in plain English. It generates the flow structure — you review, refine, and deploy.
:::

**What Copilot can do in Power Automate:**

- Generate a complete flow from a natural-language description
- Suggest actions based on what you are trying to accomplish
- Explain what an existing flow does
- Help troubleshoot errors
- Generate expressions and formulas for conditions and data transformation

**What Copilot cannot do:**

- Verify that the flow does what your business actually needs
- Know which SharePoint library is the right one for this show
- Understand that the "Company Name" field in your order form is called "Exhibitor" in your downstream system
- Test the flow against edge cases you have not mentioned
- Accept responsibility for a flow that runs incorrectly

The pattern should be familiar by now: **Copilot accelerates construction. Verification is yours.**

A flow built in five minutes with Copilot's help still needs the same testing and validation as a flow built in two hours by hand. In fact, it needs *more* careful review — because speed of construction creates the temptation to skip the review, and an untested flow running on a schedule is exactly how GES ends up sending the wrong freight target to 800 exhibitors.

---

## 6. AI Builder — Teaching Automation to Read Documents

AI Builder is Microsoft's low-code AI capability integrated into the Power Platform. For GES, its most relevant feature is **document processing** — the ability to extract structured data from unstructured documents like PDFs, scanned forms, and images.

:::{figure} ../images/ch16-ai-builder-extraction.png
:label: fig-ch16-ai-builder-extraction
:alt: Diagram showing AI Builder document processing. An exhibitor order form (PDF) enters on the left. AI Builder extracts fields: Company Name, Booth Number, Order Items, Total Amount. The extracted data flows into Power Automate, which routes it to the order system and sends a confirmation email.
:width: 80%
:align: center

AI Builder turns unstructured documents into structured data. For GES, this means exhibitor order forms, freight paperwork, and invoices can flow directly into automated workflows without manual data entry.
:::

### Pre-built models

AI Builder includes pre-built models for common document types:

- **Invoice processing** — extracts vendor, amounts, line items, dates
- **Receipt processing** — extracts merchant, total, date, payment method
- **Identity document processing** — extracts name, date of birth, document number
- **Business card processing** — extracts name, company, contact information

### Custom models

For documents specific to your business — like GES exhibitor order forms — you can train a **custom document processing model**. You upload sample documents, tag the fields you want to extract, and AI Builder learns to recognize and extract those fields from new documents.

**GES applications:**

- **Exhibitor order forms:** Extract company name, booth number, services ordered, quantities, and totals — then route to the order system automatically
- **Freight manifests:** Extract weight, dimensions, carrier, and arrival window — then compare against freight targets
- **Venue rule documents:** Extract key constraints and deadlines — then populate the show operations manual
- **Material handling invoices:** Extract line items — then match against expected charges for reconciliation

### The trade-off

Custom models require training data — typically 5-15 sample documents per document type, with fields manually tagged. The model improves as it processes more documents. But the initial investment is real, and the model needs retraining when document formats change.

For documents that arrive in high volume and consistent format — exhibitor order forms, freight paperwork — the investment pays off quickly. For one-off or highly variable documents, manual processing may still be the better path.

---

## 7. The Handoff Pattern — Cowork to Power Automate

Here is the workflow that makes automation safe:

:::{figure} ../images/ch16-cowork-to-flow-progression.png
:label: fig-ch16-cowork-to-flow-progression
:alt: Three-stage progression diagram. Stage 1 (Prototype): Cowork prompt run manually 3-4 times, edge cases discovered, constraints refined. Stage 2 (Validation): Final Cowork prompt tested against known good outputs, verified by a second person. Stage 3 (Production): Cowork prompt converted to Power Automate flow, trigger set, monitoring configured.
:width: 80%
:align: center

The prototype-to-production pathway. Cowork is your testbed; Power Automate is your deployment platform. Skip the prototype phase at your peril.
:::

**Stage 1 — Prototype with Cowork**

Run the task as a Cowork prompt three or four times. Each time, note:

- Where did it work exactly as expected?
- Where did it need correction mid-task?
- What edge case surfaced that you had not anticipated?
- What constraint did you add after the second run that you should have included from the start?

After several runs, your Cowork prompt is tight, tested, and edge-case-aware. It has constraints that emerged from real execution, not assumptions.

**Stage 2 — Validate against known outputs**

Before you automate anything, run the Cowork version against a show whose correct output you already know. Does it reproduce what a human produced? If yes, the logic is verified. If no, you have found a bug before it ran 4,000 times.

Have a second person review the prompt, the logic, and the test results. The person who built it is the worst reviewer — they know what it *should* do and miss what it *actually* does.

**Stage 3 — Convert to Power Automate**

Take the tested Cowork prompt and implement it as a flow:

- Define the trigger (scheduled, event-driven, manual)
- Build the action sequence that mirrors what Cowork did
- Add error handling for cases that could not occur in Cowork but can occur in automation (files not found, permissions denied, timeouts)
- Set up monitoring and alerting so you know when the flow fails

The flow is now in production. It runs without you. It also fails without you — which is why error handling and monitoring are not optional.

::::{admonition} 🧭 T.R.U.E. Check — Trust
:class: note

**Trust each other to always be honest and do what's right.**

A Cowork prompt you ran four times is a prototype. A Power Automate flow running on a schedule is a commitment. When your name is on a flow, you are promising every colleague who depends on its output that you did the verification work.

Trust is built by verification, not by confidence in the tool.
::::

---

## 8. Ten GES Automation Scenarios

This is the practical heart of the chapter. Each scenario names the trigger, the flow logic, the output, and the governance considerations.

:::{figure} ../images/ch16-ges-automation-map.png
:label: fig-ch16-ges-automation-map
:alt: Visual map showing ten GES automation scenarios arranged by function: Exhibitor Services (order intake, service kit questions), Logistics (freight variance, drayage report), Show Operations (post-show reconciliation, daily log distribution, site survey filing, safety escalation), Housing (hotel block monitoring), and Governance (access review). Each scenario shows the trigger type and key output.
:width: 80%
:align: center

Ten automation scenarios across GES functions. Each one saves hours of repetitive work — and each one carries governance responsibilities.
:::

### Scenario 1: Exhibitor Order Form Intake

**Trigger:** When a file is created in the Exhibitor Orders folder for a show  
**Flow logic:**
1. AI Builder extracts company name, booth number, services ordered, quantities, totals
2. Validate extracted data against the exhibitor master list (company exists, booth assignment matches)
3. If valid: create order record, send confirmation email to exhibitor
4. If invalid: flag for manual review, send notification to exhibitor services lead

**Output:** Order record in the system, confirmation sent, exceptions flagged  
**Governance note:** The AI Builder model needs retraining when the order form format changes between seasons. Build a version check into the flow.

### Scenario 2: Post-Show Reconciliation Trigger

**Trigger:** When the final labor file is created in the show's Post-Show folder  
**Flow logic:**
1. Pull labor actuals from the new file
2. Pull freight manifest, exhibitor orders, and pre-show estimate from the show library
3. Run the reconciliation calculation (labor variance, material handling variance, service revenue variance)
4. Generate the Excel workbook and Word summary
5. Save to the Post-Show folder
6. Send notification to show manager: "Reconciliation ready for review"

**Output:** Reconciliation package, notification  
**Governance note:** This flow does *not* send the reconciliation to the organizer. That remains a human decision after review.

### Scenario 3: Freight Target Variance Alert

**Trigger:** Scheduled — daily at 6 a.m. during move-in week for each show  
**Flow logic:**
1. Pull current freight receiving data from the advance warehouse
2. Compare against freight targets by exhibitor
3. Calculate variance percentage
4. If any exhibitor is more than 15% over target: send alert to logistics lead with the list
5. If all within tolerance: log run, no notification

**Output:** Alert only when threshold exceeded  
**Governance note:** The 15% threshold is a business decision, not a technical one. Document it in the flow description and review it annually.

### Scenario 4: Site Survey Filing

**Trigger:** When a file is created in the Site Surveys folder  
**Flow logic:**
1. Read file metadata (venue name, date)
2. Check if venue exists in the Venue Knowledge Library
3. If yes: move file to the venue's folder, update the venue profile's "last surveyed" date
4. If no: create venue folder, move file, notify operations to complete the venue profile

**Output:** Survey filed correctly, venue profile updated  
**Governance note:** This flow modifies the authoritative Venue Knowledge Library. Any error compounds across every show at that venue. Test thoroughly.

### Scenario 5: Move-In Daily Log Distribution

**Trigger:** Scheduled — daily at 7 p.m. during move-in for each show  
**Flow logic:**
1. Collect entries from the show's Daily Log list in SharePoint
2. Format as a summary: issues reported, resolutions, open items carried forward
3. Post to the show's Teams channel
4. Email to the show manager and organizer contact

**Output:** Daily log summary in Teams and email  
**Governance note:** The email to the organizer is external communication. Build in a review step if the show requires organizer approval before distribution.

### Scenario 6: Organizer RFP Intake and Acknowledgement

**Trigger:** When an email arrives in the RFP shared mailbox  
**Flow logic:**
1. Parse email for show name, organizer name, key dates
2. Create a new row in the RFP tracking list
3. Create a new folder in the Proposals library with show name and year
4. Move the email attachments (typically the RFP document) to the new folder
5. Send acknowledgement email to the sender: "Thank you for your inquiry. Our team will respond within [SLA] business days."

**Output:** RFP tracked, folder created, acknowledgement sent  
**Governance note:** The acknowledgement email commits GES to an SLA. Make sure the SLA in the template is accurate and approved.

### Scenario 7: Hotel Block Pickup Monitoring

**Trigger:** Scheduled — weekly, 90 days before each show through cutoff  
**Flow logic:**
1. Pull current pickup data from onPeak reporting
2. Compare against contracted block and historical pickup curves
3. Calculate projected final pickup and attrition exposure
4. If projected pickup is below 70% of block and attrition exposure exceeds threshold: alert housing manager and account director
5. Generate weekly pickup report and save to show folder

**Output:** Weekly report, alert when at-risk  
**Governance note:** This flow reads onPeak data, which may contain attendee information subject to privacy regulations. Ensure the flow's output does not expose individual attendee data.

### Scenario 8: Safety Walk Checklist Escalation

**Trigger:** When a safety checklist is submitted via Forms with any item marked "Failed"  
**Flow logic:**
1. Extract the failed items and their locations
2. Determine severity based on item category (life safety vs. general compliance)
3. If life safety: immediate notification to show manager, safety lead, and venue contact; create urgent issue in tracking system
4. If general compliance: notification to show manager; create standard issue in tracking system
5. Log the submission with timestamp for audit trail

**Output:** Escalation notifications, issue tracking records  
**Governance note:** Safety documentation has legal implications. Retention policies apply. Ensure the flow creates an auditable record.

### Scenario 9: Access Review at Move-Out

**Trigger:** When the show status changes to "Closed" in the show tracking list  
**Flow logic:**
1. Pull the current access list for the show's SharePoint site
2. Compare against the core show team (those who should retain access post-close)
3. Generate a report of access to be removed
4. Send to IT and show manager for review
5. After approval: remove access for non-core members

**Output:** Access review report, access cleanup after approval  
**Governance note:** This directly addresses the cross-client contamination risk from Chapter 12. Access that outlives the show is how a competitor's material becomes visible. This flow is governance infrastructure.

### Scenario 10: Recurring Cross-Show Drayage Variance Report

**Trigger:** Scheduled — monthly, first business day  
**Flow logic:**
1. Pull reconciliation data for all shows closed in the prior month
2. Normalize by net square footage to enable comparison
3. Calculate cost per hundredweight, freight target compliance, advance warehouse vs. direct-to-show split
4. Group by venue to identify systematic patterns vs. isolated outliers
5. Generate workbook with tabs per venue plus consolidated view
6. Post summary to Logistics Analytics channel in Teams

**Output:** Monthly variance analysis, Teams post  
**Governance note:** This is the analysis from Chapter 13, automated. Ensure the rate reference data is current — the same Rate Sheet Rule applies to automated flows as to manual analysis.

---

## 9. Governance — The Automation Multiplier

:::{figure} ../images/ch16-approval-checkpoint.png
:label: fig-ch16-approval-checkpoint
:alt: Flow diagram showing an approval checkpoint in a Power Automate flow. The flow pauses at an approval step, sends a request to the designated approver, and branches based on the response: Approved continues the flow, Rejected stops it and sends a notification.
:width: 80%
:align: center

Approval steps are designed control points. They insert human judgment exactly where the process requires it — and nowhere else.
:::

Automation multiplies whatever you built. That is the promise and the peril.

**If you automated an efficient, verified process**, you have just scaled that efficiency to every instance where the trigger fires. Every show. Every week. Forever.

**If you automated an unverified process**, you have just scaled that error to the same degree. An incorrect rate calculation, a wrong recipient list, a missing validation step — now running 4,000 times a year at machine speed with no human to notice.

::::{admonition} ⚠️ Never Automate an Unverified Process
:class: danger

The single most expensive automation mistake is not a failed flow. It is a *successful* flow running an incorrect process.

A failed flow produces an error message. Someone investigates. The problem is found and fixed.

A flow running an incorrect process produces outputs that look correct. Nobody investigates because nothing failed. The incorrect output becomes the basis for decisions, invoices, reconciliations, and client communications.

By the time someone notices, the damage is distributed across months of work.

**Before any flow goes to production:**
1. Run the equivalent process manually at least twice with verified outputs
2. Run the flow against historical data where you know the correct answer
3. Have a second person review the logic
4. Run in production with monitoring before trusting it silently
::::

### Flow Ownership and Orphaned Flows

A flow runs with the permissions of its **owner** — the person who created it or to whom ownership was transferred. When that person leaves GES, their flows do not stop. They become **orphaned**: still running, still accessing data, but owned by an account that may be disabled or reassigned.

:::{figure} ../images/ch16-flow-ownership-risk.png
:label: fig-ch16-flow-ownership-risk
:alt: Risk diagram showing orphaned flow scenario. Original creator leaves company, flow continues running with their stale permissions, accesses data they should no longer see, or fails silently when their account is disabled. Arrows show the cascading failure modes.
:width: 80%
:align: center

Orphaned flows are automation liabilities. When the owner leaves, the flow's permissions become stale — and its failures become invisible.
:::

**The risk**: A flow created by an account director who had access to client account sites continues running after that person moves to a different role — or leaves GES entirely. The flow still reads client data. If the account is disabled, the flow fails silently. Nobody finds out until someone asks why the report stopped appearing.

**The mitigation**: Flow ownership must be part of offboarding. When someone leaves a role, their flows transfer to their successor — explicitly, with documentation. IT should maintain an inventory of flows by owner and audit it quarterly.

::::{admonition} ⚠️ A Flow Runs as Its Owner
:class: danger

The permission model from Chapter 12 applies to flows exactly as it applies to Cowork: **a flow can access anything its owner can access**.

If you have broad access across client accounts and you create a flow that reads from "all show libraries," that flow inherits your broad access. It can read client material you have access to but should not be combining into a single output.

Cross-client contamination is not prevented by flow design alone. It requires that flow owners have appropriate access limits — and that flows are scoped to specific libraries rather than broad searches.

Before creating a flow that touches client data, ask: **if this flow's output were sent to the wrong person, what would be in it?** Then scope the flow so the answer is "nothing."
::::

### Error Handling and Silent Failure

:::{figure} ../images/ch16-error-handling.png
:label: fig-ch16-error-handling
:alt: Comparison diagram showing two flows. Left: flow with no error handling — an action fails, the whole flow fails, no notification, nobody knows. Right: flow with error handling — an action fails, the flow catches the error, logs it, sends notification to the owner, continues with remaining actions or fails gracefully.
:width: 80%
:align: center

The difference between error handling and hope. The flow on the left fails invisibly. The flow on the right fails loudly — which is the only kind of failure you can fix.
:::

A flow that fails silently is worse than a flow that fails loudly.

**Silent failure modes:**
- A file was not where the flow expected it; the flow logged nothing and exited
- An approval request was sent to an approver who is on leave; the flow waits forever
- A connector timed out; the flow retried three times and stopped; nobody was notified
- The flow succeeded but produced the wrong output because an upstream data source changed format

**Error handling is not optional:**

1. **Try-catch scopes** — wrap actions that might fail and define what happens when they do
2. **Notifications on failure** — send an email or Teams message to the flow owner when something breaks
3. **Logging** — write to a run history that someone can review
4. **Timeouts with escalation** — if an approval does not come within X hours, escalate or fail explicitly

The goal is not to prevent all failures — some failures are legitimate (a file really was missing). The goal is to make failures *visible* so someone can act on them.

### Approval Steps as Control Points

Not every flow should run without human oversight. Approval steps are how you insert human judgment where the process requires it.

**Use approval steps for:**
- External communications (email to organizers, exhibitors, clients)
- Rate exceptions or pricing outside standard parameters
- Safety escalations that require management awareness
- Any output that will be used as the basis for client billing

**Do not use approval steps for:**
- Every action in the flow (that defeats the purpose of automation)
- Internal logging and filing (if you trust the logic, let it run)
- Notifications that are informational rather than action-requiring

The design principle: **automate the work that does not require judgment; pause for judgment where it does**.

---

## 10. Honest Limitations

This section exists because the vendors will not write it.

**Desktop RPA is brittle.** It breaks when UIs change. It requires a machine to be running (or a hosted RPA bot, which costs money). It is maintenance-intensive. Use it only when there is no connector and no API — and budget for the maintenance.

**Premium connectors cost money.** The Power Automate Premium license is approximately $15 per user per month. Some connectors require additional licensing. Hosted RPA bots are approximately $215 per bot per month. Budget before you build.

**Not everything should be automated.** If the process requires nuanced judgment at every step, automation does not help — it just creates a flow that pauses for approval constantly. If the process runs twice a year, the automation investment may exceed the time it saves. If the process is not yet well-understood, automating it locks in whatever you think it is, which may not be what it actually is.

**Maintenance burden is real and under-estimated.** Flows break when connectors are updated, when file locations change, when personnel change, when business logic changes. Every flow is a small piece of infrastructure that requires occasional attention. Twenty flows require attention twenty times as often.

**Automation can mask problems.** A manual process forces someone to look at the data every time. An automated process runs whether the data is right or wrong. If the upstream data quality is poor, automation hides it until the downstream outputs are obviously wrong — at which point the problem has compounded.

The right mindset: automation is a trade-off, not a gift. It trades ongoing execution time for upfront design and ongoing maintenance. That trade is usually favorable for high-frequency, stable processes. It is often unfavorable for low-frequency or rapidly changing ones.

---

## 11. Build Your First Flow — A Walkthrough

This walkthrough builds a simple, practical flow that a non-technical GES employee can complete in 30 minutes. It demonstrates the core concepts without requiring premium connectors or complex logic.

**The scenario:** Every week, you want to receive an email summarizing how many files were added to your team's SharePoint folder in the past 7 days.

**Step 1 — Open Power Automate**

Go to [make.powerautomate.com](https://make.powerautomate.com) and sign in with your GES Microsoft 365 account.

**Step 2 — Create a new flow**

Click **+ Create** in the left navigation, then select **Scheduled cloud flow**. Name it "Weekly SharePoint Summary" and set the schedule: every Monday at 8 a.m.

**Step 3 — Add the first action**

Click **+ New step** and search for "SharePoint." Select **Get files (properties only)** from the SharePoint connector.

- **Site Address:** Select your team's SharePoint site
- **Library Name:** Select the document library you want to monitor

**Step 4 — Filter to recent files**

Click **+ New step** and search for "Filter array." This is a Data Operations action.

- **From:** Select the "value" output from the previous SharePoint step
- **Condition:** Select the "Created" field, choose "is greater than," and enter an expression: `addDays(utcNow(), -7)`

This filters to only files created in the last 7 days.

**Step 5 — Count the files**

Click **+ New step** and search for "Compose" (Data Operations). In the **Inputs** field, enter the expression: `length(body('Filter_array'))`

This gives you the count of recent files.

**Step 6 — Send the email**

Click **+ New step** and search for "Outlook." Select **Send an email (V2)**.

- **To:** Your email address
- **Subject:** Weekly SharePoint Summary
- **Body:** Compose a message like: "In the past 7 days, [output of Compose] files were added to [folder name]."

**Step 7 — Save and test**

Click **Save** in the top right. Then click **Test**, select **Manually**, and click **Test** again. The flow will run immediately. Check your email.

**Step 8 — Review and refine**

Look at the test results. Did it count correctly? If not, check your filter expression. Once it works, the flow will run automatically every Monday.

---

## 12. The Compounding ROI of Automation

:::{figure} ../images/ch16-automation-roi-compounding.png
:label: fig-ch16-automation-roi
:alt: Graph showing automation ROI over time. X-axis is time in months, Y-axis is cumulative hours saved. The curve shows initial investment (negative), break-even point, and then accelerating returns as the flow runs repeatedly. A callout shows the compounding effect: 20 minutes saved × 4,000 runs = 1,333 hours.
:width: 80%
:align: center

Automation ROI compounds over time. The initial investment is repaid, and then the savings accelerate — because the flow keeps running while you do other work.
:::

The math of automation at GES scale is dramatic.

A 20-minute task, automated, running 4,000 times a year, saves **1,333 hours** annually. That is not a rounding error. It is eight months of a full-time employee's working hours.

But the compounding effect is larger than the raw time savings:

**Consistency improves.** The 4,001st run of the flow is identical to the first. Human execution drifts — shortcuts, variations, forgotten steps. Automated execution does not.

**Speed improves.** The flow runs in seconds. A human takes 20 minutes. For time-sensitive processes — freight alerts during move-in, safety escalations — that speed difference matters.

**Scalability improves.** Adding ten more shows does not require ten more people running the report. The flow handles them all.

**Attention shifts.** Instead of running the report, the analyst reviews the exceptions the report flagged. That is higher-value work — pattern recognition, judgment, intervention.

The cost is real: design time, testing time, maintenance time. But at 4,000+ shows a year, the math almost always favors automation for any process that is truly repetitive.

::::{admonition} 🧭 T.R.U.E. Check — Excellence
:class: note

**Provide excellent service and execution.**

Excellence is not heroic effort. It is consistent delivery — the 4,000th show receiving the same rigorous analysis as the first. Automation is how excellence scales beyond what individual humans can sustain.
::::

---

## 13. Try This: Convert a Cowork Task to a Flow

Pick a Cowork task you have run at least three times and that produces the same output structure each time.

**Step 1 — Document the Cowork prompt**

Write out the current five-part prompt: Outcome, Inputs, Definition of done, Constraints, Approval scope.

**Step 2 — Identify the trigger**

What event would naturally start this task without you? A file posting? A date arriving? A form submission?

**Step 3 — Map the actions**

List every step Cowork takes. For each step, identify the Power Automate connector or action that would accomplish the same thing.

**Step 4 — Identify the human checkpoints**

Where in the Cowork version do you stop and review before approving? Those become approval actions in the flow.

**Step 5 — Build it (or spec it)**

If you have Power Automate access, build the flow. If not, write a specification document that someone could build from — detailed enough that they would not need to ask clarifying questions.

**Step 6 — Test against known output**

Run the flow against a show where you already know the correct output. Does it match?

---

## 14. Productive Struggle Problem

You are the logistics director for a portfolio of 140 shows across 12 venues. You have noticed that freight target compliance varies dramatically by venue — some venues consistently hit targets, others consistently miss.

You have three data sources:
1. Freight target agreements (by show, in SharePoint)
2. Advance warehouse receiving logs (by show, in a legacy system accessible only through a web portal)
3. Material handling reconciliations (by show, in Excel files in SharePoint)

**The challenge:** Design an automated analysis system.

1. **Define the trigger.** What event or schedule would initiate the analysis? Justify your choice.

2. **Map the flow.** List the actions in sequence. Identify which use cloud connectors and which require desktop flows (RPA). For each RPA action, describe why it is necessary and what maintenance burden it creates.

3. **Design the output.** What does the report look like? Where is it delivered? Who receives it?

4. **Add governance.** What approval steps, if any, belong in this flow? What error handling is required? How do you prevent cross-client contamination if venues host competing exhibitors?

5. **Estimate ROI.** If the manual version takes 4 hours per month and the flow takes 20 hours to build and 2 hours per month to maintain, how many months until break-even?

6. **Identify what you would not automate.** What part of this analysis still requires human judgment, and why?

---

## 15. Closing the Arc — From Asking to Automating

This is the final chapter of the book.

Look back at where you started. In Chapter 1, you learned what AI can and cannot do. In Chapter 4, you learned to prompt well. In Chapters 7-11, you learned to use Copilot in Word, Excel, PowerPoint, Outlook, and Teams. In Chapter 12, you learned why SharePoint governance is AI governance. In Chapter 13, you learned to build analytical systems. In Chapter 14, you learned to delegate to Cowork. In Chapter 15, you learned to build agents.

Now you have learned to automate.

The arc is not technological. It is professional.

**Asking** teaches you what AI can do and builds trust through verification. You see every output. You approve every action.

**Delegating** teaches you to scope work precisely and review like a manager. You define outcomes and constraints; AI handles execution. You step back from the middle of the work and focus on the ends.

**Automating** teaches you to remove yourself entirely — for the work that does not need you. You design once, verify carefully, and let the process run forever.

That progression describes a career, not a curriculum. The GES professional who started this book asking Copilot to rewrite an email ends it designing automation that runs 4,000 times a year without human intervention.

What does that mean for a career at GES?

It means **more time on judgment and less time on execution**. The freight variance report runs itself; you analyze the patterns it surfaces. The exhibitor order form routes itself; you handle the exceptions that require human creativity. The post-show reconciliation assembles itself; you explain the story to the organizer.

It means **higher leverage**. A single logistics analyst with well-designed automation can cover territory that previously required a team. Not because the analyst works harder, but because the repeatable work is handled by systems.

It means **new skills matter**. The ability to design a good process, verify it rigorously, and scope automation appropriately is as valuable as the ability to execute the process manually — more valuable, because the design scales and the execution does not.

GES became independent on December 31, 2024, for the first time in 55 years. That independence means GES defines its own technology roadmap. onPeak's AI Smart Suite and Visit by GES's intelligent hardware prove the company can build AI into products. This book proves the company can build AI into operations.

The work is not finished. It is barely started. Across 4,000+ shows, 150,000+ exhibitors, 75+ countries, and 24 facilities, there are thousands of processes waiting to be designed better, verified carefully, and automated permanently.

That is the work. And now you know how to do it.

::::{admonition} 🧭 T.R.U.E. Check — Responsibility
:class: note

**Be responsible for our actions and deliver on our commitments.**

Automation is a commitment. A flow you built and deployed runs on GES's infrastructure, accesses GES's data, and produces outputs that bear GES's name. It is not "the AI's" work. It is yours — automated.

The responsibility does not diminish because the execution is handled by software. If anything, it increases: you are responsible not just for one output, but for every output the flow will ever produce.

Build carefully. Verify thoroughly. Own the result.
::::

---

## 16. Leader's Takeaway

Automation changes what your team does. That requires changing how you lead them.

**First: the prototype discipline is non-negotiable.** No flow goes to production without being tested as a Cowork prompt first, validated against known outputs, and reviewed by a second person. The cost of an unverified automated process — scaled across 4,000 shows — is far higher than the cost of taking an extra week to verify.

**Second: flow ownership is a governance issue.** Every flow must have a named owner. When people leave roles, their flows transfer — explicitly, documented, that day. IT should maintain an inventory and audit it quarterly. Orphaned flows are ticking liabilities.

**Third: error handling is not optional.** A flow that fails silently produces invisible damage. Every flow must log its runs, catch its errors, and notify someone when something breaks. If you cannot answer "who gets notified when this flow fails," the flow is not ready for production.

**Fourth: automation does not reduce headcount — it changes work.** The analyst who used to run the freight report now analyzes the patterns the report surfaces. The exhibitor services rep who used to key in order forms now handles the exceptions that require judgment. Automation shifts people from execution to design, from doing to reviewing. That is a higher-value role — but only if you train for it and manage to it.

**Fifth: start with the high-frequency, stable processes.** The freight variance report that runs 4,000 times a year is a better automation target than the annual strategy deck. The exhibitor order form that arrives in consistent format is a better target than the one-off venue rule document. Prioritize by frequency × stability.

The organizations that extract the most from automation are not the ones that automate the most. They are the ones that automate *carefully* — choosing the right processes, verifying rigorously, and maintaining deliberately.

At GES, with 4,000+ live experiences a year, the opportunity is enormous. So is the risk of doing it poorly.

Lead accordingly.

---

## Glossary

```{glossary}
Power Automate
  Microsoft's automation platform for building workflows (flows) that run on triggers. Part of the Microsoft Power Platform alongside Power Apps, Power BI, and Copilot Studio.

Cloud flow
  A Power Automate flow that runs on Microsoft's servers, connecting applications through API-based connectors. More reliable and easier to maintain than desktop flows.

Desktop flow
  A Power Automate flow that runs on a Windows machine, automating applications through UI interaction (clicking, typing, reading screens). Required when applications lack API connectors. Also called RPA.

Robotic Process Automation (RPA)
  Automation that mimics human interaction with software — clicking buttons, typing into fields, reading text from screens. Necessary for legacy applications without APIs; brittle and maintenance-intensive.

Trigger
  The event that starts a Power Automate flow. Types include scheduled (runs at a set time), event-driven (runs when something happens), manual (runs when a user clicks a button), and approval-based (runs based on approval outcome).

Connector
  A standardized API integration in Power Automate that enables flows to interact with a specific service (SharePoint, Outlook, Teams, Salesforce, etc.). Microsoft offers 1,000+ connectors.

AI Builder
  Microsoft's low-code AI capability for document processing, object detection, text classification, and prediction. Integrated into Power Platform; enables extraction of structured data from unstructured documents.

Document processing model
  An AI Builder model that extracts specific fields from documents. Pre-built models exist for invoices, receipts, and identity documents; custom models can be trained for organization-specific documents like exhibitor order forms.

Flow owner
  The person responsible for a Power Automate flow. Flows run with the owner's permissions — a flow can access anything its owner can access. Ownership must transfer when people leave roles.

Orphaned flow
  A flow whose owner has left the organization or changed roles without transferring ownership. Continues running with stale permissions; may fail silently when the owner's account is disabled.

Approval action
  A Power Automate action that pauses the flow, sends an approval request to designated approvers, and branches based on the response. Used to insert human judgment at control points.

Error handling
  Flow logic that catches failures, logs them, and notifies appropriate people rather than failing silently. Includes try-catch scopes, failure notifications, and timeout escalations.

Premium connector
  A Power Automate connector that requires a Premium license ($15/user/month) to use. Includes many third-party services and advanced Microsoft capabilities.

Hosted RPA bot
  A virtual machine running Power Automate Desktop, hosted in Microsoft's cloud, that executes desktop flows without requiring the user's local machine to be running. Approximately $215/bot/month.

Cowork-to-flow progression
  The recommended pattern for building automation: prototype as a Cowork task, refine through iteration, validate against known outputs, then convert to a Power Automate flow for production deployment.

Silent failure
  A flow failure that produces no notification — the flow stops running but nobody is alerted. The most dangerous failure mode because problems compound before discovery.

Drayage
  The movement of exhibitor freight from the dock or advance warehouse to the booth space on the show floor, and back out at move-out. A core material handling service and cost line.

Freight target
  An agreed target date and time window for freight arrival, used to sequence move-in and manage marshaling yard capacity. Variance from target is a key operational metric.
```

---

## Discussion

The progression from asking to delegating to automating is not just a technology adoption curve. It is a professional development arc.

Consider your current role at GES. Which of your regular tasks belong at each level — Chat, Cowork, or Power Automate? What would need to be true before you could move a task from one level to the next?

Then consider the harder question: if your execution work were automated, what would you do with the time?

::::{admonition} 📝 Discussion Guidelines
:class: note

Post your reflection in the course discussion forum before the session closes. Your response should:

- Identify one process in your role that is currently manual, describe how it would be automated, and specify which trigger type you would use
- Identify one process you would **refuse** to automate, and explain why — referencing governance, judgment requirements, or risk considerations from this chapter
- Address the verification question: what testing would you require before deploying a flow that runs without human intervention?
- Respond to at least **two peers** with substantive engagement — challenge an automation choice, identify a governance gap they missed, or build on their ideas
- Reference at least one credible source — Microsoft Power Automate documentation, this chapter's governance framework, or GES's T.R.U.E. values

Minimum 300 words for your main post.
::::

---

::::{admonition} 🧭 T.R.U.E. Check — Understanding
:class: note

**People come first. Be understanding and compassionate.**

Automation changes jobs. Some people will see it as opportunity — less drudgery, more judgment work. Others will see it as threat — their expertise in execution becoming less valuable.

Both reactions are legitimate. The transition deserves patience, training, and honest conversation about what work looks like on the other side.

AI does not replace people. It changes what people do. How that change lands depends on how leaders manage it.
::::
