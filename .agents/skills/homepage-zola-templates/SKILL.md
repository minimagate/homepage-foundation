---
name: homepage-zola-templates
description: Create or change Zola templates, reusable partials, navigation, footers, metadata, and inline SVG icons across the homepage sites while preserving their shared document shell and accessibility conventions.
---

# Homepage Zola Templates

Use this skill for template work in any consumer site. Read [the shell and component contract](references/shell-and-components.md) before changing shared-looking markup, then read the destination repository's `AGENTS.md`.

## Work at the right level

`templates/base.html` owns document metadata, stylesheet loading, primary navigation placement, page content, and footer placement. Extend it; do not duplicate the shell in page templates. Put repeated fragments in `templates/partials/`, and use the existing lists, heading rows, prose article, and metadata classes before inventing a parallel component.

Keep links and URLs centralized in content or `zola.toml` when the site already does so. A template should remain content-independent, accessible, and valid with the empty state it can legitimately receive.

## Preserve the editorial interface

The visible shell is intentionally text-first: primary navigation, a large separation before content, compact list rows, then external/footer links and legal links. Do not add a logo treatment, hero visual, card grid, client-side behavior, tracking, remote font, or icon library without an explicit request.

For inline SVGs, keep `currentColor`, the established 24px viewBox/outline language, `aria-hidden="true"`, and `focusable="false"` when the icon is decorative. A linked icon must have a text label or equivalent accessible name. External `target="_blank"` links need an appropriate `rel` value.

## Metadata and validation

Preserve canonical, title, description, Open Graph, and article metadata blocks when editing a rendered page type. Use page/section data rather than copied strings. Check the Zola build and inspect affected pages at narrow and wide widths when markup or classes change.
