---
title: "Chapter 14: Copilot Cowork — Delegating Real Work"
subtitle: "From Answering Questions to Finishing Work — The Third Gear of Microsoft 365 Copilot"
short_title: "Copilot Cowork"
description: "Microsoft Copilot Cowork went generally available on June 16, 2026. It does not answer questions — it executes long-running, multi-step, multi-app work and returns finished artifacts. This chapter teaches the Chat vs. Cowork vs. Agents decision rule, Microsoft's five-part Cowork prompting structure, the approval and governance model, the Copilot Credits economics, and nine fully worked GES scenarios spanning show operations, creative, sales, freight, exhibitor services, onPeak housing, and ESG reporting."
label: ch14-copilot-cowork
tags: [Copilot Cowork, delegation, Work IQ, Microsoft 365, approvals, governance, Copilot Credits, Anthropic, Opus 4.8, Sonnet 4.6, show operations, drayage, material handling, GSC, Spiro, onPeak, exhibitor services, ESG, GES, T.R.U.E.]
---

```{admonition} Download this Chapter as PDF
:class: tip

[Download PDF](https://github.com/liquid-books/ges-learns-ai/raw/main/pdfs/ch14-copilot-cowork.pdf)
```

# Chapter 14: Copilot Cowork — Delegating Real Work

> *"It is easy to have a dozen tasks in flight at once, each one moving forward while you focus on what only you can do."*

It is 4:40 p.m. on the last day of move-out at a 480,000-square-foot show in Las Vegas. A GES show manager is standing in an aisle that used to be a technology pavilion, watching the last of the aisle carpet come up, holding a radio in one hand and a phone in the other. The marshaling yard is running forty minutes behind. Two exhibitors still have crates unaccounted for. The organizer wants a preliminary reconciliation summary "sometime tomorrow, ideally before my board call."

That reconciliation package is real work. It means pulling the labor hours from the on-site sheets, comparing them to the forecast, reconciling material handling weights against the freight targets, cross-referencing the exhibitor orders that changed on the floor against what was actually delivered, and writing a narrative that a show organizer can read in six minutes and understand.

It is four hours of work, minimum. It requires SharePoint, Excel, Outlook, Teams, and a document library. And the person who has to do it is currently standing in a mostly empty hall with a dying phone battery and a 7:15 a.m. flight.

Here is the change this chapter is about. That show manager can open Copilot on their phone, describe the *outcome* they want, attach the show's document library, and walk away. The task keeps running when the phone goes into airplane mode. Somewhere over Denver, the work is still progressing. By the time they land, there is a draft reconciliation workbook in the show folder, a narrative summary in Word, and a proposed email to the organizer waiting for approval — not sent, waiting.

That is Copilot Cowork. And the skill it demands is not a new kind of prompting. It is a new kind of *management*.

---

## 1. The Shift: Copilot Now Has Three Gears

Every chapter before this one taught you to work *with* Copilot. This chapter teaches you to delegate *to* it.

The distinction matters more than it sounds. Up to now, the pattern has been consistent: you prompt, Copilot responds, you evaluate, you refine. You are the loop. Every step passes through you. That is a genuinely powerful way to work, and for a large share of daily tasks it remains the right one.

Cowork breaks that pattern. You describe an outcome. Cowork plans the steps, opens the apps, retrieves the files, does the analysis, produces the documents, and pauses only when it needs a decision from you. You are no longer the loop. You are the reviewer.

Microsoft frames the Copilot family in three modes, and this table is the single most important thing in the chapter. Learn it well enough to explain it to a colleague in thirty seconds.

```{list-table} The three modes of Microsoft 365 Copilot
:header-rows: 1
:name: table-ch14-three-modes

* - 
  - **Chat**
  - **Cowork**
  - **Agents**
* - **Best for**
  - Conversational AI for drafting, Q&A, and ideation
  - Delegating and executing long-running, multi-step work across your apps
  - Ready-made assistants for specialized or repeatable tasks
* - **How you interact**
  - A conversation — you steer each step from prompt to response
  - An assignment — you describe the goal and check in at key milestones
  - A workflow — you pick an agent built for a specific job
* - **Typical work pattern**
  - **You're in the loop.** One prompt, one result, then you choose what's next
  - **You step away.** Cowork plans, manages files and tasks across apps, and delivers completed work
  - **You run it on demand.** The agent handles the same scoped task each time
* - **GES example**
  - "Rewrite this exhibitor notice so it's clearer about the advance warehouse deadline."
  - "Produce the post-show reconciliation package for Show 4412 and draft the organizer summary email."
  - The exhibitor-question triage agent that classifies inbound service-kit questions every morning
```

:::{important}
**The decision rule — memorize this**

Ask yourself one question before you open anything: **how many steps and how many apps?**

- **One step, one app, and I want to see the answer right now** → **Chat**
- **Many steps, several apps, and I want a finished artifact I can review and ship** → **Cowork**
- **The same narrow task, over and over, on demand or on a trigger** → **an agent**

If you can describe the work as a *question*, it's Chat. If you can only describe it as a *deliverable*, it's Cowork. If you find yourself describing the same deliverable every week, it's time to build an agent — or schedule the Cowork task.
:::

The professional behavior underneath this is worth naming plainly, because it is the actual skill.

The prompt-craft skill of Copilot Chat is **describing a task**. The skill of Cowork is **describing an outcome and then reviewing like a manager.**

Anyone at GES who has ever run a crew knows exactly what that means. You do not tell a lead installer which screw to pick up. You tell them what the booth looks like when it's done, what the constraints are (union jurisdiction, the venue's rigging rules, the 6 p.m. hard stop), what you want to be consulted on, and then you let them work — and you inspect the result before the exhibitor sees it. That is precisely the relationship Cowork asks for.

:::{note}
**Why this feels uncomfortable at first — and why that's normal**

Delegation is a learned skill for humans, and it is uncomfortable for the same reason with software: the first few times, you will want to watch every step, and watching every step defeats the purpose.

The mental model that helps most people over the hump is this: you are not giving up control. You are moving your control from the *middle* of the work to the *ends* of it — a tight brief at the front, a rigorous review at the back. That is more control over what matters and less over what doesn't.
:::

---

## 2. What Copilot Cowork Actually Is

### 2.1 The one-sentence definition

**Copilot Cowork executes complex, long-running, multi-tool tasks end-to-end across Microsoft 365 and returns finished artifacts — a deck, a report, an email, an updated workbook — not a draft suggestion or a recommendation.**

### 2.2 The timeline

Cowork did not appear overnight, and its history tells you something about how carefully it was built.

```{list-table} How Cowork reached general availability
:header-rows: 1
:name: table-ch14-timeline

* - Stage
  - When
  - What it meant
* - Research Preview
  - Early 2026
  - A limited set of customers testing the concept of delegated, multi-step work
* - Frontier program
  - Late March 2026 (announced March 9)
  - Broad early access inside Microsoft's Frontier program. Became the **fastest-growing feature in the history of that program** and recorded the **highest user satisfaction of any Copilot or agent experience Microsoft has shipped**
* - General Availability
  - **June 16, 2026** — worldwide
  - Available to any organization with the Microsoft 365 Copilot license, subject to admin enablement
```

At GA, **more than half of the Fortune 500** were already using it, including Accenture, Avanade, Advance Local, Capital Group, Koch, LTM, Ooredoo Qatar, and Zurich Insurance. That adoption curve is unusual, and it's the strongest available evidence that this is not a novelty feature.

### 2.3 The models — and the Anthropic relationship

Cowork's underlying intelligence is worth understanding, because it explains both its capability and its cost model.

Microsoft worked **closely with Anthropic** and **integrated the technology behind Claude Cowork into Microsoft 365 Copilot**. At general availability, Cowork runs on Anthropic's frontier models — **Opus 4.8** and **Sonnet 4.6**. Microsoft's own fine-tuned model, **Cowork 1**, was post-trained for substantially lower cost and is releasing shortly after GA.

Microsoft's positioning here is deliberate and, frankly, sensible: *your work is not limited by one brand of models.* Copilot hosts the best innovation from across the industry and chooses the right model for the job regardless of who built it. A lightweight formatting task does not need a frontier reasoning model. A 40-source deep research synthesis does. Multi-model design means the platform can match the model to the task — which is a capability story and a cost story at the same time.

### 2.4 The five things that make Cowork structurally different

```{list-table} Microsoft's five differentiators for Cowork
:header-rows: 1
:name: table-ch14-differentiators

* - Differentiator
  - What it actually means
  - Why it matters at GES
* - **Cloud hosting**
  - Runs in a protected, sandboxed cloud environment. Files aren't stored locally. **Tasks keep running even when your laptop is off.**
  - Your people are on show floors, in warehouses, and in airports. Work that requires a running laptop is work that stops at the jetway.
* - **Native Work IQ support**
  - Grounds every task in the systems your business already runs on — email, files, meetings, chats, SharePoint
  - A reconciliation task that can actually see the show's document library is a different animal from one that can't
* - **Enterprise-grade security and compliance**
  - Operates inside your Microsoft 365 trust boundary. Identity, permissions, and compliance policies apply by default; actions and outputs are auditable
  - GES holds client confidential material — competitor booth plans, unannounced product launches. The trust boundary is not optional
* - **Multi-model design**
  - Run the model a task needs; capability scales as more models become available
  - Heavy analytical work and light formatting work don't have to cost the same
* - **Lower cost**
  - Efficient runtime, model choice matched to task, billing only for what you use
  - Matters at ~2,600 employees. See §8
```

