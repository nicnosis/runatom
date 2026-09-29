# Runatom Site — Session State

## Status
Branch `redesign/clip` (tag `v1-b2b-cold-email` = old live site, `1d857df`). Repositioned to **media automation & visibility**: clipping (first), cold email, marketing automation. Brief in `REDESIGN.md`. Not yet merged/pushed; main deploys live via GitHub Actions (`.github/workflows/static.yml`).

## Design system (locked)
- Style: Minimalism/Swiss (via `ui-ux-pro-max` skill), refs: missioninbox.com, instantly.ai
- Blue: Tailwind blue scale as `accent`, main `#2563EB` (accent-600), hover `#1D4ED8`
- Font: Plus Jakarta Sans (Google Fonts import in `src/input.css`)
- Text: slate-900 headings, slate-600 body; alternating white / slate-50 sections
- Logo: `runatom-logo.svg` recolored `#2563EB`

## Build
- CSS: `npm run build` (Tailwind 3 CLI, `src/input.css` → `styles.css`); never hand-edit `styles.css`
- Preview: `python3 -m http.server 8742` in repo root
- Headless-Chrome screenshots at width <500 are misleading (500px min-window quirk) — layout is fluid and fine on real mobile

## Next Steps (TODOs flagged with comments in index.html)
1. Swap three `mailto:hello@runatom.com` "Book a demo" hrefs for GHL booking link — **blocked on Nic setting up GHL**
2. Add video to hero section
3. Clipping copy is descriptive only (no case studies yet) — don't add invented proof
