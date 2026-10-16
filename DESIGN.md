---
name: Alderney Gambling Control Commission
description: A modern, transparent, firm regulator. Evolved aubergine ink on warm island granite.
---

<!-- 2026-10-16 DIRECTION CHANGE: the user found the aubergine palette flat and boring and picked "Mix 1 and 2" from directions.html. The page is now GORSE & GRANITE with Atlantic photo moments: warm cream paper, granite charcoal (replaces aubergine as the dark field), Alderney gorse yellow as the bold accent (highlighter emphasis, drenched register chapter, ticker band, CTAs), plus a full-bleed lighthouse photo hero under a granite-to-sea overlay and the stone-cairn photo ("balance") in Why Alderney. Pills for buttons. The aubergine "Committed Ink" and "No Gold" rules below are SUPERSEDED (gorse is a flower yellow, not gold). Re-run $impeccable document in scan mode to rewrite this file from home.html. -->
<!-- SEED — re-run $impeccable document once there's code to capture the actual tokens and components. -->
<!-- First build exists: home.html (2026-10-16). Fonts chosen (user pick from type-specimen.html, option B 'Reading Room'): Literata (display/headings, opsz) + Commissioner (UI/body/data with tabular figures). No monospace: it read as AI/clinical. Source Serif 4 + Schibsted + Geist Mono were rejected as too cold. Tokens live as OKLCH custom properties on :root in home.html. Run $impeccable document in scan mode to promote them into this file. -->

# Design System: Alderney Gambling Control Commission

## 1. Overview

**Creative North Star: "The Island Register"**

The AGCC is the public record of who may operate, written with the calm of a central bank and the clarity of a modern government service, on an island that is itself the credential. Every surface should read like a well-set official document that happens to be alive: precise type, real information, nothing hidden. PRODUCT.md asks for "authority through restraint", so confidence comes from typographic contrast, generous space and one deep, owned colour, never from ornament or superlatives.

The colour is committed: a deepened aubergine ink carries the identity across a significant share of the page (the hero, the register band, the closing chapter), set against warm granite-paper neutrals. It evolves the Commission's existing plum heritage into something darker, quieter and more modern, and it is deliberately unlike any other regulator's navy. Motion is responsive, not theatrical: feedback on every interaction, crisp reveals as content enters, no choreography that delays a player looking for the register or a lawyer looking for an Ordinance.

This system explicitly rejects: **casino and gambling glitz** (chips, cards, dice, neon, gold, dark Vegas mood), the **SaaS startup template** (gradient blobs, icon-card bento, hero stat bar, logo marquee), the **dusty council website** (grey boxes, carousels, clip-art, link soup), and the **navy-and-gold bank** palette.

**Visual style (Phase 2): `minimalist-ui`, adapted.** Borrowed for craft: editorial serif + precise sans + mono for data, macro-whitespace between chapters, hairline 1px rules, crisp radii (4 to 12px, never pill containers), boxless divider-only lists and accordions, `<kbd>`-style precision details, warm desaturated photography with fine grain, quiet 600ms scroll entries. Rejected from that skill: its ban on large coloured sections (our Committed Ink fields override it), pastel decoration (pastels survive only as licence-status tints), pure white canvas, bento feature grids, Playfair, ambient drifting blobs.

**The Never Boring Rule.** Restraint is not blandness. The user's explicit brief: this home page must not be boring at all. Calm comes from the system; excitement comes from a few deliberate, high-contrast moments. Every build must include all of these:
- **Scale contrast:** a very large serif statement against small, exact sans metadata. The gap between the biggest and smallest type on screen is dramatic, not polite.
- **Colour drama:** full-bleed Aubergine Ink chapters that cut hard against Granite Paper. The page changes temperature as you scroll, at least three times.
- **A living register:** the licence search is interactive on the home page itself (instant results, status shown in words, real-feeling licence numbers in tabular mono), not a link to another page.
- **Place as identity:** Alderney is drawn, not just photographed: the island's outline, coordinates (49.71° N, 2.20° W), tide-line or chart-like linework used as a recurring graphic language.
- **One signature moment:** a single memorable interaction or reveal (for example, the island outline drawing itself, or the register band unfolding) that people mention after the pitch. One, not five.
- **Layout variance:** no two consecutive sections share a structure. Avoid the stacked "heading, paragraph, grid" rhythm entirely.

Audit test: if a screenshot of any section could belong to a generic consultancy, a council or a SaaS startup, it fails.

**Key Characteristics:**
- Committed aubergine ink as the identity carrier, on warm granite-paper neutrals
- Serif display for institutional voice, precise sans for reading and interface
- Flat, tonal surfaces; depth from colour fields and rules, not shadows
- The licence register treated as the signature utility, not a menu item
- Place-led imagery of Alderney used with intent (light, coast, geography)
- Responsive motion: fast feedback, single reveals, no scroll-jacking

## 2. Colors

A single deep, committed hue over warm tinted neutrals, with functional status colours kept strictly for meaning.

