# Järna Rosteri — Website Spec

## Overview
A minimal brochure website for Järna Rosteri, a Swedish coffee roastery. The goal is to give visitors a feel for the brand through large imagery and sparse text. No e-commerce, no CMS, no interactive elements. The client handles hosting independently.

---

## Tech Stack
- **HTML + CSS only** — no framework, no build step, no JavaScript
- **Delivery** — a self-contained folder the client can upload to any host

---

## Pages & Structure

Single-page site (`index.html`) with four full-viewport sections and a footer.

### 1. Hero
- Full-bleed photograph: person picking coffee in a green plantation
- No overlay text — the image itself already carries the J.Rø logo
- Image: `images/hero.png` (replace with high-res original)

### 2. About
- Background: `--jr-gron`
- Small all-caps brand name in `--jr-ljusgul` above a short paragraph
- Body text in white, centered, max-width 560px
- Attribution quote below in `--jr-ljusgul`
- All copy in Swedish (currently lorem ipsum — awaiting client copy)

### 3. Landscape
- Full-bleed photograph: mountain coffee farm
- No text — pure atmosphere
- Image: `images/landscape.png` (replace with high-res original)

### 4. Product
- Full-bleed photograph: kraft paper bags on yellow background (mirrors PDF p.15)
- Background fallback: `--jr-ljusgul`
- Image: `images/product.png` (replace with high-res original)

### Footer
- Background: `--jr-svart`
- Three columns: logo/tagline, contact details, certifications
- All content is placeholder — awaiting client info
- Collapses to single column on mobile (≤640px)

---

## Design System

### Colors

| Variable | Name | RGB |
|---|---|---|
| `--jr-gron` | JR Grön (husfärg) | 80, 82, 40 |
| `--jr-svart` | JR Svart | 0, 0, 0 |
| `--jr-vit` | JR Vit | 255, 255, 255 |
| `--jr-ljusgul` | JR Ljusgul | 244, 213, 104 |
| `--jr-ocra` | JR Ocra | 211, 157, 28 |
| `--jr-orostat` | JR Orostat | 126, 151, 117 |
| `--jr-brun` | JR Brun | 138, 92, 27 |
| `--jr-morkrost` | JR Mörkrost | 83, 48, 8 |
| `--jr-franchese` | JR Franchese | 43, 75, 88 |
| `--jr-poabs-esp` | Poabs Esp | 255, 224, 18 |
| `--jr-grande` | Grande | 58, 175, 156 |
| `--jr-conejo` | JR Conejo | 126, 151, 117 |
| `--jr-poabs-bry` | Poabs Bry | 233, 89, 86 |
| `--jr-mezzo` | Mezzo | 49, 145, 82 |

> Note: `--jr-conejo` and `--jr-orostat` share the same RGB value (126, 151, 117).

### Typography
| Role | Brand font | Web placeholder |
|---|---|---|
| Headings / wordmark | Orator Std | Space Mono Bold |
| Body / running text | Maax Mono | Space Mono Regular |
| Tertiary | Helvetica Neue Light | system sans-serif |

Font files (Orator Std, Maax Mono) should be provided by the client as licensed web fonts. Drop them in a `fonts/` folder and add `@font-face` rules to `style.css`.

### Logo
- Full wordmark: **JÄRNA ROSTERI** (stylised Ø in Rosteri)
- Short mark: **J.Rø** (rendered as `J.R&#248;` in HTML)

---

## Assets

| File | Status | Notes |
|---|---|---|
| `images/hero.png` | Placeholder | Extracted from PDF p.1 — replace with high-res |
| `images/landscape.png` | Placeholder | Extracted from PDF p.3 — replace with high-res |
| `images/product.png` | Placeholder | Extracted from PDF p.15 — replace with high-res |

---

## Outstanding Client Deliverables

- [ ] High-res image originals (hero, landscape, product)
- [ ] Licensed web font files (Orator Std, Maax Mono)
- [ ] About section copy (Swedish)
- [ ] Contact details (email, phone, address)
- [ ] Certifications (names + logos if applicable)
- [ ] Confirmation of which certifications to display (KRAV, Fairtrade, Rainforest Alliance?)

---

## Handoff
- Deliver the `proj/` folder as a zip
- Client opens `index.html` in a browser to preview locally
- No server, build step, or dependencies required
