```markdown
# Design System Strategy: The Cinematic Interface

## 1. Overview & Creative North Star
**The Creative North Star: "The Neon Luminary"**
This design system rejects the "SaaS-in-a-box" aesthetic in favor of a cinematic, immersive coaching experience. It bridges the gap between high-stakes gaming performance and elite executive communication. We break the standard grid through **intentional layering** and **asymmetric focal points**—where the AI isn't just a tool, but a presence. 

By utilizing deep obsidian voids contrasted against ethereal neon glows, we create a "Digital Sanctuary" that feels both private and prestigious. We avoid rigid borders; instead, we define space through light, blur, and tonal shifts.

---

## 2. Colors & Surface Philosophy
The palette is rooted in the "Deep Black" (#050505) ethos, using color not just for branding, but to signal interactive energy.

### The "No-Line" Rule
**Standard 1px borders are strictly prohibited.** Boundaries must be defined by background shifts or light.
- To separate a sidebar: Use `surface-container-low` (#1C1B1B) against a `surface` (#131313) background.
- To separate sections: Use a 32px to 64px vertical gap (Scale 8 to 16) rather than a divider line.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, frosted glass sheets.
- **Base Layer:** `surface` (#131313) or `surface-container-lowest` (#0E0E0E).
- **Secondary Layer (Content Blocks):** `surface-container` (#201F1F).
- **Floating Layer (Modals/Popovers):** `surface-bright` (#3A3939) with a 20px backdrop-blur.

### The "Glass & Gradient" Rule
Main CTAs and high-priority AI insights must use a **Signature Texture**:
- **Primary Gradient:** Linear (135deg) from `primary_container` (#6D28D9) to `secondary_container` (#0566D9). 
- **Glass Effect:** Apply `surface_variant` at 40% opacity with a `blur(12px)` for all floating navigation cards.

---

## 3. Typography: Editorial Authority
We pair **Plus Jakarta Sans** (Display/Headlines) for a modern, aggressive tech feel with **Inter** (Body/Labels) for maximum legibility during intense coaching sessions.

*   **Display-LG (3.5rem):** Reserved for "Hero" moments or major achievement milestones. Use `on_surface` with -0.02em letter spacing.
*   **Headline-SM (1.5rem):** Used for coaching module titles.
*   **Body-MD (0.875rem):** The standard for AI chat responses. Ensure a line-height of 1.6 to prevent "wall-of-text" fatigue.
*   **Label-SM (0.6875rem):** All-caps with 0.05em tracking for category tags (e.g., "TONE ANALYSIS").

---

## 4. Elevation & Depth
In a dark, premium theme, traditional shadows disappear. We use **Tonal Layering** and **Luminescent Depth**.

*   **The Layering Principle:** A `surface-container-highest` (#353534) card should sit on a `surface-container-low` (#1C1B1B) background to create a "soft lift."
*   **Ambient Shadows:** For floating glass cards, use a shadow: `0 20px 40px rgba(0, 0, 0, 0.4)`. To add "soul," add a second, very faint shadow using a tinted color: `0 0 20px rgba(109, 40, 217, 0.1)` (Primary Purple tint).
*   **The Ghost Border Fallback:** If a container lacks contrast, use `outline-variant` (#4A4455) at **15% opacity**. It should be felt, not seen.

---

## 5. Components & Interaction

### Buttons: The "Power" State
*   **Primary (The Glow):** Background is the Primary Gradient. Apply a drop-shadow matching the `primary_container` (#6D28D9) at 30% opacity to create a "neon glow" effect. Shape: `xl` (1.5rem).
*   **Secondary:** Ghost style. Transparent background, `Ghost Border` (15% opacity `outline-variant`), and `primary` text color.

### AI Communication Cards
*   **Strictly no dividers.** Use a 1.25rem (`spacing-5`) gap between metadata and body text.
*   **The "Active" Glow:** When a card is active (e.g., a current speaking prompt), give it a 1px inner stroke of `secondary` (#ADC6FF) at 20% opacity and a subtle outer glow.

### High-Contrast Status Indicators
*   **Confidence Score:** Use `secondary` (#ADC6FF) for positive metrics and `error` (#FFB4AB) for critical speech errors. 
*   **Gamification Progress:** Use a thick (8px) bar with a `primary` to `secondary` gradient. The background track must be `surface-container-highest`.

### Input Fields
*   **The "Clean" Input:** Background: `surface-container-low`. No border. On focus, the background shifts to `surface-container-high` and a subtle 2px bottom-glow in `secondary` appears.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use extreme vertical rhythm. Use `spacing-12` (3rem) or `spacing-16` (4rem) to separate major modules.
*   **Do** use "Backdrop Blur" (12px-20px) on every translucent surface to maintain text readability over background neons.
*   **Do** use asymmetrical card layouts (e.g., a small "Achievement" chip overlapping the corner of a larger "Lesson" card).

### Don’t:
*   **Don’t** use pure white (#FFFFFF) for body text. Use `on_surface_variant` (#CCC3D7) to reduce eye strain in the dark theme.
*   **Don’t** use sharp corners. Everything must use the `md` (0.75rem) to `xl` (1.5rem) scale to maintain the "premium gaming" softness.
*   **Don’t** ever use a solid grey divider. If you need a line, use a 1px gradient line that fades to 0% opacity at both ends.

---

## 7. Signature Feature: The "Aura" System
Behind key UI elements (like the "Start Coaching" button or the "User Profile"), place blurred vector shapes in `primary_container` and `secondary_container` at 10% opacity. These "Auras" move slightly on mouse-hover, creating a sense of living AI energy.```