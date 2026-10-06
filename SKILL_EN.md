---
name: community-info-visual
description: Community Public-Information Key-Visual Design Skill. Organizes any set of community public information (protection alerts, service notices, wayfinding, emergency notices, procedure guides, etc.) into a poster key visual that residents can recognize at a glance and that carries zero information error (Chinese & English bilingual). Its core strength is topic independence — whether the subject is heat, cold waves, power outages, vaccination, or a procedure guide, the same pipeline applies: inventory → filter → pick skeleton → layered production → dual-gate acceptance. Use when the user needs to turn a batch of community public-information material into a 4:5 portrait poster or other public-information visual.
metadata:
  version: "2.4.0"
  course: AI and Design Innovation
---

# Community Public-Information Key-Visual Design Skill

This is a **topic-agnostic** Skill. The brief will change (heat protection, cold-wave alerts, community power-outage notices, vaccination drives, procedure guides…), but the underlying proposition never does:

> **Turn a batch of community public information into a key visual that residents can recognize at a glance and whose key information carries zero error.**

So this Skill is not written around any single topic. It provides **one production pipeline whose visual intensity is set by the information's tone**. The first action is to judge the tone, then decide visual intensity and hierarchy emphasis.

## 0. Brief Assessment (step one — it sets visual intensity and hierarchy emphasis)

This Skill serves one proposition only: **organizing and presenting complex community public information**. The decision is driven by the **communication goal** (what residents must do), not by the topic word:

| Tone | Nature of information | Communication goal | Typical briefs | Priority |
| --- | --- | --- | --- | --- |
| **Emergency alert** (high urgency) | Action directives + urgency (when it is dangerous, what to do now) | Get residents to **act correctly at once**, avoid wasted trips | Heat/cold-wave/storm protection, power or water outage, gas & electrical safety, temporary controls | **Recognition speed first**: understand in 3s, get the action in 10s |
| **Service notice** (low urgency) | Service facts + procedure guidance (place, time, process, phone) | Let residents **know where to go and how to proceed** | Service-point opening, vaccination, health check-ups, administrative procedures, benefit notices, supply distribution | **Clarity and order first**: conclusion first, then the path |

- A single poster may contain zones of both tones (e.g., an emergency strip on top, a service-guidance zone below), but the plan must state which part is recognition-first and which is reference-first; each zone's visual intensity matches its own tone.
- **Both tones run the same production pipeline** (steps 1–6 are identical): inventory → filter → pick skeleton → layered production → dual-gate acceptance. Tone changes visual intensity and hierarchy emphasis only — never the accuracy or readability bottom line.
- **Elder-friendly is ON by default**: community information assumes elderly residents and child caregivers (see [Readability & Audience Fit](references/readability-and-elderly.md)).

Three bottom lines (enforced throughout; any violation means rework):

1. **Zero information error, zero fact fabrication**: Times, locations, phone numbers, names, and procedure steps must match the locked master copy verbatim. Any phone number, community name, address, time, or quantity **absent from the master copy must never be fabricated or filled with a "plausible-looking" sample value** — list it on the fact-confirmation sheet for the user; until confirmed, use a conspicuous `【TBC】` placeholder. Text rendered by AI image generation is never trustworthy; key information must be typeset in post-production.
2. **Recognition with metrics**: emergency alert uses "what it is in 3s / the action in 10s / the details in 30s"; service notice uses "what this is about in 3s / time and place in 10s / contact and process in 30s". Either way, the main title and key information must be legible at a distance.
3. **Audience fit**: community information assumes elderly residents and child caregivers, so elder-friendly is on by default; contrast and minimum type size are **never exempt**.

**Two human confirmation gates (hard stops, never skip)**:

- **Gate ① (fact-confirmation gate, at the end of step 2)**: before concept development, present a **fact-confirmation sheet** — every phone number, community/institution name, address, time, and quantity to appear on the poster, plus all `【TBC】` placeholders and proposed copy expansions — and **wait for the user's explicit confirmation or correction**. Without the user's go-ahead, do not proceed to step 3.
- **Gate ② (layout-plan gate, at the end of step 3)**: before production, present the layout plan (skeleton + style + zonal sketch) with **2–3 distinct layout options** and each option's trade-offs; start generation only after the user picks one. Do not decide on the user's behalf.
- The point of both gates: convert the cost of "wrong direction → redo everything" into the cost of "one confirmation".

## 1. Requirements Analysis & Input Inventory

