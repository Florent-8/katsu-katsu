# Design System Strategy: The Artisanal Path

## 1. Overview & Creative North Star: "The Modern Wabi-Sabi"
This design system is built on the philosophy of "The Modern Wabi-Sabi." It rejects the cluttered, "loud" aesthetics of traditional fast-casual apps in favor of a high-end editorial experience that feels like a curated gallery or a premium Japanese lifestyle magazine. 

We break the "template" look by embracing **Asymmetric Balance**. Do not center-align everything; use the generous spacing scale to let elements breathe. Think of the screen as a canvas where the negative space (the #FBFAEE cream background) is just as important as the content. We create a premium downtown NYC energy by pairing the organic warmth of Japanese craft with the sharp, disciplined grid of Manhattan architecture.

## 2. Colors & Surface Philosophy
The palette is rooted in natural materials: fine washi paper, scorched earth, and aged bamboo.

*   **The "No-Line" Rule:** Standard 1px solid borders are strictly prohibited for sectioning. We define boundaries through **Tonal Shifting**. A section containing "Chef’s Specials" should not be boxed in; instead, it should sit on a `surface_container_low` (#F5F4E8) background against the main `surface` (#FBFAEE).
*   **Surface Hierarchy:** Treat the UI as layers of fine paper. 
    *   **Base:** `surface` (#FBFAEE)
    *   **Subtle Depth:** `surface_container` (#EFEEE3) for secondary content.
    *   **High Focus:** `surface_container_highest` (#E4E3D7) for elevated UI elements like navigation bars or active cards.
*   **Signature Textures & Gradients:** Avoid flat, plastic-looking buttons. Use a subtle linear gradient from `primary` (#94442E) to `primary_container` (#B35C44) for primary CTAs to simulate the depth of traditional lacquerware.

## 3. Typography: Editorial Discipline
Typography is our primary tool for conveying "Chef-Driven" authority. We pair a high-contrast serif with a hyper-functional sans-serif.

*   **Display & Headlines (Noto Serif):** These are your "brushstrokes." Use `display-lg` (3.5rem) with generous tracking for hero moments. The thin strokes of Noto Serif evoke artisanal precision.
*   **Body & Labels (Inter):** The "minimal and clean" counterweight. Body text should be set in `body-md` (0.875rem) with increased line-height (1.6x) to ensure the "Calm" mood is maintained. 
*   **The Signature Treatment:** For category labels or "Chef’s Notes," use `label-md` in All Caps with 0.1rem letter spacing to create a sophisticated, architectural feel.

## 4. Elevation & Depth: Tonal Layering
We move away from the "floating card" look of 2010s Material Design. Depth here is atmospheric, not structural.

*   **The Layering Principle:** Instead of shadows, stack your surfaces. A `surface_container_lowest` (#FFFFFF) card placed on a `surface_dim` (#DBDBCF) background provides all the "lift" required.
*   **Ambient Shadows:** If an element must float (e.g., a "Cart" FAB), use a shadow tinted with `on_surface` at 4% opacity with a 32px blur. It should look like a soft glow, not a drop shadow.
*   **The Glassmorphism Rule:** For navigation overlays, use `surface` (#FBFAEE) at 85% opacity with a `20px` backdrop-blur. This allows the "Warm Ivory" base to bleed through, maintaining the organic feel while the user scrolls.
*   **Ghost Borders:** If accessibility requires a border (e.g., input fields), use `outline_variant` (#DBC1BA) at **20% opacity**. It should be felt, not seen.

## 5. Components & Interactions

*   **Buttons:**
    *   **Primary:** Rectangular (`0px` radius), `primary` background, `on_primary` text. No rounded corners. The sharpness conveys "Manhattan edge."
    *   **Secondary:** `outline` (#88726D) at 20% opacity with a `title-sm` weight label.
*   **Cards:** Forbid the use of divider lines inside cards. Use the `20` (7rem) spacing token to separate image from text. Cards should use `surface_container_low` to subtly distinguish themselves from the background.
*   **Vertical Dividers:** When a divider is essential (e.g., separating menu price from item name), use a 1px `outline_variant` but only at 50% height of the text line.
*   **Input Fields:** Minimalist. No background fill. Only a bottom border using `outline` (#88726D) at 30% opacity. Upon focus, the border transitions to `primary` (#94442E).
*   **Signature Component - The "Vertical Label":** In editorial layouts, use `label-sm` rotated 90 degrees to label vertical sections (e.g., "ORIGIN," "SEASONAL"). This breaks the horizontal grid and feels custom-designed.

## 6. Do’s and Don’ts

### Do:
*   **Embrace the Void:** Use the `24` (8.5rem) spacing token between major sections. If it feels "too empty," you are doing it right.
*   **Monochromatic Shifts:** Use the different `surface` tiers to guide the eye before resorting to color.
*   **Intentional Asymmetry:** Place a `display-md` heading on the left and a small `body-sm` description on the far right of a 12-column grid.

### Don't:
*   **No Rounded Corners:** The `roundedness` scale is set to `0px`. Do not add border-radii. This system relies on the beauty of the "Straight Edge."
*   **No Pure Black:** Never use #000000. Use `on_background` (#1B1C15) or charcoal black (#1A1A1A) to keep the look "Authentically Japanese" and soft on the eyes.
*   **No Standard Icons:** Avoid generic "Filled" icons. Use ultra-thin (1pt) stroke icons that match the "Ghost Border" aesthetic.