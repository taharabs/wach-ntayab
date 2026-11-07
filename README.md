<div align="center">

<img src="icons/og.png" alt="واش نطيبو اليوم؟" width="640"/>

# 🍲 واش نطيبو اليوم؟ — *What should we cook today?*

**An offline-first Progressive Web App that plans the day's Algerian meals from what's already in your kitchen.**

[![Live demo](https://img.shields.io/badge/▶%20Live%20demo-taharabs.github.io-1E6B4F?style=for-the-badge)](https://taharabs.github.io/wach-ntayab/)
![PWA](https://img.shields.io/badge/PWA-installable-5A0FC8?style=for-the-badge&logo=pwa&logoColor=white)
![Offline](https://img.shields.io/badge/works-offline-0f766e?style=for-the-badge)
![No build](https://img.shields.io/badge/build-none-555?style=for-the-badge)

[English](#-english) · [العربية](#-بالعربية)

</div>

---

## 🇬🇧 English

### The problem
Every day the same question: *"What do we cook today?"* — for lunch, the afternoon coffee and dinner.
I built this for my mother: she ticks the ingredients she has, and the app proposes dishes she can actually make.

### Features
- 🧺 **Ingredient-based suggestions** — mark what's in the kitchen, get matching dishes
- 🌞 ☕ 🌙 **Three moments a day** — lunch, afternoon coffee (sweets) and dinner
- 🇩🇿 **100+ Algerian dishes & desserts** — traditional and modern, with regional variants, prep time and difficulty
- 📅 **Weekly planner** + 🛒 **shopping list** that can be sent on **WhatsApp**
- 👨‍👩‍👧 **Share today's menu** with the family via a link
- 🌙 **Dark mode**, Arabic **RTL** interface
- 📴 **Works offline** and installs on Android like a native app

### Tech
| Layer | Choice | Why |
|---|---|---|
| UI | Vanilla HTML / CSS / JavaScript, single `index.html` | Zero build step, loads instantly on low-end phones |
| Offline | Service Worker (network-first for the page, cache fallback) | Updates arrive when online, still works without internet |
| Install | Web App Manifest + maskable icons | "Add to Home screen" on Android |
| Data | `localStorage` | Private, per-device, no backend or account needed |
| Hosting | GitHub Pages | Free, HTTPS, deploys on push |

### Project structure
```
.
├── index.html             # the whole app (UI + recipe data + logic)
├── sw.js                  # service worker — offline cache
├── manifest.webmanifest   # PWA manifest (RTL, Arabic, theme colours)
└── icons/                 # app icons + social preview (og.png)
```

### Run locally
```bash
git clone https://github.com/taharabs/wach-ntayab.git
cd wach-ntayab
python -m http.server 8000   # then open http://localhost:8000
```
> A local server is required for the service worker; opening `index.html` directly works but without offline mode.

### Deploy
*Settings → Pages → Deploy from a branch → `main` / root.* That's it.

### Roadmap
- [ ] Recipe detail pages with step-by-step instructions
- [ ] French interface option
- [ ] Export / import of the weekly plan
- [ ] Ramadan mode (ftour & shour)

---

## 🇩🇿 بالعربية

<div dir="rtl">

تطبيق صغير يقترح كل نهار **الغدا، قهوة العصر والعشا** حسب واش كاين في الكوزينة — من المطبخ الجزائري (تقليدي وعصري) + الحلويات.

- 🧺 علّمي على الحوايج اللي عندك، والتطبيق يقترح واش تطيّبي
- 🌞 الغدا · ☕ قهوة العصر · 🌙 العشا
- 📅 برنامج السمانة + 🛒 قائمة المشتريات (تتبعث في واتساب)
- 👨‍👩‍👧 ابعثي برنامج اليوم للعائلة برابط
- 🌙 الوضع الليلي، ويخدم حتى بلا أنترنت

**كيفاش تسطبيه في التيليفون:** افتحي الرابط في Chrome ← القائمة ⋮ ← «إضافة إلى الشاشة الرئيسية».

</div>

---

<div align="center">

Made with ❤️ in Blida by [Mohamed Tahar Ababsa](https://github.com/taharabs) · [Portfolio](https://techbytahar.vercel.app) · [LinkedIn](https://www.linkedin.com/in/mohamed-tahar-ababsa)

</div>
