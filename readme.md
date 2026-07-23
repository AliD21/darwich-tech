# Darwich Tech

A single-page Arabic (RTL) marketing website for Darwich Tech, an agency that builds websites for mobile phone and electronics shops in Lebanon. The site presents services, a portfolio of past work, the working process, client testimonials, and calls to action to reach out via WhatsApp.

## Key technologies

- Plain HTML5, CSS3, and vanilla JavaScript (no framework or build step)
- [AOS](https://michalsnik.github.io/aos/) for scroll animations
- [Font Awesome](https://fontawesome.com/) for icons
- Google Fonts (Cairo, Inter)

## Running locally

Since this is a static site with no build step, you can open `index.html` directly in a browser, or serve it locally:

```bash
netlify dev --port 8889
```

Then visit the printed local URL.

## Project structure

- `index.html` — the single page containing all sections (hero, services, portfolio, process, testimonials, CTA, footer)
- `css/style.css` — all styling
- `js/script.js` — mobile menu toggle, smooth scrolling, and scroll-based nav highlighting
