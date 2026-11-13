# math-31103

Public-facing Quarto course site for **Algebraic Structures 1** (MATH 31103), an undergraduate
abstract algebra course at UA Little Rock. Sibling to the main site
[matthewhester.com](https://matthewhester.com); lives at `/math-31103/` under that domain.

## Status: draft preview, not listed in the Course Library

This site is a **draft preview**, deliberately not carried in `courses.yml` on the hub, so it does
not appear in the Course Library listing. It is reachable only by its direct path.

The **course** is an established catalog course. The **public materials** here are an early draft
and have not been reviewed for correctness, pedagogical adequacy, or accessibility conformance.

## What this draft does and does not claim

**The term window is read, not guessed.** The dates shown, 24 August through 7 December 2026, are
the Fall 2026 full-term window published in the UA Little Rock AY2027 academic calendar, read on
31 August 2026. That is the university's calendar, not any section's own schedule.

**No assessment dates, coverage, or weights appear anywhere on this site.** The source syllabus
refers throughout to a course calendar that was not part of the document, so quiz dates, examination
dates, and what each examination covers were simply not available to this draft. Rather than invent
them, the site carries none. **The learning management system remains authoritative for section
logistics, dates, and every graded detail**, and the site says so on the syllabus and schedule pages.

**The division into fifteen weekly units is an authoring decision.** The source syllabus gives an
eight-item course outline and no week-by-week schedule. The eight items appear here in the order the
syllabus gives them, and every named sub-topic appears in exactly one week, but the placement of the
block boundaries inside the term is not a departmental one. Three developments go slightly past the
outline's exact wording: quotient groups in Week 10, the first isomorphism theorem in Week 12, and a
brief introduction to ideals in Week 14.

**Sources are zero-cost, and their licences are not confirmed here.** The course text, Judson's
*Abstract Algebra: Theory and Applications*, is openly published and is the text the syllabus itself
names; it is linked at the address the syllabus gives. MIT OpenCourseWare 18.703 and Group Explorer 3
are the two supporting references. All three were reachable at no cost when this draft was written.
Availability and licence terms are recorded as declared or unverified, never as verified, and no
rights determination is made or implied. Nothing from any source is reproduced or adapted here.

## What is here

- `index.qmd` — landing page, outcomes, how the course runs
- `syllabus.qmd` — syllabus summary; the LMS stays authoritative
- `schedule.qmd` — the fifteen units and the term window
- `notes/` — the fifteen unit notes, Weeks 1 through 15, about 39,000 words
- `resources/` — the open references
- `assets/figures/` — 60 static SVG figures, one folder per unit
- `styles/` — the course-family stylesheet, and `site_look.css` layered after it (see
  Provenance)

## Build

```
quarto render --no-execute
```

Code execution is disabled end to end: `_quarto.yml` sets `execute: enabled: false`, and no page
carries an executable cell. Mathematics renders as browser-native MathML, so the site pulls no script
from any external host.

`_site/` is a build artefact and is not committed. The hub workflow
(`matthewhester-site/.github/workflows/publish.yml`) renders this repo and copies its `_site/` into
the combined site at `/math-31103/`.

## Provenance

The private authoring workspace — approval packet, resolved plan, asset bundle, per-unit records, and
build state — stays on Drive and is excluded by `.gitignore`. It must never reach this repo.

This copy differs from the authoring draft in two respects, both only in presentation.

First, the sidebar labels here read `1 — Sets, functions, and binary operations` rather than
`1 — Week 1 — Sets, functions, and binary operations`. The site shell numbers each unit row, and the
unit titles also open with the week number, so the generated labels repeated it.

Second, `styles/site_look.css` is added, with its entry in the `css` list of `_quarto.yml`. It
carries the course-family look from 2026-11-13: white page, square corners, one accent color, a smaller
landing poster, and the navbar and footer aligned to the page.
`styles/course_family_sections.css` is the kernel's pinned asset and is unchanged. A re-promote must
keep the second stylesheet and its `css` entry, until the kernel's own stylesheet carries the look.

The page headings, the schedule table, and every word of the notes are unchanged.
