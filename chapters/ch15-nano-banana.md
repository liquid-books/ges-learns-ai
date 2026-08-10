---
title: "Chapter 15: Creative AI with Nano Banana"
subtitle: "Image Generation for Ideation — What It Can Do, What It Cannot, and Why the Boundary Matters"
short_title: "Creative AI with Nano Banana"
description: "Google's Nano Banana family of image generation models, accessed through Google AI Studio, offers GES creatives a powerful ideation tool for booth concept exploration, mood boards, pitch visuals, and rapid 'what if' iteration — while remaining firmly outside the production art pipeline and the Microsoft 365 trust boundary. This chapter covers capabilities, limitations, prompt discipline, and the confidentiality controls that matter most."
label: ch-15-nano-banana
tags: [Nano Banana, Gemini, image generation, AI art, creative ideation, Google AI Studio, booth design, exhibit design, Spiro, mood boards, pitch visuals, confidentiality, concept exploration, prompt engineering, visual AI]
---

```{admonition} Download this Chapter as PDF
:class: tip

[Download PDF](https://github.com/liquid-books/ges-learns-ai/raw/main/pdfs/ch15-nano-banana.pdf)
```

# Chapter 15: Creative AI with Nano Banana

:::{figure} ../images/ch15-nano-banana-infographic.png
:label: fig-ch15-infographic
:alt: Illustrated explainer infographic showing the Nano Banana creative workflow for GES — from text prompt to generated concept image, with labeled examples of booth concept exploration, mood board direction, and pitch visual generation, positioned firmly in the ideation phase before human designers take over for production
:width: 80%
:align: center

Nano Banana gives GES creatives a new tool for the earliest phase of design work — the "what if" exploration that happens before anyone commits to a direction. The output is never the deliverable. The output is how you find the deliverable faster.
:::

> *"The best way to have a good idea is to have lots of ideas."*
> — Linus Pauling

Here is a scene that plays out somewhere in GES every week.

A Spiro creative director is preparing for a pitch meeting in 48 hours. The client is a pharmaceutical company launching a new therapy at a major medical conference. They want an immersive booth experience that conveys "breakthrough innovation" without the cold clinical sterility that pharmaceutical booths often default to. The client has sent a brief with words like "warmth," "human connection," and "scientific precision" — concepts that mean different things to different people.

The creative director has three directions in mind. In the old workflow, she would sketch rough concepts, describe them in a deck, and hope the client can visualize what she means. In the new workflow, she opens Google AI Studio and types:

*"A pharmaceutical trade show booth, 40 by 40 feet, with warm wood accents and soft ambient lighting. The central feature is a curved LED wall showing abstract cellular imagery in soft blues and greens. Attendees are gathered in small consultation pods with fabric dividers. The overall feeling is welcoming and human, not sterile. No visible text, logos, or branding."*

Ninety seconds later, she has a visual. Not a finished design — she would never present this to a client as finished work — but a *direction*. A starting point for conversation. Something that answers "do you mean this, or something else?" before the design team commits forty hours to a concept the client did not actually want.

That is what Nano Banana is for. Concept exploration at the speed of conversation. Rapid visual iteration that compresses the early ambiguity phase of creative work. A tool that helps GES creatives arrive at the right direction faster, so they can spend their time on what only human designers can do: the final work that actually ships.

This chapter is for GES creatives — exhibit designers, environmental designers, graphics production teams, and the Spiro creative team. It covers what Nano Banana can do, what it cannot do, where it genuinely helps, and where it must not go. The distinction between ideation tooling and production art is not a footnote. It is the operating principle that makes this tool safe to use.

::::{admonition} 🧭 T.R.U.E. Check — Trust
:class: note

**Trust each other to always be honest and do what's right.**

Trust in creative AI means being honest about what the output is — and what it is not. A generated image is a concept exploration tool. It is never a client deliverable. It is never production art. When you present an AI-generated visual to a colleague or a client, you say so. Trust requires that everyone understands what they are looking at.
::::

---

## 1. What Is Nano Banana? The Three Model Tiers

"Nano Banana" is the internal nickname Google's developers gave to their image generation models — a playful name that stuck. The models are part of the Gemini family and are accessed through **Google AI Studio** at [aistudio.google.com](https://aistudio.google.com). You do not need to install anything. You do not need to be a developer. You need a Google account and a browser.

:::{figure} ../images/ch15-three-model-tiers.png
:label: fig-ch15-tiers
:alt: Three-tier comparison diagram showing the Nano Banana model family — Nano Banana (Gemini 2.5 Flash Image) on the left as the fast and economical option, Nano Banana 2 (Gemini 3.1 Flash Image) in the center as the faster successor, and Nano Banana Pro (Gemini 3 Pro Image) on the right as the highest quality option with best text rendering and reasoning
:width: 80%
:align: center

The Nano Banana family has three tiers — each with different tradeoffs between speed, cost, and quality. For GES creative work, the iteration workflow runs wide and cheap on the fast models, then re-renders only winners on Pro.
:::

**Nano Banana (Gemini 2.5 Flash Image)**

The original. Fast, economical, good for rapid iteration. At approximately $0.039 per generated image, you can explore dozens of directions without thinking about cost. Generation takes seconds, not minutes. This is your workhorse for the "let me try five different approaches" phase.

