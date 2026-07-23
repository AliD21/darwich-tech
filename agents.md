# AGENTS.md

## Project overview

Darwich Tech is a static, single-page marketing site (Arabic, RTL) for an agency building websites for phone/electronics shops in Lebanon. There is no backend, no build step, and no database — it is plain HTML/CSS/JS deployed as-is.

## Architecture

- `index.html` — all page content and section markup, in document order: navbar, hero (inside `<main>`), services, portfolio, process, pricing, testimonials, CTA, footer, WhatsApp floating button
- `css/style.css` — all styles, including responsive rules, the animated hero background (orbs/particles), and a `prefers-reduced-motion` override that disables looping animations for users who request it
- `js/script.js` — three behaviors only: mobile nav toggle (keeps `aria-expanded` in sync), smooth-scroll anchor links, and scroll-based active-link/nav-background updates
- `Assets/` — favicon and touch-icon PNGs at their real target sizes (16/32/180/192/512px); `favicon.ico` and `site.webmanifest` live at the project root and are referenced from `<head>`

External dependencies are loaded via CDN in `index.html` (Google Fonts, Font Awesome, AOS for scroll-reveal animations) — there is no package.json/npm dependency chain for the frontend.

## Conventions

- Content is in Arabic and the page is RTL (`dir="rtl"` on `<html>`); keep new content in Arabic for consistency unless asked otherwise.
- Class names describe content sections (e.g. `.service-card`, `.portfolio-card`, `.testimonial-card`) — follow this pattern when adding new cards/sections rather than introducing generic wrapper divs.
- WhatsApp links (`wa.me/...`) are the primary calls to action throughout the page — any new CTA should follow the same pattern.
- No build tooling is configured; do not add a bundler/framework unless explicitly requested, since the site is intentionally zero-build.
