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
