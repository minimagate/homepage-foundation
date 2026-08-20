# Shared editorial design system

## Character

The sites use a narrow, monochrome reading column rather than a product-marketing layout. The page is white with near-black text, subtle neutral secondary text and borders, and one blue selection colour. Content is carried by hierarchy, whitespace, and weight—not panels, shadows, gradients, badges, or decorative colour.

## Type and spacing

- Content width: `43.75rem` with a `1rem` gutter; centered from 768px upward.
- Base: `11pt`, `1.625` line-height, normally weight 300–400.
- UI and headings remain deliberately small: page titles are `13pt`/1.5 at weight 400; list and body copy stays near the base scale.
- Sans uses the platform stack; local Geist Mono is reserved for code and technical identifiers.
- The navigation has a generous 4rem separation below it. Lists and page blocks use 2rem-scale rhythm; rows use 1rem gaps.

## Shared components

- Navigation: horizontal text links, light weight, compact padding; no logo lockup or active-pill treatment.
- Links: inherit text colour by default. Prose links use a muted underline that becomes current-colour on hover.
- Lists: semantic linked rows, title first and subdued category/date second; stacked on mobile, baseline aligned on desktop.
- Prose: low-emphasis supporting copy; headings are modest; code and preformatted blocks are restrained neutral surfaces.
- Footer: external destinations as outline-link icon plus visible lowercase label, followed by copyright and legal links; vertically stacked on mobile.
- Icons: simple inline 24px-viewBox outline SVGs, `currentColor`, 1.5 stroke, decorative unless they convey unique information.

## Responsive and accessible invariants

Do not lower the `360px` document minimum without a cross-site decision. Preserve `:focus-visible`, readable text contrast, tabular dates, semantic headings, and the mobile-first stacked order. New styling should use existing tokens and `rem` units and stay local unless every consumer needs it.
