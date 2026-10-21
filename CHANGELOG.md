## [3.2.1](https://github.com/marslo/github-gruvbox/compare/v3.2.0...v3.2.1) (2026-10-21)

### Bug Fixes

* **theme**, **diff**: map uncovered button, control, tooltip and progress tokens to the palette and keep hunk expander rows readable on hover ([04390bf](https://github.com/marslo/github-gruvbox/commit/04390bfd6dc512dbe2b754a8d9616bf668aeddbc))
  - map inactive and disabled button tokens to the palette
  - add button counter, keybinding hint, tooltip, card, menu and avatar colors
  - map progress bar, reaction button and disabled control tokens
  - use `--gruv-on-emphasis` for the hunk hover foreground
  - let hunk expander text and icon inherit the row hover color

### Code Refactoring

* **theme**: recolor links and accent tints from aqua to blue and keep topic tags green ([fdb6b78](https://github.com/marslo/github-gruvbox/commit/fdb6b78256bf68216867e986523c7430b5e48b91))
  - point `--fgColor-accent`, `--fgColor-link` and legacy `--color-accent-fg` at blue
  - tint accent backgrounds and borders blue
  - color `.Link--muted` hover blue
  - scope a green accent onto primer react `TopicTag` and legacy `.topic-tag`
  - replace the hardcoded light-blue `.topic-tag-link` hover background

## [3.2.0](https://github.com/marslo/github-gruvbox/compare/v3.1.1...v3.2.0) (2026-10-21)

### Features

* **theme**, **release**: split into classic gruvbox and gruvbox-material userstyles with a switchable `Palette` option for dark/light and hard/medium/soft ([f1566a6](https://github.com/marslo/github-gruvbox/commit/f1566a674aaca91a635ace6bc881f85e38de68e0))
  - restore classic gruvbox colors in `github-gruvbox.user.css` with `Dark` / `Light` options
  - add `github-gruvbox-material.user.css` with dark/light × hard/medium/soft options
  - switch palettes via `@var select palette` and the `uso` preprocessor
  - add scheme-aware roles for `color-scheme` and text on colored backgrounds
  - bump `@version` in both userstyles on release and document them in the README

## [3.1.1](https://github.com/marslo/github-gruvbox/compare/v3.1.0...v3.1.1) (2026-10-21)

### Bug Fixes

* **theme**: mute secondary text to grey and switch links and accent tints to aqua ([611ed42](https://github.com/marslo/github-gruvbox/commit/611ed4239fa2ba2bfc72d3cbbc2fbecce2c9258b))

## [3.1.0](https://github.com/marslo/github-gruvbox/compare/v3.0.0...v3.1.0) (2026-10-20)

### Features

* **theme**, **release**: adopt gruvbox-material hard dark palette ([f146b79](https://github.com/marslo/github-gruvbox/commit/f146b792006184e89db5d98c7164bf1fd7a91685))
  - remap `--gruv-*` palette to gruvbox-material hard dark with material foreground
  - derive `-dark` variants and translucent tokens via `color-mix()` on palette vars
  - use gruvbox-material `bg_diff_*` / `bg_visual_*` colors for diff lines and line numbers
  - add `@maintainer`, `@homepageURL` and `@updateURL` userstyle metadata
  - drop `BREAKING CHANGE` footer lines from release-note bodies and the `3.0.0` changelog entry

## [3.0.0](https://github.com/marslo/github-gruvbox/compare/v2.0.0...v3.0.0) (2026-10-20)

### ⚠ BREAKING CHANGE

* **theme,release:** migrate gruvbox to GitHub's new primer tokens and adopt semantic-release tooling

### Bug Fixes

* **theme**, **release**: restore theme on new primer tokens ([a7394c2](https://github.com/marslo/github-gruvbox/commit/a7394c28ce3a35dc11feb9aa495f4a8e868c071b))
  - remap palette onto `--bgColor-*`, `--fgColor-*`, `--borderColor-*`, `--button-*`, `--control-*`, `--codeMirror-*` and `--diffBlob-*` tokens
  - apply overrides on `:root` and nested `[data-color-mode]` roots via `:not(#_gruvbox)` so chained `var()` tokens resolve to gruvbox colors
  - keep legacy `--color-*` tokens on `body` as fallback and fix undefined `--gruv-bg` reference
  - add semantic-release config, pre-commit hooks, stylelint/typos configs and pre-commit CI workflow
  - add `CHANGELOG.md` with the `2.0.0` release entry

## 2.0.0 (2025-05-13)

### ⚠ BREAKING CHANGES

* renaming `index.css` to `<repo-name>.user.css`

### Features

* add new color var `--color-accent-emphasis` for https://docs.github.com/en/enterprise-cloud@latest/copilot/copilot-chat-cookbook ([5d0f6e2](https://github.com/marslo/github-gruvbox/commit/5d0f6e221dc747d82cb4bdc73e72554fdbb35ae9))
  - remove tailing whitespace

### Styles

* renaming to `<repo>.user.css` ([43e8c35](https://github.com/marslo/github-gruvbox/commit/43e8c353cf8651c4c28333043c910330db75463a))
