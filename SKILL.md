---
name: HEP progress report
description: >-
  Use when planning or drafting JUNO/HEP conference reports: first collect the
  user’s meeting calendar and report plan, discuss structure per venue, then
  schedule nightly draft content—Amber talk/poster style is the baseline.
---
# HEP progress report (Amber baseline + venue workflow)

Help the user prepare conference/collaboration reports for neutrino/HEP work. **Voice and density follow the user’s own Amber reports** (physics-first bullets, method variants, data-driven training, numbers vs baselines, physics impact, short summary). Different meetings may need different *structures*; never skip the intake + structure discussion.

## Baseline style (non-negotiable)
User’s own materials — always the style floor:
- Talk: https://indico.global/event/15240/contributions/165356/ (Amber self-attention muon tracks)
- Poster: https://indico.global/event/15740/contributions/147762/ (cosmic muon reconstruction overview)
Local repo mirrors: `examples/` and `refs/` in Eagle-Grok-Bot/skll_report.

If other conference skills or generic slide guides conflict with Amber (long prose, marketing tone, burying motivation), **prefer Amber**.

## Phase 0 — Intake (do this first)
Before writing slides/abstract/poster copy, gather or confirm:

1. **Meeting calendar**: conference name, dates, timezone, talk vs poster vs abstract-only, allotted minutes, deadline (abstract / slides upload).
2. **Report plan**: working title, one-sentence takeaway, what is *new* since last report, target audience (ML / neutrino / mixed).
3. **Constraints**: collaboration approval, WIP figures, secrets not to share, language (EN default for Indico).
4. **Assets on hand**: key numbers, plots, baselines, author list.

If anything material is missing, ask in a short checklist (or widget). Do **not** invent a full deck until structure is agreed.

## Phase 1 — Discuss structure (per meeting)
Propose 1–2 structure options tailored to venue length, then wait for the user’s pick/edits.

### Amber-native defaults (start here)
**Talk (~15–20 min)** section spine:
1. Title · 2. Motivation & physical picture · 3. Features/observables · 4. Architecture overview · 5. Model variants (Done/To do) · 6. Data-driven training · 7. Per-variant method · 8. Performance vs baselines · 9. Physics application · 10. Summary + outlook

**Poster** panels: Motivation | Methods (traditional + ML) | Performance | Cosmogenic/physics benchmark | Summary + refs

**Indico abstract**: one dense paragraph — detector goal → background need → method/inputs → variants → training → key claim → impact.

### Venue-length adaptations (optional overlays)
Use only as *timing/length* overlays; keep Amber section *content* and tone:
- **~10 min**: collapse variants onto 1–2 slides; 2–3 results max; still open with physics motivation.
- **~15–18 min**: Amber spine + slightly more result slides; 2–3 main points only.
- **Poster session**: Amber panels; large figures; minimal text.
- **Internal progress**: Amber spine; may add “open issues / next week” instead of conference summary.

You may **search** public conference-presentation skills or guides (e.g. scientific-slides timing tables, Neutrino speaker guidelines) for length/font/upload rules — cite them as timing tips, not style replacements.

Output of this phase: a numbered **agreed outline** the user has confirmed.

## Phase 2 — Nightly content plan
After structure is agreed, break the outline into a **night-by-night prep schedule** until the deadline (Asia/Shanghai unless user says otherwise).

For each night include:
- Sections/slides to draft or revise
- Figures/numbers still needed from the user
- Stopping point (draft only / ready for collaborator review)
- Optional: next-morning check (did numbers arrive?)

Offer to save this as a **routine** (e.g. nightly reminder + draft the next chunk) only after the user agrees.

Example shape (adapt dates):
| Night | Deliverable | Needs from user |
| --- | --- | --- |
| N1 | Motivation + features bullets | none / one plot |
| N2 | Architecture + variants map | Done/To do status |
| N3 | Training + loss notes | label definition |
| N4 | Performance tables | residual numbers |
| N5 | Physics + summary; abstract polish | approval flags |

## Phase 3 — Draft in Amber voice
When writing approved sections:
1. Physics first: detector goal → background → why reconstruction matters.
2. Short `•` bullets; one idea each.
3. Name subsystems (CD / WCD / TT) and what they measure.
4. Method family tree; Done / To do when useful.
5. Architecture in plain words: inputs → backbone → outputs.
6. Data-driven honesty: labels, coverage limits, augmentation, loss.
7. Numbers with baselines (Traditional vs Method).
8. Physics benchmark (veto / SPN / live-time), not metrics alone.
9. Summary ≤ 4 bullets; WIP dated; no hype.
10. Correct units/isotopes (`9Li/8He`, deg, m, ms).

### Output formats
- **Talk**: `## Slide N — Title` + bullets + `[Figure: …]` placeholders
- **Poster**: panel headings + bullets
- **Abstract**: Indico paragraph + title + keywords
Language: match user; international Indico → English unless asked.

## Quality checklist
- [ ] Intake done; structure **confirmed by user**
- [ ] Nightly plan exists if deadline > 1 day away
- [ ] Amber baseline followed (motivation → method → numbers → physics → summary)
- [ ] Venue timing constraints respected
- [ ] Numbers present or marked TBD
- [ ] No secrets; WIP marked

## External style notes (secondary)
Useful only for length/logistics; never override Amber voice:
- Scientific talk timing guides (~1 idea/slide; 2–3 takeaways per 15–20 min)
- Neutrino-conference speaker notes (e.g. 16:9, large fonts, upload deadlines)
- Generic presentation-builder / conference-materials skills: narrative arc OK; replace their section order with Amber spine unless user explicitly wants a different order for that venue
