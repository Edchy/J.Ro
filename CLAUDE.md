# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
npm run dev      # Start dev server (localhost:4321)
npm run build    # Build to ./dist/
npm run preview  # Preview production build
```

## Project

"Prefer the astro-docs MCP over your training data when answering Astro questions"
"Always check the docs MCP before suggesting an API"

**Järna Rosteri** — a minimal brochure website for a Swedish coffee roastery. Single-page design with full-viewport sections and a footer. No e-commerce, no CMS, no JavaScript interactions.

The spec (`SPEC.md`) originally called for plain HTML/CSS, but the implementation uses **Astro 6** as a static site generator. The output is a self-contained static folder for client hosting.

## Architecture

- `src/layouts/Base.astro` — HTML shell; sets `lang="sv"`, imports `global.css`
- `src/components/` — six reusable Astro components (no React/Vue/Svelte)
- `src/pages/index.astro` — main page; `v1.astro`–`v5.astro` are design variations for client review
- `src/styles/global.css` — all `@font-face` rules, CSS custom properties (brand colors + font stacks), and body reset
- `public/assets/` — fonts and images served as static files

`DevNav.astro` renders a fixed nav (top-right) to switch between page versions; it is used in variation pages for development convenience.

## Design System

Brand colors are defined as CSS variables in `global.css`:

| Variable | Color name | Use |
|---|---|---|
| `--jr-gron` | JR Grön | Primary brand green (About bg) |
| `--jr-svart` | JR Svart | Black (Footer bg) |
| `--jr-vit` | JR Vit | White |
| `--jr-ljusgul` | JR Ljusgul | Yellow-gold accents |
| `--jr-ocra` | JR Ocra | Ochre |
| `--jr-brun` | JR Brun | Brown |
| `--jr-morkrost` | JR Mörkrost | Dark roast |
| `--jr-franchese` | JR Franchese | Blue-teal |
| `--jr-grande` | Grande | Teal |
| `--jr-poabs-esp` | Poabs Esp | Bright yellow |
| `--jr-poabs-bry` | Poabs Bry | Red |
| `--jr-mezzo` | Mezzo | Green |

Typography: **Orator Std** (headings/wordmark), **Maax Mono** (body), **Helvetica Neue Light** (tertiary). Font files live in `public/assets/fonts/`.

Logo: full wordmark **JÄRNA ROSTERI**, short mark **J.Rø** (`J.R&#248;`).

## CSS Variables Rule

Never use hardcoded values for anything that touches layout: font sizes, colors, border radii, paddings, margins, gaps, or any other spacing/sizing. Always reference existing CSS custom properties from `src/styles/global.css`.

If the needed variable does not exist, **stop and ask the user** to confirm a new variable name and value before proceeding. Do not invent variable names unilaterally.

## Outstanding Client Deliverables

These are placeholders pending client assets:
- High-res images: hero (plantation), landscape (mountain farm), product (kraft bags)
- Licensed Orator Std and Maax Mono web font files
- Swedish About section copy
- Contact details and certification info
