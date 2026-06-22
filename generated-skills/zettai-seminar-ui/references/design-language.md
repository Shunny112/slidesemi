# ZETTAi Seminar UI Design Language

## Core Look

- Canvas: 16:9, white or near-white paper surface, centered in a light gray stage when previewed.
- Mood: warm, precise, corporate, instructional. Avoid playful, glossy, rounded, or marketing-heavy styling.
- Geometry: square corners by default. Use thin lines and spacing instead of heavy shadows.
- Accent: muted orange for emphasis, sequence numbers, arrows, active states, and key terms.
- Background: very subtle radial warmth only. It should be barely visible and never compete with content.

## Tokens

Use these tokens unless the project already has a stronger brand system:

```css
:root {
  --paper: #ffffff;
  --paper-2: #fafafa;
  --ink: #121212;
  --text: #2f2f2f;
  --muted: #5f5b56;
  --line: #ded8d2;
  --orange: #d86f32;
  --orange-2: #eda56a;
  --orange-soft: #fff7f1;
  --rose: #c9655c;
  --rose-soft: #fff0ed;
  --green: #3f8b52;
  --red: #c64b3c;
  --glass: rgba(255,255,255,.96);
  --shadow: 0 24px 58px rgba(30, 24, 18, .10);
  --sans: -apple-system, BlinkMacSystemFont, "Segoe UI", "Noto Sans JP", "Helvetica Neue", Arial, sans-serif;
}
```

## Slide Shell

- Use a fixed 1600 x 900 design coordinate system for HTML slide decks.
- Use `padding: 46px 54px 34px`.
- Structure slides as `kicker`, `body`, `foot`.
- Footer: left URL/source text, right logo, thin rule above footer. Keep it quiet.
- Keep the deck itself square-cornered; stage shadow may be present only in browser preview.
- Do not place content behind fixed nav controls.

Suggested background:

```css
.slide {
  background:
    linear-gradient(135deg, rgba(255,255,255,.76), rgba(255,255,255,0) 46%),
    radial-gradient(ellipse at 84% 16%, rgba(237,165,106,.10), transparent 36%),
    radial-gradient(ellipse at 18% 84%, rgba(201,101,92,.06), transparent 38%),
    var(--paper);
}
```

## Typography

- Use system Japanese sans stack. Do not introduce decorative fonts.
- Letter spacing: `0`.
- Use `line-break: strict` for Japanese text.
- Use `text-wrap: balance` for headings and prominent copy.
- Use no negative tracking and no viewport-only font scaling.
- Heading scale for 1600 x 900:
  - H1: 50-78px, line-height 1.12, weight 760.
  - H2: 36-58px, line-height 1.18, weight 740.
  - H3: 22-29px, line-height 1.25-1.35, weight 720.
  - Lead: 23-32px, line-height 1.48, weight 600.
  - Body in panels: 16-20px, line-height 1.45-1.65, weight 540-620.
- For one-line Japanese headlines, use explicit classes and test at target aspect ratio; do not rely on accidental fitting.

## Emphasis

- Use orange text for the key phrase only.
- Use an underline highlight for important Japanese words:

```css
.highlight-text {
  display: inline;
  padding: 0 .12em .04em;
  color: var(--orange);
  background: linear-gradient(180deg, transparent 58%, rgba(237,165,106,.28) 58%);
  box-decoration-break: clone;
  -webkit-box-decoration-break: clone;
}
```

- Use a stronger inline chip sparingly:

```css
.highlight-strong {
  display: inline-block;
  padding: .05em .18em .1em;
  color: var(--ink);
  background: rgba(255,244,234,.95);
  border-bottom: 3px solid var(--orange);
}
```

## Layout Rules

- Use large whitespace and aligned grids. Do not fill every area.
- Favor 2-column, 3-column, hub-and-spoke, before/after, and pipeline layouts.
- Use `gap` values around 16-28px for components and 44-58px for major cover spacing.
- Use thin `1px solid var(--line)` borders for all panels.
- Use `border-radius: 0` for panels, controls, cards, and agenda items.
- Use no heavy drop shadows inside slides.
- Cards and panels should sit directly on the slide, not inside another card.

## Motion

- For HTML slides, use restrained enter animations:
  - Headings rise 22px while fading in.
  - Panels use a soft punch: rise 18px, slight overshoot, settle.
  - Lines reveal from left.
  - Progress bars grow from width 0.
- Always respect `prefers-reduced-motion`.

## Accessibility and QA

Before delivery:

- Confirm every slide/screen fits at 1600 x 900 and at the requested preview sizes.
- Confirm Japanese headings do not collide with panels or footers.
- Confirm no horizontal scroll on responsive previews.
- Keep body text contrast at least equivalent to `#2f2f2f` on white.
- Do not use emojis as icons. Use text labels, Lucide/SVG icons, or simple typographic marks.
- Make clickable controls `cursor: pointer` with visible hover/focus states.
- Use alt text for photos and logos.
- Keep backgrounds subtle enough that screenshots and projected slides remain readable.

## Anti-Patterns

- Rounded SaaS cards, gradient button-heavy layouts, purple/blue tech gradients, dark mode by default.
- Decorative blobs, bokeh, oversized hero compositions, stock-photo atmosphere.
- Dense paragraphs inside panels.
- Small footer logos as the only brand signal on brand slides.
- Multiple accent colors competing with orange.
- Random icon styles or emoji markers.
