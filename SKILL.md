---
name: HEP progress report
description: >-
  Use when drafting JUNO/HEP progress reports, Indico abstracts, talk outlines,
  or poster text in the Amber-style physics-first slide/poster structure.
---
# HEP progress report (Amber-style)

Generate conference/collaboration progress reports for neutrino/HEP work in the style of Amber muon-reconstruction talks and posters: physics motivation first, clear method variants, data-driven training, quantitative performance vs baselines, then physics impact and a short summary.

## When to use
- Indico abstract, parallel-talk outline, poster panel text, or internal progress slides
- JUNO / neutrino / reconstruction / ML-for-physics updates
- User asks to “write like the Amber report” or pastes Indico links as style refs

## Style rules (match Amber)
1. **Physics first**: open with detector goal → background problem → why this reconstruction matters for sensitivity.
2. **Short bullets**, not long paragraphs. Prefer `•` lists; keep one idea per bullet.
3. **Name the system**: detector (e.g. JUNO 20 kt LS), subsystems (CD / WCD / TT), and what each measures.
4. **Method family tree**: traditional baselines + ML variants side by side; label Done / To do when status matters.
5. **Architecture in plain words**: inputs (hit features), backbone (e.g. self-attention), outputs (track parameters).
6. **Data-driven honesty**: labels (e.g. TT tracks), coverage limits, augmentation (3D rotation), loss (incl. permutation-invariant for multi-track).
7. **Numbers with baselines**: tables or paired bullets (Traditional vs Method) for spatial residual, angle, timing, or rate.
8. **Physics benchmark**: connect tracks to cosmogenic veto / SPN correlations / live-time — not metrics alone.
9. **Summary**: 2–4 bullets — capability established, impact on background, next steps.
10. **Attribution**: speaker/authors, “on behalf of the Collaboration” when appropriate; mark WIP figures with date.
11. **No hype**: avoid marketing adjectives; prefer “demonstrates”, “adopted”, “promising”.
12. **Units and isotopes**: write `9Li/8He`, degrees, meters, ms windows correctly.

## Standard slide / section order (talk)
1. Title — topic, author, affiliation, venue/date, collaboration line
2. Motivation and physical picture
3. Features / observables (what the detector sees)
4. Method overview / architecture diagram caption
5. Model variants (e.g. classification, single-track, multi-track, high-multiplicity OCR-style)
6. Data-driven training + labels + augmentation
7. Per-variant method details (inputs, loss)
8. Performance vs traditional / other ML
9. Physics application (veto, cosmogenic suppression)
10. Summary + outlook

## Standard poster panel order
Left→right / top→bottom:
1. Motivation
2. Reconstruction methods (Traditional | ML family)
3. Reconstruction performance (angular spectra, TT residual comparison)
4. Cosmogenic suppression / physics benchmark
5. Summary + key refs

## Indico abstract recipe
Write 1 dense paragraph (or 2 short ones) that covers, in order:
1. Detector + primary physics goal
2. Background / reconstruction need
3. Method idea (attention / GNN / traditional) and inputs
4. Task-specific models or method set
5. Training strategy (data-driven labels)
6. Key quantitative or deployment claim
7. Closing impact sentence

## Inputs the user should provide (ask only if missing)
- Venue type: talk | poster | abstract | internal progress
- Topic / working title
- What is new since last report
- Key numbers (residuals, angles, rates, inference time)
- Baselines to compare
- Open items / WIP
- Author list and collaboration line

## Output formats
Default to what they asked for. If unspecified:
- **Talk**: markdown slide outline with `## Slide N — Title` and bullets; note where figures go as `[Figure: …]`
- **Poster**: five panel headings with bullet copy
- **Abstract**: Indico-ready paragraph + optional title + 3–5 keywords
Keep Chinese or English to match the user’s request; for international Indico default to English unless they ask for Chinese.

## Quality checklist before delivery
- [ ] Motivation links to a named physics goal
- [ ] Methods named and distinguished
- [ ] At least one quantitative comparison if numbers exist; otherwise explicit “numbers TBD”
- [ ] Physics impact section present
- [ ] Summary ≤ 4 bullets
- [ ] No proprietary secrets; mark WIP where needed

## Reference examples (structure only)
Style anchors (do not copy slides verbatim):
- Talk: Amber self-attention muon track reconstruction (ML4Jets-style): Motivation → Features → Architecture → Variants (S/D/OCR) → Data-driven TT labels → Performance tables → Summary
- Poster: Cosmic muon track reconstruction overview: Motivation | Traditional + ML methods | Performance vs TT | Cosmogenic / SPN benchmark | Summary
