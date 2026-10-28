# Website Change Log

All changes to the Alherz Lab website are recorded here in reverse chronological order.

---

## 2026-10-28

### New Content
- **TOC graphics on the publications page:** Added `images/toc/` with one TOC / graphical-abstract image for each of the 23 publications, named after its `_publications/` file (e.g. `2018-001.png`). Source files were downloaded by hand from the publisher article pages into `Alherz_Website/toc_figures/` (left untouched). All are copied byte-for-byte except `2018-001.png` (Chem Soc Rev, `c7cs00171a-ga.png`), which was scaled from 1536×945 (1.25 MB) to 520×320 (156 KB) to match the other images' 520 px width. Source → target: `c7cs00171a-ga.png`→2018-001, `m_ja8b09653_0009.png`→2018-002, `m_jp8b08536_0008.png`→2018-003, `m_jp7b12093_0017.png`→2018-004, `m_c9cc00928k-ga.png`→2019-001, `m_cs9b04773_0008.png`→2020-001, `m_c9dt04691g-ga.png`→2020-002, `m_ja1c03428_0008.png`→2021-001, `m_jp1c07484_0001.png`→2021-002, `m_jz0c03662_0005.png`→2021-003, `m_d1cp02193a-ga.png`→2021-004, `m_cs2c01832_0001.png`→2022-001, `m_d2ya00114d-ga.png`→2022-002, `Predictive energetic tuning of C-Nucleophiles ….jpg`→2022-003, `m_cs3c01978_0008.png`→2023-001, `m_jp4c06826_0011.png`→2024-001, `m_ec4c00073_0008.png`→2024-002, `m_d5ta01163a-ga.png`→2025-001, `m_ao5c06914_0010.png`→2025-002, `m_tz5c00857_0006.png`→2025-003, `m_ef5c05539_0010.png`→2026-001, `ejic70274-blkfxd-0001-m.jpg`→2026-002, `m_ie6c01601_0009.png`→2026-003.
- **Front matter:** Added `tocimage: 'toc/<id>.<ext>'` (path relative to `/images/`) to every file in `_publications/`.
- **`_includes/archive-single.html`:** For publications with a `tocimage`, renders an `<img class="archive__item-toc">` (lazy-loaded, alt text "TOC graphic for <title>") under the title and adds an `archive__item--toc` modifier class to the `<article>`. Other collections (talks, teaching) are unaffected.
- **`assets/css/main.scss`:** Added `.archive__item-toc` styles: floats right at 40% width (max 400px) from the `$medium` breakpoint (768px) up, and stacks full-width above the text on smaller screens. It has a white background so the transparent RSC graphics stay readable in dark mode. `.archive__item--toc` uses the theme's `clearfix` mixin so tall figures don't spill into the next entry.
- To add a TOC graphic for a future paper: save it as `images/toc/<pub-file-id>.<ext>` and add `tocimage: 'toc/<pub-file-id>.<ext>'` to its front matter.

---

## 2026-08-18

### New Content
- **New publication:** Added `_publications/2026-003.md` — "Molecular Property Prediction via Sparse Binary Matrix Representation and Convolutional Neural Networks," *Industrial & Engineering Chemistry Research*, published online August 15, 2026. DOI: https://doi.org/10.1021/acs.iecr.6c01601. Authors: Alherz, A. W., Tezak, C. R., & Alhajeri, M. S.

### Fixes
- **Talk title (`_talks/2025-SBMR.md`):** Changed title from placeholder "SBMR Model for something something" to "SBMR Model for HOMO and LUMO Energy Predictions."
- **Talk description (`_talks/2025-SBMR.md`):** Superscripted the −1 exponent in "kcal mol−1" using `<sup>` tag.

---

## 2026-07-17 (update 10)

### Style
- Restored `text-align: justify` for `p`, `li`, `.page__content`. Author sidebar name/bio left at original left-aligned defaults.

---

## 2026-07-17 (update 9)

### Reverted
- Removed all text-align changes from `assets/css/main.scss`: reverted justified text and author name/bio centering. Site is back to original left-aligned defaults.

---

## 2026-07-17 (update 8)

### Fixes
- **Author sidebar centering:** Replaced blanket `.author__content { text-align: center }` with a `@media (min-width: 925px)` rule targeting `.author__name` and `.author__bio` directly. On mobile the sidebar is a table-cell layout (avatar left, content right), so blanket centering was pushing the name to the far right of the cell. Now centering only applies on desktop where the sidebar is a full-width block.

