# ETS website

The Easy Tech Solutions company site — `https://etsproducts.in`.

Plain static HTML/CSS/JS. No build step, no dependencies.

## Pages

| File | URL |
|---|---|
| `index.html` | `/` |
| `products.html` | `/products.html` |
| `about.html` | `/about.html` |
| `privacy.html` | `/privacy.html` |
| `terms.html` | `/terms.html` |
| `404.html` | served by GitHub Pages on any unknown path |

Shared: `styles.css`, `main.js`, `favicon.svg` (the ETS "Half-resolved" mark).
Also `robots.txt`, `sitemap.xml`, `CNAME` (custom domain), `.nojekyll` (skip
Jekyll processing).

Logos: `favicon.svg` is used in the header and the browser tab; `eas-mark.svg`
and `ecs-mark.svg` sit next to each product on the home and products pages.
All logo sources and variants live in `../brand/logo/`.

## Edit it

Open any `.html` file and edit the markup directly. The header `<nav>` and the
`<footer>` are copied into each page — if you change one, change all of them
(6 files, `404.html` included).

Design tokens (colors, spacing) are CSS variables at the top of `styles.css`
under `:root` and the `prefers-color-scheme: dark` block.

## Preview locally

```bash
python3 -m http.server 8000
# then open http://localhost:8000
```

Or just open `index.html` in a browser (relative links work either way).

## Deploy

Push to `main` on `github.com/rahulag1997/ets-website`; GitHub Pages publishes
the root of the branch. Domain, DNS and HTTPS setup are tracked in
`../admin-actions.md`.
