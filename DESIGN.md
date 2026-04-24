---
name: Järna Rosteri
description: Minimal brochure site for a Swedish biodynamic coffee roastery
colors:
  ocra: "#bc9548"
  gron: "#3f452c"
  morkrost: "#3a2817"
  svart: "#000000"
  vit: "#ffffff"
  ljusgul: "#efd678"
  brun: "#6b502d"
  orostat: "#839678"
  franchese: "#2b4b58"
  grande: "#3aaf9c"
  poabs-esp: "#ffe012"
  poabs-bry: "#e95956"
  mezzo: "#319152"
  conejo: "#7e9775"
  footer-warm: "#f3efe7"
typography:
  display:
    fontFamily: "Orator Std, Maax Mono, monospace"
    fontSize: "clamp(3rem, 11vw, 10rem)"
    fontWeight: 400
    lineHeight: 0.92
    letterSpacing: "-0.04em"
  heading:
    fontFamily: "Maax Mono, Courier New, monospace"
    fontSize: "clamp(1.5rem, 3.5vw, 2.75rem)"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "-0.03em"
  body:
    fontFamily: "Maax Mono, Courier New, monospace"
    fontSize: "clamp(0.85rem, 1.2vw, 1rem)"
    fontWeight: 400
    lineHeight: 1.75
  label:
    fontFamily: "Maax Mono, Courier New, monospace"
    fontSize: "0.75rem"
    fontWeight: 400
    lineHeight: 1
    letterSpacing: "0.22em"
  nav:
    fontFamily: "Maax Mono, Courier New, monospace"
    fontSize: "0.65rem"
    fontWeight: 400
    letterSpacing: "0.45em"
rounded:
  none: "0"
  pill: "9999px"
  card: "1.5rem"
  card-sm: "1.25rem"
  link: "1rem"
spacing:
  sm: "0.5rem"
  lg: "2rem"
  xl: "4rem"
components:
  hamburger:
    backgroundColor: "{colors.ljusgul}"
    textColor: "{colors.morkrost}"
    rounded: "{rounded.pill}"
    size: "2.35rem"
  tag:
    backgroundColor: "transparent"
    textColor: "{colors.svart}"
    rounded: "{rounded.none}"
    padding: "0.35rem 0.7rem"
  contact-link:
    backgroundColor: "{colors.vit}"
    textColor: "{colors.morkrost}"
    rounded: "{rounded.link}"
    padding: "1.05rem 1.15rem 1rem"
  contact-panel:
    backgroundColor: "rgba(255,255,255,0.72)"
    textColor: "{colors.morkrost}"
    rounded: "{rounded.card}"
    padding: "1rem 1.25rem"
---

# Design System: Järna Rosteri

## 1. Overview

**Creative North Star: "The Soil Record"**

This is a design system built from the ground up, not layered on top. Like a field ledger or a seed log, every element earns its place by being useful, specific, and true. The system doesn't perform warmth — it inherits it from the materials: a palette drawn from dried clay, dark roast, and unbleached parchment; a typeface that reads like a typewriter pressed into quality paper.

The register is brand, but the brand behaves like infrastructure. Nothing announces itself. The wordmark sits in a corner. The typography is monospace and matter-of-fact. Sections breathe. Images carry weight without commentary. The site's job is to make the visitor feel that they've already met the people who run this place — competent, quiet, specific.

This system explicitly rejects the aesthetics of contemporary specialty coffee: branded mascots, illustrated characters, subscription-upsell layouts, dark-mode + gold-type "premium" clichés, and the over-designed Shopify brochure that performs craft rather than demonstrating it.

**Key Characteristics:**
- Monospace throughout — precision without coldness
- Full-viewport sections — no pagination, no cards, no grids
- Ochre as dominant surface — warm but never sweet
- Typography as primary design element — layout serves type, not the reverse
- Restraint that reads as confidence, not blankness

## 2. Colors: The Working Palette

*Note: the current palette is provisional. Colors are under active review and may shift. These tokens document the current state, not a final decision.*

The palette is drawn from organic matter: dried grains, dark soil, roasted beans, unbleached cloth. Colors are earth-derived and functionally assigned — each section has a dedicated surface, not a shared neutral.

### Primary
- **Amber Loam** (`#bc9548` / `color(display-p3 0.737 0.584 0.282)`): The dominant hero surface. Warm, dry, specific. Not yellow, not gold — the color of unpainted clay walls. Used as `html` background so it bleeds behind the scrollbar track.
- **Forest Floor** (`#3f452c` / `color(display-p3 0.247 0.271 0.173)`): Body background and default text-on-light context. Deep olive-green with no blue. The color of compost at rest.

