# Design System Specification: High-End Creative Editorial

## 1. Overview & Creative North Star: "The Digital Architect"
This design system is built for 'ROOK', a creative agency that sits at the intersection of architectural precision and digital innovation. We are moving away from the "standard SaaS" look of rounded bubbles and heavy borders. Instead, we embrace **The Digital Architect**—a North Star that prioritizes structural integrity, intentional asymmetry, and a high-contrast, "Electric" energy.

The system breaks the template through "Breathing Scale": utilizing extreme whitespace to make content feel like a curated gallery piece. We use a grid not as a cage, but as a foundation for overlapping elements and bold, confident typography.

---

## 2. Colors & Surface Philosophy
The palette is rooted in deep blacks and pristine whites, punctuated by a high-energy `primary` (Electric Blue).

### The "No-Line" Rule
**Explicit Instruction:** Prohibit the use of 1px solid borders for sectioning or containment. Boundaries are defined exclusively through background shifts.
- **Example:** A `surface-container-low` section sitting against a `background` base.
- Use `surface-container-lowest` (#0E0E0E) for deep, immersive sections.
- Use `surface-bright` (#3A3939) for elevated interactive cards.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of fine materials.
- **Base Layer:** `surface` (#131313).
- **Secondary Content Layer:** `surface-container-low` (#1C1B1B).
- **Interactive/Feature Layer:** `surface-container-high` (#2A2A2A).
By nesting a "High" container within a "Low" section, we create depth through tonal shifts rather than structural lines, maintaining a clean, professional aesthetic.

### The "Glass & Gradient" Rule
To inject "soul" into the minimalism:
- **Glassmorphism:** Use `surface` colors at 60-80% opacity with a `backdrop-blur` of 20px-40px for floating navigation or modals.
- **Signature Gradients:** For primary CTAs and Hero accents, transition from `primary` (#B9C3FF) to `primary_container` (#0047FF). This adds a three-dimensional "glow" that flat colors cannot replicate.

---

## 3. Typography: Confident Contrast
We utilize a dual-font strategy to balance technical precision with creative flair.

*   **Display & Headlines (Space Grotesk):** This is our "Statement" face. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) for hero headlines to convey authority.
*   **Body & Labels (Inter):** Our "Workhorse." Inter provides maximum readability for high-density information in E-commerce or Healthcare sectors.
*   **The Contrast Rule:** Always pair a `display-sm` headline with `body-md` metadata. The drastic scale difference creates the "Editorial" feel required for a premium agency.

---

## 4. Elevation & Depth
Traditional drop shadows are forbidden. We use **Tonal Layering** and **Ambient Light**.

*   **The Layering Principle:** Stack `surface-container-lowest` on `surface-container-low` to create a "sunken" or "lifted" effect.
*   **Ambient Shadows:** For floating elements (e.g., high-quality mockups), use a blur of 60px-80px with 4% opacity. The shadow color should be a tinted version of `on-surface` (#E5E2E1), mimicking natural light.
*   **The "Ghost Border" Fallback:** If a container needs separation on a complex background, use `outline-variant` (#434657) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons
*   **Primary:** Gradient fill (`primary` to `primary_container`). `0.25rem` (sm) corner radius. No border. On hover, increase `surface-tint` brightness.
*   **Secondary:** Ghost style. No background. `outline` color for text. On hover, a subtle `surface-container-high` background fade-in.
*   **Tertiary:** Underlined `label-md` text. The underline should be 2px thick and offset by 4px.

### Cards & Lists
*   **Forbid Dividers:** Use `0.75rem` (xl) vertical spacing or a subtle shift from `surface` to `surface-container-low` to separate list items.
*   **The "Floating Grid":** Cards should have no borders. Use `surface-container-highest` for the card body to make it pop against the background.

### Input Fields
*   **Style:** Minimalist underline style or subtle `surface-container-low` fills.
*   **States:** On focus, the underline or "Ghost Border" transitions to `primary` (Electric Blue). Error states use `error` (#FFB4AB) text with no background change.

### Signature Component: The "Perspective Mockup"
For the Real Estate/E-commerce audience, create a component that tilts high-quality screenshots on a 3D axis, using the `primary` accent as a soft glow behind the frame.

---

## 6. Do's and Don'ts

### Do
*   **Do** use asymmetrical layouts. Let a headline sit on the left while the body text starts at the 50% grid mark.
*   **Do** use "Electric Blue" sparingly. It is a laser, not a paint brush. Use it for CTAs, active states, and small abstract accents.
*   **Do** prioritize `surface-container` shifts over lines.

### Don't
*   **Don't** use "Standard" 8px or 16px corner radiuses. Stick to the specified `sm` (4px) or `md` (6px) for a sharper, more professional edge.
*   **Don't** use pure grey shadows. Always tint shadows with the surface color to avoid a "dirty" look.
*   **Don't** crowd the layout. If a section feels "full," double the padding. This agency sells whitespace as a luxury.

---

## 7. Spacing Scale
Maintain a strict 8pt grid, but favor the larger ends of the scale (`48px`, `64px`, `96px`) to ensure the "Minimalist" brand personality is felt. Section padding should never be less than `80px` on desktop.