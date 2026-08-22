# Shared editorial design system

## Character

The sites use a narrow, Hacker News-inspired reading column rather than a product-marketing layout. A warm off-white content field sits on white, with black text, classic browser-coloured links, muted grey metadata, and a quiet `#ebebe2` header. Content is carried by density, hierarchy, and familiar browser conventions—not panels, shadows, gradients, badges, or decorative effects.

## Type and spacing

- Content width: `38rem` with a `1rem` gutter; centered from 768px upward.
- Base: `10pt`, `1.25` line-height at weight 400.
- UI and headings remain deliberately small: headings stay at the base scale and use weight 700; metadata is `9pt`.
- Sans uses Verdana with Geneva as fallback; local Geist Mono is reserved for code and technical identifiers.
- The navigation has a compact 1rem separation below it. Lists and prose use a .75rem/.35rem rhythm, with .375rem below section headings.

## Shared components

- Navigation: a `#ebebe2` strip with compact, underlined classic-blue links; no logo lockup or active-pill treatment.
- Links: classic browser states everywhere outside the footer—blue and underlined, purple when visited, and red while active. Footer links remain muted grey without underlines.
- Lists: semantic linked rows with an underlined classic-colour title followed by plain, subdued 9pt role/category/date metadata in parentheses; stacked on mobile, baseline aligned on desktop.
- Prose: compact black copy with bold, base-size headings; code and preformatted blocks remain restrained neutral surfaces.
- Footer: external destinations use a tilde mark plus a visible lowercase label, followed by copyright and legal links; vertically stacked on mobile.
- Section headings use a black typographic asterisk. Keep SVG icons only where they convey a site-specific function or identity.

## Responsive and accessible invariants

Below `768px`, the warm page field spans the full viewport with no exterior side gutter or top offset; `.site-main` keeps its compact internal padding so text does not touch the screen edge. Do not lower the `360px` document minimum without a cross-site decision. Preserve the black `:focus-visible` outline, readable text contrast, tabular dates, semantic headings, and the mobile-first stacked order. New styling should use existing tokens and `rem` units and stay local unless every consumer needs it.
