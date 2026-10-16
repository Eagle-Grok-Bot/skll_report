---
name: HEP progress report
description: >-
  Use when planning or drafting JUNO/HEP conference reports: align direction
  with the user, deliver an outline HTML (per-page core content) for
  confirmation, then only after approval draft page-by-page with figures
  (PDF/PNG)—Amber talk/poster style is the baseline.
---
# HEP progress report (Amber baseline + two-step gate)

Help the user prepare conference/collaboration reports for neutrino/HEP work. **Voice and density follow the user’s own Amber reports** (physics-first bullets, method variants, data-driven training, numbers vs baselines, physics impact, short summary).

## Hard gate (do not skip)

Work in **two steps**. Never start per-page drafting, figure collection, or nightly deep writing until **Step A** is done and the user has **confirmed** the outline HTML.

| Step | What you produce | User must… |
| --- | --- | --- |
| **A — Direction + outline HTML** | Discuss report direction → one HTML file: full outline + each page/panel’s **core content** | Confirm or edit the HTML |
| **B — Per-page prep** | Page-by-page bullets, figures (discuss → PDF/PNG → place), nightly schedule | Confirm each page / send plots as needed |

If the user asks to “just write the slides,” still run Step A first unless they explicitly waive the outline HTML for this meeting.

Reports almost always need **result distribution / performance plots**. In Step B, discuss meaning with the user, ask for PDF or PNG, then place them. Do not invent plots or caption claims the user has not confirmed.

## Baseline style (non-negotiable)
User’s own materials — always the style floor:
- Talk: https://indico.global/event/15240/contributions/165356/ (Amber self-attention muon tracks)
- Poster: https://indico.global/event/15740/contributions/147762/ (cosmic muon reconstruction overview)

Prefer the user’s Indico links when they shared them; local repo mirrors live in `examples/` and `refs/` of Eagle-Grok-Bot/skll_report.

If other conference skills or generic slide guides conflict with Amber, **prefer Amber**.

---

# STEP A — Direction + outline HTML (first)

## A0 — Intake + direction
Gather or confirm:

1. **Meeting calendar**: conference name, dates, timezone, talk vs poster vs abstract-only, allotted minutes, deadline.
2. **Report direction** (discuss openly before outlining):
   - Working title and one-sentence takeaway
   - What is *new* since last report
   - Audience (ML / neutrino / mixed) and tone (progress vs conference)
   - Must-include vs nice-to-have topics; what to cut for time
3. **Constraints**: collaboration approval, WIP figures, secrets, language (EN default for Indico).
4. **Assets / links**: numbers, plots status, author list, prior Indico pages to match.

Ask in a short checklist or widget if anything material is missing. Do **not** write full slide prose yet.

## A1 — Propose structure
Propose 1–2 structure options tailored to venue length (Amber spine below), wait for pick/edits.

### Amber-native defaults
**Talk (~15–20 min)**: Title → Motivation & physical picture → Features/observables → Architecture → Model variants (Done/To do) → Data-driven training → Per-variant method → Performance vs baselines → Physics application → Summary + outlook

**Poster panels**: Motivation | Methods (traditional + ML) | Performance | Cosmogenic/physics benchmark | Summary + refs

**Indico abstract**: one dense paragraph — detector goal → background → method/inputs → variants → training → key claim → impact.

### Venue-length overlays (timing only)
- **~10 min**: collapse variants; 2–3 results max; still open with physics.
- **~15–18 min**: Amber spine + slightly more results; 2–3 takeaways.
- **Poster**: large figures; minimal text.
- **Internal progress**: may add “open issues / next week.”

You may search public conference guides for length/font/upload rules — timing tips only, not style replacements.

## A2 — Deliver outline HTML (required artifact)
After direction and structure are roughly agreed, produce a **single HTML file** the user can open in a browser. This is the gate artifact for Step B.

**File naming**: `outline-<meeting-slug>-YYYYMMDD.html` (e.g. `outline-nu2026-20261016.html`) in the working report folder.

**Must include**:
1. Header: meeting name, dates, talk/poster, minutes, working title, one-sentence direction/takeaway.
2. **Full outline** as a numbered list (slide or panel order).
3. **Per page/panel card** for every item:
   - Page number + title
   - **Core content** (3–6 short bullets: what this page must convey — not full Amber prose yet)
   - Planned figure slot(s) if any (`F?` id + one-line intent), or “no figure”
   - Open questions / TBD for that page
4. Optional footer: version + “Awaiting user confirmation before per-page drafting.”

Keep HTML self-contained (inline CSS), readable on laptop/phone. Use `examples/outline-html-template.html` in the skill repo as a starting layout.

Deliver the HTML to the user (attach / path / link). **Stop and wait** for confirmation or edits. Revise the HTML until they say the outline and per-page cores are OK.

**Do not** enter Step B, collect figure files in bulk, or write full per-page drafts until that confirmation.

---

# STEP B — Per-page content (only after outline HTML confirmed)

## B1 — Nightly / page order plan
Break the **confirmed** outline into a schedule (Asia/Shanghai unless told otherwise). Each night or session: which pages, which figure IDs still needed, stopping point.

Offer a **routine** for nightly reminders only after the user agrees.

## B2 — Figures: discuss, collect, place
For each result page in the confirmed outline:

1. **Discuss meaning** before asking for files: what / why on this page / sample & cuts / axes & legend / takeaway / WIP or confidential.
2. If the user shares Indico/PDF links, open them and ask which plots to reuse — do not copy captions blindly.
3. **Ask for PNG** (slides/web) or **PDF** (vector/poster/LaTeX). Track an inventory (`examples/figure-inventory-template.md`).
4. Save under `figures/`; embed or mark `TBD — awaiting PNG/PDF`; never fabricate histograms.
5. Re-check one-line captions with the user before final.

## B3 — Draft each page in Amber voice
Page by page (or night by night), expand core bullets into full Amber content:
1. Physics first: detector goal → background → why reconstruction matters.
2. Short `•` bullets; one idea each.
3. Name subsystems (CD / WCD / TT).
4. Method family tree; Done / To do when useful.
5. Architecture in plain words: inputs → backbone → outputs.
6. Data-driven honesty: labels, coverage, augmentation, loss.
7. Numbers with baselines, **backed by placed figures** when claiming distributions.
8. Physics benchmark (veto / SPN / live-time).
9. Summary ≤ 4 bullets; WIP dated; no hype.
10. Correct units/isotopes (`9Li/8He`, deg, m, ms).

### Output formats (Step B)
- **Talk**: `## Slide N — Title` + bullets + `[Figure Fid: …]` or embedded paths
- **Poster**: panel headings + large-figure slots
- **Abstract**: Indico paragraph + title + keywords
- Optional: later full HTML/PDF deck built from confirmed pages

Language: match user; international Indico → English unless asked.

---

## Quality checklist
- [ ] Direction discussed with user
- [ ] Outline HTML delivered with per-page core content
- [ ] User **confirmed** outline HTML before Step B
- [ ] Each result page: figure meaning discussed + file status
- [ ] PNGs/PDFs placed or marked awaiting upload; captions agreed
- [ ] Nightly/page plan if deadline > 1 day away
- [ ] Amber baseline followed
- [ ] Venue timing respected; numbers present or TBD; secrets/WIP marked

## External style notes (secondary)
Useful only for length/logistics; never override Amber voice or the Step A HTML gate.