Strengths: Speed. Cost. Good enough quality for concept exploration. Strong at understanding scene composition and style direction.

Limitations: Text rendering is unreliable. Fine details can be inconsistent. Not suitable for images that will be shown to clients without heavy caveats about what they are seeing.

**Nano Banana 2 (Gemini 3.1 Flash Image)**

The faster successor. Released as an evolution of the original, with improved speed, better adherence to prompts, and more consistent character and object representation. Still economical, still fast, now with fewer quirks.

Strengths: Better consistency than the original. Improved prompt adherence. Good for iterating when you need more reliability.

Limitations: Still struggles with text rendering on anything beyond simple short labels. Still not production quality.

**Nano Banana Pro (Gemini 3 Pro Image)**

The flagship. Built on Gemini 3 Pro's reasoning capabilities, this model produces the highest-quality output with the best text rendering — around 94% accuracy on short text, according to Google's benchmarks. Supports 4K resolution output. Better at understanding complex scene descriptions with multiple elements.

Strengths: Highest visual quality. Best text rendering (though still not perfect). Strong reasoning about spatial relationships and composition. 4K output for high-resolution needs. Supports up to 14 reference images for character and style consistency.

Limitations: Slower than Flash models. More expensive (though still far cheaper than a photographer or a stock image license). Text rendering, while improved, still fails on long words or unusual terms.

**Which tier when?**

The iteration workflow that works for GES creative teams: generate wide and cheap on Nano Banana or Nano Banana 2, explore many directions, identify the winners, then re-render only the selected concepts on Pro for higher quality output. Do not start with Pro. Start with volume.

---

## 2. Where to Find It — Google AI Studio

:::{figure} ../images/ch15-ai-studio-interface.png
:label: fig-ch15-interface
:alt: Screenshot-style diagram of the Google AI Studio interface showing the prompt input area, model selection dropdown, and generated image output panel — with labels pointing to key interface elements for first-time users
:width: 80%
:align: center

Google AI Studio is a browser-based interface — no installation required. Select your model, type your prompt, and generate. The interface is intentionally simple; the complexity is in learning to prompt effectively.
:::

**Getting started:**

