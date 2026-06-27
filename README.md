# Al-Mustafa Quran Academy 🌙

A bilingual (Arabic/English), single-page responsive landing site for **Al-Mustafa Quran Academy** (دار المصطفى) — a Quran memorization institute offering Ijazah (certified recitation licenses), Tajweed correction, and Hifz review programs under Azhari supervision.

> Built by **El Sab3 Company** — Web Development.

---

## 📖 Overview

This is a static marketing/landing page designed to:
- Introduce the academy and its founder/sheikh
- Showcase student testimonials
- List core services (Ijazah, Tajweed correction, Hifz review)
- Recommend useful companion Quran/Islamic apps
- Provide direct contact options (WhatsApp, phone, Facebook, Google Maps)

The page uses scroll-based section navigation (`#home`, `#about`, `#highlight`, `#services`, `#apps`, `#contact`) and animates content on scroll using **AOS (Animate On Scroll)**.

## ✨ Features

- **Responsive navigation bar** with a desktop menu and a collapsible mobile menu (built using native `<details>`/`<summary>`, no JS required for the toggle)
- **Hero section** with academy intro, key stats counter (graduates, full Quran memorizers, years of experience), and quick-access social/contact icons
- **About section** describing the academy's mission, founding year, location, and supervising sheikh
- **Highlights / Testimonials section** with a two-column layout — academy strengths on one side, real student testimonials with photos on the other
- **Services section** with icon-based cards for:
  - Certified Ijazah with connected chain of transmission (سند متصل)
  - Tajweed and recitation correction
  - Hifz review & retention programs
- **Apps section** recommending external Quran/Islamic Play Store apps (Mushaf Al Qiyam, Mushaf Light, Azkar, Ghareeb Al-Quran, Tarteel) with direct download links
- **Footer/Contact section** with a call-to-action, quick links, app links, and developer credit (El Sab3 Company)
- **Scroll animations** powered by [AOS](https://github.com/michalsnik/aos)
- **Icon support** via [Font Awesome 7](https://fontawesome.com/)
- **Custom web fonts**: Poppins, Cairo, Tajawal, Reem Kufi, and Lavishly Yours (via Google Fonts) to support both Latin and Arabic typography

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| HTML5 | Page structure/markup |
| CSS3 (`css/style.css`) | Styling (not included in this upload — see note below) |
| [AOS](https://unpkg.com/aos@next/dist/aos.css) | Scroll-triggered animations |
| [Font Awesome 7](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/7.0.1/css/all.min.css) | Icon library |
| Google Fonts | Poppins, Cairo, Tajawal, Reem Kufi, Lavishly Yours |

No build tools, frameworks, or package managers are required — this is a plain HTML/CSS/JS project that runs directly in the browser.

## 📁 Expected Project Structure

```
.
├── index.html
├── css/
│   └── style.css
└── image/
    ├── man one.jpg
    ├── man two.jpg
    ├── man three.jpg
    ├── women.jpg
    ├── quaam quran.png
    ├── light quran.png
    ├── azkar.png
    ├── ghareep.png
    ├── tarteel.png
    └── sab3 logo.png
```

> ⚠️ **Note:** Only `index.html` was provided/analyzed for this README. The `css/style.css` stylesheet and all files in `image/` are referenced by the markup but were not included — make sure to add them to the project folder above for the page to render and look as intended.

## 🚀 Getting Started

1. Clone or download this repository.
2. Make sure the `css/style.css` file and all images referenced in `index.html` (see structure above) are placed in the correct folders.
3. Open `index.html` directly in your browser, **or** serve it locally for best results (recommended, since some browsers restrict local file access):

   ```bash
   # Using Python
   python -m http.server 8000

   # Using Node (http-server)
   npx http-server
   ```

4. Visit `http://localhost:8000` in your browser.

No installation or dependencies are required beyond an internet connection (for the CDN-hosted fonts, icons, and AOS library).

## 🔗 External Links Used in the Page

- WhatsApp contact: `whatsapp://send?phone=+2001114625823`
- Phone: `tel:01114625823`
- Facebook page
- Google Maps location
- Play Store links for recommended apps

## 🧹 Known Issues / Suggested Improvements

A few issues were spotted in the markup that are worth cleaning up:

- **Malformed Play Store links in the footer** — several `href` values in the "important apps" list contain extra text (e.g. app descriptions) appended directly inside the URL string, which breaks the links:
  ```html
  href="https://play.google.com/store/apps/details?id=com.smartech.mushaf.qiyam
   Quran app with ayat search"
  ```
  These should be cleaned up to contain only the URL.
- **Duplicate/stray closing `</div>` tags** in the About section (lines ~137–139) that don't appear to pair with an opening tag — worth auditing with an HTML validator.
- **Image alt text** is generic (`"this file is not supported"`) across all images — consider writing descriptive alt text for accessibility and SEO.
- **`whatsapp://` protocol links** only work on devices with WhatsApp installed; consider using `https://wa.me/<number>` as a more universally compatible fallback (already used correctly once in the footer's "work together" link).
- **Lazy-loaded images** are already correctly using `loading="lazy"` — good practice, keep this consistent across any new images added.

## 👤 Credits

- **Design & Development:** El Sab3 Company (for web development)
- **Academic Supervision:** Sheikh Mostafa Abu El-Naga (مصطفى أبو النجا), licensed in the Ten Qira'at (القراءات العشر), Al-Azhar

## 📄 License

No license was specified in the uploaded source. Add a `LICENSE` file to clarify usage rights if this project will be shared or reused publicly.