### Secondary
- **Dark Roast** (`#3a2817` / `color(display-p3 0.227 0.157 0.09)`): Text on light backgrounds, interactive accents, scrollbar thumb. The darkest warm tone — not black, not brown, but the color of the bean at full roast.
- **Pale Straw** (`#efd678` / `color(display-p3 0.937 0.839 0.471)`): Packages section background and hamburger button fill. Warmer and lighter than Amber Loam — the color of dried grass in late summer.

### Neutral
- **Unbleached** (`#f3efe7`): Footer background. The lightest surface — off-white with a warm undertone. Never pure white.
- **Full Black** (`#000000`): Used sparingly for logo and text on the warmest light surfaces.
- **Full White** (`#ffffff`): About and Products section backgrounds. Reserved for sections where image contrast requires it.

### Extended Palette (product-specific, used for named coffees)
- **Unroasted** (`#839678`): Orostat — green-grey, used for the unroasted bean color reference.
- **Teal Depth** (`#2b4b58`): Franchese — a muted teal. Reserved for named product contexts.
- **Bright Canary** (`#ffe012`): Poabs Esp — high-saturation yellow. Product accent only.
- **Tomato** (`#e95956`): Poabs Bry — warm red. Product accent only.
- **Meadow** (`#319152`): Mezzo — mid green. Product accent only.

**The Named-Coffee Rule.** The extended palette (Franchese, Poabs Esp, Poabs Bry, Mezzo, Grande) is reserved exclusively for named product contexts. Never use these on structural UI surfaces — they belong to the beans, not the roastery.

## 3. Typography

**Display Font:** Orator Std (with Maax Mono fallback)
**Body / UI Font:** Maax Mono (with Courier New fallback)

**Character:** A single monospace family carries all text weight, with Orator Std reserved strictly for the wordmark and J.Rø logotype. The system doesn't pair serif + sans or display + body in the conventional sense — it uses typographic scale and letter-spacing to create hierarchy within a single register. The result reads like a document from a technical institution that happens to care about craft.

### Hierarchy
- **Display** (400 weight, `clamp(3rem, 11vw, 10rem)`, line-height 0.92, tracking −0.04em): Hero wordmark and section titles. Orator Std only — never used for body content or labels. Uppercase always.
- **Heading** (400 weight, `clamp(1.5rem, 3.5vw, 2.75rem)`, line-height 1, tracking −0.03em): Section headings and the Instagram CTA. Maax Mono. Uppercase. The tightest tracking for non-display text.
- **Body** (400 weight, `clamp(0.85rem, 1.2vw, 1rem)`, line-height 1.75): Running copy. 42–65ch max-width. Maax Mono. The generous line-height offsets the monospace texture.
- **Label** (400 weight, `0.75rem`, line-height 1, tracking 0.22em, uppercase): Section kickers, contact field labels, caption text. Maax Mono. All-caps with wide tracking — the system's smallest readable unit.
- **Nav** (400 weight, `0.65rem`, tracking 0.45em, uppercase): Corner annotations and hero meta text. Maax Mono. Reduced opacity (0.5). Directional signage, not content.

**The One Font Rule.** Maax Mono is the voice of the roastery. Orator Std is the name only. Never use Orator Std for labels, captions, navigation, or any text that isn't the literal wordmark "JÄRNA ROSTERI" or the short mark "J.Rø".

**The Tracking Rule.** Letter-spacing increases as size decreases — display text has negative tracking, label text has wide tracking. Never apply wide tracking to large type; never apply tight tracking to small type.

## 4. Elevation

This system is flat at rest. Depth is conveyed through color surface changes between full-viewport sections — each section has its own background, and the stack of sections creates vertical rhythm without any shadows at the section level.

Shadows appear only in two controlled contexts: the contact panel (a frosted card on a gradient background) and the hamburger button (a soft ambient drop shadow). Both use warm-tinted shadow values derived from Dark Roast, not neutral grey.

### Shadow Vocabulary
- **Ambient button** (`0 0.2rem 0.7rem color-mix(in srgb, #3a2817 18%, transparent)`): Used on the hamburger button only. Soft, warm, barely perceptible.
- **Panel lift** (`0 1.25rem 3rem rgba(58,40,23,0.08)`): Used on the contact panel card. Low-opacity, large-radius — the shadow of a piece of paper on a warm surface.
- **Link hover** (`0 0.75rem 1.5rem rgba(58,40,23,0.08)`): Contact link cards on hover. Appears as the card lifts 2px.

**The Warm Shadow Rule.** If a shadow is needed, derive it from Dark Roast (`#3a2817`) at low opacity — never from neutral black or grey. Warm shadows disappear naturally against warm backgrounds; grey shadows look like errors.

**The Flat-By-Default Rule.** Surfaces are flat at rest. Shadows appear only as a response to state (hover) or as structural separation (the contact panel). Never add shadows to sections, hero containers, or typographic elements.

## 5. Components

