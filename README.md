# kettlebellkon-manual

Static product manual site for KETTLEBELLKON, hosted on GitHub Pages.

This is **not** a marketing site. It is a minimal electronic instruction manual,
designed to be read on a phone after scanning the QR code printed on product
packaging. Japanese first, with short English labels.

## Status

All manual content is **provisional (準備中)**. Pages are placeholders and are
clearly marked as such. Final instructions and safety guidance have not been
written yet — do not add technical or safety claims until they are approved.

## URLs

- Public site: https://kettlebellkon.com/
- Rucking Plate Carrier manual: https://kettlebellkon.com/manual/rucking/
- Package QR target:
  `https://kettlebellkon.com/manual/rucking/?utm_source=package&utm_medium=qr`

## File structure

```
.
├── index.html                 # Manuals landing page (product list)
├── 404.html                   # Not-found page (root-absolute links; see note)
├── assets/
│   └── style.css              # Shared responsive styles
├── manual/
│   └── rucking/
│       ├── index.html         # Rucking Plate Carrier user guide (contents)
│       ├── setup.html         # プレートのセット・装着 / Setup & Fit
│       ├── usage.html         # 使い方 / How to Use
│       └── safety.html        # 安全上の注意 / Safety
├── CNAME                      # Custom domain: kettlebellkon.com
├── .nojekyll                  # Disable Jekyll processing on GitHub Pages
└── README.md
```

## Development

Plain HTML and CSS only — no frameworks, package manager, or build step. The
only external script is the Google tag (gtag.js) for GA4 (see Analytics).
Open `index.html` directly in a browser to preview.

- Pages use **relative links** so they work both on the custom domain and when
  opened locally.
- Exception: `404.html` uses root-absolute paths (`/`, `/assets/style.css`)
  because GitHub Pages serves it for missing URLs at any depth. It resolves
  correctly on `kettlebellkon.com`.
- Directory links (e.g. `manual/rucking/`) rely on the server serving
  `index.html`; when browsing local files, some browsers show a directory
  listing instead.

## Analytics

GA4 is installed with Measurement ID **`G-WEXM54D0QD`**. Every HTML page
includes the standard Google tag (gtag.js) snippet once, inside `<head>`.

Package QR visits are attributed via `utm_source=package&utm_medium=qr` on the
QR target URL (see URLs above).
