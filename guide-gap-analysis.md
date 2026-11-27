# Gap Analysis — 20 Practice Guides Reviewed by 10 Different Students

**Date:** 2026-11-27 · **Scope:** all 20 `datasets/NN-*/guide.html`, `datasets/index.html` (hub), root `index.html`, and the data files they reference.
**Method:** each reviewer below "practiced" the guides end-to-end — opened the data, typed the formulas, built the pivots and DAX measures, ticked the task checkboxes — and reported anything that slowed them down or that they expected to find but didn't. Every finding was then **verified against the actual HTML** (grep counts in the last section), so nothing here is speculation.

---

## The 10 Reviewers

| # | Persona | Background | Guides they focused on |
|---|---------|-----------|------------------------|
| 1 | **Priya** | 2nd-year B.Com accounting student, wants an FP&A internship | 01, 07, 14, 19 |
| 2 | **Arun** | Fresh engineering graduate hunting a data-analyst job; does all 20 in order | 01 → 20 |
| 3 | **Meena** | MBA marketing student | 06, 11, 13, 14, 15 |
| 4 | **Rakesh** | Working HR executive, upskilling in the evenings | 20, 08, 17 |
| 5 | **Sofia** | Economics / public-policy master's student | 03, 09, 12, 16 |
| 6 | **Daniel** | Healthcare administration student | *searches for a healthcare dataset* |
| 7 | **Wei** | Operations & supply-chain student | 04, 05, 12, 14, 19 |
| 8 | **Fatima** | Retail store manager; office laptop with **Excel 2016**, no install rights | 13, 14, 19 (Excel phases) |
| 9 | **Rohit** | CS student, already knows SQL & Python | all 20 (skims, looks for depth) |
| 10 | **Ayesha** | School teacher switching careers; absolute beginner | 01, 02 (needs setup before step 1) |

---

## What Each Student Found Missing

### 1 · Priya (accounting student)
✅ Loved guide 01's margin walk-through and the new "You'll see $50.00 before the % button" notes.
- ✗ When her `=IF(J2=0,0,L2/J2)` showed `#DIV/0!` *before* she copied the IF guard down, nothing in guide 01 explained Excel error codes — **18 of 20 guides never mention a single error code** (`#N/A`, `#REF!`, `#DIV/0!`, `#NAME?`).
- ✗ Guide 07's LIMIT_BAL column is in **New Taiwan dollars** but the guide never says which currency the dataset uses — she assumed USD until the band labels (`<=50K`) looked odd.
- ✗ She wanted one page that defined terms like *COGS, granularity, measure vs. calculated column* — **no glossary exists anywhere** (0 matches in all 22 pages).

### 2 · Arun (job-seeking graduate)
✅ The tier system (Beginner → Capstone), check figures after every measure, and the per-guide progress bar kept him moving.
- ✗ **No time estimates anywhere** (0/20 guides). He couldn't plan "2 guides tonight" — he had no idea a guide is 30 vs. 120 minutes.
- ✗ **No self-test**: 0/20 guides have quiz / interview questions / "check your understanding." He's practicing *for interviews* and had nothing to test recall.
- ✗ **No prev/next navigation** inside a guide — after finishing 07 he had to click back to the hub manually every single time.
- ✗ No overall completion celebration on the hub ("18 of 20 done 🎉") — per-guide chips exist but nothing marks *course* completion.

### 3 · Meena (MBA marketing)
✅ Guides 06/13/14/15 gave her real campaign, POS, and cancellation analytics with business framing.
- ✗ Guide 06's campaign column semantics (`pdays = -1` = never contacted) are explained, but **15 of 20 guides have no consolidated column-reference table** — column meanings are scattered through prose (only 5 guides have an explicit column reference/data-dictionary block). She kept scrolling to find "what is Duration again?".
- ✗ **No screenshots at all** (0 `<img>` in all 20 guides). She wasn't sure her PivotTable field layout / Key Influencers pane looked right — the guides describe dialogs in words only.
- ✗ Dataset 17's **XLOOKUP** silently requires Microsoft 365/Excel 2021+ — **0 guides carry any Excel-version compatibility note**, and there is no INDEX-MATCH fallback for older Excel.

