---
name: homepage-research-publication
description: Publish or review Geometry of Meaning archive content, charts, and presentation while preserving immutable-run provenance, research scope, and the shared editorial site system.
---

# Homepage Research Publication

Use this skill for `research.homepage` content, observation charts, research templates, and research-specific CSS. Read that repository's `AGENTS.md` before acting; it is the detailed publication contract.

Treat the sibling `geometry-of-meaning` repository as the source of truth for corpus, protocol, runs, notebooks, metrics, and figure builders. The website owns editorial presentation, chart manifests, imported public charts, and explanatory text. Never modify immutable runs or manually alter imported chart HTML.

## Publish by evidence type

- Experiments document controlled changes and intended measurements; outcomes belong in observations.
- Observations report one completed immutable run and cite its model, population, aggregation, projection, and limitations.
- Data pages describe canonical corpus membership and provenance.

Use the chart manifest and importer for every published Plotly output. Preserve grayscale encodings, same-origin dynamic iframe sizing, meaningful captions, and responsive overflow behavior. Do not use a colourful palette, fixed iframe height, or hand-copied charts.

Keep research-only maths, figures, plots, source lists, and table rules in `research.css`; route stable shell changes through `shared-homepage-styles` and cross-site changes through `homepage-network`.
