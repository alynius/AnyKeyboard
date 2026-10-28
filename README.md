# AnyKeyboard.io ⌨️

![anykeyboard](https://github.com/user-attachments/assets/154be5bd-df84-43e2-af4b-4f8fe9853918)

A browser-based virtual keyboard and typing practice platform that lets you type in **100+ languages** instantly — without installing anything.

**Features:**
- 🌍 100+ keyboard layouts across Latin, Cyrillic, Arabic, CJK, Indic, and more
- ⚡ Multilingual typing speed test with real-time WPM and accuracy tracking
- 🔤 Phonetic typing for Arabic, Russian, Hindi, Greek, Hebrew and Ukrainian (type Latin letters, get the script)
- 📝 Your name in 30+ scripts, plus sign-language fingerspelling charts
- 🔒 Privacy-first — all typing happens locally in your browser
- ♿ Accessible — keyboard navigation, every key named for screen readers, and reduced-motion support

👉 **Live app:** [anykeyboard.io](https://anykeyboard.io)

---

## What's new (October 2026)

- **"How to type it" help** on the Tamil and Arabic keyboards: the keys for every Tamil vowel sign (கி, கு, கொ …), the pulli and ஸ்ரீ, and for Arabic short vowels, tanween, shadda and the small alif. The keys are read from each layout, and a browser test types every row.
- **Phones:** tapping the on-screen keys no longer opens the phone's own keyboard over the board; tap the text box when you want it.
- **Numbers:** Western digits 0–9 on AltGr for the Arabic, Kurdish Sorani and Malay (Jawi) boards, where the standard layouts put them.
- **Names in more scripts:** Baybayin with sound-based respelling, a hieroglyph cartouche maker, Tifinagh (and an IRCAM Tifinagh keyboard), Hebrew gematria values, and BSL/Auslan/NZSL fingerspelling with printable strips.
- **Names by sound, not by letter:** name tools work from pronunciation, backed by a dictionary of about 3,800 common names, so Michael comes out the way it is written in each script rather than letter by letter.

## Earlier: April 2026 product audit

A full audit across security, performance, code quality, UI and accessibility took the site from 4.9/10 to 8/10: zero dependency vulnerabilities and a tightened CSP, about 600 KB less per page, a modular keyboard runtime, RTL layouts for 10 languages, and ARIA labels, focus handling and reduced-motion support throughout.

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
