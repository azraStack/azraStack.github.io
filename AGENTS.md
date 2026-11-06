# AGENTS.md

## What this is

Static single-page portfolio for Abid Zikry, published with GitHub Pages at
`azraStack.github.io`. Only `index.html` and `style.css` — no framework, no
package manager, no build step, no dependencies, no tests.

## Verify changes

There is nothing to build or lint. Check the page by opening `index.html` in a
browser, or serve it locally:

    python -m http.server 8000

Do not add a bundler/npm toolchain without also reconfiguring Pages; the site is
served from the repo as-is.

## Deploy

GitHub Pages serves the root of `main`. Pushing or merging to `main` publishes
the public site immediately — there is no CI gate or staging step.

## Editing rules

- All styling lives in `style.css` (linked relatively from `index.html`). No
  inline styles and no JavaScript are used; keep it that way.
- Nav links are hash anchors (`#about`, `#skills`, ...). Each must match the
  `id` of its `<section>`; renaming a section requires editing both files.
- Top-level CSS rules are indented 4 spaces; the only breakpoint is
  `@media (max-width: 768px)`; use the existing palette (`#0f172a` surfaces,
  `#38bdf8` accent).
- `README.md` is a stale one-liner (`# abid.github.io`) and is not
  documentation.
