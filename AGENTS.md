# Repository instructions

## Project overview

This is a static, single-page personal website for Juan José Amor (DrAmor.NET), based on the HTML5 UP “Big Picture” template. The repository is primarily served as-is; there is no package manifest or build configuration.

## Key files

- `index.html`: main page structure, metadata, section content, footer links, and Google Analytics setup.
- `assets/sass/main.scss`: Sass entry point. It imports variables, vendor helpers, base styles, components, layouts, and section-specific backgrounds.
- `assets/css/main.css`: compiled CSS loaded by `index.html`.
- `assets/css/noscript.css`: noscript-specific overrides.
- `assets/js/main.js`: page initialization, breakpoint handling, scroll transitions, and Poptrox gallery setup.
- `assets/js/`: vendored jQuery and HTML5 UP support plugins.
- `images/`: site backgrounds and optional full-size/thumbnail gallery assets.
- `0x7CC1E39B.txt`: published PGP public key. Changes must remain synchronized with the PGP fingerprint/key link in `index.html`.
- `robots.txt`, `sitemap.xml`: public search indexing metadata.

## Working conventions

- Prefer small, direct edits. Preserve the existing HTML5 UP/Big Picture structure and class names.
- Keep `index.html` self-contained except for existing local assets and vendored scripts.
- Edit `assets/sass/` as the source of truth for style changes, then update `assets/css/main.css` consistently. Do not overwrite compiled CSS and Sass sources with unrelated formatting changes.
- Preserve relative asset paths and check paths against the Sass and CSS locations:
  - CSS background paths in `assets/sass/main.scss` resolve from `assets/css/main.css`.
  - Site backgrounds live under `images/intro.jpg`, `images/one.jpg`, and `images/two.jpg`.
- Do not introduce a framework, package manager, or build step unless the task explicitly requires it.
- Preserve accessibility attributes, semantic section structure, navigation anchors, and descriptive labels in social icons.
- Keep external links and analytics configuration unchanged unless the task specifically requests an update.
- Treat PGP key, license, credits, and attribution text as sensitive content. Verify exact values before modifying them.

## Local preview

No dependencies or environment variables are required.

```bash
python3 -m http.server 8080
```

Open `http://localhost:8080` and verify the page on both desktop and small-screen widths.

For CSS source edits, compile the Sass entry point with a local Sass compiler compatible with the repository's source, for example:

```bash
sass assets/sass/main.scss assets/css/main.css
```

## Validation

Before finishing a change:

1. Start a local static server and load `index.html`.
2. Check all modified navigation anchors, background paths, scripts, stylesheets, icons, and images.
3. Verify desktop and mobile layouts, including the header, all fullscreen sections, and footer.
4. If JavaScript changed, confirm browser-console errors are absent and scroll/touch/breakpoint behavior still works.
5. If Sass or CSS changed, confirm both source and compiled output remain consistent.
6. If PGP content changed, verify the public-key block and displayed fingerprint match exactly.
7. Review `robots.txt`, `sitemap.xml`, and SEO metadata only when relevant to the change.

## Change discipline

- Do not commit generated caches or local server files.
- Keep vendored JavaScript and CSS changes isolated and minimal; avoid reformatting entire third-party files.
- Preserve the existing template license and attribution comments.