:::{note}
**"Protected, sandboxed cloud environment" — in plain language**

Cowork does not run on your machine. It runs in an isolated environment inside Microsoft's cloud, within your organization's tenant boundary. Two practical consequences follow:

1. **Continuity.** You can close your laptop, switch from desktop to phone, get on a plane, or walk the floor. The task keeps progressing.
2. **Containment.** The work happens in a controlled space with your identity, your permissions, and your organization's compliance policies applied by default. Nothing is quietly copied to a local drive.
:::

---

## 3. What Cowork Can Actually Do

Cowork's capability surface breaks into five areas. Read this section with your own week in mind — the goal is for at least three of these to trigger a "wait, I do that every show" reaction.

### 3.1 Communication

Cowork can draft and send email through Outlook — new messages, replies, forwards. It can post updates in Teams channels and send direct messages in 1:1 or group chats. It can build and send HTML newsletters. It can manage an inbox: sorting into folders, deleting, responding inline. And it can prepare full stakeholder communication sets — status updates, announcements, follow-ups.

**At GES:** the pre-move-in exhibitor notice that goes to 800 exhibitors on a show; the daily on-site status post to the show team's Teams channel; the "your freight has arrived at the advance warehouse" confirmation wave; the organizer weekly update during the 90 days before a show.

### 3.2 Documents and files

Cowork can create Word documents, Excel workbooks, PowerPoint decks, and PDFs from scratch. It can edit and refine documents shared into the session. It can browse your entire Work IQ to pull in the content it needs. It can create SharePoint and OneDrive folders and reorganize existing files into them.

**At GES:** the show operations manual; the exhibitor service kit refresh; a post-show recap deck; the labor forecast workbook; a Spiro spec document; the show folder structure itself, built and populated at kickoff.

### 3.3 Calendar and meetings

Cowork can schedule meetings from natural language, manage a calendar (adding, moving, resolving conflicts, declining with a reason message to the organizer), surface meeting intelligence and prep insights, and deliver a daily briefing of what's ahead.

**At GES:** the week of a show, when a single account lead has an organizer walkthrough, three exhibitor escalations, a union steward meeting, and a client dinner all colliding on the same afternoon.

### 3.4 Research and search

Cowork can search across the organization for documents, messages, and information; run deep research that synthesizes many sources into a comprehensive report; and browse SharePoint and OneDrive folders to select files.

**At GES:** "What did we learn at this venue last year?" — a question whose answer is currently distributed across three people's memories, a OneNote site survey, and an email thread nobody can find.

### 3.5 Automation

Two forms, and they're the ones most people miss:

- **Scheduled prompts** — run a prompt on a schedule so recurring tasks happen automatically. *Every Monday at 6 a.m., produce the freight-target compliance summary for all shows in move-in this week.*
- **Event-driven tasks** — run when something happens. *When an email arrives from the venue's exhibitor services desk, extract the request, classify it, and post it to the show channel.*

:::{tip}
**The scheduled-prompt discipline**

The single highest-return Cowork habit is this: any time you finish a Cowork task and think *"I'll need this again next show,"* stop and convert it into a scheduled prompt or save the prompt text into your team's SharePoint prompt library. The prompt you spent twenty minutes perfecting is an asset. Treat it like one.
:::

---

## 4. The Session Experience — What It's Actually Like to Use

A Cowork session has a rhythm, and knowing it removes most of the first-week friction.

**Step 1 — Describe your task.** You type or dictate the outcome you want. The input field accepts up to **250,000 characters**, so you are not constrained to a one-liner — paste the whole organizer brief if that's what's useful. You can drag files directly into the chat, use **Add work context** to attach specific files, people, emails, Teams chats, channels, or meetings, upload from your device, or attach cloud files from OneDrive, SharePoint, or Teams.

There is a **microphone button** for voice input. This is not a gimmick for GES. Dictating a task while walking a show floor, hands full, is a materially different experience from typing it.

The home page offers suggested prompts — *Catch me up, Organize my inbox, Organize my week, Prep for a meeting, Plan an event, Prepare for my 1:1, Research a company* — and lists your recent tasks so you can resume any previous session.

**Step 2 — Watch Cowork work.** Cowork breaks the request into steps and works through them one at a time, visibly. You see a thinking indicator, step-by-step status updates ("Searching OneDrive," "Composing your email"), responses streaming word by word, and interactive cards. Active skills appear in the side panel as they load. A connection status indicator shows Connecting / Connected / Reconnecting / Failed, with a Retry option.

**Step 3 — Steer, interrupt, or queue.** You can send another message while Cowork is busy. Queued messages are processed in order, and Cowork adjusts direction if what you send changes the plan. You can pause at any point to add context or correct a wrong assumption. Cowork will also ask you clarifying questions — often with multiple-choice options — and you can **Skip** them if the answer doesn't matter to you.

**Step 4 — Approve actions when asked.** Cowork pauses before consequential actions. This is important enough to have its own section (§7).

**Step 5 — Review the results.** Download the documents, check what was sent, and request changes in the same session.

:::{tip}
**Queued messages are the delegation superpower**

Most people discover this late. You do not have to wait for Cowork to finish before adding context. If you're two minutes into a reconciliation task and remember that the labor sheets for Hall C were logged under the wrong show code, just say so. Cowork picks it up in order and adapts.

This is exactly how you'd correct a crew lead mid-task. The interaction model is the same because the relationship is the same.
:::

---

## 5. Skills and Plugins — How Cowork Gets Specialized

Cowork loads specialized **skills** as it works. You don't invoke them by name; Cowork selects them based on what the task needs, and the active ones appear in the side panel so you can see what it's using.

```{list-table} Built-in Cowork skills
:header-rows: 1
:name: table-ch14-skills

* - Skill
  - What it handles
  - A GES use
* - **Word**
  - Creating and editing documents
  - Show operations manual, site survey writeup, SOW
* - **Excel**
  - Building and analyzing workbooks
  - Labor forecast vs. actual, drayage cost analysis, hotel block pickup
* - **PowerPoint**
  - Building decks
  - Organizer QBR, Spiro concept presentation, post-show recap
* - **PDF**
  - Reading and producing PDFs
  - Exhibitor service kits, carnet documentation, venue rule sets
* - **Email**
  - Drafting, replying, forwarding, inbox management
  - Exhibitor notices, organizer updates, escalation responses
* - **Scheduling**
  - Setting up meetings
  - Pre-con calls, walkthroughs, I&D crew briefings
* - **Calendar Management**
  - Moving, declining, resolving conflicts, adding focus time
  - Show-week calendar triage
* - **Meetings**
  - Meeting intelligence and prep
  - Organizer pre-con prep packets
* - **Daily Briefing**
  - What's ahead today
  - Move-in morning briefing for a show manager
* - **Enterprise Search**
  - Finding content across the organization
  - "What did we do at this venue last year?"
* - **Communications**
  - Structured stakeholder comms
  - Multi-audience show announcements
* - **Deep Research**
  - Multi-source synthesis into comprehensive reports
  - Competitive analysis for an organizer RFP
* - **Adaptive Cards**
  - Interactive cards in Teams
  - Approval and status cards in a show channel
```

**Custom skills.** You can create up to **50**. Cowork discovers them automatically at the start of each session. For GES, the obvious candidates are the things that are specific to how *this* company works: the standard post-show reconciliation format, the freight-target compliance calculation, the exhibitor service kit house style, the Spiro spec document template, the ESG emissions data schema.

**Plugins.** Cowork supports plugins from the Microsoft 365 App Store. These add new skills and connectors — specialized expertise (financial analysis, legal research) or connections to external data sources. Admins can deploy plugins org-wide, which is the right pattern for anything that touches a system of record.

:::{note}
**The 50-custom-skill budget is a governance decision, not a technical one**

Fifty is more than enough — if the skills are chosen deliberately. It is not nearly enough if every team builds their own slightly different version of "post-show summary." Somebody at GES should own that list the way somebody owns the show document template library. The skills that deserve a slot are the ones that encode *how GES does it*, not the ones that encode how one person prefers it.
:::

---

## 6. The Five-Part Cowork Prompt — The Core Skill of This Chapter

Here is the honest truth about Cowork: **most disappointing results are scoping failures, not capability failures.**

"Clean up my calendar" leaves almost everything open to interpretation. Cowork has to guess what you value, and guessing shapes the result. The same request, scoped properly, produces something you'd actually ship.

