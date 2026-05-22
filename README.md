# Djordje Gvozdenovic - CV

Personal CV site for Djordje Gvozdenovic. Enterprise Account Executive based in Sydney, currently at Salesforce on Agentforce and Data Cloud.

Live at: https://djordje050182.github.io/

---

## What's in this repo

- `index.html` - the full CV site, single self-contained file (no build step, no dependencies, no external JS frameworks)

## How to host on GitHub Pages

1. Push this repo to GitHub as a **public** repo
2. Repo Settings → Pages → Source: **Deploy from a branch**
3. Branch: **main** (or `master`), folder: **/ (root)** → Save
4. Wait 1-2 minutes - live at `https://djordje050182.github.io/<repo-name>/` or `https://djordje050182.github.io/` if the repo is named `djordje050182.github.io`

## How to update

The whole site is one file: `index.html`. Edit it directly in GitHub's web UI or locally, then push. Changes go live within ~1 minute.

The main sections to edit are clearly marked:
- Hero (name, tagline, contact)
- 01 Profile + stats grid
- 02 AI Fluency & Hands-on Use
- 03 Experience (each role is an `<article class="role">` block)
- 04 Capabilities (4-block grid)
- 05 Education and Beyond Work
- Ask the CV chat (the `qa` array in the `<script>` block at the bottom)

## Features

- **Dark editorial design** - warm rust accent, Fraunces serif, grain texture, subtle glow
- **Fully responsive** - mobile-friendly down to ~320px wide
- **Print / PDF button** - top-right nav button triggers `window.print()`. Print stylesheet swaps the dark theme for a clean light-navy ATS-friendly two-page CV. Works in Chrome and Safari.
- **Ask the CV chat widget** - bottom-right floating button. Keyword-matched Q&A across 18 topics including AI experience, achievements, the Sellers to Builder Sellers training programme, the Pepperstone business value example, contact, etc.
- **External artifact links** - AI Fluency section links to:
  - Sellers to Builder Sellers training: https://djordje050182.github.io/AFD360-Team-Training/#hero
  - Pepperstone business value example: https://djordje050182.github.io/Pepperstone-Agentforce/
- **SEO optimised** - Open Graph tags, Schema.org JSON-LD Person markup, proper meta description, canonical URL
- **ATS-friendly** - real semantic HTML (proper `<article>`, `<section>`, headings hierarchy), no images of text

## Tech notes

- No frameworks, no build tools. Just HTML + CSS + a small bit of vanilla JS.
- Fonts: Fraunces (serif), Inter Tight (sans), JetBrains Mono (code accents) - all from Google Fonts via `<link>` in the head
- Layout: CSS flexbox throughout
- Print: dedicated `@media print` stylesheet with light navy/blue palette for a professional printed copy

## Custom domain (optional)

If you want `djordjegvozdenovic.com` or similar instead of `.github.io`:

1. Buy the domain (~£10/year on Namecheap, Porkbun, etc)
2. In repo Settings → Pages → Custom domain, enter the domain
3. At the registrar, add a CNAME record pointing to `djordje050182.github.io`
4. GitHub Pages auto-issues an HTTPS cert via Let's Encrypt
