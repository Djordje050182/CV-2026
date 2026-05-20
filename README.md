# Djordje Gvozdenovic - CV

Personal CV site for Djordje Gvozdenovic. Enterprise Account Executive based in Sydney, currently at Salesforce selling Agentforce and Data Cloud.

Live at: _to be populated once GitHub Pages is enabled_

---

## What's in this repo

- `index.html` - the full CV site, single self-contained file (no build step, no dependencies, no external JS frameworks)

## How to host on GitHub Pages

1. Push this repo to GitHub as a **public** repo
2. Repo Settings → Pages → Source: **Deploy from a branch**
3. Branch: **main** (or `master`), folder: **/ (root)** → Save
4. Wait 1-2 minutes
5. Site goes live at one of these URLs depending on the repo name:
   - If repo is named `<username>.github.io` → live at `https://<username>.github.io/`
   - If repo is named anything else (e.g. `cv`) → live at `https://<username>.github.io/<repo-name>/`

The `.github.io` repo name gives the cleaner URL. Recommend that one.

## How to update

The whole site is one file: `index.html`. Edit it directly in GitHub's web UI or locally, then push. Changes go live within ~1 minute.

The main sections to edit are clearly marked in HTML comments:
- Hero (name, tagline, contact)
- Profile + stats grid
- Experience (each role is a `<article class="role">` block)
- Capabilities (4-block grid)
- Education and Beyond Work
- Ask the CV chat (the `qa` array in the `<script>` block at the bottom - each entry is a topic with keywords + answer)

## Features

- **Dark editorial design** - warm rust accent, Fraunces serif, grain texture, subtle glow
- **Fully responsive** - mobile-friendly down to ~320px wide
- **Print / PDF button** - top-right nav button triggers `window.print()`. Print stylesheet swaps the dark theme for a clean light-navy ATS-friendly two-page CV. Works in Chrome and Safari.
- **Ask the CV chat widget** - bottom-right floating button. Keyword-matched Q&A across 16 topics (AI experience, achievements, verticals, why hire, contact, Salesforce, GroupM, builder credibility, etc). Suggestion chips on first open. Honest disclaimer at the bottom that it's keyword Q&A, not a live LLM.
- **SEO optimised** - Open Graph tags, Schema.org JSON-LD Person markup, proper meta description, canonical URL
- **ATS-friendly** - real semantic HTML (proper `<article>`, `<section>`, headings hierarchy), no images of text, no icon fonts blocking parse

## Tech notes

- No frameworks, no build tools, no `node_modules`. Just HTML + CSS + a small bit of vanilla JS.
- Fonts: Fraunces (serif), Inter Tight (sans), JetBrains Mono (code accents) - all from Google Fonts via `<link>` in the head
- Layout: CSS flexbox throughout (with sensible fallbacks)
- Print: dedicated `@media print` stylesheet with light navy/blue palette for a professional printed copy

## Before going public

A few things worth double-checking before sharing the URL:

1. **Canonical URL** in the `<head>` currently points to `https://djordjegvozdenovic.github.io/`. If hosting at a different URL, update this.
2. **Open Graph tags** ditto - check the og:title and og:description match what you want shared on LinkedIn/Slack previews.
3. **Phone number** is currently visible in the header. Fine for a CV site shared with recruiters, but if you're going to put the URL on LinkedIn publicly, you may want to swap it for an email-only contact.
4. **Print test** - open in Chrome, hit the Print / PDF button, check the resulting PDF looks right on your machine before sharing the link with anyone.

## Custom domain (optional, later)

If you want `djordjegvozdenovic.com` or similar instead of `<username>.github.io`:

1. Buy the domain (~£10/year on Namecheap, Porkbun, etc)
2. In repo Settings → Pages → Custom domain, enter the domain
3. At the registrar, add a CNAME record pointing to `<username>.github.io`
4. GitHub Pages auto-issues an HTTPS cert via Let's Encrypt

Adds 10 mins setup, looks far more professional than a `.github.io` URL on a CV link.