Microsoft's official guidance gives a five-part structure. Learn it, use it every time, and your success rate with Cowork changes immediately.

```{list-table} The five-part Cowork prompt structure
:header-rows: 1
:name: table-ch14-five-part

* - Part
  - What it answers
  - What it looks like
* - **1. Outcome**
  - What does *done* look like, in one sentence?
  - "A post-show reconciliation package for Show 4412 that the organizer can read before their board call."
* - **2. Inputs**
  - Which specific people, files, sites, or time ranges should this use?
  - "The Show 4412 SharePoint library, the on-site labor sheets, the freight manifest workbook, and my email thread with the organizer since May 1."
* - **3. Definition of done**
  - What is the concrete deliverable, and where does it live?
  - "An Excel workbook and a two-page Word summary saved to the Show 4412 library, plus a draft email to the organizer."
* - **4. Constraints**
  - What must be avoided or honored?
  - "Use the FY27 reconciliation template. Do not contact the exhibitors directly. Keep the summary under two pages. Flag variances over 8% rather than explaining them."
* - **5. Approval scope**
  - Which actions do you want to review explicitly, beyond the default checkpoints?
  - "Ask me before sending anything external. You can create and save files without asking."
```

**The before-and-after that makes this click:**

:::::{tab-set}
::::{tab-item} ❌ Under-scoped
```
Help me prep for my offsite next week.
```

Cowork will do *something*. It will probably be generic, probably include content you didn't want, and probably miss the one thing that mattered. You'll conclude Cowork "isn't that good."
::::
::::{tab-item} ✅ Properly scoped
```
Outcome: A briefing pack and a draft agenda for the offsite on June 12.

Inputs: The offsite calendar invite, the three pre-reads I've attached, 
and the notes from our last two leadership syncs.

Definition of done: One Word briefing document and one draft agenda, 
both saved to the Leadership Offsite folder in SharePoint.

Constraints: Keep the briefing to four pages. Use our standard agenda 
format. Do not include budget figures — those come from Finance separately.

Approval scope: Don't send anything to attendees. Just save the files 
and tell me when they're ready.
```
::::
:::::

:::{important}
**Why "Approval scope" is the part people skip — and shouldn't**

Parts 1 through 4 are about getting good output. Part 5 is about not being surprised.

Approval scope is where you tell Cowork the difference between actions you're comfortable with (creating a file, building a workbook, scheduling internal prep time) and actions that carry consequence (emailing a show organizer, posting in a client-facing Teams channel, declining a meeting on someone's behalf).

Set it explicitly at the front of every task and you will almost never find yourself hitting Cancel in a hurry. Skip it and you're relying entirely on Cowork's defaults to match your judgment about what's sensitive at GES. They usually will. "Usually" is not a standard we apply to client-facing communication.
:::

:::{tip}
**A pocket version you can actually remember on a show floor**

**O-I-D-C-A.** Outcome. Inputs. Done. Constraints. Approvals.

Say it out loud into the microphone button in that order and you've written a good Cowork prompt without typing a word.
:::

---

## 7. Approvals and Control — The Governance Heart of Cowork

If you read only one section of this chapter twice, make it this one.

Cowork can send email. It can post in Teams. It can update records and move files and decline meetings. That capability is the whole point — and it is also the reason the approval model exists and the reason you need to understand it properly rather than click through it.

### 7.1 The approval dialog

Before a sensitive action, Cowork pauses and shows you what it intends to do. For many actions you get a **rich preview** — the actual draft email, the actual Teams message, the actual meeting invite. For others you get a summary. Medium and high risk actions carry a **risk level indicator**.

You then have four choices.

```{list-table} Your four options at an approval prompt
:header-rows: 1
:name: table-ch14-approvals

* - Option
  - What it does
  - When to use it at GES
* - **Action button** (Send / Post / Create)
  - Proceeds with this one action, this one time
  - Your default. Every external communication. Anything a client will see.
* - **More options** dropdown
  - Approves and skips prompts for *similar* actions for the rest of the session. For email and Teams you can scope it: **Only to** a specific recipient, **Only to** recipients at a domain, or **Always allow** for the session. Other action types get a single "Approve & don't ask again."
  - The scoped versions are genuinely useful — "only to @ges.com" during an internal-only task means you stop being interrupted for internal posts while still being stopped cold before anything leaves the company.
* - **Approve All**
  - Approves all pending approvals at once. The button shows the count, e.g. **Approve All (3)**
  - Only when you have actually read all three. See the warning below.
* - **Cancel**
  - Stops that action. Cowork skips it and continues with the rest of the request.
  - Use freely. Cancelling one action does not kill the task — this is a lower-cost button than people assume.
```

### 7.2 The permission model — the part that should give you confidence

**Every Cowork task runs with your permissions and sees only what you can see.**

That sentence deserves to be read slowly. Cowork does not have a privileged view of GES data. It is not an administrator. If you cannot open a SharePoint site, Cowork cannot open it on your behalf. If an organizer's contract folder is restricted to the account team, Cowork working for someone outside that team cannot read it.

Data stays in your tenant. Existing user and admin permissions are respected. Identity and compliance policies apply by default. And **Cowork actions are auditable** — there is a record of what was done, when, and on whose behalf.

This is architecture, not policy language. It's the same principle that governs Microsoft 365 Copilot generally, extended to a tool that can now *act* rather than only *answer*.

### 7.3 Where this meets T.R.U.E.

GES's values are not decoration in this chapter. Two of the four map directly onto the approval model, and one maps onto the whole idea of delegation.

```{list-table} The approval model through the T.R.U.E. lens
:header-rows: 1
:name: table-ch14-true

* - Value
  - What it means here
* - **Trust** — *trust each other to always be honest and do what's right*
  - Trust is earned through verification, not assumed through convenience. **Verify before you approve.** Read the recipient list. Read the actual draft, not the summary of the draft. Trust in a tool means trusting it to do what you told it to — which requires checking that you told it the right thing.
* - **Responsibility** — *be responsible for our actions and deliver on our commitments*
  - **You own every output that carries your name.** If Cowork drafts an email and you approve it, that email is yours. It is not "the AI's" email. There is no version of this where the tool absorbs the accountability. A show organizer who receives a wrong number does not care which software produced it.
* - **Understanding** — *people come first*
  - Cowork can decline a meeting on your behalf with a reason message. It cannot read the room. Some declines need a human phone call, and knowing which ones is your job, not the model's.
* - **Excellence** — *provide excellent service and execution*
  - Cowork raises the floor — nothing you ship should be rougher than it used to be. Humans raise the ceiling. The reconciliation package Cowork produces in twenty minutes should free you to think about the *pattern* across the last six shows, which is where the real value to the organizer sits.
```

:::{warning}
**The Approve All trap — read this before your first session**

**Approve All (3)** is a convenience button. It is also the single most likely place for a GES employee to cause real damage with Cowork.

Here is the failure mode, and it is not hypothetical. You are running a task that drafts exhibitor notices. Cowork queues three approvals. Two are internal Teams posts. The third is an email to 800 exhibitors containing a move-in time that changed yesterday. You hit **Approve All** because you skimmed the first two and assumed the third was the same kind of thing.

That email cannot be recalled from 800 inboxes. The organizer will hear about it before you do.

**The rule for GES: never use Approve All on a batch that contains any externally-facing action.** If the queue has an email to a client, an exhibitor, an organizer, or a venue in it, approve items one at a time and read each preview in full. Approve All is for batches of internal, low-consequence, obviously-identical actions — and even then, glance at the count and make sure it matches what you expect.

Reflexive approval is not delegation. It is abdication.
:::

:::{note}
**Microsoft's own guidance, verbatim in spirit**

*Always review details before approving — check recipients, content, and other details.*

Note the word order. Recipients first. In a company that runs 4,000+ events a year for competing brands in the same industries, the recipient list is the highest-risk field on the screen.
:::

### 7.4 Auditability as an operational asset

It's easy to read "actions are auditable" as a compliance checkbox. At GES it's more useful than that.

An audit trail means that when an organizer asks "when did you tell us about the freight target change?", the answer is retrievable. It means that when a show team hands off from pre-show to on-site crew, the record of what was communicated and when is intact. It means a post-show dispute about what an exhibitor was told has evidence behind it rather than three conflicting recollections.

Delegation without a record is risk. Delegation with a record is process.

---

## 8. Economics and Governance — What Cowork Costs and How to Think About It

Cowork is not free, and pretending otherwise makes it harder to adopt well.

### 8.1 The licensing structure

- The **Microsoft 365 Copilot User Subscription License (USL)** is a **prerequisite**. Cowork sits on top of it.
- Cowork itself is billed on **usage**, denominated in **Copilot Credits**.

The USL separately includes Copilot Chat; Copilot in Word, Excel, PowerPoint, Outlook, and Teams; the Work IQ context engine; multi-model frontier intelligence; the pre-built agents (Researcher, Analyst); and custom agents via Agent Builder. Cowork is the delegation layer added on top of all of that.

### 8.2 The four cost inputs

The price of a Cowork task is calculated from four things:

