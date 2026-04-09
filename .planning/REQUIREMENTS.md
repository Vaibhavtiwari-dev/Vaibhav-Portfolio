# Requirements — Portfolio Codebase Cleanup

## Milestone: v1.0 — Dead Code & Contradiction Removal

### Must-Haves

| ID | Requirement | Acceptance Criteria |
|----|-------------|---------------------|
| R1 | Delete all legacy Deep Space pages | `about.html`, `projects.html`, `contact.html` removed from repo |
| R2 | Delete dead CSS | `style.css` (1,547 lines) removed — not referenced by any remaining page |
| R3 | Delete dead JS | `main.js` (542 lines) removed — not referenced by any remaining page |
| R4 | Remove stale service worker | `sw.js` deleted; `index.html` includes unregistration script for returning visitors |
| R5 | Fix 404 page | `404.html` rewritten with editorial theme (inline styles, matches `index.html` aesthetic) |
| R6 | Fix sitemap | `sitemap.xml` uses correct Firebase domain; only lists `index.html` and `resume.html` |
| R7 | Add Firebase redirects | `firebase.json` redirects `/about.html`, `/projects.html`, `/contact.html` → `/` |
| R8 | Optimize favicon | `favicon.png` compressed to <10 KB (currently 573 KB) |

### Should-Haves

| ID | Requirement | Acceptance Criteria |
|----|-------------|---------------------|
| S1 | Update `robots.txt` | Points to correct sitemap URL if needed |
| S2 | Clean `README.md` | Remove references to deleted pages/old architecture |

### Won't-Haves (This Milestone)

- New page designs or content
- Custom domain setup
- Analytics integration
- CI/CD pipeline

---
*Last updated: 2026-04-09*
