# Runatom Site — Session State

## Status
Branch `redesign/clip` pushed to origin (tag `v1-b2b-cold-email` = old live site, `1d857df`). **Not merged to main**, so runatom.com is still the old B2B cold email site; main deploys via GitHub Actions (`.github/workflows/static.yml`).
Redesign = media automation & visibility, services in order: clipping, cold email, marketing automation (clipping targets creators and brands). Brief: `REDESIGN.md` (**untracked**, Nic hasn't said whether to commit it).

Current copy (Nic chose it, irreverent on purpose): hero badge "Fire your stupid agency", h1 "Get eyeballs on your thing", CTA heading "Fire your stupid agency." Keep the tone; don't soften.

## Design system (locked)
- Style: Minimalism/Swiss (via `ui-ux-pro-max` skill), refs: missioninbox.com, instantly.ai
- Blue: Tailwind blue scale as `accent`, main `#2563EB` (accent-600), hover `#1D4ED8`
- Font: Plus Jakarta Sans (Google Fonts import in `src/input.css`)
- Text: slate-900 headings, slate-600 body; alternating white / slate-50 sections
- Logo: `runatom-logo.svg` recolored `#2563EB`

## Build
- CSS: `npm run build` (Tailwind 3 CLI, `src/input.css` → `styles.css`); never hand-edit `styles.css`
- Preview: `python3 -m http.server 8742` had stale/hanging issues in Nic's Brave; use `python3 -c "import http.server as h\nclass H(h.SimpleHTTPRequestHandler):\n def end_headers(self): self.send_header('Cache-Control','no-store'); super().end_headers()\nh.ThreadingHTTPServer(('127.0.0.1',8800),H).serve_forever()"` and open `http://127.0.0.1:8800/`
- Sections fade in on scroll (`.reveal` in `script.js`), so below-the-fold content looks blank until scrolled to; the CTA is at the bottom, not in the hero
- Headless-Chrome screenshots at width <500 are misleading (500px min-window quirk) — layout is fluid and fine on real mobile

## Next Steps
1. Ask Nic: merge `redesign/clip` into `main` to go live? (PR: github.com/nicnosis/runatom/pull/new/redesign/clip). Also commit `REDESIGN.md`?
2. Swap three `mailto:hello@runatom.com` "Book a demo" hrefs for GHL booking link, **blocked on Nic setting up GHL**
3. Add video to hero section (TODO comment in `index.html`)
4. Clipping copy is descriptive only (no case studies yet), so don't add invented proof
