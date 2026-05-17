# Wichita Campus Capabilities

An interactive, single-file capabilities deck for **Envision's Wichita, Kansas campus** — U.S. manufacturing since 1933, built for federal scale.

## What it is

A self-contained static presentation (`index.html`) with no build step and no
runtime dependencies. All styles and scripts are inline; the only external
request is Google Fonts (loaded with `preconnect`).

- Keyboard navigation: `←` / `→` / `Space`, `1`–`9` jump to sections, `F` fullscreen, `Esc` to exit
- Touch swipe on mobile
- Section progress bar with hover tooltips
- SKU drawers and expandable capability cards

## Deploy on Vercel

This is a zero-config static deployment.

1. Import the repository into Vercel (no framework preset needed — it's static).
2. Leave build & output settings empty; Vercel serves `index.html` at the root.
3. Deploy.

[`vercel.json`](./vercel.json) configures security headers (HSTS, no-sniff,
frame options, referrer/permissions policy), `cleanUrls`, and a
revalidate-on-every-request cache policy so content updates go live immediately
on the next deploy.

### Local preview

Open `index.html` directly in a browser, or serve the folder:

```bash
npx serve .
```
