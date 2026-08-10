# GES Learns AI — Image Style Guide

All book images MUST follow this guide so the visual layer is consistent across chapters.

## Generation Command

```bash
cd /home/node/openclaw
node skills/book-writer/scripts/generate-image.js \
  /home/node/openclaw/books/ges-learns-ai/images/<exact-filename>.png \
  "<prompt>" \
  --aspect-ratio landscape
```

- Almost all interior images are `--aspect-ratio landscape` (16:9).
- The script prints JSON. `"success": true` means it saved. Retry once on failure.
- Overwrite the existing file at the exact same filename. NEVER rename files or change paths.

## Visual Style (append to EVERY prompt)

> Style: clean modern corporate infographic, flat vector illustration with subtle depth.
> Color palette: deep navy blue (#0B2545) as the dominant base, vibrant orange (#F26522) as
> the accent color, light cool grey (#F4F6F8) backgrounds, white space used generously.
> Crisp geometric shapes, clear visual hierarchy, professional business-publication quality.
> Typography: bold clean sans-serif headings, highly legible. Wide landscape 16:9 composition.

## Content Rules — MANDATORY

1. **ZERO banking content.** No banks, loans, credit, deposits, mortgages, borrowers,
   collateral, underwriting, fraud detection, financial regulators (OCC/FDIC/Fed/CFPB),
   examiners, branches, DSCR, LTV, AML/KYC, or bank logos. This book was converted from a
   banking book — the old images are all bank-themed and must be fully replaced.

2. **The company is GES (Global Experience Specialists)** — a global trade show, exhibition,
   and experiential marketing services company. Founded 1939. Las Vegas HQ. 4,000+ events a
   year, 150,000+ exhibitors, 75+ countries, 24 facilities, ~2,600 employees.

3. **Use GES visual vocabulary:** trade show floors, exhibition halls, booths and stands,
   truss and rigging, aisle carpet, freight trucks and crates, advance warehouse, marshaling
   yard, forklifts, install & dismantle crews, badges and lanyards, floor plans, convention
   centers, hard-hat safety vests, shipping containers, hotel room blocks.

4. **Use GES terminology in labels:** drayage, material handling, freight targets, move-in /
   move-out, I&D (install & dismantle), GSC (General Service Contractor), EAC (Exhibitor
   Appointed Contractor), show organizer, exhibitor, exhibitor service kit, site survey,
   post-show reconciliation, union jurisdiction, carnet.

5. **Text in images must be MINIMAL and CORRECT.** Image models garble long text. Use short
   labels of 1–4 words. Never request paragraphs. Prefer 4–8 labeled elements maximum.

6. **If the image needs a company name, use "GES"** — never "BankUnited". Do not attempt to
   reproduce the real GES logo; use the plain letters "GES" or no branding at all.

7. **Microsoft Copilot** may appear as a generic colorful ribbon/swirl AI icon. Do not attempt
   exact Microsoft logos.

8. **People:** diverse, professional, realistic mix of office workers AND field/show-floor
   workers (hard hats, safety vests, tablets on a show floor). GES is NOT a desk-only company —
   reflect that.

## Filename Discipline

- Regenerate to the EXACT existing filename. The chapters reference these paths.
- Do not create new filenames unless the file is listed as MISSING in your task.
- Do not touch any file outside your assigned list.

## Verification

After generating your batch, confirm every assigned file exists and is > 50KB:

```bash
cd /home/node/openclaw/books/ges-learns-ai/images
ls -la <your files>
```
