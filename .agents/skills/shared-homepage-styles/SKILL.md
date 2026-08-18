---
name: shared-homepage-styles
description: Maintain the shared editorial CSS system used by the personal, research, and Bivouac Zola sites. Use when aligning a visual component across sites, modifying homepage-foundation/core.css, adding a common design token, or deciding whether a CSS rule belongs in the core or in a site-local stylesheet.
---

# Shared Homepage Styles

The shared source is `homepage-foundation/core.css`. Each Zola site imports it from its `static/styles/foundation` submodule before its local stylesheet rules.

## Decide the boundary

Put a rule in `core.css` only when it is a stable shared component: tokens, reset, shell, navigation, headings, links, list rows, prose, footer, focus treatment, or responsive behavior.

Keep these local:

- Personal: project/work presentation and icons.
- Research: semantic-model links, MathJax, figures, plots, and research tables.
- Bivouac: component presentation, calls to action, and project/status UI.

Favor shared selectors and aliases already present in the core. Do not create a site-specific exception merely to rename an otherwise common component.

## Change workflow

1. Inspect all three consumers before changing a shared rule.
2. Edit `homepage-foundation/core.css`; never edit a checked-out submodule file from a consumer repository.
3. Ensure the core still loads the local Geist Mono font with a path valid from `styles/foundation/core.css`.
4. Commit the foundation revision, then update the submodule pointer in each affected site.
5. Keep each consumer's `ignored_static` entries for `styles/foundation/.git`, `styles/foundation/.agents`, and `styles/foundation/.agents/**` so Zola never publishes submodule metadata or agent instructions.

## Validate

For every affected consumer, run:

```sh
git submodule update --init --recursive
zola check --skip-external-links
zola build
git diff --check
```

Confirm the build contains both the local stylesheet and `public/styles/foundation/core.css`, but not `public/styles/foundation/.git`.
