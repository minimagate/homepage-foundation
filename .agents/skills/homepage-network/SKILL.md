---
name: homepage-network
description: Coordinate work across the personal, research, Bivouac, and homepage-foundation repositories. Use when a request spans repositories, affects a shared submodule, requires choosing between a shared or local change, or needs cross-site validation.
---

# Homepage Network

Work from the repository that owns the requested outcome. The sibling repositories are:

- `homepage`: personal site; local CSS is `static/styles/personal.css`.
- `research.homepage`: Geometry of Meaning; local CSS is `static/styles/research.css`.
- `bivouac.homepage`: Bivouac site; local CSS is `static/styles/bivouac.css`.
- `homepage-foundation`: shared `core.css` source and shared agent skills.

## Start safely

1. Read the target repository's `AGENTS.md` before changing its content or templates.
2. Run `git submodule update --init --recursive` in every consumer repository in scope.
3. Inspect each worktree. Preserve unrelated changes, especially content and generated research artifacts.
4. Keep `public/` generated and unedited.

## Choose the owner

- Change `homepage-foundation/core.css` only for a component that should look and behave the same on every site.
- Change a consumer's local CSS for a site-specific layout or feature.
- Keep research maths, figures, plots, and data-table rules in `research.css`.
- Keep personal project/work variants in `personal.css`.
- Keep Bivouac component, download, and status UI in `bivouac.css`.

## Complete cross-repository work

1. Make and validate the foundation change first.
2. Commit the foundation revision before updating consumer gitlinks.
3. Update each affected consumer submodule with `git submodule update --remote static/styles/foundation`.
4. Check that consumers still exclude `styles/foundation/.git`, `styles/foundation/.agents`, and `styles/foundation/.agents/**` through `ignored_static` in `zola.toml`.
5. Run `zola check --skip-external-links`, `zola build`, and `git diff --check` in every affected consumer.

Do not use a remote stylesheet, duplicate the core into a local stylesheet, or change a submodule pointer without a matching foundation revision.
