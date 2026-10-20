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
  BREAKING CHANGE: migrate gruvbox to GitHub's new primer tokens and adopt semantic-release tooling

## 2.0.0 (2025-05-13)

### ⚠ BREAKING CHANGES

* renaming `index.css` to `<repo-name>.user.css`

### Features

* add new color var `--color-accent-emphasis` for https://docs.github.com/en/enterprise-cloud@latest/copilot/copilot-chat-cookbook ([5d0f6e2](https://github.com/marslo/github-gruvbox/commit/5d0f6e221dc747d82cb4bdc73e72554fdbb35ae9))
  - remove tailing whitespace

### Styles

* renaming to `<repo>.user.css` ([43e8c35](https://github.com/marslo/github-gruvbox/commit/43e8c353cf8651c4c28333043c910330db75463a))
