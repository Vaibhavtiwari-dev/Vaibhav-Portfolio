# Portfolio Codebase Cleanup

## What This Is

A cleanup milestone for Vaibhav's personal portfolio site. The portfolio was redesigned from a multi-page "Deep Space" dark theme (canvas starfield, neon cyan, planet animations) to a modern **editorial single-page** design (light theme, serif typography, inline styles). The new `index.html` and `resume.html` are the production pages. However, the legacy architecture was never removed — 4 orphaned pages, ~2,100 lines of dead CSS/JS, a stale service worker, and broken SEO remain deployed.

## Core Value

**Remove every file and line that contradicts the current professional brand.** A recruiter who finds an old URL should land on the new design, not a stale page claiming "Freelance Full-Stack Developer" or listing vaporware projects.

## Context

- **Domain:** Personal portfolio / resume site
- **Stack:** Static HTML + CSS + JS, hosted on Firebase Hosting
- **Live URLs:** `vaibhav-portfolio-930c6.web.app` / `.firebaseapp.com`
- **Production pages:** `index.html` (editorial SPA), `resume.html` (print-ready resume)
- **Support files:** `resume.css`, `favicon.png`, `favicon.svg`, `profile.jpg`, `robots.txt`, `sitemap.xml`, `firebase.json`, `404.html`

## Requirements

### Validated

- ✓ Editorial single-page `index.html` — existing
- ✓ Print-ready `resume.html` with `resume.css` — existing
- ✓ Firebase Hosting deployment — existing

### Active

- [ ] Remove all legacy Deep Space pages (`about.html`, `projects.html`, `contact.html`)
- [ ] Remove dead CSS (`style.css` — 1,547 lines, only referenced by legacy pages)
- [ ] Remove dead JS (`main.js` — 542 lines, only referenced by legacy pages)
- [ ] Remove stale service worker (`sw.js`) and unregister it for returning visitors
- [ ] Fix contradictions (Nexus Arena vaporware, wrong Mind-Sync stack labels, freelance claim)
- [ ] Redesign `404.html` to match editorial theme
- [ ] Fix `sitemap.xml` domain (`VaibhavFolio.com` → actual Firebase domain)
- [ ] Add Firebase redirect rules (old page URLs → `index.html`)
- [ ] Optimize `favicon.png` (573 KB → <10 KB)

### Out of Scope

- New features or content additions — cleanup only
- Domain purchase or custom domain setup
- Analytics or tracking integration
- Redesign of `index.html` or `resume.html` — already done

## Key Decisions

| Decision | Rationale | Outcome |
|----------|-----------|---------|
| Delete legacy pages, not update them | Content is duplicated in `index.html`. Updating creates maintenance burden. | Pending |
| Redirect old URLs via Firebase rules | Preserves bookmarks, prevents 404s for returning visitors | Pending |
| Unregister service worker in `index.html` | `sw.js` actively caches stale pages. Must clear for returning visitors. | Pending |

## Evolution

This document evolves at phase transitions and milestone boundaries.

---
*Last updated: 2026-04-09 after initialization*
