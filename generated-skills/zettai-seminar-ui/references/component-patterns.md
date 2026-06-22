# ZETTAi Seminar UI Component Patterns

Use these patterns to reproduce the seminar slide system in new decks or presentation-style web UI.

## Kicker and Footer

Kicker:

- Left aligned, 14-18px, 680-820 weight.
- Split kicker uses title on left and section number on right.
- Section number is orange.

Footer:

- Grid with source/URL on the left and logo on the right.
- Add a horizontal rule about 74px above the bottom edge.
- Footer text is muted, 14px, 650 weight.

## Cards and Panels

Use for repeated ideas, comparisons, proof points, and short explanations.

```css
.card,
.panel {
  border: 1px solid var(--line);
  border-radius: 0;
  background: var(--glass);
  box-shadow: none;
}
.card { min-height: 150px; padding: 22px; }
```

Content rules:

- One clear heading per panel.
- Body copy should be 1-3 short lines.
- Use orange only for labels, numbers, or key phrase.
- Avoid placing cards inside a parent card.

## Comparison

Use two panels with a centered arrow for before/after or good/bad choices.

- Grid: `1fr auto 1fr`, gap 24px.
- Panel min-height around 280px.
- Use green check marks and red crosses only for status lists.
- Use the arrow as orange typography, not an illustrated icon.

## Checklist Lists

```css
.check-list,
.x-list {
  display: grid;
  gap: 12px;
  margin: 0;
  padding: 0;
  list-style: none;
  color: var(--text);
  font-size: 18px;
  line-height: 1.58;
  font-weight: 560;
}
.check-list li,
.x-list li {
  display: grid;
  grid-template-columns: 24px 1fr;
  gap: 10px;
}
```

Use simple generated marks:

- Check: `✓`, color `--green`
- Cross: `×`, color `--red`

## Pipeline Diagram

Use for input-process-output narratives.

- Grid: `1fr auto 1fr auto 1fr`.
- Box min-height 190px, padding 24px.
- Label: orange 15px uppercase-like text.
- Main text: 29px, 740 weight.
- Description: 16px, line-height 1.45.
- Key box: orange border and soft orange background.

## Hub Map

Use when one concept enables several capabilities.

- Three columns: flexible left, fixed-ish center, flexible right.
- Center uses 2px orange border and soft radial orange background.
- Six surrounding items work well: three left, three right.
- Center item can include logo, mascot, or a strong two-line phrase.
- Surrounding item labels use orange sequence numbers and black body text.

## Curriculum or Step Map

Use for 3-4 step frameworks.

- Three columns for long explanations, four columns for compact steps.
- Each step is a square panel.
- Add thin connector lines between steps.
- Step number is orange and small.
- Main step title is 24-29px.
- For detailed steps, use mini-flow rows with left orange border.

## Time or Effort Diagram

Use for showing before-state effort or workload distribution.

- Left side: stacked bars in a bordered panel.
- Right side: single automation card with a large numeric claim.
- Bar track has a white fill and line border.
- Fill uses orange-to-light-orange gradient.
- Keep numeric claims large enough to scan quickly.

## Agenda and TOC

- Two-column list with thin top and bottom rules.
- Number column around 54px.
- Agenda title 23px, description 16px.
- Use column flow for 6-8 items.
- Avoid card backgrounds for the whole agenda; the rules are enough.

## Photo Layouts

- Use real seminar, office, product, or team photos when available.
- Photos use square corners, thin border, and slight saturation/contrast moderation.
- Add a subtle dark gradient only when a caption sits over the image.
- Captions: white, 12-14px, 620-640 weight.
- Do not use generic atmospheric images when real proof images exist.

## Contact Slide

- Center the company name/logo and contact lines.
- Use no form-like cards.
- Keep email and website readable at 24px or larger.
- Footer may remain, but the center content is the primary signal.

## Responsive Web Adaptation

When adapting this slide language to a web UI:

- Use the same tokens and square panels.
- Convert 1600 x 900 grids into responsive CSS grid with clear breakpoints.
- Keep headings smaller in dashboards and tools; do not use slide-scale type in compact UI.
- Preserve thin rules, orange labels, and calm white backgrounds.
- Replace slide footers with page-level metadata or subdued headers.
