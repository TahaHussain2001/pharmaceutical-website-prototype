# Design System Strategy: Clinical Precision & Tonal Depth

## 1. Overview & Creative North Star
**The Creative North Star: "The Clinical Curator"**
This design system moves beyond the generic medical template to establish an editorial-grade experience that feels authoritative yet visionary. By combining the rigid reliability of pharmaceutical standards with the fluid elegance of high-end digital design, we create a "Clinical Curator" aesthetic. 

The system rejects the "box-inside-a-box" layout in favor of **intentional asymmetry** and **tonal layering**. We use expansive white space (breathing room) and high-contrast typography scales to guide the eye through complex data, ensuring that "trust" is not just a brand pillar, but a tactile visual sensation.

---

## 2. Colors
Our palette is rooted in deep, institutional blues and clinical neutrals, elevated by a sophisticated light-refraction model.

### Primary & Secondary Palette
- **Primary Blue (`#15157d` / `primary`):** Our foundation. Use for deep immersion sections and high-authority headers.
- **Secondary Blue (`#264dd9` / `secondary`):** Use for interactive elements and accents that require a modern, digital-first energy.
- **Tertiary Accent (`#590005` / `tertiary`):** A sophisticated deep red for critical alerts or specific high-end callouts, moving away from "emergency red" toward a more "academic mahogany."

### Color Application Rules
*   **The "No-Line" Rule:** 1px solid borders are strictly prohibited for sectioning. Boundaries must be defined through background color shifts. Transition from `surface` to `surface-container-low` to define new content areas. 
*   **Surface Hierarchy & Nesting:** Treat the UI as physical layers. An "Information Card" should be `surface-container-lowest` placed on a `surface-container-low` background. This creates a natural, soft lift.
*   **The Glass & Gradient Rule:** For floating navigation or modal overlays, use `surface-variant` with a **backdrop-blur (12px–20px)** and 80% opacity. This creates a "frosted glass" effect that keeps the user grounded in the clinical environment.
*   **Signature Textures:** For Hero sections, use a subtle radial gradient transitioning from `primary` (`#15157d`) to `primary-container` (`#2e3192`). This prevents the flat, "cheap" look of solid fills.

---

## 3. Typography
We utilize a dual-font strategy to balance high-end editorial aesthetics with clinical legibility.

*   **Display & Headlines (Manrope):** Chosen for its geometric precision and modern professional tone.
    *   `display-lg` (3.5rem): Use for bold, disruptive pharmaceutical claims.
    *   `headline-md` (1.75rem): For section titles, using tight letter-spacing (-0.02em) for an authoritative look.
*   **Body & Labels (Inter):** The industry standard for legibility.
    *   `body-lg` (1rem): Optimized for long-form medical research or product descriptions.
    *   `label-md` (0.75rem): All-caps with increased letter-spacing (0.05em) for category tags or metadata.

**Hierarchy Strategy:** Always pair a large `display-sm` headline with a significantly smaller, high-contrast `body-md` description to create the "Editorial" feel. Avoid "middle-ground" font sizes that create visual clutter.

---

## 4. Elevation & Depth
In this system, depth is a function of light and tone, not structure.

*   **The Layering Principle:** Stack containers to show importance. 
    *   *Level 0:* `surface` (Base background)
    *   *Level 1:* `surface-container-low` (Content groupings)
    *   *Level 2:* `surface-container-lowest` (Interactive cards/Active states)
*   **Ambient Shadows:** Use only when elements must "float" (e.g., Modals). Shadows must be diffused: `box-shadow: 0 10px 40px rgba(25, 28, 30, 0.06);`. The shadow color should be a tint of `on-surface` rather than pure black.
*   **The Ghost Border:** If a divider is required for accessibility in forms, use the `outline-variant` token at 15% opacity. It should be felt, not seen.

---

## 5. Components

### Buttons
*   **Primary:** `primary` background with `on-primary` text. Use `rounded-md` (0.375rem). For hover states, transition to `secondary`.
*   **Secondary (Outlined):** Use a "Ghost Border" (20% opacity `primary`) with `primary` text. This maintains a clean, medical aesthetic without the heaviness of a solid stroke.

### Cards & Information Modules
*   **Constraint:** Forbid divider lines.
*   **Styling:** Use `surface-container-lowest` with a `rounded-lg` (0.5rem) corner. Separate header and body content using 24px of vertical white space (from the Spacing Scale) rather than a line.

### Input Fields
*   **State:** Default state uses `surface-container-high` as a subtle fill rather than an outline.
*   **Focus:** Transition to a 2px `secondary` bottom-border only. This mimics the "high-end stationary" feel.

### Pharmaceutical "Trust" Badges (Custom Component)
*   Used for certifications (FDA, GMP, etc.). Use `surface-container-highest` with `label-sm` typography and 50% opacity icons to ensure they feel like an "official seal" rather than a marketing sticker.

---

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical grid layouts (e.g., a 2-column layout where the left column is 65% width and the right is 35%).
*   **Do** use high-quality, macro-photography of laboratory glass or clinical environments as semi-transparent background textures.
*   **Do** prioritize `surface` shifts over lines to separate content.

### Don't
*   **Don't** use 100% black text. Always use `on-surface` (`#191c1e`) to maintain a softer, premium contrast.
*   **Don't** use "Alert Red" for decorative elements. `tertiary` (`#590005`) is the only acceptable red for non-critical UI.
*   **Don't** crowd elements. If a section feels "busy," increase the vertical padding by 2x the standard spacing.
*   **Don't** use "Drop Shadows" on cards. Use tonal elevation (Background color shifts) instead.