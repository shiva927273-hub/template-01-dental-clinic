# Template 01 — Dental Clinic

A single-file, no-build website template for a dental clinic. Open `index.html`
in a browser, or drop the file on any static host (GitHub Pages, Netlify,
Cloudflare Pages). No npm, no framework, no bundler.

![no build](https://img.shields.io/badge/build-none-brightgreen) ![single file](https://img.shields.io/badge/files-1-blue) ![licence MIT](https://img.shields.io/badge/licence-MIT-black)

## What's in it

| Section | Notes |
|---|---|
| Video hero | Autoplaying muted Pexels clip + gradient scrim |
| Stats strip | Count-up numbers (rating, reviews, patients, years) |
| Split about | Practice story, doctor credentials |
| Bento services | One hero cell + smaller cells (not N identical cards) |
| Works gallery | Asymmetric grid, 3D tilt + zoom on hover |
| Review marquee | Infinite CSS marquee, pauses on hover, 3D layers |
| Team | Monogram avatars (no fake stock faces) |
| Steps | Numbered 4-step patient journey |
| Contact | Phone, hours, address, embedded map link |
| Footer | Dark, sitemap + socials |

## Effects you can lift into other projects

All vanilla JS/CSS, no libraries:

- **Scroll reveals** — `.rv` class + `.d1..d4` delay helpers, driven by an `IntersectionObserver`.
- **Parallax** — a passive scroll listener nudging the hero media.
- **3D tilt cards** — `perspective: 1000px`, cursor offset ÷ 25 for `rotateY/rotateX`, per-layer `translateZ` via `data-z` attributes. Port of Aceternity's `CardContainer`/`CardItem` for people who don't want React.
- **Count-up numbers** — `data-count`, `data-dec`, `data-comma`, `data-suffix` attributes, cubic ease-out, `en-IN` number grouping. The static HTML text is the no-JS fallback.
- **Marquee** — content duplicated ×2, `translateX(-50%)` keyframes, `animation-play-state: paused` on hover.

## Make it yours

Search `index.html` for these and replace:

| What | Where |
|---|---|
| Clinic name, `SR Dental Zone` | `<title>`, header logo, footer, schema |
| Phone `+91 80 …` / `tel:` links | hero CTA, contact, footer |
| Address, map link | contact section |
| Doctors (`Dr. Suman Reddy`, `Dr. Keerthi Reddy`) | about + team |
| Reviews | the `reviews` array in the inline `<script>` |
| Pexels media URLs | hero `<video>`, gallery `<img>`, portrait |
| Palette — `--ink`, `--paper`, `--gold` | `:root` at the top of the `<style>` block |
| Fonts — Fraunces + Onest | the Google Fonts `<link>` |

The demo content is a **real clinic** (SR Dental Zone, Bengaluru) used as a design
concept — their name, reviews and address are factual, not invented. Replace all of
it before publishing: you are not licensed to use their brand, reviews or identity.

## Accessibility / performance notes

- Videos and images are remote (Pexels CDN). Self-host them for production and add
  `width`/`height` to avoid layout shift.
- All motion respects nothing yet — if you ship this, wrap the observers and marquee
  in `@media (prefers-reduced-motion: no-preference)`.
- Buttons and links are real `<a>`/`<button>` elements; the mobile nav is keyboard
  reachable in the current build but has no focus trap.

## Licence

Code: MIT (see `LICENSE`). Demo copy, clinic identity and reviews: not licensed —
replace them.
