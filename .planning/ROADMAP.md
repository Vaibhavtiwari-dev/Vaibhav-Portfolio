# Roadmap — Portfolio Codebase Cleanup

## Milestone: v1.0 — Dead Code & Contradiction Removal

### Phase 1: Purge Legacy Files
**Goal:** Remove all orphaned Deep Space pages, dead CSS/JS, and the stale service worker.

| Plan | Description | Requirements | Files Touched |
|------|-------------|--------------|---------------|
| 1.1 | Delete legacy HTML pages | R1 | `about.html`, `projects.html`, `contact.html` |
| 1.2 | Delete dead CSS and JS | R2, R3 | `style.css`, `main.js` |
| 1.3 | Delete service worker + add unregistration | R4 | `sw.js` (delete), `index.html` (add unregister script) |

**Exit criteria:** Only production files remain (`index.html`, `resume.html`, `resume.css`, `404.html`, `profile.jpg`, `favicon.*`, `firebase.json`, `sitemap.xml`, `robots.txt`).

---

### Phase 2: Fix Remaining Files
**Goal:** Update all surviving files to be correct and consistent.

| Plan | Description | Requirements | Files Touched |
|------|-------------|--------------|---------------|
| 2.1 | Redesign 404 page | R5 | `404.html` (rewrite with editorial theme) |
| 2.2 | Fix sitemap + robots.txt | R6, S1 | `sitemap.xml`, `robots.txt` |
| 2.3 | Add Firebase redirects + 404 config | R7 | `firebase.json` |

**Exit criteria:** `404.html` matches editorial design; sitemap has correct domain and only lists live pages; Firebase redirects old URLs to `/`.

---

### Phase 3: Optimize & Finalize
**Goal:** Compress assets and clean up documentation.

| Plan | Description | Requirements | Files Touched |
|------|-------------|--------------|---------------|
| 3.1 | Optimize favicon | R8 | `favicon.png` (compress to <10 KB) |
| 3.2 | Clean README | S2 | `README.md` |

**Exit criteria:** Favicon <10 KB; README reflects current architecture; repo is deploy-ready.

---

## Phase Summary

| Phase | Plans | Requirements Covered | Risk |
|-------|-------|---------------------|------|
| 1 — Purge Legacy Files | 3 | R1, R2, R3, R4 | Low — pure deletion |
| 2 — Fix Remaining Files | 3 | R5, R6, R7, S1 | Low — small edits |
| 3 — Optimize & Finalize | 2 | R8, S2 | Low — asset compression |

**Total: 3 phases, 8 plans**

---
*Last updated: 2026-04-09*
