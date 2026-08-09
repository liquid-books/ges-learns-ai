# Microsoft Copilot Cowork — Research Reference
*Internal source of truth for Chapter 14. Not published.*

## Timeline
- **March 9, 2026** — Announced/preview inside Microsoft's "Frontier" early-access program
- **June 16, 2026** — **Generally Available worldwide**
- Fastest-growing feature in the history of the Frontier program
- Highest user satisfaction of any Copilot or agent experience Microsoft has shipped
- **Adoption at GA:** more than half of the Fortune 500. Named customers: Accenture, Avanade, Advance Local, Capital Group, Koch, LTM, Ooredoo Qatar, Zurich Insurance

## What It Is (one-sentence)
Cowork executes complex, long-running, multi-tool tasks end-to-end across Microsoft 365 and returns **finished artifacts** — a deck, report, email, or update — not a draft or a recommendation.

## The Core Distinction (critical teaching point)

| Tool | Use When |
|---|---|
| **Copilot Chat** | Quick answers and back-and-forth in the flow of your work |
| **A specialized agent** | A narrow, repeatable task needs automating |
| **Cowork** | Work spans multiple steps and apps — drafting, planning, coordinating, producing finished artifacts you can review and ship |

## Five Differentiators (Microsoft's own framing)
1. **Cloud hosting** — files aren't stored locally, security strongly enforced, and **tasks keep running even when your laptop is off**
2. **Native Work IQ support** — grounds every task in the systems your business already runs on
3. **Enterprise-grade security and compliance** — operates within your Microsoft 365 trust boundary
4. **Multi-model design** — run the model a task needs; capability scales as more models become available
5. **Lower cost** — efficient runtime, model choice matched to task, billing only for what you use

## Models
- At GA, runs on **Anthropic models: Opus 4.8 and Sonnet 4.6**
- **Cowork 1** — Microsoft's own secure, fine-tuned model, post-trained for substantially lower cost, releasing shortly after GA
- Not locked into one model — use the most efficient or the frontier model

## Pricing / Economics (important for adoption + governance)
- Requires the **Microsoft 365 Copilot User Subscription License (USL)** as a prerequisite
- Cowork itself is **usage-based billing**, denominated in **Copilot Credits**
- Price per task calculated from **four inputs**: model use, context retrieval, tool calls, runtime
- **Three task patterns** observed:
  - **Light** — small number of knowledge sources, limited reasoning, one or fewer outputs
  - **Medium** — multiple sources, structured reasoning, two or more outputs
  - **Heavy** — aggregates broadly, deep reasoning, many outputs
- Microsoft identified **four user personas** with distinct usage patterns
- Cost model = (users per segment) × (expected prompt volume across light/medium/heavy) × (cost per prompt type), summed
- Microsoft offers a customer estimator spreadsheet: aka.ms/CustomerCoworkEstimator (estimates assume Anthropic Opus 4.8)
- Microsoft's testing claims Copilot Cowork averaged **30–40% cheaper per prompt** than Claude Cowork with its Microsoft 365 connector

The M365 Copilot USL separately includes: Copilot Chat; Copilot in Word, Excel, PowerPoint, Outlook, Teams; the Work IQ context engine; multi-model frontier intelligence; pre-built agents (Researcher, Analyst); and custom agents via Agent Builder.

## What Cowork Can Do

**Communication**
- Draft and send emails through Outlook (drafts, replies, forwards)
- Post updates in Teams channels; send DMs in 1:1 or group chats
- Create and send HTML newsletters via email
- Manage inbox — sort into folders, delete, respond inline
- Prepare stakeholder communications: status updates, announcements, follow-ups

**Documents and files**
- Create Word docs, Excel spreadsheets, PowerPoint decks, and PDFs from scratch
- Edit and refine existing documents shared in session
- Browse entire Work IQ to pull in needed content
- Create SharePoint and OneDrive folders
- Reorganize existing files into new or existing folders

**Calendar and meetings**
- Schedule meetings with natural language
- Manage calendar — add events, move things, clean up conflicts, decline with a reason message to the organizer
- Meeting intelligence and prep insights
- Daily briefing highlighting what's ahead

**Research and search**
- Search across the organization for documents, messages, information
- Deep research synthesizing multiple sources into comprehensive reports
- Browse SharePoint/OneDrive folders and select files

