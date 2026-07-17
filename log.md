# Website Change Log

All changes to the Alherz Lab website are recorded here in reverse chronological order.

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