Before starting, inventory the inputs item by item and record each as "confirmed / missing":

| Input | Description |
| --- | --- |
| Communication goal | Read from the brief what residents must do (act now / go and get service / understand a policy); it decides the information tone |
| Audience profile | Age, language, presence of elderly or international visitors — decides the elder-friendly tier and language strategy |
| Locked master copy | Official bilingual (CN-EN) text: names, times, locations, phone, items. **The master copy is the single source of truth** |
| Canvas spec | Default: portrait 4:5, PNG output; follow the user when they specify otherwise |
| Graphic assets | Scene photos, institutional logos, existing icons, diagram assets. User-provided assets take priority over AI generation |

- When key items are missing (especially times, locations, phone numbers in the master copy): put them on the fact-confirmation sheet (Gate ①). **Never fabricate; never fill with sample values** (fake numbers and names get spread as real). If a placeholder is truly needed, mark it with a conspicuous `【TBC】` flag; placeholder items must not enter the final image before Gate ① passes.
- Distinguish "content locked verbatim" (institution name, title, action items, times, locations, phone, fees) from "creatable parts" (visual style, scene illustration, decorative graphics, copy tone). Confusing the two is the most common accident.
- **Switching briefs**: when the topic changes, do not carry over the previous case's checklist; return to this table, inventory the new brief's information items completely, then proceed to step 2.

## 2. Material Organization, Information Filtering & Grading

- Sort the master copy into an information hierarchy and write an inventory table (item / Chinese / English / level / rendering method). **Levels follow the table below**:

  | Level | Content |
  | --- | --- |
  | **L1 Recognition** (3s) | Main title + logo + key visual: what this is, does it concern me |
  | **L2 Action** (10s) | What to do / where to go / when (service point + hours + phone) |
  | **L3 Detail** (30s) | Help-seeking, precautions, procedure details, required documents, full English text |

- **Filter item by item — never default to including everything**: The master copy is the source of truth, not the layout list. Every entry must receive a verdict — lock verbatim / compress (a paragraph → one sentence + bolded keywords) / pointerize (replace with QR code or signpost) / drop. Record every verdict in the "not-included items list" and disclose it in the delivery notes. See [Information Filtering & Density Grading](references/information-filtering.md).
- **Assign a density grade (D-grade)**: count the content blocks on the poster (one indivisible information unit = 1 block) — ≤5 blocks = D1 (sparse: supplement + large-scale division), 6–10 = D2 (standard typography), **>10 = D3 (overload: filter down to ≤10 blocks before any typesetting; the first move is to cut and merge, never to shrink type)**. The D-grade determines skeleton and illustration strategy.
- Each L2 entry must be "one action / one fact, one sentence." Split long sentences; do not merge. Confirm compound-sentence splits with the user first.
- Order information by the **audience's decision sequence**: when to be alert → what to do → where to go → when to seek help; for a service notice: what this is → when & where → how to proceed → how to ask.
- Bilingual does not mean "a shrunken English copy tucked in a corner." The English version is an independent deliverable with an identical hierarchy; verify item by item against the Chinese version (see [Information Accuracy & Master-Copy Verification](references/information-accuracy.md)).

> **⛔ Gate ① (fact-confirmation gate)**: at the end of this step, present the **fact-confirmation sheet** — every phone number, name, address, time, and quantity to appear on the poster, plus all `【TBC】` placeholders and proposed copy expansions — and **stop until the user explicitly confirms or corrects**. No reply = not confirmed; the pipeline halts here.

## 3. Concept Development

- Set the tone from the information tone and audience; choose a main style + supporting strategy from the [Visual Style Library](references/visual-style-library.md), with a one-sentence rationale. **Default tone-style matching**:

  | Tone | Default style direction | Avoid |
  | --- | --- | --- |
  | Emergency alert | S1 mono-color alert, S4 high-saturation sticker, S5 dot-matrix diagram — high contrast, strong recognition; panoramic themes use S11 | Low-contrast art styles (unless a readability compensation plan is given) |
  | Service notice | S2 map wayfinding, S3 editorial, S7 illustration narrative, S9 journal grid, S11 panoramic narrative, color-block/puzzle languages — clear, orderly, friendly | Decoration overpowering readability; alert strips used as ornament |

