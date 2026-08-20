---
name: homepage-bivouac-publication
description: Create or revise Bivouac website pages, component updates, documentation, and status content while preserving the project's text-first design and release-accurate presentation.
---

# Homepage Bivouac Publication

Use this skill for `bivouac.homepage` editorial, template, and site-specific component work. Read its `AGENTS.md` first.

Bivouac has three first-class components: Format, Base, and Field. Their section metadata drives their page heading, introduction, version, call to action, and empty-update message. Keep destinations in `zola.toml`'s `[extra]` values and use the existing component, post, docs, and status templates rather than duplicating them.

Describe an implementation only at its known version and maturity. Releases need ISO dates, `post.html`, and an optional matching component backlink. Make a clear distinction between current functionality, a prototype, an in-development capability, and an unreleased component.

Use the existing compact outline icons for the three components and the labelled GitHub-style CTA for project actions. Keep component, download, and status UI in `bivouac.css`; escalate a stable shell change to the shared styles workflow. Preserve the no-JavaScript, locally hosted-font, accessible static-site model.
