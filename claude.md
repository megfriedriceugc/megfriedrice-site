# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

Static single-page portfolio website for "Meg Fried Rice" — a UGC (user-generated content) creator specializing in travel and diving content. Deployed on Netlify.

## Architecture

- **Single-file site**: Everything lives in `index.html` — HTML, CSS (in `<style>`), and JavaScript (in `<script>`) are all inline. There is no build step, bundler, or framework.
- **Images**: Static assets in `images/` (hero.jpg, portraitImg.jpg, whaleImg.jpg, forestImg.jpg, campImg.jpg, suriImg.jpg, djiImg.jpg).
- **Hosting**: Netlify with config in `netlify.toml` (CSP headers for Vimeo/TikTok embeds). Note: `netlify.toml` is in RTF format.
- **Fonts**: Google Fonts loaded externally — Cormorant Garamond (headings/accents) and Syne (body text).
- **Contact form**: Uses Netlify Forms (`data-netlify="true"`) with honeypot spam protection.

## Key Features

- CSS scroll-reveal animations (`.reveal`, `.reveal-left`, `.reveal-right`) triggered by IntersectionObserver
- Canvas-based floating particle effect (`#particles`)
- Video lightbox that embeds Vimeo iframes (work items with `data-embed` attributes)
- Mobile-responsive with hamburger nav at 640px breakpoint
- CSS custom properties for theming defined in `:root` (ocean/deep-sea color palette)

## Development

No build commands. Open `index.html` in a browser or use any local server:

```
python3 -m http.server 8000
# or
npx serve .
```

## Deployment

Push to the connected Netlify site. No build step configured — Netlify serves static files directly.