```{list-table} What drives the cost of a Cowork task
:header-rows: 1
:name: table-ch14-cost-inputs

* - Input
  - What increases it
  - How to control it
* - **Model use**
  - Deeper reasoning, more complex synthesis
  - Don't send a formatting job to a frontier model. Multi-model design exists so you can match the model to the job
* - **Context retrieval**
  - The more sources Cowork has to search, the more it costs
  - Point at specific libraries and date ranges instead of "search everything." This is the *Inputs* line of your five-part prompt earning its keep
* - **Tool calls**
  - Every app action — creating a file, sending an email, reading a workbook
  - Ask for the deliverables you need, not every deliverable you can imagine
* - **Runtime**
  - How long the task runs
  - Tighter scope, fewer clarification loops, fewer mid-task corrections
```

Notice that three of the four are directly controlled by prompt quality. **A well-scoped prompt is a cost-control mechanism**, not just a quality mechanism. That is not a coincidence and it's worth saying to anyone at GES who has to sign off on the budget.

### 8.3 Light, medium, heavy

Microsoft observes three task patterns in practice:

```{list-table} Cowork task patterns
:header-rows: 1
:name: table-ch14-task-patterns

* - Pattern
  - Profile
  - GES example
* - **Light**
  - Small number of knowledge sources, limited reasoning, one output or fewer
  - "Organize my inbox into show folders for the three shows I'm on this month."
* - **Medium**
  - Multiple sources, structured reasoning, two or more outputs
  - "Build the move-in schedule and the crew briefing document for Show 4412 from the organizer's floor plan and our labor forecast."
* - **Heavy**
  - Aggregates broadly, deep reasoning, many outputs
  - "Analyze drayage and material handling cost variance across all 14 shows we ran at this venue in the last 18 months and produce the workbook, the narrative analysis, and the client-ready deck."
```

Microsoft also identified **four user personas** with distinct usage patterns, and publishes a customer estimator spreadsheet at **aka.ms/CustomerCoworkEstimator** (its figures assume Anthropic Opus 4.8). The underlying cost model is straightforward:

> (users per segment) × (expected prompt volume across light / medium / heavy) × (cost per prompt type), summed across segments.

Microsoft's own testing reports that Copilot Cowork averaged **30–40% cheaper per prompt** than Claude Cowork operating through its Microsoft 365 connector — a consequence of efficient runtime and matched model selection.

### 8.4 What this means at a company of ~2,600 people

If everyone at GES ran three heavy tasks a day because heavy tasks are fun to watch, the bill would be real. If nobody used Cowork because they were unsure about credits, the opportunity cost would be larger. Neither extreme is the answer.

Here is a practical rule of thumb for GES.

:::{tip}
**When is a Cowork task worth the credits?**

Ask two questions:

1. **How long would this take me?** If the honest answer is under fifteen minutes and it's one app, use **Chat**. Cowork's overhead — planning, retrieval, tool calls — isn't worth it for a task you can finish in a Word window.
2. **Does it produce something I'd otherwise not do at all?** This is the important one. The post-show cross-show pattern analysis that nobody has time for. The venue history summary that lives in three people's heads. The freight-target compliance review that gets skipped in a busy season. These are the highest-value Cowork tasks precisely *because* they currently don't happen.

The worst use of credits is asking Cowork to do a five-minute job. The best use is asking Cowork to do the four-hour job you keep postponing.
:::

Governance guidance for GES leaders deploying this:

- **Give teams a monthly credit budget and visibility into it.** People manage what they can see.
- **Build a shared prompt library.** A well-scoped prompt costs less and produces more. Reusing a good one is free efficiency.
- **Convert the repeated heavy tasks into scheduled prompts.** A weekly scheduled task with a tight scope costs less than six people improvising the same analysis.
- **Watch for the "just re-run it" habit.** Re-running a whole heavy task because one number was wrong is expensive. Steering mid-task, or asking for a targeted correction in the same session, is cheaper.

---

## 9. Microsoft's Four Flagship Scenarios, Translated to GES

Microsoft leads with four demonstration scenarios. Each has a direct GES analogue, and walking the translation is a fast way to see the shape of what Cowork does.

### 9.1 "Clean up your calendar" → Show-week calendar triage

**What Microsoft shows:** Cowork reviews your Outlook schedule, asks what you're prioritizing, flags conflicts and low-value meetings, and proposes changes. On approval it accepts, declines, or reschedules meetings and adds focus blocks. It can also send a prep document for a meeting.

**The GES analogue:** It is the Tuesday of move-in week. A GES account director has an organizer walkthrough, two internal syncs, a Spiro design review, and a supplier call — three of which overlap with the hours they physically need to be on the floor.

> **Outcome:** A show-week calendar that protects Wednesday 7 a.m.–1 p.m. and Thursday 7 a.m.–noon for on-floor time during move-in.
> **Inputs:** My Outlook calendar for June 8–12; the Show 4412 move-in schedule.
> **Definition of done:** Conflicts resolved, focus blocks added, declines sent with a reason.
> **Constraints:** Never move or decline anything with the organizer on it — flag those for me instead. Internal meetings can be moved freely.
> **Approval scope:** Ask before any decline that goes to someone outside GES.

### 9.2 "Build the meeting packet and align the team" → The organizer pre-con packet

**What Microsoft shows:** Cowork pulls inputs from email, meetings, and files; schedules prep time; and produces a connected set of deliverables — a briefing document, supporting analysis, and a client-ready deck, all saved in Microsoft 365 — plus a draft customer status email with the latest files attached.

**The GES analogue:** The pre-conference meeting with a show organizer, ninety days out. Currently this is assembled by three people across a week from a floor plan, a labor forecast, last year's post-show report, and an email thread.

The Cowork version produces the briefing doc, the supporting analysis workbook, the organizer-ready deck, a scheduled internal prep session the day before, and a draft email to the organizer with the deck attached — waiting for approval.

### 9.3 "Research a company fast" → Organizer and prospect intelligence

**What Microsoft shows:** Cowork gathers earnings reports, filings, analyst commentary, and news with an emphasis on primary sources, organizes findings with citations, and returns an executive summary formatted for email, a structured research memo with clear assumptions, and an Excel workbook with labeled tabs.

**The GES analogue:** GES is pitching to become GSC for an association's annual convention. Chuck Grouzard's exhibition sales team needs to know the show's history, its growth trajectory, its stated sustainability commitments, who currently holds the contract, and what the association has publicly said about attendee experience.

Same three artifacts: an email-ready executive summary, a cited research memo with assumptions stated plainly, and a workbook with tabs for show history, exhibitor counts, square footage trend, and competitive incumbency.

### 9.4 "Create the launch plan" → The new service or product rollout

**What Microsoft shows:** Cowork builds a competitive comparison in Excel, distills differentiation into a value proposition document, generates a customer pitch deck, and outlines milestones, owners, and next steps.

**The GES analogue:** Rolling out a sustainable modular exhibit product line into a new region — the competitive comparison against other modular offerings, the value proposition document that sales can actually use, the exhibitor-facing pitch deck, and the milestone plan with owners across creative, operations, and the warehouse network.

---

## 10. Nine GES Scenarios, Worked in Full

This is the practical heart of the chapter. Each scenario names the persona, the trigger, the badly-scoped prompt most people would write first, the properly structured five-part version, what Cowork does step by step, where it pauses, and what comes back.

Read the ones closest to your role carefully. Skim the rest — the patterns transfer.

---

### Scenario 1 — Post-show reconciliation package

**Persona:** Show Manager, GES Exhibitions
**Trigger:** Move-out finished last night. The organizer wants a preliminary reconciliation before their board call in 36 hours. You have a flight in four hours.

:::::{tab-set}
::::{tab-item} ❌ What most people write first
```
Do the post-show reconciliation for the show that just ended.
```
Cowork doesn't know which show, which files, what format, what "reconciliation" includes at GES, or whether it may email the organizer. Best case it asks five clarifying questions you're not around to answer. Worst case it guesses.
::::
::::{tab-item} ✅ The five-part version
```
Outcome: A preliminary post-show reconciliation package for Show 4412 
that the organizer can read before their board call on Thursday morning.

Inputs: The Show 4412 SharePoint library — specifically the on-site 
labor sheets, the material handling and freight manifest workbook, the 
exhibitor order change log, and the original labor forecast. Also my 
email thread with Karen at the organizer since May 1.

Definition of done: (1) An Excel workbook with tabs for labor 
forecast vs. actual, material handling weights vs. freight targets, 
and exhibitor order variances. (2) A two-page Word summary written 
for the organizer, not for internal ops. (3) A draft email to Karen 
with both files attached. Save all files to the Show 4412 library 
under /Post-Show.

Constraints: Use the FY27 reconciliation template. Flag any variance 
over 8% in a callout list rather than explaining it — I'll add the 
narrative. Do not contact any exhibitors. Do not include internal 
margin figures anywhere in the organizer-facing summary.

Approval scope: Create and save the files without asking. Ask me 
before sending anything to the organizer.
```
::::
:::::

