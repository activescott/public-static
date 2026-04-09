# Test Fixtures

Static HTML pages used as stable, version-controlled test fixtures for automated benchmark comparisons.

## Purpose

These pages provide known, unchanging content so that web scraping and content extraction benchmarks produce reproducible results. Instead of depending on external websites that can change, trigger bot detection, or go down, benchmarks fetch these fixture pages.

## Pages

| File | Description |
|------|-------------|
| `links-page.html` | A page with multiple hyperlinks in the main content. Tests whether link URLs are preserved during content extraction. |
| `listing-page.html` | A product listing page with titles, prices, and sidebar categories. Tests extraction of listing/catalog content. |
| `product-page.html` | A product detail page with title, price, feature bullets, and specs table. Tests extraction of structured product data. |

## Usage

These fixtures are served via GitHub Pages at:
```
https://activescott.github.io/public-static/test-fixtures/<filename>.html
```

They are referenced by benchmark tests in the private `activescott/tinkerbell` repo.

## Editing

When modifying a fixture page, update the corresponding benchmark scorer expectations in the consuming repo to match the new content.
