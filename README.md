# public-static

Static assets and test fixtures hosted via GitHub Pages.

**GitHub Pages URL:** `https://activescott.github.io/public-static/`

## Structure

- `test-fixtures/` — Static HTML pages used as stable, version-controlled test fixtures for automated benchmark comparisons. These pages provide known content so that web scraping and extraction tests produce reproducible results regardless of changes to external websites.

## Adding Content

Add static HTML/CSS/JS files to any directory. After pushing to `main`, content is automatically published via GitHub Pages at:

```
https://activescott.github.io/public-static/<path-to-file>
```