- **Choose a layout skeleton**: style is the "skin", skeleton is the "bones". From the skeleton library (B1–B10, incl. full-canvas illustration) in [Layout Composition & Illustration Directives](references/layout-composition.md), pick a skeleton by density grade and information temperament, with a one-sentence rationale. **Hard rule: form follows content** — parallel short items of the same kind use vertical column cards; a single long warning or reminder uses a full-width bar; two sections of similar weight sit **side by side in two columns** filling each other's horizontal gaps; no full-page stack of equal-width horizontal bars, at most 2 full-width info rows; side-by-side columns must align at top and bottom lines (surplus height distributed across the cards); **every card group carries a group heading** (summarizing what the group is / when / where / what it provides, the heading hugging its own group); ≥ 3 levels of type-size contrast.
- **Density-based visual strategy (the D-grade directly sets layout & illustration tactics)**:

  | D-grade | Layout strategy | Key-visual area | Illustration requirement |
  | --- | --- | --- | --- |
  | **D2–D3 (info-rich)** | **Compact and orderly**: tighten the info zones without losing breathing room (block spacing still meets spec) | **≥ 25%**, however dense the info | Illustration must carry **real complexity** — figures + props + scene depth; **a "color block + one sun" token key visual is forbidden** (see layout-composition.md §3.0 complexity standard) |
  | **D1 (info-sparse)** | First **expand the copy** (see information-filtering.md §5.1; expansion passes Gate ①), then divide the canvas into large zones | **≥ 65%**, the illustration is the protagonist | Same complexity requirement: multiple figures / buildings / rich props & fill layers — sparse info never means a simpler illustration |

- **Illustration decision**: answer the three questions from layout-composition.md §3 — "what does it act out / where does it sit / how does it relate to the text". An illustration is a **visualized call to action** (acting out "how to do it") and must connect to a concrete information entry; pure decoration is not allowed. D1/D2 carries illustrations by default. **Complexity is verified against §3.0; failing it means rework.** While planning, tick the **image-text craft** items to use from layout-composition.md §5 (numbering through, speech bubble, callout lines, path as flow, texture fill…) — they constrain post-production typesetting and also go into the image prompt's composition slots.
- Style decisions follow the tone's priority (emergency alert = recognition speed only; service notice = clarity and order first, appeal may add value, without regressing readability).
- Produce a text-based layout plan (no drawing yet): position, proportion, hierarchy, icon and illustration concept of each information block. Enter generation only after the information architecture holds.
- Institutional logos and organizer logos must not be redrawn or AI-regenerated; use the original image or a vector reconstruction.

> **⛔ Gate ② (layout-plan gate)**: at the end of this step, present **2–3 distinct layout options** (each = skeleton + style + one-sentence trade-off + a simple zonal sketch) and start step 4 only after the user **explicitly picks one** (or gives revision notes). Never decide "I'll just go with option A" on the user's behalf.

## 4. Generation & Production (Layered Production Route)

**Core technical route: graphics and backgrounds may be AI-generated; text and key information must be typeset in post-production.** (Always true, whatever the brief.)

- AI image generation is used for: scene backgrounds, **narrative illustrations / key-visual imagery**, decorative graphics, icon drafts. Follow the prompt template in [Layout Composition & Illustration Directives](references/layout-composition.md) §3.2: fill the six slots (style / scene / subject action or form / composition with reserved whitespace / palette / negatives), with **whitespace reserved up front** (text lands on the light areas left open). After generation, run three checks: no residual text, no watermark residue, palette consistent with the poster.
- All readable text, numbers, times, phone numbers, locations, and names on the final image are overlaid via post-production typesetting (code typesetting or design-tool typesetting). **Never rely on AI image generation to render text.**
- When the user provides scene assets (e.g., community photos or service-point photos), add icons and information layers on top; do not regenerate the whole image.
- Keep the icon system consistent across the poster: one line/filled language, one stroke weight, one corner-radius rule; icons are always paired with text and never carry meaning alone. **Gap spacing follows Hard Rule 9 of layout-composition.md**: icon-to-text ≥ 0.4× icon height, icon-to-icon ≥ 0.5× within a group / ≥ 0.8× across groups, icon-to-container-edge ≥ 0.5×; same-group icons share size, axis alignment, and equal spacing.
- Apply contrast and font sizes per the [Readability & Audience Fit](references/readability-and-elderly.md) spec; when the background is busy, add a solid panel or soft mask behind text — never place text directly over high-texture photos (especially when photos or illustrations sit behind the text).
- When comparing multiple generated drafts, judge only "background & graphic quality"; the text layer is uniformly applied afterwards, so AI-rendered wrong text never misleads the comparison.

