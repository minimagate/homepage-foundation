# homepage-foundation

Shared visual foundation for the personal, research, and Bivouac websites.

`core.css` owns the stable editorial system: local fonts, design tokens, page
shell, navigation, headings, list rows, prose, footer, focus states, and
responsive behavior. It deliberately excludes site-specific features such as
research maths and figures, personal project metadata, and Bivouac component
cards.

Each consuming site includes this repository as the `static/styles/foundation`
submodule and imports it first:

```css
@import url("foundation/core.css");

/* Site-specific rules only. */
```

Keep the core limited to components that should look and behave the same across
all sites. Update consumers to the new submodule revision whenever the core
changes, then run their normal Zola validation.

## Agent skills

The ignored `.agents/skills/` workspace contains the operating skill set for
this site family:

- `homepage-network` for cross-repository ownership and validation.
- `shared-homepage-styles` for the common visual system.
- `homepage-editorial` for shared voice, content structure, and metadata.
- `homepage-zola-templates` for document shells, partials, metadata, and icons.
- `homepage-research-publication` for Geometry of Meaning evidence and charts.
- `homepage-bivouac-publication` for Bivouac components and release content.

These complement, rather than replace, each consumer repository's `AGENTS.md`.