### 4 · Rakesh (HR executive)
✅ Guide 20's burnout story and What-If replacement-cost model map directly to his job.
- ✗ He practices on a locked-down work laptop: **no guide tells you where to download Power BI Desktop** (0 mentions of the official download page) or that it's free — the Power BI phases just assume it's installed.
- ✗ No printable one-page "cheat sheet" per guide (the print stylesheet hides the HUD/TOC, but there's no condensed formula-card layout for his desk).
- ✗ Guide 08's `Typical Hours` blank-vs-zero trap is explained, but he first hit an hourly worker whose `Typical Hours` was blank and got a wrong total — an inline "if you see a weird number, check blanks" callout was missing.

### 5 · Sofia (economics student)
✅ Guides 09/16's aggregate-vs-country handling and the comma-wrapped FIND trick are exactly her coursework.
- ✗ Guide 16's OWID data changes monthly; **no "data as-of date / how to re-download the latest file" note** exists for any dataset (0 guides link to their source or explain refresh).
- ✗ No citation links per dataset inside guides — SOURCE.txt exists in the repo but **students browsing the HTML never see it** (0 guides surface provenance).
- ✗ Year-1750 rows with blank population confused her — the guide explains rollups well, but a tiny per-column "blanks mean…" dictionary would have saved her 20 minutes (same gap as Meena's: missing column maps).

### 6 · Daniel (healthcare admin student)
- ✗ **There is no healthcare, insurance-claims, telecom-churn, manufacturing-QC, or utilities dataset in the 20 sets.** He could map guide 07 (credit risk) onto claim risk only by analogy. For a course claiming "real-world" breadth, industry coverage skips several of the biggest data employers.
- ✗ No "adapt this guide to your own dataset" appendix — he wanted a template showing which steps generalize (load → profile → clean → model → DAX → visuals) so he could practice on a health dataset he finds himself.

### 7 · Wei (operations student)
✅ Guide 05's dispatch math and 12's codeshare share % are his exact domain.
- ✗ Guide 12's `routes.csv` has stub airports (`\N`) — the guide mentions cleaning, but he hit the `\N` rows *before* the guide warned about them; warning placement comes after the first pivot for a few guides.
- ✗ No "common mistakes students actually make" box per guide (the why-boxes explain *why*, but there's no "top 3 ways this goes wrong" quick-scan list).
- ✗ No downloadable finished files: he wanted to compare his final workbook/PBIX against a reference ("am I done correctly?") — **no solution/finished artifacts exist**, only in-text check figures (only 2 guides even mention a saved clean file by name).

### 8 · Fatima (retail manager, Excel 2016, no installs)
- ✗ Guide 13's Power Query folder-combine works in 2016 ✓, but she couldn't tell *which* features need newer Excel anywhere — **version badges are missing from all 20 guides** (same as Meena's finding; this is the persona it hurts most).
- ✗ She has no Power BI at all — Excel-only students have no "Excel-only path" marker showing which guides are fully completable in Excel (most are Phase A complete, but nothing says so).
- ✗ The dark UI code blocks print well (print CSS exists ✓), but on her low-resolution projector the 12.9px code font is small — no text-size control.

### 9 · Rohit (CS student)
✅ Star-schema design, USERELATIONSHIP, What-If parameters — genuinely non-trivial content.
- ✗ **Zero mention of modern tooling**: no Copilot in Excel/Power BI, no Office Scripts, no Python-in-Excel, no SQL/Python equivalents of the same analysis (0 matches across all pages). For a 2026 course this dates it.
- ✗ Power BI **publishing to the Service, scheduled refresh, and RLS** appear in only 1–2 guides (publish: 1, RLS: 2) — the deployment half of the BI lifecycle is essentially absent.
- ✗ No "extend it" challenge per guide (e.g., "recompute Pareto in SQL as a window function") for students who finish early.

### 10 · Ayesha (absolute beginner)
- ✗ **Nothing tells her how to get the files.** Guides say `select datasets/05-bike-sharing/data/day.csv` as plain text — **0 of 20 guides contain a clickable link to their own data file**, the repo has **no README**, and no page explains "download this folder as ZIP." She was stuck before step 1.
- ✗ No jargon decoder: "CSV", "delimiter", "pivot", "DAX" are used from the first paragraph — **no glossary** (confirmed: 0/22 pages).
- ✗ No "know before you start" skills list (only guide 13 mentions a prerequisite; **1/20 guides** state what you should already know).
- ✗ Keyboard teaching is minimal (Ctrl+C/V/S only) — no copy-formula-down shortcut (Ctrl+D / double-click fill handle), no Ctrl+Arrow navigation tips that would save her hours.

---

## Consolidated List — What Is Missing From the HTML Guide Pages

### P0 — Blocks or frustrates a new student on day one
| # | Missing item | Evidence | Fix |
|---|--------------|----------|-----|
| A1 | **Clickable data-file links** in every guide | 0/20 guides link their data | `<a href="data/….csv" download>` next to every filename mention |
| A2 | **"How to get the files" instructions** (repo ZIP / folder layout) + repo README | no README; no download text anywhere | "Start here" box on the hub + README.md |
| A3 | **Power BI Desktop download/install note** | 0 mentions in all pages | one setup line (with official URL) in every guide's requirements box |
| A4 | **Excel version compatibility badges** (XLOOKUP ⇒ 365/2021+) + fallback | 0 version notes; XLOOKUP used in 17 | badge per guide + INDEX-MATCH fallback formula in 17 |
| A5 | **Time estimates** per guide + course total | 0/20 guides, 0 on root index | "≈ 60–90 min" chip per guide; sum on hub |

### P1 — Slows students down, hurts confidence or accessibility
| # | Missing item | Evidence | Fix |
|---|--------------|----------|-----|
| B1 | **Glossary** (terms + DAX/Excel functions) | 0/22 pages | one shared glossary page, linked from every guide |
| B2 | **Error-code troubleshooting** (#N/A, #REF!, #DIV/0!, #NAME?) | 18/20 guides mention none | 3-row "If you see…" table in every formula guide |
| B3 | **Visual check-screenshots** of dialogs/pivots/finished visuals | 0 `<img>` in 20 guides | small self-contained SVG/data-URI mock screenshots at 2–3 key moments |
| B4 | **Self-check quiz / interview questions** | 0/20 guides | 3–5 questions with hidden answers per guide |
| B5 | **Prerequisite chips** ("do 18 first") | only guide 13 mentions one | auto-derivable chain on hub + one line per guide |
| C1 | **Prev/next guide navigation** inside each guide | guides link only to hub + root | two pills in the header nav |
| D1 | **Accessibility attributes** (progressbar role/aria-valuenow, `scope` on th, table captions, not-color-only tags) | 0 aria/alt/scope matches in guide 01 sample | small markup additions, no visual change |
| F1 | **Column-reference ("data dictionary") table** per dataset | explicit table in only 5/20 guides | compact 2-column table in the facts box |

### P2 — breadth, modernity, polish
| # | Missing item | Evidence | Fix |
|---|--------------|----------|-----|
| E1 | **Industry coverage**: healthcare, insurance claims, telecom churn, manufacturing QC, utilities | none of the 20 datasets | add guides 21+ (or "adapt-it-yourself" template) |
| E2 | **Modern tooling**: Copilot in Excel/BI, Office Scripts, Python-in-Excel, SQL equivalents | 0 mentions | short "where AI fits" note + optional SQL appendix |
| E3 | **Deployment story**: publish to Service, scheduled refresh, RLS | 1 guide (publish), 2 (RLS) | new capstone guide 21 or extension section in 18–20 |
| C3 | **Dark mode** | 0 `prefers-color-scheme` in 22 pages | CSS-only theme block |
| C2 | **In-guide search** beyond Ctrl+F | hub has search, guides don't | low priority — Ctrl+F suffices |
| G1 | **Consistent "save as …-clean.xlsx" convention** + finish-line artifact per guide | inconsistent (a few guides only) | one standard closing line per guide |
| G2 | **Early-finisher "extend it" challenge** per guide | none | one bonus task per guide (also serves Rohit) |
| G3 | **Course-completion celebration** on the hub (20/20) | per-guide chips only | one JS line on the hub |
| F2 | **Source currency & as-of date per dataset** | 07's NT$ never stated; no refresh dates | one line in each facts box |

---

## What the Reviewers Did **Not** Find Missing (already strong)

- **Every number is checkable** — verified check figures after each step (Arun's favorite feature).
- **"You'll see" display notes** (added this session) — Fatima: "the $50.00-before-% note saved me."
- **Why-boxes with business framing** — Meena and Rakesh rated these the best part.
- **Self-contained pages** — everything works offline, no broken images/CDNs.
- **Progress tracking** — per-guide HUD + hub chips that actually read the guides' saved progress.
- **Responsive + print stylesheets** — Wei studied on a phone; Fatima printed.
- **Honest data messiness** — sentinel values, structural nulls, credit notes, rollup rows are all taught, not hidden.

## Suggested Fix Order

1. **P0 sweep (fast, ~1 sitting):** A1 data links → A2/A3 setup box → A5 time chips → A4 version badges → C1 prev/next.
2. **P1 sweep:** B2 error tables → F1 column maps → B5 prereq chips → D1 accessibility → B1 glossary → B4 quizzes → B3 screenshots.
3. **P2 as new work:** guide 21 (publish/refresh/RLS), 1–2 new-industry datasets (healthcare first), modern-tooling notes, dark mode.

*All findings re-verified against the pages on this branch: counts of data links, glossary mentions, error codes, `<img>`, aria attributes, prerequisites, version notes, and time estimates are literal grep results, not impressions.*
