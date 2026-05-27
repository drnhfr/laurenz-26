# laurenz.drnh.fr — Birthday Gift Website

## What this is
A single-page password-protected birthday gift reveal for **Laurenz**, gifted by Moritz & Julian.
The site is hosted at `laurenz.drnh.fr` via GitHub Pages.

## Password / Unlock
Coordinate input: `47.776194, 12.292800`
(The STUBN / Frasdorfer Hütte coordinates — Laurenz must enter these to unlock the page)

## One thing to configure before deploying
In `index.html`, find the line:
```js
const to = 'DEINE-EMAIL@example.com';
```
Replace with **Moritz's actual email address** so the mailto pre-fill works correctly.

## Deployment (GitHub Pages)
1. Commit `index.html` and `CNAME` to `main` branch root
2. GitHub → Settings → Pages → Deploy from branch: `main`, folder: `/ (root)`
3. DNS: Add `CNAME` record: `laurenz` → `<github-username>.github.io`
4. Wait ~5 min for DNS propagation

## Architecture
- Pure `index.html` — no build step, no dependencies, no framework
- All fonts via Google Fonts CDN
- All JS is vanilla (Intersection Observer, Canvas API, mailto)

## If you want to change anything
- **Dates**: Search for `20.` and `27.` in the HTML
- **Names**: Search for `Julian` or `Moritz`
- **Menu courses**: The 4 `.course` divs in the menu section
- **Komoot link**: The `href` on `.klink`

## Page structure
1. Lock screen (star canvas + mountain SVG + coordinate input)
2. Hero: "Eine Einladung." 
3. Section 01: Route (stats grid + elevation profile animation)
4. Section 02: Chiemgauer Alpen (two-col layout + highlights)
5. Section 03: Küche (chef card + example dishes)
6. Section 04: 4-Gänge Menü (full-width dark panel)
7. Section 05: Date picker (20.06.26 / 27.06.26) + mailto CTA
8. Footer
