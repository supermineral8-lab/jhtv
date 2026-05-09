# Changelog

## v3.1.3 - clickable header brand

- Fix: made the header brand clickable on the English and Chinese home pages.
- English header links to `index.html`; Chinese header links to `index-zh.html`.
- No copy, layout, images, language selector or navigation labels changed.

## v3.1.2 - remove visible skip link

- Fix: removed the visible skip-link anchors from the site pages so “Skip to profile” no longer appears at the top.
- No layout, copy, imagery, navigation or language-selector behavior changed.

## v3.1.1 - local-safe language selector

- Fix: changed visible language selector links from root-absolute paths to relative paths, so local testing via `file://` no longer resolves to `file:///index-zh.html`.
- Fix: changed 404 navigation links to relative paths for the same reason.
- Fix: changed the physical `/zh/index.html` fallback redirect to `../index-zh.html`, preserving compatibility when opened locally and on the server.
- Kept canonical, hreflang, sitemap and server redirects as absolute production URLs where appropriate.

## v3.1.1 — Chinese language route hardening

- Made `/index-zh.html` the primary Chinese page.
- Changed the English language selector from `/zh/index.html` to `/index-zh.html`.
- Redirected `/zh` and `/zh/index.html` to `/index-zh.html` in `.htaccess`.
- Added a physical `/zh/index.html` fallback redirect page for hosts that ignore `.htaccess`.
- Updated canonical, hreflang and sitemap entries to the flat Chinese route.
- Kept `Options -Indexes` in root and `/zh/` as an additional safety net.


## v3.0.0 - 2026-05-09

- Fix: Chinese language switch now points to `/zh/index.html` instead of `/zh/` to avoid directory listings on servers where directory indexes are exposed.
- Fix: added rewrite rule from `/zh` and `/zh/` to `/zh/index.html`.
- Fix: added `/zh/.htaccess` with `Options -Indexes` and `DirectoryIndex index.html` as an extra guard.
- Fix: updated Chinese canonical, hreflang and sitemap URL to `https://javierhidalgo.tv/zh/index.html`.
- Fix: 404 page internal links now use absolute paths.
- Verification: internal site links and asset references checked after the changes.

## v2.0.0 - 2026-05-09

- Fix: removed repeated eyebrow labels inside cards.
- Improvement: grouped repeated headings outside the card grid.
- Applied to English and Chinese versions.

## v1.0.0 - 2026-05-09

- Initial cleanup of the site package.
- Optimized major images and converted heavy assets to WebP/AVIF where useful.
- Added canonical, hreflang, Open Graph and Twitter metadata.
- Added single-page redirects for legacy URLs.
- Improved accessibility, lazy loading, contact links and security headers.
