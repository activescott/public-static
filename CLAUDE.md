# Claude Code Instructions

This is a simple static assets repository. Content is served via GitHub Pages at `https://activescott.github.io/public-static/`.

## Key Facts

- This is a **public** repository. Do not add sensitive information, secrets, or detailed internal architecture descriptions.
- Files pushed to the `main` branch are automatically published via GitHub Pages.
- The primary consumer of these assets is the private `activescott/tinkerbell` repository, which uses the test fixture pages for automated benchmark comparisons.

## Structure

- `test-fixtures/` — Static HTML pages for web scraping and content extraction benchmarks. See `test-fixtures/README.md` for details.

## Editing Fixtures

When editing fixture HTML files, keep in mind:
- The content must remain stable — benchmark scorers assert on specific text, URLs, and data values.
- If you change content in a fixture, the corresponding benchmark expectations in the consuming repo must also be updated.
- Fixture pages should be simple, self-contained HTML with no external dependencies (no CDN scripts, no external CSS).
