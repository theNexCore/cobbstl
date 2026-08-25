# cobbstl.com

Static rebuild of the Cobb Property Management site — plain HTML, CSS, and images.
No build step, no JavaScript, no external requests.

## Structure

```
index.html            Home
privacy-policy.html   Privacy Policy
terms-of-use.html     Terms Of Use
favicon.ico
css/style.css         Site styles
css/fonts.css         @font-face declarations
fonts/                29 self-hosted .woff2 files
images/               Logo, hero photo, maintenance button
```

## Changes from the previous Weebly site

- The phone number is no longer baked into the hero banner image. It is now a
  sticky navigation CTA (`tel:` link) pinned to the top of every page.
- Fonts are self-hosted instead of loaded from the Weebly CDN.
- Cloudflare-obfuscated email addresses were decoded into working `mailto:` links.

Everything else — copy, layout, typography, favicon, images, footer — matches the
original.

## Local preview

Open `index.html` directly, or serve the directory with any static file server.

## Deploying

These are plain files; drop them on any static host. The repo is also ready for
GitHub Pages (serve from the root of the default branch).