**What Cowork does:** Locates the Show 4412 library → opens the labor sheets and forecast → builds the variance analysis → opens the freight manifest and computes material handling weight against the agreed freight targets → reads the exhibitor order change log and reconciles against delivered orders → builds the workbook on the FY27 template → writes the two-page summary in organizer-appropriate language → drafts the email.

**Where it pauses:** At the email to Karen. You get a rich preview showing recipient, subject, body, and the two attachments.

**What comes back:** A reconciliation workbook, a two-page organizer-ready summary, and an email sitting in draft — reviewed on your phone at the gate, approved after you check the variance callouts and confirm no margin figures leaked into the summary.

---

### Scenario 2 — Move-in / move-out planning

**Persona:** Operations Director
**Trigger:** A 620,000 sq ft show at a venue with tight dock access and a hard union jurisdiction boundary between freight and I&D labor. Move-in starts in eleven days.

:::::{tab-set}
::::{tab-item} ❌ Under-scoped
```
Plan the move-in for the big show next month.
```
::::
::::{tab-item} ✅ Five-part
```
Outcome: A move-in and move-out plan for Show 5108 that the on-site 
crew leads and the marshaling yard supervisor can work from directly.

Inputs: The organizer's approved floor plan, the venue dock schedule, 
our labor forecast workbook, the target freight arrival windows for 
the advance warehouse, and last year's post-show report for this 
same show at this same venue.

Definition of done: (1) A Word operations plan with a day-by-day 
move-in sequence by hall, dock assignments, and crew allocation. 
(2) An Excel schedule showing carrier arrival windows against 
marshaling yard capacity by hour. (3) A one-page crew briefing 
document for the I&D leads. All saved to the Show 5108 library.

Constraints: Respect the union jurisdiction boundary — freight 
handling and booth install crews must be scheduled as separate 
resources, never interchangeable. Assume the advance warehouse 
closes to receiving 7 days before move-in. Flag any hour where 
marshaling yard demand exceeds capacity rather than smoothing it 
silently.

Approval scope: Files only. Do not post anything to the show 
Teams channel or email the venue — I'll circulate it myself.
```
::::
:::::

**What Cowork does:** Reads the floor plan and hall breakdown → maps the dock schedule against hall access → pulls the labor forecast and allocates crews by trade respecting the jurisdiction constraint → models carrier arrivals against marshaling yard capacity hour by hour → surfaces last year's documented problems from the post-show report and checks whether the new plan repeats them → produces the three artifacts.

**Where it pauses:** Nowhere externally — you scoped it to files only. It may ask one clarifying question about crew shift length.

**What comes back:** A plan, a capacity schedule with over-capacity hours flagged in red, and a crew briefing sheet. Your job is now the interesting part: deciding what to do about the three flagged hours on Tuesday morning.

---

### Scenario 3 — Site survey writeup

**Persona:** Show Operations Lead
**Trigger:** You just walked a new venue for four hours. You have 60 photos, a OneNote page of scrawled notes, and a voice memo.

:::::{tab-set}
::::{tab-item} ❌ Under-scoped
```
Write up my site survey.
```
::::
::::{tab-item} ✅ Five-part
```
Outcome: A venue site survey document for [Venue] that a show 
manager who has never been there could plan a move-in from.

Inputs: My OneNote site survey page from yesterday, the photos in 
my OneDrive /Site Surveys/[Venue] folder, and the venue's published 
exhibitor rules PDF I've attached.

Definition of done: A Word document saved to the Venue Knowledge 
Base library in SharePoint, following our standard site survey 
structure: access and docks, ceiling heights and rigging, floor 
load, power and utilities, labor and jurisdiction notes, marshaling 
and staging, known constraints, and open questions.

Constraints: Keep every observed fact separate from every inference 
— put anything you inferred rather than observed under a clearly 
labeled "To verify" heading. Do not fill gaps with assumptions from 
other venues.

Approval scope: Files only.
```
::::
:::::

**Where it pauses:** File creation in a shared library may prompt for confirmation depending on your admin's configuration.

**What comes back:** A structured survey document — and, critically, an explicit "To verify" list that tells you exactly what you failed to capture while you were there. That list is worth more than the document.

---

### Scenario 4 — Design brief to spec doc to client-ready concept deck

**Persona:** Creative Director / Designer, Spiro custom exhibits
**Trigger:** An exhibitor client has approved the direction from a discovery call. You need a spec document for engineering and a concept deck for the client, and the client review is Friday.

:::::{tab-set}
::::{tab-item} ❌ Under-scoped
```
Turn my design brief into a deck for the client.
```
Cowork produces a deck. It will look fine. It will also not know the booth's actual footprint constraints, your engineering team's spec format, or that this client's product launch is embargoed.
::::
::::{tab-item} ✅ Five-part
```
Outcome: An engineering-ready spec document and a client-ready 
concept deck for the [Client] 40x50 island stand, both consistent 
with the approved design brief.

Inputs: The approved design brief document, my discovery call notes 
in OneNote, the client's brand guidelines PDF, the venue rigging and 
ceiling height constraints from the Show 5108 site survey, and our 
standard Spiro spec template.

Definition of done: (1) A Word spec document following the Spiro 
template — structure, materials, graphics, lighting, AV, storage, 
I&D assumptions, and open engineering questions. (2) A PowerPoint 
concept deck of 10–12 slides using our client presentation template: 
concept narrative, plan view, three key experience moments, materials 
and finish direction, and next steps. Both saved to the [Client] 
project folder.

Constraints: The stand must respect the venue's 22 ft rigging height 
limit and the show's 50% sightline rule on perimeter elements. Do not 
include any product names or launch messaging — the client's launch is 
under embargo until the show. Do not include cost estimates.

Approval scope: Files only. Nothing goes to the client from Cowork — 
Tony reviews before anything leaves.
```
::::
:::::

**What Cowork does:** Reads the brief and discovery notes → extracts design intent → checks it against the venue constraints from the site survey → produces the spec document flagging where the brief is silent (which is exactly where engineering will push back) → builds the concept deck on the client template using brand guideline colors and typography → saves both.

**Where it pauses:** File creation only. Notice the constraint doing real work: the embargo instruction is the difference between a deck that's safe to circulate internally and a deck that could genuinely damage a client relationship.

**What comes back:** A spec doc with an explicit list of unresolved engineering questions, and a concept deck at roughly the 80% mark — which is the right handoff point. The design judgment, the story arc, and the moment that makes the client lean forward are still yours.

---

### Scenario 5 — Organizer RFP response

**Persona:** Exhibition Sales Director
**Trigger:** A major association has issued an RFP for GSC services for its annual convention. Response due in nine days. It's 40 pages of requirements.

:::::{tab-set}
::::{tab-item} ❌ Under-scoped
```
Write our response to this RFP.
```
::::
::::{tab-item} ✅ Five-part
```
Outcome: A complete first-draft response to the [Association] GSC 
RFP that our proposal team can edit rather than write.

Inputs: The RFP PDF I've attached; our three most recent winning GSC 
proposals in the Proposals library; the GES capability boilerplate 
library; the ESG and Net Zero roadmap materials; and the case study 
folder for association conventions of similar size.

Definition of done: (1) A Word response document structured section 
by section in the RFP's own order, with every requirement addressed 
and cross-referenced to the RFP section number. (2) An Excel 
compliance matrix listing every stated requirement, our response 
status, and the owner who needs to confirm it. (3) A short internal 
memo listing the five weakest sections and what evidence we'd need 
to strengthen them. All saved to the [Association] RFP folder.

Constraints: Do not invent any metric, client name, or case study — 
if the source material doesn't support a claim, write "[EVIDENCE 
NEEDED]" and move on. Do not commit to any pricing. Use the 
organizer's own terminology from the RFP, not our internal terms.

Approval scope: Files only. Nothing external.
```
::::
:::::

**What Cowork does:** Parses the RFP into a structured requirement list → searches the proposals library for the strongest matching language → drafts each section in RFP order → builds the compliance matrix → runs a self-critique pass to identify weak sections → produces the internal memo.

**Where it pauses:** File creation. The `[EVIDENCE NEEDED]` constraint is the most important line in the prompt — it converts hallucination risk into a visible to-do list.

**What comes back:** Nine days of proposal work reduced to about two, plus a compliance matrix that stops the classic failure mode of an RFP response that reads beautifully and misses requirement 4.7.3.

---

### Scenario 6 — Stalled pipeline review and QBR prep

**Persona:** Account Director, Exhibition Sales
**Trigger:** Quarter end is three weeks out. Your QBR is next Tuesday. You know some opportunities have gone quiet but you don't know which or why.

