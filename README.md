# cobbstl.com

Static rebuild of the Cobb Property Management site — plain HTML, CSS, and images.
No build step and no framework; the only script is the Vercel Analytics tag.

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
- Vercel Analytics is enabled via `<script defer src="/_vercel/insights/script.js">` on
  every page. The path is served by Vercel itself, so it only reports when the
  site is deployed there; on any other host it 404s harmlessly and nothing else
  on the page is affected.

Everything else — copy, layout, typography, favicon, images, footer — matches the
original.

## Local preview

Open `index.html` directly, or serve the directory with any static file server.

## Deploying

These are plain files; drop them on any static host. The repo is also ready for
GitHub Pages (serve from the root of the default branch).
