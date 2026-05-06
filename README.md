# AcaNova-X

Modern academic homepage template with a two-column landing page, JSON-driven content, selected publication cards, and an expanded publications page with optional demo preview support.

The original `1.0.0` template introduction remains valid for users who prefer the lighter initial layout and simpler presentation. Version `1.1.0` keeps that foundation, while extending the template with stronger publication showcase and documentation support.

## Version Preview

### Version 1.1.0

<p align="center">
  <img src="docs/version_1.1.0.gif" alt="AcaNova-X v1.1.0 Preview" width="760">
</p>

Latest version preview with selected publications, expanded publication cards, and updated documentation.

### Version 1.0.0

<p align="center">
  <img src="docs/version_1.0.0.gif" alt="AcaNova-X v1.0.0 Preview" width="760">
</p>

Original template preview retained for reference, so users can compare the earlier default presentation with the newer release.

## Latest Version

Current release: `version 1.1.0`

## Features

- Clean homepage layout with sticky profile card and modular sections
- `news.json`, `honors.json`, and `publications.json` as the main editable data sources
- Selected publications on the homepage controlled by `showOnHomepage` and `featuredOrder`
- All publications page with built-in filters for `all`, `first-author`, and `accepted`
- Default expanded publication cards with thumbnail preview
- Automatic `demo.gif` loading when it exists beside a paper thumbnail

## What's New in 1.1.0

- Adds homepage selected publications controlled by `showOnHomepage` and `featuredOrder`
- Upgrades the publications page to default expanded cards instead of the previous compact layout
- Adds built-in publication filters for all papers, first-author papers, and accepted papers
- Adds automatic `demo.gif` preview loading with fallback to the static thumbnail
- Keeps PDF, Code, and Project Page buttons visible in the template, even when placeholder links are still `"#"`
- Adjusts the default publication thumbnail box to a flatter horizontal preview ratio
- Updates the README preview assets from the old single `example.gif` naming to versioned files

## 1.0.0 Baseline

The original `1.0.0` version still represents the base spirit of AcaNova-X:

- A clean and lightweight academic homepage template
- JSON-driven content editing for news, honors, and publications
- Easy deployment for personal academic websites
- A simpler publication presentation style for users who prefer a minimal starting point

## Version History

### version 1.1.0

- Syncs the template with the latest website behavior and presentation style
- Introduces demo preview support for publication cards
- Introduces selected publications on the homepage
- Improves the all-publications page with filtering and expanded presentation
- Refines template defaults and documentation for easier reuse

### version 1.0.0

- Original base template release
- Includes the initial homepage, data files, and documentation assets

## Quick Start

1. Replace `assets/profile.jpg` with your own portrait.
2. Edit the placeholder text in `index.html`.
3. Update `data/news.json`, `data/honors.json`, and `data/publications.json`.
4. Put publication images under `assets/publications/<paper-folder>/`.
5. Open `index.html` locally or deploy the folder to GitHub Pages.

## Publication Data

Each publication entry supports the following commonly used fields:

```json
{
  "title": "Paper Title",
  "displayTitle": "Optional alternate title shown on the homepage",
  "authors": "<strong>Your Name</strong>, Coauthor A, Coauthor B",
  "type": "accepted",
  "isFirstAuthor": true,
  "showOnHomepage": true,
  "featuredOrder": 1,
  "venue": "CVPR 2025",
  "year": "2025",
  "highlight": "(Oral)",
  "thumbnail": "assets/publications/paper-name/paper-thumb.png",
  "tags": [
    { "text": "Paper", "link": "https://arxiv.org/abs/xxxx.xxxxx" },
    { "text": "Code", "link": "https://github.com/your-repo" }
  ]
}
```

## Demo Preview

To enable animated preview for a paper card, place a `demo.gif` in the same folder as the thumbnail:

```text
assets/publications/paper-name/
  demo.gif
  paper-thumb.png
```

The template tries to load `demo.gif` first and falls back to the static thumbnail automatically.

## Pages

- `index.html`: homepage
- `pages/all-publications.html`: full publications list with filters
- `pages/all-news.html`: full news list
- `pages/all-honors.html`: full honors list

## Notes

- The template uses Tailwind CDN plus a small custom stylesheet in `styles.css`.
- Relative asset paths in JSON are handled automatically for subpages under `pages/`.
- README previews now use `docs/version_1.0.0.gif` and `docs/version_1.1.0.gif`.
- The darker look in a GIF preview usually comes from the GIF export itself rather than GitHub Markdown rendering. The README now reduces the preview size to make the page easier to scan, but if needed, the source GIF can be re-exported later with a brighter palette.