1. Go to [aistudio.google.com](https://aistudio.google.com)
2. Sign in with a Google account (personal or Google Workspace)
3. Click "Create new prompt" or use one of the template apps
4. Select the model from the dropdown (look for "gemini-2.5-flash-image" or "gemini-3-pro-image")
5. Type your prompt and click Generate

Google AI Studio includes "Build Mode" templates that let you try specific capabilities — character consistency, image editing, multi-image fusion — without starting from scratch. These are worth exploring when you are learning what the model can do.

**What it costs:**

As of this writing, Nano Banana (Gemini 2.5 Flash Image) is priced at approximately $0.039 per generated image. Nano Banana Pro is higher but still in the dollars-per-session range, not dollars-per-image-at-scale. Google offers a free tier with rate limits for experimentation.

For GES usage, the cost is negligible compared to the design time saved. A creative director exploring ten booth concepts costs less than a single cup of coffee.

---

## 3. What It Is For — Ideation, Not Production

This is the most important section in this chapter. Read it carefully.

:::{figure} ../images/ch15-ideation-vs-production.png
:label: fig-ch15-ideation-production
:alt: Two-column comparison diagram showing ideation uses on the left (booth concept exploration, mood boards, pitch visuals, client clarification, texture studies) with green checkmarks, versus production uses on the right (final client deliverables, print-ready graphics, fabrication specs, production art) with red X marks — the division between where Nano Banana helps and where it must not go
:width: 80%
:align: center

The bright line: Nano Banana is for everything to the left of the handoff to production. Human designers own everything to the right. A generated image never goes to a client as finished work or to a printer as production art.
:::

**Nano Banana is ideation tooling, not production art.**

That sentence is the operating principle. Let me unpack what it means in the GES context.

**Ideation** is the early, exploratory phase of creative work. It is the "what if we tried this direction?" phase. It is mood boards, concept sketches, look-and-feel exploration, rapid visual brainstorming. The goal of ideation is to find the right direction before committing significant design time. Nano Banana accelerates this phase dramatically.

**Production art** is the finished work. The graphics that go to the printer. The renderings that go into the client deck. The signage files that go to fabrication. The visual deliverables that carry the GES name. Human designers own production art. Always.

**Why the distinction matters:**

1. **Quality.** Nano Banana output is good enough to explore directions. It is not good enough to represent GES's standard of work. A generated booth concept has inconsistencies, artifacts, and details that would embarrass us in a final deliverable.

2. **Accuracy.** Generated images invent details. They cannot be trusted for dimensions, proportions, or specifications. A generated booth image might show a structure that is physically impossible to build, or a layout that violates fire code. Never use output as a spec, measurement, or build drawing.

3. **Rights and attribution.** AI-generated images carry legal ambiguity around copyright. The work that goes to clients must be work GES can warrant and stand behind.

4. **Client expectation.** Clients expect GES to deliver professional design work created by professional designers. That expectation is part of why they hire us.

**Where Nano Banana genuinely helps:**

::::{tab-set}

:::{tab-item} Booth Concept Exploration
Before a designer commits forty hours to a rendering, explore the direction with five generated concepts in ten minutes. "Is the client thinking dramatic and dark, or bright and welcoming?" Find out before you build.
:::

:::{tab-item} Mood Boards and Look-and-Feel
Generate visual explorations of texture, color palette, lighting mood, and environmental feel. "What does 'industrial elegance' actually look like?" Show three interpretations before the client says "not that one."
:::

:::{tab-item} Pitch and RFP Response Visuals
When responding to an RFP with a 72-hour turnaround, generate concept visuals that communicate your direction without pulling designers off active projects. The pitch is not the deliverable — winning the pitch earns the right to do the real work.
:::

:::{tab-item} Signage and Wayfinding Mockups
Explore how signage might look in context before committing to design. "What does a 10-foot directional sign look like at the end of that aisle?" Generate the scenario, not the production file.
:::

:::{tab-item} Environmental Design Comps
Test how a space might feel with different lighting, materials, or layouts. "What if the lounge area had warm wood instead of metal?" See it before you spec it.
:::

:::{tab-item} Texture and Material Studies
Explore surface treatments, finishes, and material combinations. "What does brushed aluminum look like against dark fabric?" Generate options before ordering swatches.
:::

:::{tab-item} Client Clarification
When a client says something vague, generate interpretations. "When you say 'modern but approachable,' do you mean something like this? Or more like this?" Visual clarification beats verbal ambiguity.
:::

::::

**The workflow in practice:**

1. Brief arrives or pitch opportunity opens
2. Creative lead generates 5-10 concept directions in Nano Banana
3. Team reviews, selects 2-3 directions worth developing
4. Human designers develop selected directions into production-quality work
5. Production work goes to client

Step 2 is what Nano Banana is for. Steps 4 and 5 are where human designers do what they do. The tool compresses step 2 from days to minutes. It does not replace steps 4 and 5.

---

## 4. The Confidentiality Boundary — This Is Not Inside the Trust Perimeter

::::{admonition} ⚠️ STOP — Read This Before You Generate Anything
:class: danger

**Google AI Studio is NOT inside the Microsoft 365 trust boundary.**

Chapter 12 established that the GES Collective operates within five distinct confidentiality perimeters on one Microsoft 365 tenant: GES Exhibitions (GSC), Spiro (EAC), onPeak, SHOWTECH, and Visit by GES. Copilot respects those boundaries because it operates within Microsoft's enterprise trust architecture.

Google AI Studio is a general-purpose consumer AI tool. It is not part of GES's enterprise environment. It does not know GES's permission structure. It does not enforce client confidentiality.

**What this means:**

- **Never upload unreleased client product imagery.** If a client has not publicly announced a product, do not put images of it into any external AI tool.
- **Never upload competitor-sensitive booth designs.** GES serves direct competitors in adjacent aisles. A booth design for one exhibitor must never be processed through a tool where cross-contamination cannot be controlled.
- **Never upload confidential floor plans.** Show floor layouts, exhibitor positions, and space allocations are commercially sensitive.
- **Never upload client brand assets.** Logos, brand guidelines, and proprietary visual assets belong to clients, not to AI training sets.

**The safe pattern:**

Describe what you want in words. Do not upload what you have. A prompt that says "a pharmaceutical trade show booth with warm lighting and curved LED walls" is safe. A prompt that attaches the actual client's preliminary booth rendering is not.
::::

:::{figure} ../images/ch15-confidentiality-boundary.png
:label: fig-ch15-confidentiality
:alt: Diagram showing the confidentiality boundary between Microsoft 365 (inside the trust perimeter, containing SharePoint, Teams, Copilot, and GES client data) and Google AI Studio (outside the trust perimeter, accessed via browser with no enterprise integration) — with a clear barrier between them and warning labels on what must not cross
:width: 80%
:align: center

The trust boundary is architectural, not optional. Google AI Studio operates outside GES's enterprise security perimeter. Client confidential material stays inside the perimeter. Prompts go out; confidential assets do not.
:::

**Why this is more serious at GES than at most companies:**

Chapter 12 covered this in detail, but it bears repeating in the creative context.

GES serves **direct competitors at the same show**. A pharmaceutical company's booth is thirty feet from its rival's. Both are GES clients. Both trust GES with unreleased product information before launch. That trust is the foundation of an 87-year relationship with the exhibition industry.

A prompt that includes "here is what Client A is planning" and then gets used to generate concepts that inform work for Client B is a cross-client contamination incident — even if no human intended it. The tool does not know which client is which. You do.

**Practical prompting for confidentiality:**

Instead of: *"Here is a photo of the client's unreleased product. Generate a booth concept featuring it."*

Do this: *"Generate a pharmaceutical trade show booth concept featuring a central product display area with dramatic lighting. The product is a medical device approximately the size of a small refrigerator. The overall feel should be high-tech but approachable."*

The difference: the first prompt leaks client IP. The second prompt describes what you need without exposing anything confidential. The generated image will not be of the actual product — it will be a conceptual placeholder that shows the *type* of display you are imagining. That is exactly what ideation needs.

::::{admonition} 🧭 T.R.U.E. Check — Responsibility
:class: note

**Be responsible for our actions and deliver on our commitments.**

Every prompt you type is a choice about what to expose. The tool has no judgment. You have judgment. Responsibility means using it — every time, without exception, even when you are in a hurry and the client meeting is in an hour and it would be so much easier to just upload the file.
::::

---

## 5. The Real Limitations — What Actually Goes Wrong

Nano Banana is powerful, but it has specific failure modes that every GES creative needs to understand. These are not theoretical concerns — they are observable, repeatable behaviors that will bite you if you do not plan for them.

:::{figure} ../images/ch15-text-failure-modes.png
:label: fig-ch15-text-failures
:alt: Grid of six example images showing common Nano Banana text rendering failures — garbled words on signage, invented copyright notices, fabricated company names, nonsense text on document props, unwanted captions, and inconsistent letter spacing — each with a label describing the failure mode
:width: 80%
:align: center

Text rendering is the #1 failure mode. The model attempts to write what it thinks you want — and frequently invents, garbles, or hallucinates text that was never requested.
:::

### Text Rendering Fails

This is the number one problem. Nano Banana struggles with text, especially:

- **Long words.** Anything beyond 6-7 characters becomes unreliable. "FREIGHT SCHEDULE" becomes "FREISHT SEHEDULE." "EXPANDED FLOOR PLAN" becomes "EAPANDED FLOOR PLAN." "POWER DISTRIBUTION MAP" becomes "POWER DISTINATION MAP." This is not occasional — it is the default behavior. Expect every long word to fail unless proven otherwise.

- **Uncommon terms.** Industry vocabulary that the model has not seen frequently in training data becomes unrecognizable. "DRAYAGE" may render as "DRAYGE" or "DRAYGAE." "MARSHALING YARD" may become something completely nonsensical. The more specialized the term, the more likely it fails. General consumer vocabulary ("SALE," "OPEN," "INFO") works. Exhibition industry vocabulary does not.

- **Any text on props.** If your generated image includes a clipboard, a document, a computer screen, a spreadsheet, or any surface that could have text on it, the model will put text there — and that text will be gibberish. Generated documents show words like "CHAGAPE" and "PROPDEN" that have no meaning in any language. In one test, a generated image of an exhibitor service kit showed a document prop with the heading "IMPORDENT FREISHT INFORMATON" — a creative interpretation of "Important Freight Information" that would embarrass anyone who showed it to a client.

- **Numbers and dates.** Dates, times, and numerical sequences are equally unreliable. A booth rendering showing a schedule board might display "March 23-26" as "Mach 2326" or "Mrch 23-6." Booth numbers, hall designations, and any numerical labeling will require post-generation editing or careful prompt exclusion.

### Invented Attribution

This is a real legal exposure. When generating images, Nano Banana sometimes invents:

- **Fabricated copyright notices.** "© 2024 Meridian Displays LLC" stamped on an image — except Meridian Displays LLC does not exist. You generated that copyright claim. The model sees that professional images often have copyright notices, so it adds one. The specific company name is pure fabrication.

- **Fake website URLs.** "www.phoenixexhibits.com" appearing on generated signage — except that is either a real company you did not intend to reference, or a fake company whose name you just created. Either way, it is a liability. A URL in a generated image could direct someone to a real website you have no relationship with, or create confusion about whether a fictional company is real.

- **Invented trademarks.** In one observed case, a generated image included "GES®" stamped four times across a booth rendering — a registered trademark symbol on a logo placement the user never requested. The model invented a trademark assertion for a real company (our company) without any instruction to do so. This is a real legal issue if the image goes anywhere beyond your own screen. Even for internal use, seeing fabricated trademark placements creates confusion about what was requested and what was invented.

- **Fake accreditations and certifications.** Generated images of professional settings sometimes include fabricated certification badges, award logos, or industry association marks. These do not exist and should never appear in anything shown to clients.

### Unwanted Captions and Labels

The model often adds descriptive text nobody asked for:

- "A modern trade show booth featuring innovative design" as a caption along the bottom of an image
- "Concept rendering" watermarked across the image
- Explanatory labels pointing to features in the image

These additions make the output unusable without editing — and editing AI-generated images is its own skill set.

### Dimensional Unreliability

Generated images look plausible but are not accurate:

- A "40 by 40 booth" prompt produces an image that might show a 20 by 60 space
- Structural elements violate physics — beams that connect to nothing, cantilevers that would collapse
- Human figures are scaled inconsistently — making booth size impossible to judge from the image

**Never use a generated image as a specification.** It is a visual direction, not a build drawing.

### The Prompt Discipline That Fixes This

After extensive use, the following prompt structure produces dramatically cleaner results:

**Explicit text control:**

End every prompt with explicit instructions about text:

*"...the only text visible in the image should be [LIST EXACT LABELS]. Do not include any other text, copyright notices, URLs, logos, watermarks, captions, or readable content on any props, documents, screens, or surfaces."*

**Keep text short:**

Any text you do want should be 1-3 SHORT common words:

- ✅ "WELCOME" (one word, 7 letters)
- ✅ "INFO DESK" (two short words)
- ✅ "EXIT" (one word, 4 letters)
- ❌ "REGISTRATION DESK" (too long)
- ❌ "FREIGHT SCHEDULE" (will garble)
- ❌ "POWER DISTRIBUTION CENTER" (will become nonsense)

**Forbid props that invite text:**

If you do not need documents, clipboards, or screens in the image, explicitly exclude them:

*"...no visible documents, papers, screens, or readable materials in the scene."*

---

## 6. Prompt Structure for Visual Work

Prompting for images is different from prompting for text. When you ask a text model for help, you are having a conversation. When you ask an image model for a visual, you are describing a scene.

:::{figure} ../images/ch15-prompt-anatomy.png
:label: fig-ch15-prompt-anatomy
:alt: Annotated prompt example showing the six components of an effective image generation prompt — Subject, Setting, Style, Palette, Composition/Lighting, and Aspect Ratio — each highlighted and labeled with examples relevant to exhibition design
:width: 80%
:align: center

The anatomy of an effective visual prompt: Subject → Setting → Style → Palette → Composition/Lighting → Aspect Ratio. Each element adds control. Missing elements leave the model to guess.
:::

**The six components:**

```{list-table} Visual Prompt Components
:header-rows: 1
:label: table-ch15-prompt-components

* - Component
  - What It Controls
  - Example
* - Subject
  - What is the main focus of the image?
  - "A 30 by 30 trade show booth for a technology company"
* - Setting
  - Where is this? What surrounds it?
  - "On a convention center show floor with high ceilings and other booths visible in background"
* - Style
  - What is the visual treatment?
  - "Photorealistic rendering" or "Architectural sketch style" or "Watercolor concept art"
* - Palette
  - What colors dominate?
  - "Cool blues and whites with warm wood accent tones"
* - Composition
  - Where is the camera? What is the lighting?
  - "Three-quarter view from elevated angle, dramatic spotlighting from above"
* - Aspect Ratio
  - What shape is the final image?
  - "Landscape format" or "16:9 aspect ratio" or "Square format"
```

**Example prompt structure:**

*"[SUBJECT] A 40 by 40 trade show booth for a healthcare technology company, featuring a central meeting area surrounded by product demonstration stations. [SETTING] On the show floor of a large convention center with high ceilings, other booths visible in soft focus in the background. [STYLE] Photorealistic 3D rendering. [PALETTE] Clean whites and light grays with accents of deep teal and warm copper. [COMPOSITION] Three-quarter elevated view showing the full booth footprint, soft ambient lighting with dramatic accent lights on the product stations. [ASPECT] 16:9 landscape format. [TEXT CONTROL] The only visible text should be 'WELCOME' on the main entrance arch. No other text, logos, copyright notices, URLs, or readable content on any surface."*

**Common mistakes:**

- **Too vague.** "A nice booth" gives the model nothing to work with. What makes it nice? What size? What style?

- **Too specific on wrong dimensions.** "Exactly 12 feet 4 inches tall" will not produce accurate dimensions. Describe relative scale instead.

- **Forgetting text control.** If you do not forbid unwanted text, you will get unwanted text.

- **No style direction.** Without a style cue, the model picks one — and it may not be what you wanted.

---

## 7. The Iteration Workflow — Generate Wide, Refine Narrow

:::{figure} ../images/ch15-iteration-ladder.png
:label: fig-ch15-iteration
:alt: Vertical workflow diagram showing the iteration ladder — starting at the bottom with "Generate 10 concepts on Nano Banana (fast, cheap)" rising through "Review with team, select 3 directions" then "Refine selected concepts on Nano Banana 2" then "Final concepts on Nano Banana Pro" and ending at the top with "Human designers take over for production"
:width: 80%
:align: center

The iteration ladder: start wide and cheap, narrow as you climb, hand off to human designers at the top. The tool accelerates exploration. Humans own execution.
:::

**Step 1: Generate Wide on Nano Banana**

Start with 10-15 concepts on the fast model. Try different directions. Do not self-edit at this stage — the point is volume. A concept that looks strange in your head might look interesting when you see it.

Prompt variations to try:
- Different color palettes for the same booth concept
- Different lighting moods (bright and welcoming vs. dramatic and moody)
- Different central features (product display vs. meeting lounge vs. demonstration area)
- Different architectural styles (angular and modern vs. organic and curved)

Cost for 15 generations: roughly $0.60. Time: under 10 minutes.

**Step 2: Review and Select**

With your team (or alone if you are the creative lead), review the generated concepts. Most will be wrong. Some will be interesting. A few will spark a direction worth pursuing.

Select 2-3 directions to develop further.

**Step 3: Refine on Nano Banana 2**

For your selected directions, refine the prompts based on what you learned. Be more specific. Add the details that were missing. Generate 3-5 variations of each direction.

**Step 4: Final Concepts on Nano Banana Pro**

For the 1-2 concepts you want to show to the team or use in a pitch, re-generate on Pro for higher quality output. Use the refined prompts from Step 3.

**Step 5: Human Handoff**

The winning concept goes to human designers for actual development. The generated image is reference material — visual direction, not production art.

**What you have at the end:**

- A clear visual direction agreed upon by the team
- Reference images that communicate that direction
- Significantly less time spent on exploration
- Designers free to focus on execution, not ideation

**What you do not have:**

- A finished rendering ready for a client deck
- Production-ready graphics
- Accurate dimensions or build specifications
- Work that can be presented as "GES design work"

The distinction matters. The iteration workflow produces *direction* — the answer to "which way should we go?" It does not produce *deliverables* — the polished work that goes to clients. That gap is filled by human designers, and it is not a small gap. The translation from "AI-generated concept that captures a direction" to "professional rendering that GES stands behind" is where design skill lives.

---

## 8. Integrating with the GES Creative Workflow

:::{figure} ../images/ch15-booth-concept-workflow.png
:label: fig-ch15-workflow
:alt: Horizontal workflow diagram showing how Nano Banana integrates with GES creative process — Brief Intake, AI Concept Exploration (10-15 concepts in Nano Banana), Team Review and Direction Selection, Designer Development, Internal Review, Client Presentation, Revision Cycles, Production Art — with the AI phase clearly bounded and labeled as ideation only
:width: 80%
:align: center

Nano Banana slots into the existing GES creative workflow at the concept exploration phase — after brief intake, before design development. It compresses a days-long exploration into a morning's work.
:::

**Where it fits:**

| Workflow Phase | Who Does It | Nano Banana Role |
|----------------|-------------|------------------|
| Brief intake and discovery | Account team, Creative lead | None — understand the ask first |
| Concept exploration | Creative lead | **Primary use** — generate directions |
| Direction selection | Creative team | Review generated concepts |
| Design development | Designers | Reference only — AI concepts as direction |
| Internal review | Creative director | None — reviewing human work |
| Client presentation | Account team, Creatives | None — presenting human work |
| Revision cycles | Designers | Optional — quick visual exploration of revisions |
| Production art | Graphics, Fabrication | **Never** — production is human work |

**Communication conventions:**

When sharing a generated concept internally:
- "Here's an AI-generated concept for direction — this is ideation, not a deliverable"
- Include the prompt used so others can refine it
- Do not present it as design work — it is exploration work

When using it as reference for designers:
- "Here's the visual direction we're going for"
- Expect the designer to interpret and improve, not replicate
- The generated image is a starting point, not a target

---

## 9. What Nano Banana Cannot Do — Honest Limits

:::{figure} ../images/ch15-creative-workflow-integration.png
:label: fig-ch15-creative-integration
:alt: Venn diagram showing the overlap and boundaries between AI capabilities and human designer capabilities — AI excels at rapid exploration, volume, and consistent style application; humans excel at judgment, accuracy, production quality, and client relationships; the overlap zone shows direction finding and concept refinement
:width: 80%
:align: center

The capabilities Venn diagram: AI tools and human designers have different strengths. Effective creative teams use both — AI for speed and volume in exploration, humans for judgment and quality in execution.
:::

::::{admonition} 🧭 T.R.U.E. Check — Understanding
:class: note

**People come first. Be understanding and compassionate.**

Understanding in the context of AI tools means recognizing that the tool's limitations are not failures to be frustrated by — they are boundaries to be understood. A designer who sees their AI-generated concept fail to render text correctly should not feel like the tool failed them. The tool worked exactly as expected. Understanding its limits is part of using it well.

More importantly: understanding applies to clients. A client who sees an AI-generated concept and asks "why can't we just use this?" deserves a thoughtful explanation, not dismissal. They are not trying to cut corners — they are trying to understand what is possible. Meet them where they are.
::::

**Cannot do:**

- **Production-ready graphics.** Output is not print-ready and should not go to fabrication. Resolution, color accuracy, and detail quality are insufficient for production work.
- **Accurate dimensions.** Cannot be trusted for measurements, scale, or build specifications. A "40 by 40 booth" prompt produces an image of indeterminate actual size.
- **Reliable text.** Long words, technical terms, and industry vocabulary fail frequently. Text rendering remains the model's most consistent weakness.
- **Client logos.** Cannot reproduce actual brand assets accurately or legally. Even if you could get a logo to render, you should not — it creates attribution confusion.
- **Structural accuracy.** Generated structures may be physically impossible. Beams that connect to nothing, cantilevers without support, walls that float.
- **Code compliance.** Cannot know fire code, ADA requirements, or venue regulations. A generated booth may violate every rule in the exhibitor manual.
- **Photography replacement.** Cannot replace actual photos of actual products. Generated "products" are inventions, not documentation.
- **Final renderings.** Cannot produce the polished 3D renderings that go in client decks. The quality gap is immediately visible to anyone who has seen professional design work.

**Can do, with caveats:**

- **Concept exploration** — but requires review and selection by humans
- **Mood communication** — but is not a finished mood board
- **Direction finding** — but the direction must be executed by designers
- **Rapid iteration** — but quality requires refinement and human polish
- **Visual brainstorming** — but judgment about what is good still requires humans

::::{admonition} 🧭 T.R.U.E. Check — Excellence
:class: note

**Provide excellent service and execution.**

Excellence means knowing what each tool is for. Nano Banana is excellent at ideation. Human designers are excellent at execution. Using each for what it does well — that is excellence. Using AI output as a client deliverable is not faster. It is lower quality presented as finished work. That is the opposite of excellence.
::::

---

## 10. Try This — A Complete Ideation Session

::::{admonition} 🧪 Try This: AI-Assisted Booth Concept Exploration
:class: tip

**Time required:** 30-45 minutes

**What you need:**
- A browser and a Google account
- Access to Google AI Studio ([aistudio.google.com](https://aistudio.google.com))
- A fictional brief (create one, or use the example below)

**Fictional brief:**

*"TechFlow Solutions is exhibiting at CES 2027. They are launching a new smart home hub that integrates all home automation systems. Their brand is modern, approachable, and tech-forward without being cold. Budget supports a 30 by 30 island booth. They want a space that feels like walking into a smart home, not a showroom. Key activities: product demos, private meetings with retail buyers, and a social media photo moment."*

---

**Step 1: Generate Initial Concepts (Nano Banana)**

Open Google AI Studio. Select the Gemini 2.5 Flash Image model.

Generate 5 different booth concepts using different approaches:

1. **Living room approach:** *"A 30 by 30 trade show booth designed to look like a modern smart home living room. Warm wood floors, comfortable seating areas, subtle technology integration. Convention center setting, other booths visible in background. Photorealistic rendering, warm color palette with tech blue accents. Three-quarter elevated view. No text, logos, or branding visible."*

2. **Tech showcase approach:** *"A 30 by 30 trade show booth with a dramatic central product display on a glowing pedestal. Curved LED walls showing abstract digital patterns. Modern angular architecture in white and chrome. Dark dramatic lighting with bright accents. Photorealistic, three-quarter view. No text or logos."*

3. **Hybrid space approach:** *"A 30 by 30 trade show booth that blends home comfort with technology showcase. Half the space is a warm living environment, half is a sleek product demonstration area. The two zones flow together. Soft and dramatic lighting in different zones. No visible text."*

4. **Immersive tunnel approach:** *"A 30 by 30 trade show booth entered through a short immersive tunnel that leads into an open central space. Projection-mapped walls creating a 'surrounded by technology' feeling. Modern minimal furniture. Cool blue palette. No text or logos."*

5. **Modular pod approach:** *"A 30 by 30 trade show booth with multiple small pod-like spaces connected by a central circulation path. Each pod demonstrates a different smart home room type. Consistent modern aesthetic throughout. Bright, welcoming lighting. No text."*

---

**Step 2: Review and Select**

Look at your five generated concepts. Ask yourself:

- Which one best captures "modern, approachable, tech-forward without being cold"?
- Which one would work for the three activities (demos, meetings, photo moment)?
- Which one feels most like "walking into a smart home"?

Select 2 directions to refine.

---

**Step 3: Refine Selected Concepts**

For your selected directions, generate 3 variations each, refining the prompt based on what you learned:

- Add details that were missing
- Adjust elements that did not work
- Try different color variations
- Explore different camera angles

---

**Step 4: Final Quality on Pro (Optional)**

If you have access to Nano Banana Pro, re-generate your best 1-2 concepts for higher quality output.

---

**Step 5: Document Your Process**

Write a brief note:
- Which concepts resonated and why
- What prompt adjustments produced better results
- What you would hand to a designer as direction

---

**Debrief questions:**

1. How did the AI-generated concepts compare to what you imagined before generating?
2. Did any concept surprise you in a useful way?
3. What limitations did you encounter?
4. How would you describe the "direction" to a designer based on what you generated?
5. What would you do differently next time?
::::

---

## 11. Productive Struggle Problem

::::{admonition} 🔨 Productive Struggle: The Difficult Client Brief
:class: important

**Scenario:**

A Spiro client has sent a brief that is unusually abstract. They are launching a new brand identity at their industry's largest trade show and want their 50 by 50 booth to "embody transformation." The brief uses words like "metamorphosis," "emergence," and "the moment between what was and what will be."

When asked for visual references, the client says: "We don't have any — that's why we're asking you."

**Your challenge:**

Using Nano Banana, generate a range of concept directions that might communicate "transformation" and "emergence" in a trade show booth context. You have 45 minutes.

**The struggle points:**

1. How do you translate abstract concepts into visual prompts?
2. What physical elements could represent "metamorphosis" in a booth structure?
3. How do you avoid clichés (butterfly imagery, "before and after" layouts)?
4. How do you generate enough range that the client sees genuinely different directions?

**Constraints:**

- Do not use the client's actual brand (they do not have one yet — that is the point)
- Do not include text in the generated images
- Generate at least 8 distinct concept directions
- Document your prompt evolution as you learn what works

**What to submit to your team:**

- Your 3 best concepts with the prompts that generated them
- A brief explanation of how each concept communicates "transformation"
- Notes on what prompt strategies worked and what failed
- Honest assessment: which concept would you recommend, and why?

**Why this is hard:**

Most briefs are concrete: "we want to showcase these products" or "we need a meeting space for 12." This brief asks you to make an idea visible. That is a translation challenge that AI cannot do alone. You have to figure out what "transformation" might look like, then describe it well enough for the model to generate it, then evaluate whether it actually communicates what the brief asked for.

The productive struggle is the translation — from abstract concept to visual prompt to generated image to professional judgment about whether it worked.
::::

---

## Glossary

```{glossary}
Nano Banana
  Internal nickname for Google's Gemini-based image generation models. The family includes Nano Banana (Gemini 2.5 Flash Image), Nano Banana 2 (Gemini 3.1 Flash Image), and Nano Banana Pro (Gemini 3 Pro Image).

Google AI Studio
  Browser-based interface for accessing Google's AI models, including the Nano Banana image generation family. Accessible at aistudio.google.com with a Google account.

Ideation
  The early, exploratory phase of creative work where multiple directions are explored before committing to development. Nano Banana accelerates ideation; it does not replace production.

Production Art
  Finished creative work that goes to clients, to print, or to fabrication. Production art is created by human designers. AI-generated images are never production art.

Text Rendering
  The ability of an image generation model to include readable text in generated images. Nano Banana's text rendering is unreliable, especially for long words and technical terms.

Prompt
  The text description given to an image generation model to specify what image should be created. Effective prompts include subject, setting, style, palette, composition, and text control elements.

Character Consistency
  The ability of an image model to maintain the appearance of a character or object across multiple generated images. Useful for generating consistent booth concepts or design elements.

Multi-Image Fusion
  The capability to combine elements from multiple input images into a single generated output. Useful for placing objects into scenes or combining visual elements.

Grounding
  The connection between a generative AI model and the source data it draws upon. In image generation, this relates to how well the model follows prompt instructions rather than inventing details.

Trust Boundary
  The security perimeter that defines what data an AI tool can access and what confidentiality protections apply. Google AI Studio operates outside the Microsoft 365 trust boundary that protects GES's Copilot usage.

SynthID
  Google's invisible digital watermarking technology applied to AI-generated images, allowing them to be identified as AI-created or edited.
```

---

:::{seealso}
**Resources for Chapter 15**

- 🎨 Google AI Studio (access Nano Banana models): [aistudio.google.com](https://aistudio.google.com)
- 📖 Gemini API Image Generation Documentation: [ai.google.dev/gemini-api/docs/image-generation](https://ai.google.dev/gemini-api/docs/image-generation)
- 🔒 Google AI Studio Terms of Service: [ai.google.dev/terms](https://ai.google.dev/terms)
- 🛡️ SynthID Digital Watermarking: [deepmind.google/science/synthid](https://deepmind.google/science/synthid/)
- 📋 OpenRouter (alternative API access): [openrouter.ai](https://openrouter.ai)
:::

---

## Discussion Questions

1. **The ideation boundary.** Where exactly does ideation end and production begin in your team's workflow? How would you communicate to a new team member that AI-generated images are for exploration, not delivery?

2. **Confidentiality in practice.** A colleague is rushing to prepare for a pitch and asks if they can "just upload the client's preliminary rendering to get better AI concepts." How do you respond? What is the principle, and how do you make it practical under time pressure?

3. **Quality judgment.** You generate a booth concept that looks good, but something feels off. It would take three hours to explain to a designer what you want; the generated image seems close enough. What is the right call? What criteria should guide the decision?

4. **Client communication.** A client sees an AI-generated concept you used internally and asks: "Can we just use that? It looks good enough." How do you explain why the final deliverable will be better — and worth the additional time?

5. **Text failure workarounds.** Your booth concept needs to show "REGISTRATION DESK" on a sign, but Nano Banana keeps garbling it. What options do you have? When is it worth fighting the tool, and when is it better to work around it?

6. **Cross-client awareness.** You are working on a pitch for Company A. While generating concepts, you accidentally type a prompt that includes details you remember from Company B's booth last year. You did not upload anything, but you drew on your memory. Is this a problem? Where is the line?

---

## Leader's Takeaway

Nano Banana gives GES creative teams a powerful new tool for the ideation phase of design work — but only if the boundaries are clear and the discipline is maintained.

**What leaders need to ensure:**

1. **The ideation/production boundary is understood.** Every creative team member needs to understand that AI-generated images are exploration tools, not deliverables. This is a professional standard, not a guideline.

2. **Confidentiality discipline is enforced.** Google AI Studio is outside the Microsoft 365 trust boundary. Client IP, unreleased products, and competitor-sensitive designs must never be uploaded. Prompts describe; they do not expose.

3. **Designers are not threatened; they are freed.** The value proposition is clear: AI handles rapid exploration so designers can focus on execution. The tool does not replace design skill. It accelerates finding the direction that design skill will develop.

4. **Prompt skills are developed.** Effective prompting is a learnable skill. Invest in a few hours of experimentation so your team knows what works and what fails.

5. **Quality gates remain.** The workflow still ends with human review, human judgment, and human accountability. AI accelerates the early stages. It does not change who is responsible for the final work.

**The opportunity:**

A pitch that used to require pulling designers off active projects can now be explored with AI-generated concepts in hours, not days. A creative director can show a client three visual directions before anyone has committed to building them. A mood board that used to require stock image research can be generated directly from a creative brief.

The time saved is real. The risk is manageable with clear discipline. The combination gives GES creatives an edge in the RFP process and a faster path from brief to direction.

Use the tool. Respect the boundaries. Keep humans in the loop where humans belong.
