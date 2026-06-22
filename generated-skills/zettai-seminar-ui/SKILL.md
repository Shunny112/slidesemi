---
name: zettai-seminar-ui
description: Reusable ZETTAi-style Japanese seminar slide and UI design system. Use when Codex needs to create, redesign, review, or polish seminar slides, HTML slide decks, presentation-style web pages, Japanese training decks, or UI screens based on the existing warm-white ZETTAi seminar slide design with orange accents, strict typography, thin rules, square panels, structured diagrams, and non-decorative business presentation layouts.
---

# ZETTAi Seminar UI

Apply the visual language extracted from the seminar deck in this workspace: warm white canvas, subtle orange/rose atmospheric light, large Japanese headings, thin ruled structure, square panels, clear diagram systems, and restrained corporate presentation polish.

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

When the task is broader UI/UX design rather than this specific seminar aesthetic, also use `$ui-ux-pro-max` first to generate a general design system, then adapt the result through this skill if the user wants the ZETTAi seminar look.
