# Design System Strategy: The Nocturnal Botanical Editorial

## 1. Overview & Creative North Star: "The Shadowed Herbarium"
This design system rejects the clinical, bright aesthetics of typical educational platforms in favor of a "Shadowed Herbarium" approach. Our Creative North Star is the **Digital Curator**: an experience that feels like flipping through a rare, 19th-century botanical leather-bound book under candlelight. 

To break the "template" look, we utilize **Intentional Asymmetry**. Imagery and text should rarely sit on a centered axis; instead, botanical illustrations should bleed off the edges of the viewport, and headlines should overlap container boundaries. High-contrast shifts between `surface` (deep black) and `primary` (vibrant red) create a rhythmic pulse through the scroll, moving the user from moody atmospheric sections to high-alert calls to action.

## 2. Colors & Surface Philosophy
The palette is a high-drama interplay between the depth of the greenhouse at night and the visceral life of the flora.

*   **Primary Palette:** `primary` (#ffb4ac) and `primary_container` (#d42d2b) represent the "vibrant red accents." Use these for moments of critical conversion or to highlight rare botanical species.
*   **The "No-Line" Rule:** Do not use 1px solid borders to define sections. High-end editorial design relies on **Tonal Carving**. Use `surface_container_low` (#1c1b1b) against a `surface` (#131313) background to create a "well" for content. If a section needs to feel "elevated," use `surface_bright` (#393939).
*   **Surface Hierarchy & Nesting:** Treat the UI as layers of vellum. 
    *   *Base:* `surface` (#131313)
    *   *Nesting:* A search bar or card should use `surface_container_high` (#2a2a2a) to sit *within* a section, creating depth through value shifts rather than lines.
*   **The Glass & Gradient Rule:** For floating navigation or modal overlays, apply `surface_container` at 80% opacity with a `24px` backdrop blur. Use a subtle linear gradient from `primary_container` to `on_primary_fixed_variant` for large CTA buttons to give them a "petal-like" velvet texture.

## 3. Typography: The Editorial Contrast
We use a "Serif-First" hierarchy to ground the experience in history and prestige.

*   **Display & Headlines (Noto Serif):** These are your "Signature" elements. `display-lg` should be used with tight letter-spacing (-0.02em) to feel like a premium magazine masthead. These fonts convey the "botanical feel"—stately, organic, and authoritative.
*   **Body & UI (Manrope):** A clean, high-x-height sans-serif used for readability. `body-md` is the workhorse for course descriptions. 
*   **Hierarchy Note:** Use `label-md` in uppercase with `0.1rem` letter-spacing for category tags (e.g., "PERENNIALS") to create a modern, curated contrast against the flowing Noto Serif headlines.

## 4. Elevation & Depth
In a dark-mode botanical environment, traditional shadows are often too "muddy."

*   **The Layering Principle:** Depth is achieved via color temperature. Place a `surface_container_lowest` (#0e0e0e) card on a `surface_container` (#201f1f) background to create a "carved out" effect.
*   **Ambient Shadows:** If an element must float (like a FAB), use a shadow color derived from `on_primary_fixed` (#410002) at 15% opacity with a `40px` blur. This creates a "warm glow" rather than a grey shadow, mimicking light passing through a red flower.
*   **The Ghost Border Fallback:** If a boundary is required for accessibility, use `outline_variant` (#5b403d) at 15% opacity. It should be felt, not seen.

## 5. Components Style Guide

### Buttons
*   **Primary:** Background `primary_container`, text `on_primary_container`. Shape: `DEFAULT` (0.25rem) for a sharp, architectural feel.
*   **Secondary:** Background `none`, border `Ghost Border` (outline-variant @ 20%).
*   **Interaction:** On hover, the `primary` color should shift to `primary_fixed` (#ffdad6) to "bloom" under the cursor.

### Cards & Lists
*   **The "No Divider" Rule:** Never use a horizontal line to separate list items. Use `2rem` (spacing scale 6) of vertical whitespace or a subtle background shift to `surface_container_low`.
*   **Botanical Cards:** Cards should have no borders. Use `surface_container` backgrounds and let botanical illustrations "break out" of the top-right corner, overlapping the card edge.

### Input Fields
*   **Styling:** Use `surface_container_lowest` for the input fill. The label (`label-md`) should sit above the field in `on_surface_variant`. 
*   **Focus State:** The bottom border (and only the bottom border) should animate to `primary` (#ffb4ac) at 2px thickness.

### Chips
*   **Selection Chips:** Use `secondary_container` with `on_secondary_container` text. Use `full` roundedness to contrast against the sharper architectural buttons.

## 6. Do's and Don'ts

### Do
*   **DO** use "Delicate Lines" sparingly as decorative accents (like botanical diagram lead-lines), using `outline` (#ab8985) at 30% opacity.
*   **DO** utilize the `16` (5.5rem) and `20` (7rem) spacing tokens to create an expansive, "gallery" feel between sections.
*   **DO** use `surface_container_lowest` for the main background of long-form reading sections to maximize focus.

### Don't
*   **DON'T** use pure white (#FFFFFF) for body text; use `on_surface` (#e5e2e1) to prevent eye strain against the dark background.
*   **DON'T** use standard "drop shadows" on cards; they break the "dark greenhouse" immersion. Use tonal layering instead.
*   **DON'T** center-align long blocks of text. Stick to editorial left-alignment to maintain the "curated" look.