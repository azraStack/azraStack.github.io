# AGENTS.md

## What this is

Static single-page portfolio for Abid Zikry, published with GitHub Pages at
`azraStack.github.io`. Only `index.html` and `style.css` — no framework, no
package manager, no build step, no dependencies, no tests.

## Verify changes

There is nothing to build or lint. Check the page by opening `index.html` in a
browser, or serve it with any static file server. (`python -m http.server` does
not work on this machine — `python` is the Windows Store stub — but Node is
installed.)

Do not add a bundler/npm toolchain without also reconfiguring Pages; the site is
served from the repo as-is.

## Deploy

GitHub Pages serves the root of `main`. Pushing or merging to `main` publishes
the public site immediately — there is no CI gate or staging step.

## Editing rules

- All styling lives in `style.css` (linked relatively from `index.html`). No
  inline styles and no JavaScript are used; keep it that way.
- Theme tokens live in `:root` in `style.css`. The palette is dark and warm:
  `--ink` `#0a1018`, `--paper` `#e9e3d6`, `--brass` `#c6a664`, with hairline
  rules in `--line`. Build new UI from these tokens instead of adding one-off
  colors.
- Typography is Bodoni Moda (display) plus Instrument Sans (body), loaded from
  Google Fonts in the `<head>`. Keep it to these two families.
- Nav links are hash anchors (`#about`, `#skills`, ...). Each must match the
  `id` of its `<section>`; renaming a section requires editing both files.
- Top-level CSS rules are indented 4 spaces. The only viewport breakpoint is
  `@media (max-width: 768px)`; reduced-motion handling sits beside it near the
  end of the file.
- For design work, load the `frontend-design` skill in
  `.opencode/skills/frontend-design/`.
- `README.md` is a stale one-liner (`# abid.github.io`) and is not
  documentation.
