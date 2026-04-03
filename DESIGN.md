```markdown
# Design System Document: The Hearth & Heritage Framework

## 1. Overview & Creative North Star
**Creative North Star: "The Modern Chulha"**
The objective of this design system is to translate the smoke, clay, and soul of traditional Indian hearth cooking into a high-end digital editorial experience. We are moving away from the "generic restaurant template" by embracing **Organic Layering**. 

The digital experience for 'Hotel Pangat' should feel like a well-worn, premium cookbook—tactile, warm, and deeply intentional. We break the rigid grid through **Asymmetrical Editorial Layouts**: large-scale serif typography overlapping subtle, earth-toned containers, and high-contrast tonal shifts that mimic the glow of an earthen stove against a dim interior.

---

## 2. Colors & Surface Philosophy
The palette is rooted in the earth (Terracotta/Saffron) but elevated through sophisticated neutral backgrounds.

*   **Primary (`#973100`) & Secondary (`#8d4f11`):** These represent the fire and the clay. Use them sparingly for high-impact brand moments and key CTAs.
*   **Surface Hierarchy (The Depth Rule):** Avoid flat white screens. Use the `surface-container` tiers to create "pockets" of warmth.
    *   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Define boundaries through background shifts. For example, a `surface-container-low` section should sit against a `surface` background to define its start and end.
    *   **Nesting:** Place `surface-container-lowest` cards atop `surface-container-high` sections to create a soft, natural lift that feels like stacked handmade paper.
*   **The "Glass & Glow" Rule:** To mimic the heat and transparency of a flame, use **Glassmorphism** for navigation overlays or floating action buttons. Utilize semi-transparent versions of `surface-variant` with a `backdrop-blur` of 12px-20px.
*   **Signature Textures:** Apply a subtle linear gradient from `primary` to `primary_container` on main CTAs to give them a "fired" look, moving beyond flat, digital-first colors.

---

## 3. Typography: The Editorial Voice
We use a high-contrast pairing to balance heritage with modern legibility.

*   **Display & Headlines (Noto Serif):** This is the soul of the brand. Use `display-lg` for evocative food descriptions or heritage quotes. The elegant serifs should be treated as a design element—don't be afraid of tight tracking or intentional overlaps with images.
*   **Body & Labels (Work Sans):** A clean, architectural sans-serif that provides a "modern breath" to the rustic aesthetic. It ensures the menu and pricing remain highly legible and functional.
*   **The Hierarchy Rule:** Use `headline-lg` for section headers in `on_surface_variant` (the warm charcoal-brown) to maintain a soft, vintage feel rather than a harsh black.

---

## 4. Elevation & Depth: Tonal Layering
In this design system, depth is a result of light and shadow, not lines and boxes.

*   **The Layering Principle:** Physicality is key. Use the `surface-container` scale to create a "Z-axis." 
    *   *Base:* `surface`
    *   *Section:* `surface-container-low`
    *   *Interactive Card:* `surface-container-lowest`
*   **Ambient Shadows:** For floating elements, use extra-diffused shadows. 
    *   *Spec:* `0px 10px 40px rgba(14, 29, 38, 0.06)`. Note the use of the `on_surface` color for the shadow tint; never use pure black.
*   **The Ghost Border Fallback:** If a separation is mandatory for accessibility, use the `outline_variant` token at **15% opacity**. It should be felt, not seen.
*   **Glassmorphism:** Use `surface_bright` at 80% opacity with a blur to create floating "Menu" or "Reservation" bars that feel light and premium.

---

## 5. Components

### Buttons
*   **Primary:** Solid `primary` background with `on_primary` text. Use `xl` (0.75rem) roundedness to maintain a soft, approachable feel.
*   **Secondary:** `surface_container_highest` background with `primary` text. No border.
*   **Tertiary:** Text-only in `secondary` with an animated underline on hover.

### Cards & Menu Items
*   **The "No Divider" Rule:** Forbid the use of line dividers. Use `1.5rem` to `2rem` of vertical white space or a shift to `surface_container_low` to separate items.
*   **The Imagery Rule:** Food photography should always have a `sm` (0.125rem) corner radius—just enough to soften the edges without looking "bubbly."

### Inputs & Forms
*   **Field Style:** Use "Floating Label" inputs. The field background should be `surface_container_low`. 
*   **Focus State:** Instead of a thick border, use a 2px `primary` underline or a subtle `surface_tint` glow.

### Signature Component: The "Chulha Counter"
*   A specialized list item for live-cooking status or "Chef's Specials." Use a `secondary_container` background with a subtle inner glow of `on_secondary_fixed_variant` to mimic the warmth of an ember.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical margins. A hero image might be offset to the right while text sits partially over it in a `surface_container` box.
*   **Do** use `notoSerif` for numbers in pricing; it adds a vintage, hand-written ledger feel.
*   **Do** embrace negative space. The "welcoming" feel of Pangat comes from room to breathe, not from clutter.

### Don't:
*   **Don't** use 100% opaque black. Use `on_background` (Charcoal) for all "black" text to keep the palette warm.
*   **Don't** use sharp 0px corners. Even the most "brutalist" layout needs the `sm` (0.125rem) radius to stay "welcoming."
*   **Don't** use standard "drop shadows" on buttons. Use tonal shifts or slight "lift" through background color changes.
*   **Don't** use icons that are too "tech-heavy." Prefer hand-drawn or thin-stroke icons that feel artisanal.

---

## 7. Accessibility & Motion
*   **Contrast:** Ensure all `on_surface` text against `surface_container` tiers meets WCAG AA standards. 
*   **Motion:** Transitions should be slow and "heavy," mimicking the slow-cooking process. Use `cubic-bezier(0.4, 0, 0.2, 1)` for all surface transitions—a "natural" easing that feels high-end and deliberate.