:::::{tab-set}
::::{tab-item} ❌ Under-scoped
```
Which of my deals are stalled?
```
::::
::::{tab-item} ✅ Five-part
```
Outcome: A ranked view of my at-risk opportunities with the specific 
follow-up that went cold on each, plus a QBR deck built on that 
analysis.

Inputs: My Outlook mail and calendar for the last 120 days; the 
account files in my Accounts SharePoint folder; the opportunity 
tracker workbook; and the last two QBR decks.

Definition of done: (1) An Excel workbook ranking open opportunities 
by risk, with columns for last meaningful contact, days since, the 
specific commitment or follow-up that lapsed, and the recommended 
next action. (2) A QBR PowerPoint on our standard template covering 
quarter performance, at-risk opportunities, and the recovery plan. 
(3) Draft follow-up emails for the top five at-risk accounts — 
drafts only, in my Drafts folder.

Constraints: "Stalled" means no substantive two-way exchange in 21 
days — a newsletter or an out-of-office does not count as contact. 
Do not send anything. Do not include any account where the client 
has explicitly told us they've gone to a competitor; list those 
separately.

Approval scope: Ask before creating anything in my Drafts folder. 
Never send.
```
::::
:::::

**What comes back:** This is the direct GES analogue of one of Microsoft's own reported customer outcomes — a sales lead who pointed Cowork at a stalled pipeline and got back a ranked list of at-risk opportunities with the exact follow-up that had gone cold on each, collapsing a week of manual review into a single morning.

The value is not the ranking. It is the "specific commitment that lapsed" column. *You told the organizer you'd send the sustainability case study on May 3. You never did.* Nobody's CRM captures that. Your email does.

---

### Scenario 7 — Drayage and material handling cost analysis across shows

**Persona:** Logistics Manager
**Trigger:** Three organizers in the same vertical have separately asked why material handling costs rose year over year. You suspect the answer differs by venue but you've never had time to prove it.

:::::{tab-set}
::::{tab-item} ❌ Under-scoped
```
Analyze our drayage costs.
```
::::
::::{tab-item} ✅ Five-part
```
Outcome: An analysis of material handling and drayage cost variance 
across our shows at the four venues in the [Vertical] portfolio over 
the last 18 months, with the drivers identified.

Inputs: The freight and material handling workbooks in the Logistics 
SharePoint library for shows 4180 through 5210; the freight target 
agreements for each show; and the advance warehouse receiving logs.

Definition of done: (1) An Excel workbook with a tab per venue plus 
a consolidated comparison — cost per hundredweight, percentage of 
freight arriving in the advance warehouse window vs. direct-to-show, 
and freight target compliance rate. (2) A Word analysis of the top 
three cost drivers with evidence for each. (3) A six-slide deck I 
can use in an organizer conversation.

Constraints: Normalize for show size using net square footage — 
absolute cost comparisons across shows of different sizes are 
meaningless. Exclude the two shows with incomplete manifest data 
and note the exclusion. Do not include any organizer's rates in a 
deliverable that another organizer will see — build the deck with 
indexed figures, not absolute rates.

Approval scope: Files only.
```
::::
:::::

**What Cowork does:** Opens each show's freight workbook → normalizes by net square footage → computes cost per hundredweight and freight target compliance by venue → cross-references advance warehouse receiving logs to establish what proportion of freight arrived in-window → identifies correlation between direct-to-show percentage and cost → writes the analysis → builds the indexed deck.

**Where it pauses:** File creation. That confidentiality constraint — indexed figures rather than absolute rates — is a GES-specific instruction that Cowork would never infer on its own. This is exactly what the Constraints line exists for.

**What comes back:** The analysis nobody had time to run, with the answer to a question three clients asked. This is a heavy task. It is unambiguously worth the credits.

---

### Scenario 8 — Exhibitor service kit refresh and question triage

**Persona:** Exhibitor Services Manager
**Trigger:** Two things at once. The service kit for next season needs updating across 40 pages of deadlines, rates, and venue rules. And your shared inbox is taking 200+ exhibitor questions a day during move-in.

**Task A — the service kit:**

```
Outcome: An updated exhibitor service kit for Show 5108 reflecting 
the new venue rules, the FY27 rate card, and the revised advance 
warehouse deadlines.

Inputs: Last year's Show 5108 service kit PDF; the FY27 rate card; 
the venue's updated exhibitor rules document; and the current show 
schedule with the advance warehouse and direct-to-show dates.

Definition of done: An updated Word document saved to the Show 5108 
library, plus a one-page change summary listing every change made 
and its source.

Constraints: Do not change any section where the source documents 
don't show a change — preserve existing wording exactly. Every 
deadline date must trace to the show schedule; flag any date you 
cannot verify rather than carrying it forward.

Approval scope: Files only.
```

The change summary is the whole point. It turns an unreviewable 40-page diff into a one-page review.

**Task B — the question triage (an event-driven, scheduled pattern):**

```
Outcome: A daily triage of the Show 5108 exhibitor services inbox 
so my team starts each morning with a prioritized queue instead 
of an undifferentiated pile.

Inputs: The Show 5108 shared exhibitor services mailbox, previous 
24 hours.

Definition of done: A Teams post to the Exhibitor Services channel 
each morning at 6:30 a.m. show-local time, grouping questions into: 
(1) deadline-critical — anything about move-in times, freight 
targets, or advance warehouse cutoffs; (2) orders and billing; 
(3) venue and rules; (4) answerable from the service kit — with 
the relevant kit section cited. Include a count per category and 
name the five most urgent.

Constraints: Do not reply to any exhibitor. Categorize only. 
Do not include exhibitor contact details in the Teams post.

Approval scope: Ask before the first post. Then only to the 
Exhibitor Services channel for the rest of the show.
```

Note the approval scoping in the last line — this is precisely what the **More options → Only to** feature is for. You approve once, scope it to one internal channel, and stop being interrupted, while everything external still stops for review.

---

### Scenario 9 — onPeak hotel block pickup analysis, and the ESG compilation

**Persona A:** onPeak Housing Manager
**Trigger:** Room block pickup for a convention is at 61% with six weeks to cutoff. The organizer wants to know whether to release rooms.

```
Outcome: A hotel block pickup analysis for [Convention] with a 
recommendation on whether and how much to release, in a format 
I can send to the organizer.

Inputs: The pickup reports in the onPeak reporting library for this 
convention for the last three years; the current block contracts 
with attrition terms; and the current-year pickup data by property 
and rate tier.

Definition of done: (1) An Excel workbook comparing this year's 
pickup curve against the prior three years at the equivalent 
weeks-to-cutoff, by property and rate tier. (2) A two-page Word 
recommendation with the attrition exposure quantified per property. 
(3) A draft email to the organizer.

Constraints: Compare at equivalent weeks-to-cutoff, not calendar 
dates — the show moved two weeks later this year. Quantify attrition 
exposure using the actual contract terms per property, not a blended 
assumption. Do not recommend releasing rooms at any property where 
the attrition clause makes release more expensive than holding.

Approval scope: Ask before the organizer email. Files freely.
```

**Persona B:** Corporate Sustainability / ESG Reporting Lead
**Trigger:** The annual ESG report and the EMEA Roadmap to Net Zero need current-period emissions data compiled from facilities, freight, and event-level sources across regions.

```
Outcome: A compiled emissions dataset and draft narrative section 
for the FY27 ESG report covering our reporting scope.

Inputs: The facility utility data workbooks for all 24 production 
and warehouse facilities; the freight and transport data in the 
Logistics library; the event-level emissions reporting from the 
EMEA program; and last year's published ESG report for structure 
and methodology continuity.

Definition of done: (1) An Excel workbook with a tab per data source 
and a consolidated summary using last year's methodology and units. 
(2) A Word draft of the emissions narrative section. (3) A data 
quality memo listing every gap, inconsistency, and unit mismatch 
found.

Constraints: Use exactly the same methodology and boundary 
definitions as last year's published report — flag any place where 
this year's source data doesn't support that methodology rather 
than substituting an alternative. Never estimate a missing figure; 
mark it as a gap.

Approval scope: Files only. Nothing leaves this session.
```

:::{important}
**The data quality memo is the real deliverable**

In both of these — and in most analytical Cowork tasks at GES — the artifact that changes your week is not the polished output. It's the honest list of what's missing, inconsistent, or unverifiable.

Always ask for it. A constraint like *"never estimate a missing figure; mark it as a gap"* is the difference between a report you can defend and a report that looks complete because the software filled in the holes.
:::

---

## 11. Microsoft's Customer Proof Points, in GES Terms

Three reported outcomes from Microsoft's own customers translate directly.

```{list-table} What other companies did — and the GES equivalent
:header-rows: 1
:name: table-ch14-proof-points

* - What Microsoft reports
  - The GES analogue
* - A team compared nearly **4,000 files** across two product versions — work that would have taken weeks
  - Compare this year's exhibitor service kits, venue rule sets, and show operations manuals across an entire portfolio of shows to find every place a deadline, rate, or venue rule changed. Nobody does this today because nobody has weeks. It is a single Cowork task.
* - A sales lead pointed Cowork at a **stalled pipeline** and got a ranked list of at-risk opportunities with the exact follow-up that had gone cold on each — a week of review collapsed into one morning
  - Scenario 6 above. Directly transferable to exhibition sales and to agency account management, where the lapsed commitment is usually buried in an email thread rather than a CRM field.
* - An engineering team taught Cowork to safely **edit batch-job spreadsheets and generate dependency flow charts** after every change — automating work that previously required careful manual intervention
  - The labor forecast and freight manifest workbooks that get edited by five people across a show cycle. Teach Cowork the safe-edit rules and have it regenerate the dependency view — which crews depend on which freight arriving in which window — after every change. This is where a **custom skill** earns its slot.
```

