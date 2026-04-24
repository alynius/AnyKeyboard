# AnyKeyboard.io ⌨️

![anykeyboard](https://github.com/user-attachments/assets/154be5bd-df84-43e2-af4b-4f8fe9853918)

A browser-based virtual keyboard and typing practice platform that lets you type in **100+ languages** instantly — without installing anything.

**Features:**
- 🌍 100+ keyboard layouts across Latin, Cyrillic, Arabic, CJK, Indic, and more
- ⚡ Multilingual typing speed test with real-time WPM and accuracy tracking
- 🔤 Phonetic typing for major languages (type transliterated text on your QWERTY keyboard)
- 📝 Name transliteration across 30+ scripts
- 🔒 Privacy-first — all typing happens locally in your browser
- ♿ Accessible — WCAG-compliant with keyboard navigation, screen reader support, and reduced-motion respect

👉 **Live app:** [anykeyboard.io](https://anykeyboard.io)

---

## Recent: Full Product Audit (April 2026)

A comprehensive deep-dive audit was completed across **5 dimensions**, resulting in 40+ fixes shipped in a single session:

| Dimension | Before | After | Key Improvements |
|-----------|--------|-------|------------------|
| **Security** | 7/10 | 9/10 | 0 vulnerabilities, tightened CSP, SRI on analytics, API auth |
| **Performance** | 4/10 | 7/10 | ~600 KB less per page, browser caching, ISR, font optimization |
| **Code Quality** | 4/10 | 8/10 | -15K lines removed, consolidated locale variants, modular JS |
| **UI/UX** | 5/10 | 7/10 | RTL support for 10 languages, theme detection, loading skeletons |
| **Accessibility** | 3/10 | 7/10 | Skip navigation, ARIA labels, focus management, reduced motion |

**Overall: 4.9/10 → 8/10**

### What changed

**Performance**
- Removed forced re-download of 345 KB layout bundle on every navigation
- Dynamic font loading — each keyboard page only loads fonts for its script (saves 200-400 KB)
- CSS minification added to build pipeline
- Cache-Control headers for all static assets
- Incremental Static Regeneration (ISR) on 7 page types
- Typing sentences split from 1 monolith (49 KB) into 78 per-language files

**Security**
- Patched all 6 npm dependency vulnerabilities (0 remaining)
- Added Subresource Integrity (SRI) hash on third-party analytics
- Added authentication + rate limiting to IndexNow API endpoint
- Added `.env` files to `.gitignore`
- Restored and documented CSP policy requirements

**Code Quality**
- Consolidated 14 locale-specific hub page variants into 1 parameterized component (-10,000 lines)
- Consolidated 15 locale-specific footer variants into 1 component (-1,650 lines)
- Converted 32 copy-paste utility pages into 1 dynamic route (-1,100 lines)
- Refactored keyboard page to single source of truth (792 → 219 lines)
- Modularized 2,500-line vanilla JS runtime into 5 focused ES modules
- Centralized `SITE_URL` from 18+ independent definitions to 1
- Extracted shared error boundary component
- Deleted orphaned files and analysis artifacts
- Added ESLint (next/core-web-vitals) + Prettier

**UI/UX**
- Defined 9 missing CSS custom properties (light + dark themes)
- Added 40 RTL CSS overrides for proper Arabic/Hebrew/Urdu/Persian layout mirroring
- Added OS `prefers-color-scheme` detection (respects system theme preference)
- Added keyboard loading skeleton and pre-populated layout selector
- Fixed RTL `dir` attribute detection for 10 RTL languages
- Added global error boundary for crash protection

**Accessibility**
- Added skip-to-content link on every page (WCAG 2.4.1)
- Added `aria-label` to all 50+ virtual keyboard keys including special keys (WCAG 4.1.2)
- Added global `prefers-reduced-motion` rule disabling all animations (WCAG 2.3.3)
- Fixed textarea `lang`/`dir` — now dynamic per keyboard instead of hardcoded Arabic
- Audited 23 `outline: none` instances, fixed 9 missing focus indicators (WCAG 2.4.7)
- Added mobile menu focus trap with Escape key handler (WCAG 2.4.3)
- Fixed `role="menu"` misuse and `aria-pressed` → `aria-selected` tab pattern
- Added `lang` attributes to foreign-language hero text (WCAG 3.1.2)
- Added `aria-label` to all search inputs and `<main>` landmarks to 17 pages

---

## Tech Stack

- **Framework:** Next.js 15 (Pages Router)
- **Deployment:** Vercel
- **Rendering:** 100% Static Generation (SSG) with ISR
- **Styling:** CSS custom properties with dark/light theme support
- **Analytics:** Umami (self-hosted, privacy-first)
- **SEO:** Custom pipeline with JSON-LD, hreflang, sitemap generation, IndexNow

---

## Contents

- [Overview](overview.md)
- [How It Works](how-it-works.md)
- [Speed Writing Utility](speed-writing.md)
- [Phonetic Typing](phonetic-typing.md)
- [Supported Languages](supported-languages.md)
- [Use Cases](use-cases.md)
- [Privacy & Security](privacy-security.md)
- [SEO & Language Pages](seo-language-pages.md)
- [FAQ](faq.md)
- [Roadmap](roadmap.md)
- [Links](links.md)
