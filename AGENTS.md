# Agents Instructions

This is a simple static assets repository served via GitHub Pages at `https://activescott.github.io/public-static/`.

## Key Facts

- This is a **public** repository. Do not add sensitive information, secrets, or detailed internal architecture.
- Files pushed to `main` are automatically published via GitHub Pages.
- The primary consumer is the private `activescott/tinkerbell` repository, which references these pages in automated benchmarks.

## Structure

- `test-fixtures/` — Static HTML fixture pages for web scraping benchmarks. See `test-fixtures/README.md`.

## Guidelines

- Keep fixture HTML simple and self-contained (no external CDN scripts or CSS).
- Content in fixtures must remain stable — benchmark tests assert on specific text, URLs, and values.
- When editing fixtures, corresponding benchmark expectations in the consuming repo need updating too.
