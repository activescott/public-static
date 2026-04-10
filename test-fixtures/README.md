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
| `image-quote-wrapper.html` | An HTML page wrapping `images/quote.png` (a famous quote rendered as an image). Tests whether tools can extract text from images on a page. |
| `image-infographic-wrapper.html` | An HTML page wrapping `images/infographic.png` (a bar chart with known data). Tests numeric extraction from visual content. |
| `cln-snapshot.html` | A locally-saved snapshot of a real cln.sh screenshot hosting page (with the underlying screenshot also saved locally). Tests against a realistic third-party DOM where the primary content is a single image. |

## Image Fixtures

Binary image files used by the wrapper pages above (and also fetched directly as image URLs):

| File | Description |
|------|-------------|
| `images/quote.png` | 1600x1000px PNG containing the Steve Jobs quote "The only way to do great work is to love what you do." rendered as text. Source for OCR/vision benchmarks. |
| `images/infographic.png` | 1600x1000px PNG containing a bar chart with three data points: Apples 42, Oranges 17, Bananas 29. Source for numeric extraction from visual content. |
| `screenshots/cln-b7cHjbPmP8gHkPzlDcDq.jpeg` | A real screenshot from CleanShot containing a wolf photo and a Schopenhauer quote. Used by `cln-snapshot.html`. |

The PNG fixtures are generated from HTML templates by `scripts/generate-image-fixtures.ts` in the consuming repo. To regenerate, run that script.

## Usage

These fixtures are served via GitHub Pages at:
```
https://activescott.github.io/public-static/test-fixtures/<filename>.html
```

They are referenced by benchmark tests in the private `activescott/tinkerbell` repo.

## Editing

When modifying a fixture page, update the corresponding benchmark scorer expectations in the consuming repo to match the new content.
