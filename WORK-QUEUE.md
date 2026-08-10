# GES Learns AI — Work Queue

Concurrency cap is 5 subagents. Launch queued items as slots free.

## DONE
- [x] Cover regenerated — GES branding, exhibition hall visual (commit b827059)
- [x] Cover proportions fixed — normal 6x9 hardcover, not elongated (commit 2c5948c)
- [x] IMAGE-STYLE-GUIDE.md written
- [x] Ch12 SharePoint rewritten (8,032 words, 0 BankUnited)

## IN FLIGHT
- [ ] ges-ch10 (OneNote rewrite)
- [ ] ges-ch13 (Advanced Excel rewrite)
- [ ] img-ch00-01 (11 images)
- [ ] img-ch02-03 (20 images)
- [ ] img-ch04-05 (20 images)

## QUEUED — IMAGES (launch as slots free)
- [ ] img-ch08-09 — 20 images (ch08 PowerPoint x10, ch09 Teams x10)
- [ ] img-ch10 — 10 images (OneNote). BLOCKED until ges-ch10 finishes (refs may change)
- [ ] img-ch12 — 11 images, ALL MISSING FROM DISK. Ch12 text is DONE, so safe to run now.
- [ ] img-ch13 — 10 images, ALL MISSING FROM DISK. BLOCKED until ges-ch13 finishes.
- [ ] ch14 — HAS ZERO IMAGES AND ZERO FIGURE REFERENCES. 13,461 words, 16 sections,
      no figures at all. Needs ~12 figure directives INSERTED into the chapter, then
      12 images generated. This is an insertion job, not a regeneration job.
- [ ] img-ch15 — new NanoBanana chapter images (after chapter written), 10 files
- [ ] img-ch16 — new Power Automate chapter images (after chapter written), 12 files

## VERIFY AGAINST LIVE SITE, NOT COMMITS
Lesson 2026-08-10: pushing != rendering. Verify at the real URLs.
- Chapter URL pattern is FLAT: https://geslearnsai.com/ch01-the-essentials
  (NOT /chapters/ch01-...). A wrong guess returns the GitHub 404 page.
- MyST rewrites images to hashed build paths: /build/<name>-<hash>.png
  Source path ../images/foo.png is NOT served at /images/foo.png.
- To count images on a live page:
  curl -sSL https://geslearnsai.com/<chapter> | grep -oE 'src="/build/[^"]*"' | wc -l

## SCREENSHOT POLICY (decided 2026-08-10)
Dr. Lee asked about capturing real screenshots. Constraint: we have NO licensed M365
Copilot / Cowork tenant, so we cannot capture authentic product UI. AI-generated fake UI
screenshots are the WORST case for this model — they produce garbled fake menu text
(confirmed: "FREISHT SEHEDULE", "EAPANDED FLOOR PLAN").
DECISION: Do NOT attempt photorealistic fake screenshots. Use stylized schematic UI
diagrams — simplified panes, boxes, and 1-3 word labels — which read as intentional
diagrams rather than failed screenshots. Revisit if Dr. Lee can supply real captures.

## QUEUED — CONTENT
- [ ] NEW Chapter 15: Creative AI with Nano Banana (via AI Studio)
      - Covers Nano Banana (Gemini 2.5 Flash Image), Nano Banana 2 (Gemini 3.1 Flash Image),
        Nano Banana Pro (Gemini 3 Pro Image)
      - Access path: aistudio.google.com
      - Audience: GES creatives — exhibit designers, graphics production, Spiro creative
      - Use cases: booth concept renders, graphics mockups, client pitch visuals,
        rapid concept iteration, signage/wayfinding mockups, environmental design comps
      - MUST cover: this is CONCEPT/IDEATION tooling, not production art. Human designers
        still own final deliverables. Client confidentiality — do not upload unreleased
        client product imagery.
      - Target: 7,000-8,000 words
      - Add to myst.yml TOC

- [ ] Introduction (ch00): add "be hmn" (behmn.com) company section
      - Founder & CEO: Alex Schwartz — message from the founder
      - Chief Data Officer & Co-founder: Dr. Ernesto Lee
      - Tagline: "Be hmn, adapt faster" / "The glue that binds AI capabilities with
        human adaptability."
      - Frame: behmn delivered this master class for GES

## FROZEN — DO NOT TOUCH
Dr. Lee's explicit instruction: the 10 existing oversized chapters stay AS-IS.
No compression pass. No edits. Ch00-Ch09 prose is final.
(Exception: ch00 introduction gets the behmn founder section added — that is an ADDITION,
approved separately, not a rewrite of existing prose.)