**Automation**
- **Scheduled prompts** — run prompts on a schedule so recurring tasks happen automatically
- **Event-driven tasks** — run when something happens (an email arrives, a Teams message posts)

## Skills System
Cowork loads specialized **skills** as it works; active skills appear in the side panel.

**Built-in skills:** Word, Excel, PowerPoint, PDF, Email, Scheduling, Calendar Management, Meetings, Daily Briefing, Enterprise Search, Communications, Deep Research, Adaptive Cards

**Custom skills:** you can create up to **50**. Cowork discovers them automatically at the start of each session.

**Plugins:** supported from the Microsoft 365 App Store — add new skills and connectors, give Cowork specialized expertise (financial analysis, legal research) or connect external data sources. Admins can deploy plugins org-wide.

## How a Session Works
1. **Describe your task** — describe an *outcome*, not a process. Can attach files by dragging into chat.
2. **Watch Cowork work** — breaks the request into steps, works through one by one, visible in session
3. **Interrupt, steer, or pause** at any point to add context or clarify
4. **Approve actions when asked** — pauses before important actions
5. **Review the results** — download documents, check sent messages, request changes

## Session Interface Details
- Chat input accepts up to **250,000 characters**
- Suggested prompts on home page: *Catch me up, Organize my inbox, Organize my week, Prep for a meeting, Plan an event, Prepare for my 1:1, Research a company*
- Recent tasks listed on home page — resume any previous session
- **Attachments:** drag and drop; "Add work context" (files, people, emails, Teams chats/channels/meetings); upload from device; attach cloud files from OneDrive/SharePoint/Teams
- **Voice input** — microphone button, speech-to-text dictation
- While working: thinking indicator, step-by-step updates ("Composing your email", "Searching OneDrive"), streaming response word-by-word, interactive cards
- Connection status indicator: Connecting / Connected / Reconnecting / Failed (with Retry)
- **Queued messages** — you can send another message while Cowork is busy; processed in order; Cowork adjusts direction if needed
- Cowork asks clarifying questions with multiple-choice options; you can **Skip**

## Approvals & Control (the governance heart of the feature)
Cowork asks permission before sensitive actions — sending email, posting in Teams, updating a record.

| Option | What it does |
|---|---|
| Action button (**Send** / **Post** / **Create**) | Proceed with the action this one time |
| **More options** dropdown | Approve and skip prompts for similar actions for the rest of the session. For email/Teams you can scope it: **Only to** a specific recipient, **Only to** a domain's recipients, or **Always allow** for that session. Other actions get a single "Approve & don't ask again". |
| **Approve All** | Approve all pending approvals at once; button shows count, e.g. **Approve All (3)** |
| **Cancel** | Stop the action; Cowork skips it and continues with the rest of the request |

- Rich previews shown for many actions (draft email, Teams message, scheduled meeting); summaries for others
- **Risk level indicator** for medium and high risk actions
- Microsoft's own guidance: *always review details before approving — check recipients, content, and other details*
- **Every task runs with your permissions and sees only what you can see**
- Data stays in your tenant; respects existing user and admin permissions
- **Cowork actions are auditable**
- People remain responsible for business decisions

## Access & Deployment
- Admins enable Cowork in the **Microsoft 365 admin center**
- Users launch from the Copilot app on **web, desktop, or mobile**
- Locations: **m365.cloud.microsoft** (browser), Microsoft 365 Copilot desktop/mobile app, or in **Outlook and Teams** via the toggle next to Chat. Some versions show it in the left navigation rail or under "All agents".

## Real Customer Examples (from Microsoft)
- An engineering team taught Cowork to safely edit batch-job spreadsheets and generate dependency flow charts after every change — automating work that previously required careful manual intervention
- A team compared nearly **4,000 files** across two product versions — work that would have taken weeks
- A sales lead pointed Cowork at a stalled pipeline and got back a ranked list of at-risk opportunities with the exact follow-up that had gone cold on each — collapsing a week of manual review into a single morning

## Key Teaching Angle for GES
The prompt-craft skill of Copilot Chat is *describing a task*. The skill of Cowork is **describing an outcome and then reviewing like a manager**. This is a genuine shift in professional behavior — from doing the work to delegating and quality-controlling the work. For a company running 4,000+ events a year across 75+ countries with lean teams and hard show dates, the "tasks keep running when your laptop is off" property is not a footnote — it's the whole point. A show manager on the floor in Las Vegas can delegate a post-show reconciliation package and review it between meetings.
