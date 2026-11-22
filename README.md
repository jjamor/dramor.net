# DrAmor.NET

DrAmor.NET is Juan José Amor’s responsive personal website, presenting his professional background, current work, PGP key, credits, and social links.

The site is based on the **Big Picture** template by [HTML5 UP](https://html5up.net) and is released under the CCA 3.0 license.

## Technology

- HTML
- SCSS/Sass and compiled CSS
- JavaScript, jQuery, and jQuery plugins
- Static assets: images, favicons, and webfonts

This is a static website. It does not require Node.js, a package manager, or an application server.

## Local preview

From the repository root, start a local HTTP server:

```bash
python3 -m http.server 8080
```

Then visit [http://localhost:8080](http://localhost:8080).

You can stop the server with `Ctrl+C`.

## Project structure

- `index.html` — page content, metadata, navigation, scripts, and analytics configuration
- `assets/sass/` — editable Sass sources
- `assets/css/` — compiled CSS and third-party stylesheets
- `assets/js/` — page behavior and vendored JavaScript libraries
- `assets/favicons/` — browser and mobile icons
- `assets/webfonts/` — icon fonts
- `images/` — section backgrounds and gallery images
- `0x7CC1E39B.txt` — published PGP public key
- `robots.txt` — crawler directives
- `sitemap.xml` — search engine sitemap

## Editing

### Page content

Edit `index.html` to change the introduction, About Me text, current role, credits, PGP details, or social links.

The page uses section anchors such as `#intro`, `#one`, `#two`, and `#credits`. When changing a section ID or navigation link, update both references.

### Styles

Edit the relevant Sass partial under `assets/sass/` for source-level style changes. `assets/sass/main.scss` is the main entry point and imports the base, component, and layout partials.

If Sass is changed, compile it so `assets/css/main.css` stays synchronized:

```bash
sass assets/sass/main.scss assets/css/main.css
```

If a Sass compiler is unavailable, changes to `assets/css/main.css` can be made directly, but the corresponding source files should be kept consistent when practical.

### Images

Update section backgrounds by replacing `images/intro.jpg`, `images/one.jpg`, or `images/two.jpg`, or change the matching URL in `assets/sass/main.scss`.

Use optimized images and retain meaningful filenames. Preserve image licenses and attribution information.

### PGP key

The PGP fingerprint and download link appear in `index.html`, while `0x7CC1E39B.txt` contains the public-key block. Verify both match exactly before publishing a key update.

## Validation

Before publishing a change:

1. Start the local server.
2. Open the site in a desktop browser and in a narrow mobile viewport.
3. Test every navigation link and footer/social link.
4. Confirm all section backgrounds, stylesheets, scripts, and icons load without browser-console errors.
5. Verify that all text and external links remain accurate.
6. For PGP changes, validate the key and fingerprint independently.

## Deployment

The repository can be deployed by publishing the repository root on any static web host. No build output directory or server-side runtime is required.

Because the site is hosted through GitHub Pages, changes pushed to the configured deployment branch should become available according to the repository's Pages settings.

## Attribution

- Original template: [Big Picture](https://html5up.net/big-picture) by HTML5 UP
- Icons: Font Awesome
- JavaScript components: jQuery, Poptrox, Scrollex, Breakpoints, and HTML5 UP utilities
- Photos and credits: listed in the Credits section of `index.html`