### Hamburger Button
The only persistent interactive element. A pill-shaped button in Pale Straw with Dark Roast bars. Fixed top-right, z-index 60. Animates bars to ×-close on open state with a smooth cubic-bezier transition.
- **Shape:** Full pill (`border-radius: 9999px`)
- **Size:** 2.35rem × 2.35rem
- **Background:** Pale Straw (`#efd678`)
- **Icon color:** Dark Roast (`#3a2817`)
- **Hover:** `opacity: 0.8`
- **Open state:** `opacity: 0.5`, bars rotate ±45°

### Menu Dialog
Full-screen overlay using `<dialog>`. Background: Amber Loam with a darkening image overlay. Links centered vertically. Enters with a 100ms opacity + 12ms translateY fade.
- **Background:** `#bc9548` + `rgba(0,0,0,0.42)` overlay on a landscape image
- **Link style:** Maax Mono, `clamp(1.15rem, 3vw, 2rem)`, `opacity: 0.8` at rest, 1 on hover
- **Animation:** `opacity` + `translateY(0.25rem → 0)` on open/close

### Tags / Chips
Used on product listings. Flat, no fill — border only. All-caps Maax Mono label style.
- **Shape:** Square corners (`border-radius: 0`)
- **Border:** `1px solid rgba(0,0,0,0.18)`
- **Background:** Transparent
- **Text:** Dark Roast at `opacity: 0.6`, Label style (0.75rem, tracking 0.1em, uppercase)
- **No hover state** — these are informational, not interactive

### Contact Links
Clickable blocks for email and phone. Slightly warm white fill, rounded corners, subtle border.
- **Shape:** Gently rounded (`border-radius: 1rem`)
- **Background:** `color-mix(in srgb, #ffffff 86%, #efd678)` — barely warm white
- **Border:** `1px solid rgba(58,40,23,0.1)`
- **Hover:** `translateY(-2px)`, border deepens to 0.22 opacity, shadow appears
- **Internal layout:** Label (uppercase, 0.5 opacity) above value (1–1.15rem)

### Contact Panel
The only "card" in the system — used once, for the contact section. Frosted warm-white surface on a gradient background.
- **Shape:** `border-radius: 1.5rem` (1.25rem on mobile)
- **Background:** `rgba(255,255,255,0.72)` with `backdrop-filter: blur(12px)`
- **Border:** `1px solid rgba(58,40,23,0.12)`
- **Shadow:** Panel lift (see Elevation)

### Navigation (Corner Annotations)
Fixed-position text labels at corners of the hero. Not links — directional metadata.
- **Style:** Maax Mono, `0.65rem`, tracking `0.45em`, uppercase, `opacity: 0.5`
- **Color:** Dark Roast (`#3a2817`)
- **Mobile:** Reduced to 75% size on screens ≤480px

## 6. Do's and Don'ts

### Do:
- **Do** use Orator Std exclusively for "JÄRNA ROSTERI" and "J.Rø" — the wordmark is the only context.
- **Do** derive shadow colors from Dark Roast (`#3a2817`) at low opacity — never from neutral grey or black.
- **Do** let sections carry their own background color rather than nesting content in cards or panels.
- **Do** use wide letter-spacing (`0.22em–0.45em`) on all-caps label and nav text at small sizes.
- **Do** use negative tracking (`−0.03em` to `−0.05em`) on heading-scale and display text.
- **Do** keep body copy to 42–65ch max-width — Maax Mono's fixed-width spacing rewards short lines.
- **Do** use `color(display-p3 ...)` values for the brand greens and ochres where supported — they're richer than sRGB equivalents.
- **Do** reserve the extended product palette (Franchese, Poabs colors, Mezzo) for named-coffee contexts only.

### Don't:
- **Don't** use Orator Std for labels, navigation, captions, or any text that isn't the literal wordmark.
- **Don't** build card grids. The product and content layout is rows or full-viewport sections — never a repeating card grid.
- **Don't** add drop shadows to section containers, hero areas, or typographic elements. Flat at rest.
- **Don't** use neutral-grey shadows — they read as errors against the warm palette.
- **Don't** use gradient text (`background-clip: text`). Single color only; emphasis through weight or size.
- **Don't** use `border-left` or `border-right` as a colored stripe accent on any element.
- **Don't** import the generic specialty-coffee Shopify aesthetic: product grids, aggressive CTAs, subscription upsells, illustrated characters.
- **Don't** use the dark-mode + gold-type treatment — it's the most common "premium coffee" cliché and directly contradicts the Soil Record personality.
- **Don't** use lifestyle photography of people drinking coffee in loft apartments or any third-wave café visual clichés.
- **Don't** add decorative flourishes to soften the layout — the warmth lives in the palette, not in ornamental details.
- **Don't** make the site look like it's trying. If an element looks effortful, simplify it.