## 5. Evaluation & Acceptance (Independent Gates, Item by Item)

Never judge merely "the poster was generated." Acceptance has two independent channels; both must pass:

**Channel A: Information accuracy (verbatim check against the master copy)**
- [ ] Every CN/EN entry matches the master copy verbatim; numbers, times, phone numbers, place names, and names ticked off one by one
- [ ] No residual AI-rendered text errors (check backgrounds, icon interiors, decorations for hidden glyphs)
- [ ] **Information skeleton complete**: what it is (name/cause) + when + where + what to do / how to proceed + how to ask (where applicable) — check each item the current brief's master copy actually contains; do not apply another brief's items
- [ ] Bilingual versions match in hierarchy, item count, and order

**Channel B: Readability & Layout (check the final image against the spec, not the parameters)**
- [ ] Time test passes (what it is in 3s / the action or time-and-place in 10s / contact and details in 30s)
- [ ] Minimum body font size and contrast meet spec; step up the elder-friendly tier for elderly-dominant audiences
- [ ] No text overflow, no overlaps, no text fighting background textures (photo/illustration backgrounds must carry a panel or mask)
- [ ] Icons consistent in style; every icon meaning backed by text; **icon gap spacing meets Hard Rule 9 (icon-text / icon-icon / icon-container margins ≥ specified multiples; same-group icons aligned on one axis with equal spacing)**
- [ ] **Group heading & grid rhythm meet Hard Rule 10**: every card group has a semantic group heading; the heading hugs its own group (near below, far above); multi-row card grids keep row gap ≥ column gap; between-group gap ≥ 1.5× within-group card gap
- [ ] **Layout checks**: no full-page equal-width bar stack; key-visual area meets spec; parallel info points use a form matching their content (vertical cards / full-width bars / side-by-side columns), ≤ 2 full-width info rows; side-by-side columns aligned at top and bottom lines, no continuous right-side void ≥ 1/4 of the canvas width; ≥ 3 levels of type-size contrast; at least 1–3 keywords or key visuals rendered as oversized graphic anchors; block spacing gives the layout breathing room
- [ ] **Illustration checks**: every illustration maps to the information it serves; placed adjacent to its text; no residual text or watermarks; **complexity meets §3.0 — the key visual is not a "color block + single symbol" token combo**; key-visual share matches the D-grade strategy (D2–D3 ≥ 25%, D1 ≥ 65%)

If any item fails: fix → re-export → re-check that item. **Keep check records in the workspace; never record an unexecuted check as passed.**

## 6. Iteration & Delivery

- Each iteration keeps an issue list (issue / source / fix / re-check result); fix, re-check, and never leave an "it should be fine" item open.
- Deliverables: Chinese poster PNG, English poster PNG, information inventory table, acceptance record.
- The delivery note lists only unresolved limitations (missing information, unconfirmed placeholders), never inflated completion claims.
- When the user gives feedback, first confirm whether it targets "information hierarchy/filtering" or "visual style" — the two follow different fix paths; mixing them up often breaks what was right.
- **When switching briefs**: the new brief reuses this pipeline, but the inventory, D-grade, style, skeleton, and acceptance items must all be re-derived for the new brief. Treat the previous case's outputs (skeleton, style, list) as experience, not as a template to copy.

## References (Load as Needed)

- [Information Filtering & Density Grading](references/information-filtering.md) — required for step 2; filtering criteria, cut-order priorities, D-grade assignment, and both playbooks (dense → cut, sparse → supplement)
- [Information Accuracy & Master-Copy Verification](references/information-accuracy.md) — required for steps 1, 2, 5; verification workflow and placeholder rules
- [Readability & Audience Fit](references/readability-and-elderly.md) — required for steps 4, 5; font sizes, contrast, elder-friendly tiers (by audience), pixel-forensics rules
- [Layout Composition & Illustration Directives](references/layout-composition.md) — required for steps 3, 4; ten layout skeletons (B1–B10, incl. chapter cards / path guide / big-number anchor grid / full-canvas illustration), layout hard rules (incl. form-choosing, side-by-side alignment, icon gap spacing, and group heading & grid rhythm), illustration prompt template, and the §5 image-text craft library
- [Visual Style Library](references/visual-style-library.md) — required for step 3; style profiles (S1–S11), tone-matching table, and applicable conditions
