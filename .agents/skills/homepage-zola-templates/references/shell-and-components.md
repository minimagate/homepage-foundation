# Shell and component contract

All three sites share this sequence inside `main.site-main`:

1. `partials/nav.html` wraps the primary `nav` in `.nav-shell`.
2. The page template renders a semantic `section`, usually with a page heading/title, optional compact metadata, and an `article.prose`.
3. `partials/footer.html` renders external links, a copyright line, and `partials/legal-links.html`.

The footer differs only in site-specific destinations and copyright holder. Keep its structure, legal nav label, external-link icon-plus-label pattern, and the three legal links consistent.

## Reusable patterns

- `.page-heading` is for a homepage or section heading; `.page-title` / `.post-title` is for a detail page.
- `.intro` holds a short homepage or section lede; `.quote` supports one restrained closing quotation.
- `.list-heading-with-icon` joins a decorative 18px section icon with `.list-heading`.
- `.entry-list` / `.post-list` contains linked rows; `.entry-row` / `.post-row` switches from stacked mobile content to baseline-aligned desktop metadata.
- `.page-meta` / `.post-meta` is subdued, compact supporting context.
- `.prose` is the sole normal Markdown rendering surface.

The canonical external-link glyph is `partials/arrow.html`: decorative 24px outline SVG with a visible adjacent label. Site subject icons are local partials, not a generic icon dependency.

## Site navigation

- Personal: Home, Projects, Essays and Dissertations, Contact.
- Research: Home, Experiments, Data, Observations.
- Bivouac: Home, Format, Base, Field, Docs, Status.

Navigation labels are short, title-cased, and direct. Keep their order intentional and do not mark an active item unless that behavior is requested across the family.
