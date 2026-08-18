# Website Change Log

All changes to the Alherz Lab website are recorded here in reverse chronological order.

---

## 2026-08-18

### New Content
- **New publication:** Added `_publications/2026-003.md` — "Molecular Property Prediction via Sparse Binary Matrix Representation and Convolutional Neural Networks," *Industrial & Engineering Chemistry Research*, published online August 15, 2026. DOI: https://doi.org/10.1021/acs.iecr.6c01601. Authors: Alherz, A. W., Tezak, C. R., & Alhajeri, M. S.

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