### Primary
- **Aubergine Ink** ([to be resolved during implementation]; anchor reference: the AGCC's existing #601A58 / #300D2C, pushed darker and slightly desaturated toward near-black): the identity. Hero field, register band, footer chapter, primary actions, focus rings.
- **Heather Plum** ([to be resolved during implementation]; lighter tint of the primary, descended from the current #885682): secondary emphasis on aubergine fields, link hover, selected states. Never as large fills on paper.

### Neutral
- **Granite Paper** ([to be resolved during implementation]): main page ground. Warm, faintly mineral off-white, tinted toward the primary hue. Never pure white.
- **Island Stone** ([to be resolved during implementation]): secondary surfaces, subtle bands, table zebra.
- **Slate Ink** ([to be resolved during implementation]): body text. Near-black, tinted. Never #000.
- **Rule Grey** ([to be resolved during implementation]): hairline dividers and table rules.

### Functional (status only)
- **Licensed / Valid, Suspended, Revoked / Warning** ([to be resolved during implementation]): reserved for licence status and alerts, always paired with a text label and icon.

### Named Rules
**The Committed Ink Rule.** Aubergine Ink carries 30 to 60 percent of the page across a few large, intentional fields. It is a field colour, not a sprinkle: no aubergine confetti on small chips, badges and icons across paper sections.

**The No Gold Rule.** Gold, brass, champagne and amber are prohibited anywhere in the system. They read as casino or as navy-and-gold bank; both are anti-references.

**The Meaning-Only Status Rule.** Green, amber and red appear only to communicate licence or alert status, always with a word beside them. Never decorative.

## 3. Typography

**Display Font:** [serif display to be chosen at implementation; must feel institutional and current, not heritage cosplay, and must not be a default AI pick like Fraunces or Playfair]
**Body Font:** [precise sans to be chosen at implementation; excellent at small sizes, tabular figures available, never Inter]
**Label/Mono Font:** [optional; only if licence numbers, dates and register data benefit from a mono or tabular face]

**Character:** A serif with the poise of a central-bank report sets the Commission's voice in headlines; a crisp, highly legible sans does the work everywhere a visitor reads, searches or acts.

### Hierarchy
- **Display** ([weight, size and line-height to be resolved]): hero statement and chapter openers only. Two to three lines maximum at desktop.
- **Headline** ([to be resolved]): section titles.
- **Title** ([to be resolved]): route names, news headlines, register entries.
- **Body** ([to be resolved], minimum 16px): all reading text, capped at 65 to 75ch.
- **Label** ([to be resolved]): metadata such as dates, licence types, categories. Sentence case preferred over shouting uppercase.

### Named Rules
**The Two Voices Rule.** Serif speaks for the Commission (statements, headings). Sans serves the visitor (navigation, search, forms, data, body). Never swap them: no serif buttons, no sans hero statements.

**The Tabular Truth Rule.** Every number that is data (licence counts, dates, fees, licence numbers) is set with tabular figures so columns align and nothing jitters.

## 4. Elevation

Flat by default. Depth is conveyed by tonal layering: aubergine fields against granite paper, stone bands, and fine hairline rules, the way a printed annual report separates content. Shadows are not part of the resting vocabulary.

### Named Rules
**The Flat-By-Default Rule.** Surfaces are flat at rest. A shadow may appear only as a response to state (an open menu, a focused search panel) and must be soft, wide and tinted toward the primary hue. If a shadow is visible on a static element, remove it.

## 5. Components

[Omitted in seed mode: no components exist yet. Re-run `$impeccable document` once the home page is built.]

## 6. Do's and Don'ts

### Do:
- **Do** let Aubergine Ink own a few large fields (hero, register band, closing chapter) so the identity is unmistakable at a glance.
- **Do** make the licence register search a first-class, visible tool on the home page, as PRODUCT.md says: "The register is the hero utility."
- **Do** name every route in the visitor's language ("Check a licence", "Make a complaint", "Apply in Alderney"), not the Commission's org chart.
- **Do** use real information: actual licence counts, real news headlines, real dates. "Practise what you regulate."
- **Do** use Alderney imagery with intent: specific light, coastline and geography, treated consistently, never generic stock scenery.
- **Do** keep motion responsive: 150 to 250ms feedback, one reveal per section, opacity-only under `prefers-reduced-motion`.
- **Do** meet WCAG 2.2 AA everywhere, with visible focus rings in the primary hue and status never conveyed by colour alone.

### Don't:
- **Don't** use **casino and gambling glitz**: no chips, cards, dice, neon, gold, dark Vegas mood or slot-machine energy.
- **Don't** use the **SaaS startup template**: no gradient blobs, no bento of icon cards, no hero stat bar, no "trusted by" marquee.
- **Don't** build a **dusty council website**: no grey boxes, no carousels or sliders, no clip-art, no walls of link soup.
- **Don't** fall back to the **navy-and-gold bank** palette; the generated MASTER.md defaulted to exactly this and it is rejected.
- **Don't** hide content behind sliders or auto-rotating carousels; news is listed, not rotated.
- **Don't** use gradient text, glassmorphism, side-stripe accent borders, or identical icon-card grids.
- **Don't** use em dashes in interface copy.
