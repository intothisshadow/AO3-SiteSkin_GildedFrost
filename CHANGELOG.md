# Gilded Frost — Changelog

This changelog documents significant changes only: new features, architectural decisions, notable bug fixes and new companion skins. Individual CSS tweaks are not logged.

---

## V1.0.0 — Initial release
**Released:** 2026-10-12

First public release of Gilded Frost, together with its mobile add-on.

### Theme

- A dark, wintry palette of near-black stone surfaces, icy blue accents and antique gold, defined as CSS variables in one `:root` block. Muted text colours are tuned to meet WCAG AA contrast on every surface.
- A signature ice-to-gold gradient on the header, work titles, dashboard bars and fandom tags. News pages use a frost/violet/gold variant.
- Cinzel for headings and UI, EB Garamond for reading text, with Georgia/serif fallbacks.

### Type scale

- One font-size scale as CSS variables (`--fs-xs`, `--fs-sm`, `--fs-md`, `--fs-base`, `--fs-h1` to `--fs-h3`), used by every font size in both stylesheets.
  - The mobile add-on scales the whole set down together.
  - It keeps body and fic text at a single comfortable 18px on phones.

### Blurbs and work pages

- Colour-coded tag pills:
  - warnings red
  - relationships gold
  - characters icy blue
  - freeforms slate
  - fandoms the ice-to-gold gradient
- Pills wrap as whole units and never split across lines.
- Gradient work titles with gold italic authors.
- Long titles and fandom lists wrap underneath the rating and warning icons.
- A kudos card with a recoloured kudos icon; long kudos lists wrap under the icon.
- A recoloured statistics chart. It matches on the chart's fill colours, so it falls back to the stock look if Google Charts changes them.

### Companion files

- **`style_mobile.css`**: a mobile add-on, installed as a child skin. It covers:
  - the Sort and Filter drawer, which opens on the right
  - a two-by-two footer
  - the dashboard and profile header layout
  - the comment form
  - fic-text lists
  - Fandoms page buttons
  - tighter spacing throughout

  It's written as a flat set of rules, because AO3 flattens inner `@media` blocks on save.
- **`stylus_fonts.css`**: loads Cinzel and EB Garamond through the Stylus browser extension, since AO3 skins can't load external fonts.
- **Icon replacements**: ZerafinaCSS "Replace the AO3 Icons 2.0", recoloured to the palette and built into the desktop stylesheet as Section 34.

### Development history

The skin began life under the working name **House Stark** and was renamed to Gilded Frost before release.