---

## 2026-07-17 (update 7)

### Style
- **Centered author sidebar:** Added `text-align: center` to `.author__content` in `assets/css/main.scss` so the name and bio are centered under the profile photo.

---

## 2026-07-17 (update 6)

### Style
- **Justified text:** Added `text-align: justify` to `p`, `li`, and `.page__content` in `assets/css/main.scss` for site-wide justified text.

---

## 2026-07-17 (update 5)

### Fixes
- **Mobile image scaling (about.md):** Fixed all fixed-size images on the homepage to be responsive. Changes: KU Logo (`height:200px` → `max-height:200px; max-width:100%`), CU Boulder logo (`height:100px` → `max-height:100px; max-width:100%`), ResearchAreas.png (`width:800px` → `max-width:100%`), software logos flex container (`width:600px` → `max-width:600px; width:100%; flex-wrap:wrap` with `max-width:40%` per logo so they wrap on small screens).

---

## 2026-07-17 (update 4)

### New Content
- **Replaced CarbonCycle image:** Swapped `images/CarbonCycle.jpeg` for `images/MNCs-TOC.png` in `_pages/about.md`. Fixed inline style from fixed `height:800px` to `max-width:100%; height:auto` for proper mobile scaling.

---

## 2026-07-17 (update 3)

### Analytics
- **GA4 Measurement ID added:** Set `tracking_id: "G-WT34ZS286N"` in `_config.yml` (stream: Alherz Lab Website, URL: https://azizalherz.github.io).

---

## 2026-07-17 (update 2)

### New Content
- **_team/ collection:** Added `_config.yml` entry for `team` collection (`output: false`).
- **Team files:** Created `_team/ali-albather.md` (grad, project: Systematic Improvement of NECs as Liquid Organic Hydrogen Carriers) and `_team/aseel-malallah.md` (undergrad, project: Exploring Potential Applications of Quinones and Thioquinones in Electrochemistry).
- **Group page refactor:** Rewrote `_pages/group.md` to loop over `site.team` filtered by `role` field (graduate / undergraduate / postdoc / alumni). Adding or graduating a member now only requires editing their individual file. Alumni section supports `current_position` field for future use.

---

## 2026-07-17

### Fixes
- **Fix #1 — Removed placeholder files:** Deleted `_portfolio/portfolio-1.md`, `_portfolio/portfolio-2.html`, `_workshops/workshop-1.html`, `_workshops/workshop-1.md` (template placeholders with no real content).
- **Fix #2 — Author name:** Uncommented `name: "Aziz Alherz"` in `_config.yml` so the name appears in the sidebar.
- **Fix #2 — LinkedIn URL:** Changed `linkedin` value in `_config.yml` from full URL to username-only (`alherzaziz`) to match the template's auto-prefix behavior.
- **Fix #2 — Analytics:** Enabled `google-analytics-4` provider in `_config.yml`. Tracking ID placeholder set to `G-XXXXXXXXXX` — must be replaced with real GA4 Measurement ID.
- **Fix #3 — Publication URL:** Fixed `paperurl` in `_publications/2025-003.md` — replaced Google search redirect with direct ACS DOI link `https://pubs.acs.org/doi/full/10.1021/acsmaterialslett.5c00857`.

### New Content
- **Group page:** Created `_pages/group.md` with sections for Graduate Students, Undergraduate Students, Postdoctoral Researchers, and Alumni. Added Aseel Malallah (undergrad) and Ali Albather (grad student).
- **Navigation:** Added "Group" link to `_data/navigation.yml`.
- **New publication:** Added `_publications/2026-002.md` — "Temperature-Driven Nickel Phosphide Phase Transformation and Its Impact on Furfural Hydrogenation Catalysis," *European Journal of Inorganic Chemistry*, July 2026.

### SEO
- Added `description:` meta fields to: `_pages/about.md`, `_pages/publications.html`, `_pages/teaching.html`, `_pages/talks.html`, `_pages/cv.md`, `_pages/group.md`.

### Housekeeping
- Created `log.md` (this file) to track all future changes.
- Updated `CLAUDE.md` with rule to update `log.md` on every edit.
