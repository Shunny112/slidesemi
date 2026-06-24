---
name: zettai-seminar-ui
description: Reusable ZETTAi-style Japanese seminar slide and UI design system. Use this skill whenever the user wants to create, redesign, review, or polish seminar slides, HTML slide decks (especially 1600x900 16:9 decks), presentation-style web pages, Japanese training/研修 decks (セミナースライド), or business UI screens — even if they don't explicitly say "ZETTAi". Trigger it for any warm-white deck with orange accents, strict Japanese typography, thin rules, square panels, structured diagrams (pipeline / hub map / before-after / time table / agenda), and non-decorative corporate presentation layouts.
---

# ZETTAi Seminar UI

Apply the visual language extracted from the ZETTAi seminar deck (reference implementation: `~/slidesemi/デザインセミナー.html`): warm white canvas, subtle orange/rose atmospheric light, large Japanese headings, thin ruled structure, square panels, clear diagram systems, and restrained corporate presentation polish. That deck is the canonical, full-fidelity example — read it when you need a complete worked reference beyond the bundled starter template.

## Workflow

1. Identify the target output: HTML slide deck, PowerPoint/Keynote-like deck, landing section, dashboard screen, or review-only task.
2. Read `references/design-language.md` before making visual decisions.
3. Read `references/component-patterns.md` when building slide sections, cards, diagrams, comparison tables, timelines, agenda pages, or proof/contact slides.
4. Use `assets/seminar-slide-template.html` as a starter only when creating a new standalone HTML slide deck.
5. Use bundled visual references when useful:
   - `assets/example-before-after.png`
   - `assets/example-hub-map.png`
   - `assets/zettai-logo-transparent.png`
6. Verify the result against the checklist in `references/design-language.md`, especially Japanese line wrapping, 16:9 framing, thin borders, contrast, and no horizontal overflow.

## Design Intent

Favor clarity over ornament. The style should feel like a polished executive seminar deck: calm, structured, legible from a screen share, and business-focused. Use accent color to direct attention, not to decorate everything.

## Coordination

When the task is broader UI/UX design rather than this specific seminar aesthetic, generate a general design system first, then adapt the result through this skill if the user wants the ZETTAi seminar look. (If a general-purpose `ui-ux-pro-max` design skill is available in the environment, use it for that first pass.)