---

## 12. Why Cowork Fits GES Specifically

There is a reason this chapter exists in a GES book rather than being a generic Cowork overview.

Most software productivity features assume a knowledge worker at a desk with a laptop open. That describes a minority of GES.

GES runs **4,000+ live experiences a year**, serves **150,000+ exhibitors**, operates in **75+ countries**, and runs **24 global production and warehouse facilities** with roughly **2,600 people**. The work happens on show floors, in marshaling yards, on warehouse docks, in venues at 5 a.m., and in airports between cities. The people who most need analytical and documentation work done are frequently the people least able to sit still and do it.

The property that makes Cowork disproportionately valuable here is the least glamorous one on the feature list: **tasks keep running when your laptop is off.**

Think about what that actually unlocks:

- A show manager delegates the reconciliation package at 5 p.m. during move-out, reviews it on their phone during a layover, and approves the organizer email from the gate.
- An EMEA account lead starts a deep research task on a prospective organizer at the end of the London day; a Las Vegas colleague picks up the finished memo at the start of theirs.
- A logistics manager kicks off a cross-venue drayage analysis before walking the floor and reads the result over lunch.
- A Spiro designer sets a spec document running before a client call and comes back to a draft with the engineering questions already flagged.

The quote from the top of this chapter is the mindset in one line: *"It is easy to have a dozen tasks in flight at once, each one moving forward while you focus on what only you can do."*

For a company where the thing only you can do is often *physically stand in a hall and make a judgment call*, that sentence is not a productivity slogan. It is a description of how the job could work.

:::{note}
**The multi-timezone dividend**

GES already runs across Las Vegas, Chicago, Toronto, London, Paris, Amsterdam, Dubai, and India. Cloud-hosted tasks that persist across devices and sessions turn timezone spread from a coordination cost into a relay. Work started at the end of one region's day is finished and reviewable at the start of another's — without anyone staying late.
:::

---

## 13. Cautions — What Cowork Does Not Change

Everything above is genuine capability. This section is the counterweight, and it is not optional reading.

### 13.1 Cowork does not transfer accountability

This is the most important sentence in the chapter.

If Cowork drafts a number and you approve the email, it is your number. If Cowork produces a reconciliation and the organizer builds a board slide on it, that reconciliation is GES's work product. If Cowork writes a spec and engineering builds to it, the spec is the designer's.

There is no arrangement in which "Copilot generated it" is an acceptable answer to a client. **Responsibility** in T.R.U.E. means being responsible for our actions and delivering on our commitments. A delegated action is still your action.

### 13.2 Review before approving — properly

Skimming a preview is not reviewing it. A real review checks, in this order:

1. **Recipients.** Who is on this? Is anyone on it who shouldn't be? Is this the client's whole distribution list or just my contact?
2. **Numbers.** Spot-check at least two figures against the source. If they're right, the method is probably right. If either is wrong, stop and re-scope.
3. **Claims.** Does anything assert something GES has not verified? Any commitment on timing, cost, or capability that hasn't been approved?
4. **Confidentiality.** Is there anything in here that belongs to a different client, a different show, or a different internal audience?
5. **Tone.** Does this sound like GES — warm, precise, partnership-focused — or does it sound like software?

### 13.3 Oversharing risk

Cowork can search everything you have permission to see. That's the feature. It is also the risk.

If you have broad access — many account directors and operations leaders do — a loosely scoped research task can pull material from one client's show into a deliverable intended for another. Cowork is not doing anything wrong; it is doing what you asked, with the access you have.

The mitigation is entirely in your hands, and it's the **Inputs** and **Constraints** lines of the five-part prompt:

- Name the specific libraries, folders, and date ranges. Don't say "search our files."
- State confidentiality boundaries explicitly. *"Only use material from the Show 5108 library."* *"Do not reference any other organizer's rates."*
- When in doubt, run the task with narrow inputs and widen it if the result is thin. Widening is cheap. Un-sending is impossible.

:::{warning}
**Client confidentiality at GES is not an abstraction**

GES routinely sees things before the world does: competitor booth plans sitting side by side in the same production schedule, unannounced product launches in Spiro design files, an organizer's attendance figures, an exhibitor's spend relative to their competitor across the aisle.

Two direct competitors in the same industry are frequently both GES clients at the same show. Our access to both is precisely why they trust us — and precisely why a carelessly-scoped Cowork task is a serious matter, not a minor error.

Before you run any task that touches client material, ask one question: *if this output were forwarded to the wrong client, what would be in it?* Then scope so the answer is "nothing."
:::

### 13.4 Cowork is confident about things it should be uncertain about

Like every model-driven system, Cowork produces fluent output regardless of whether the underlying source material supported it. The countermeasure is structural, not vigilance-based — build it into the prompt:

- *"Flag anything you cannot verify rather than carrying it forward."*
- *"Write [EVIDENCE NEEDED] rather than inventing a figure."*
- *"Separate observed facts from inferences under a clearly labeled heading."*
- *"Never estimate a missing figure; mark it as a gap."*

Every one of those lines appeared in a scenario above. They are not decoration. They are the difference between a deliverable you can defend and one you can't.

### 13.5 Some things should not be delegated at all

An apology to a client whose booth went up wrong. A conversation with a crew member about a safety incident. A negotiation with a union steward. The moment when an organizer needs to hear a human voice take responsibility.

**Understanding** — people come first — is the value that draws this line. Cowork can prepare you for those conversations. It should never have them for you.

---

## 14. Getting Started — Your First Week with Cowork

### 14.1 Where to find it

```{list-table} How to access Copilot Cowork
:header-rows: 1
:name: table-ch14-access

* - Surface
  - Where
* - **Browser**
  - **m365.cloud.microsoft** — the same front door as the rest of Microsoft 365 Copilot
* - **Desktop / Mobile**
  - The Microsoft 365 Copilot app. The mobile app matters more at GES than at most companies — it's how you delegate from a show floor
* - **Outlook and Teams**
  - Via the **toggle next to Chat**. Some versions surface it in the left navigation rail or under "All agents"
```

### 14.2 Admin enablement

Cowork is enabled by administrators in the **Microsoft 365 admin center**. If you don't see the toggle next to Chat, that is the first thing to check — it is an enablement question, not a licensing mystery. Admins also control which **plugins** are deployed org-wide, which is the right control point for anything that connects to an external data source or a system of record.

Two prerequisites, in order: the **Microsoft 365 Copilot USL**, then Cowork enablement plus a **Copilot Credits** allocation.

### 14.3 Three starter tasks for your first week

Do these in order. They're deliberately sequenced from low stakes to real work.

::::{tab-set}
:::{tab-item} Day 1 — Organize your week
```
Outcome: My calendar for next week organized so I have two 
protected two-hour blocks for focused work.

Inputs: My Outlook calendar for next week.

Definition of done: Focus blocks added; conflicts flagged in a 
summary message to me.

Constraints: Do not decline or move anything — just propose 
changes and tell me. Never touch anything with an external 
attendee.

Approval scope: Ask before any calendar change at all.
```
**Why this one first:** zero external risk, immediate visible value, and you get to see the approval dialog in a situation where mistakes cost nothing. Pay attention to the previews — that's the real lesson.
:::
:::{tab-item} Day 2–3 — Catch up on a show
```
Outcome: A one-page catch-up on everything that's happened on 
Show [X] in the last two weeks.

Inputs: My email and Teams messages related to Show [X], and 
the Show [X] SharePoint library, last 14 days only.

Definition of done: A Word document saved to my OneDrive, 
organized by: decisions made, open issues, deadlines in the 
next 21 days, and anything waiting on me.

Constraints: Only the last 14 days. Cite the source message 
or file for every item so I can go check it.

Approval scope: Files only. Do not send or post anything.
```
**Why this one second:** it teaches you Work IQ grounding and the discipline of citing sources — and the "waiting on me" section is usually a genuinely uncomfortable surprise.
:::
:::{tab-item} Day 4–5 — Produce a real artifact
Pick the scenario from §10 closest to your role. Write the five-part prompt yourself. Run it. Review it properly using the five-step review in §13.2.

**Why this one last:** by now you understand approvals, grounding, and scoping. This is where you find out what Cowork is actually worth in your job — and the honest answer will be specific to you.

Then do the one thing that compounds: **save the prompt.** Put it in your team's SharePoint prompt library with a note on what you'd change next time.
:::
::::

:::{tip}
**The first-week habit that predicts success**

