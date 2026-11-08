# Personal Page — Rafael Moraes

## Vision

A clean, minimalist personal site inspired by [dmoraes.org](https://dmoraes.org/) — typography-driven, monochrome, single-column, fast. Two pages: **Home** and **Portfolio**.

---

## Decisions (Resolved)

| # | Decision | Answer |
|---|----------|--------|
| 1 | Repo | Private `rbmrs` repo, GitHub Pages from `main` branch |
| 2 | Colors | Monochrome — black/white, blue underlined links only |
| 3 | Profile photo | No |
| 4 | Domain | `rbmrs.github.io` (no custom domain) |
| 5 | Projects | Ship with Thumbcraft + Omarchy Smart Enter |
| 6 | Fonts | System fonts only (`system-ui`, `monospace`) — zero external requests |
| 7 | Accessibility | Semantic HTML, good contrast, focus styles |
| 8 | Dark mode | Deferred to v2 (light only, CSS properties ready for it) |

---

## Tech Stack

| Layer | Choice |
|-------|--------|
| Framework | Plain HTML + CSS (static, zero build step) |
| Styling | Single CSS file with custom properties |
| Hosting | GitHub Pages from `main` branch |

---

## File Structure

```
rbmrs/
├── index.html
├── portfolio.html
├── css/
│   └── style.css
└── assets/
    └── (favicon)
```

---

## Pages

### Home (`index.html`)

```
<header>  → nav: "Rafael Moraes" (left) · Home, Portfolio (left-aligned below name)
<main>    → "Now" (Headless commerce with Shopify Hydrogen/Remix/TS at Form Factory + tooling)
          → "Background" (10+ yrs, 8 yrs Senior Game Dev at Main Leaf Games, Unity/C#, CS degree)
<footer>  → Email · GitHub · LinkedIn · Twitter/X icons + Theme toggle (light/dark)
```

### Portfolio (`portfolio.html`)

```
<header>  → same nav
<main>    → "Selected projects" heading + simple <ul> list:
             • Thumbcraft — Lightweight macOS thumbnail editor
             • Omarchy Smart Enter — Wayland lock-screen auto-submit plugin
<footer>  → same footer
```

---

## Design Tokens

```css
--font-body:   system-ui, sans-serif;
--font-mono:   monospace;
--color-bg:    #fafafa;
--color-text:  #1a1a1a;
--color-muted: #555;       /* 7:1 contrast on #fafafa */
--color-link:  #0057ff;
--max-width:   640px;
--spacing:     1.5rem;
```

---

## Meta / SEO

- `<title>`, `<meta name="description">`
- `og:title`, `og:description`
- Inline SVG favicon (no external file needed)