The people who get the most out of Cowork in month one are not the ones who run the most tasks. They're the ones who, after each task, spend two minutes writing down *what they'd change in the prompt*.

Cowork rewards scoping skill more than any Copilot surface before it. Scoping skill is built by iteration, and iteration only compounds if you write it down.
:::

---

## 15. Try This: Convert Your Worst Recurring Task

Pick the task you dread most in your show cycle. The one that always slips. The one you do at 10 p.m. the night before it's due.

Now write it as a five-part Cowork prompt. Be specific enough that a competent colleague who has never done your job could produce the right thing from your description alone.

Then answer three questions:

1. **Which part was hardest to write?** For most people it's *Definition of done* — because we do these tasks by habit and have never articulated what "finished" means. That's a useful thing to learn about your own work regardless of AI.
2. **What constraint did you almost forget?** There's usually a confidentiality or template constraint that's so obvious to you it never got said out loud. Those are the ones that cause problems.
3. **What's your approval scope?** If the honest answer is "I want to check everything," that's fine for task one. Notice how it changes by task ten.

---

## 16. Productive Struggle Problem

You are the GES account director for a major association client. Their annual convention closed nine days ago. Three things land in the same hour on a Tuesday morning:

- The organizer emails asking why material handling costs were 14% over the estimate, and requests an explanation "with data" by Thursday.
- Your VP asks for a QBR-ready view of the account, including renewal risk, by Friday.
- An exhibitor at that show has escalated a claim that their freight was misrouted through the marshaling yard, costing them a full day of install. Legal wants a factual timeline.

You have two days of actual working time, and you're travelling on Wednesday.

**The challenge:** design your Cowork approach.

- Decide which of the three is a Cowork task, which is a Chat task, and which should not be delegated at all — and justify each choice using the decision rule from §1.
- Write the full five-part prompt for each task you'd delegate.
- Specify your approval scope for each and explain what you'd refuse to let Cowork do.
- Identify one confidentiality constraint that must appear in each prompt, given that the exhibitor claim may become a legal matter and the organizer is asking about costs that involve third-party carriers.
- Estimate whether each task is light, medium, or heavy, and say whether the credits are justified.

There is no single right answer. The quality of your reasoning about *what you refused to delegate* matters more than the prompts themselves.

---

## Glossary

```{glossary}
Copilot Cowork
  The Microsoft 365 Copilot capability, generally available June 16, 2026, that executes complex, long-running, multi-step tasks across apps and returns finished artifacts rather than drafts or recommendations.

Copilot Credits
  The usage-based billing unit for Cowork. Consumption is driven by four inputs: model use, context retrieval, tool calls, and runtime.

Microsoft 365 Copilot USL
  The User Subscription License that is a prerequisite for Cowork. Separately includes Copilot Chat, Copilot in the Office apps, Work IQ, multi-model intelligence, pre-built agents (Researcher, Analyst), and Agent Builder.

Work IQ
  The context engine that grounds Copilot in an organization's actual systems — email, files, meetings, chats, and sites — subject to the signed-in user's permissions.

Five-Part Prompt Structure
  Microsoft's official guidance for scoping a Cowork task: Outcome, Inputs, Definition of done, Constraints, and Approval scope.

Approval Scope
  The fifth part of a Cowork prompt — an explicit statement of which actions you want to review, beyond Cowork's default checkpoints.

Approve All
  An approval option that clears all pending approvals at once, displaying the count (e.g. Approve All (3)). Should not be used on any batch containing an externally-facing action.

Risk Level Indicator
  A signal shown on medium and high risk actions in the approval dialog, alerting the user to actions with greater consequence.

Scheduled Prompt
  A Cowork prompt configured to run automatically on a recurring schedule.

Event-Driven Task
  A Cowork task configured to run when a defined event occurs, such as an email arriving or a Teams message posting.

Custom Skill
  A user- or organization-defined Cowork skill. Up to 50 can be created; Cowork discovers them automatically at the start of each session.

Plugin
  An add-on from the Microsoft 365 App Store that extends Cowork with new skills, specialized expertise, or external data connections. Can be deployed org-wide by admins.

Sandboxed Cloud Environment
  The protected, isolated cloud environment in which Cowork tasks execute — the reason tasks continue running when a user's device is off and the reason files are not stored locally.

Light / Medium / Heavy Task
  Microsoft's three observed Cowork task patterns, distinguished by number of knowledge sources, depth of reasoning, and number of outputs.

Drayage
  The movement of exhibitor freight from the dock or advance warehouse to the booth space on the show floor, and back out at move-out. A core material handling service and cost line.

Material Handling
  The receiving, transporting, storing, and returning of exhibitor freight at a show. Billed by weight, typically per hundredweight.

Freight Target
  An agreed target date and time window for freight arrival, used to sequence move-in and manage marshaling yard capacity.

Advance Warehouse
  A facility that receives exhibitor freight ahead of a show, allowing material to be staged and delivered to the show floor on a controlled schedule.

Marshaling Yard
  The staging area where carriers check in and are sequenced for dock access during move-in and move-out.

GSC (General Service Contractor)
  The official on-site service provider appointed by a show organizer, responsible for services including decorating, material handling, labor, and floor plan execution.

EAC (Exhibitor Appointed Contractor)
  A contractor engaged directly by an exhibitor rather than appointed by the organizer. Spiro operates in this capacity for custom exhibit work.

I&D (Install & Dismantle)
  The labor and process of building and taking down exhibits on the show floor.

Exhibitor Service Kit
  The document issued to exhibitors containing deadlines, rates, venue rules, order forms, and logistics information for a specific show.

Union Jurisdiction
  The rules governing which trades may perform which work at a given venue. Determines how crews must be scheduled and cannot be worked around.

Carnet
  An international customs document allowing temporary duty-free import of exhibit materials into a foreign country.
```

---

## Discussion

Cowork changes what "doing the work" means. When the production of an artifact is delegated, the professional value shifts from the production to two things: the quality of the brief at the front, and the rigor of the review at the back.

Consider your own role at GES. Which parts of your work are genuinely craft — where your judgment, relationship knowledge, or on-the-ground read is the value — and which parts are assembly, where you are moving information between systems and formats because nobody else will?

Then consider the harder question: if the assembly work were delegated, would you actually use the recovered time on the craft work? Or would it fill with more assembly?

::::{admonition} 📝 Discussion Guidelines
:class: note

Post your reflection in the course discussion forum before the next session. Your response should:

- Identify one specific recurring task in your role that you would delegate to Cowork, and write out its five-part prompt in full — Outcome, Inputs, Definition of done, Constraints, Approval scope.
- Identify one task in your role that you would **refuse** to delegate, and explain which of the T.R.U.E. values drives that refusal.
- Address the approval question directly: what is your personal rule for when you would and would not use Approve All, and why?
- Respond to at least **two peers** with substantive engagement — challenge a scoping decision, point out a confidentiality constraint they missed, or push back on something they chose to delegate.
- Reference at least one credible source — Microsoft's Cowork documentation, GES's own T.R.U.E. values framework, or research on human oversight of automated systems.

Minimum 300 words for your main post.
::::

---

## Leader's Takeaway

Every previous chapter in this book made your people faster at work they were already doing. This one changes what they do.

That is a bigger deal than a feature release, and it should be managed like one. Three things determine whether Cowork becomes an operational advantage at GES or an expensive experiment.

**First: scoping is the skill, and it has to be taught.** The five-part structure — Outcome, Inputs, Definition of done, Constraints, Approval scope — is not a nice-to-have. It is the difference between a deliverable your team ships and a generic document they quietly throw away. It is also, not incidentally, the primary cost-control lever. Teach it explicitly, build a shared prompt library, and treat a well-scoped prompt as the reusable asset it is.

**Second: the approval habit is a culture question, not a training question.** Somebody on your team will hit **Approve All** on a batch containing a client email. The only reliable defense is a culture where reviewing a preview properly is understood as professional behavior rather than friction — the same way checking a booth before the exhibitor walks in is understood as professional behavior. **Trust** means verify before you approve. **Responsibility** means you own every output that carries your name. Say both out loud, repeatedly, until they're reflex.

**Third: the value is in the work nobody currently has time for.** The temptation is to use Cowork on the tasks you already do, and there's real value there. But the larger return sits in the analyses that get skipped every busy season — the cross-show cost patterns, the venue history that lives in three people's memories, the service kit comparison nobody has weeks for. Those are the tasks where Cowork doesn't make an existing process faster; it makes a previously impossible process routine.

GES has just spent its first period as an independent company under Truelink, setting its own technology roadmap for the first time in 55 years. onPeak already shipped an AI Smart Suite. Visit by GES already ships intelligent hardware. The organization has proven it can build AI into products.

Cowork is the same capability turned inward — on the operational work of running 4,000 events a year with lean teams and immovable show dates.

The tool will keep improving. Cowork 1 is coming. More models will follow. What will not change is the underlying professional shift: from doing the work, to briefing the work and standing behind the result.

That has always been what excellent leadership looks like on a show floor. Now it's what excellent individual work looks like too.
