# eid-project

# 🌙 Bakra Eid Mubarak — Interactive Greeting Card

A beautifully animated, single-file HTML greeting card for **Eid ul Adha 1447H**, featuring a rich night-sky scene with hand-crafted SVG animals, lanterns, confetti, and Arabic/Urdu typography.

---

## ✨ Features

- **Pure HTML/CSS/JS** — zero dependencies, zero build step, zero framework
- **Hand-drawn SVG animals** — a detailed goat (بکرا) and cow (گائے) with idle animations
- **Animated night sky** — twinkling stars, a glowing crescent moon, swaying grass blades
- **Swinging lanterns** on a rope, each with a warm inner glow
- **Confetti burst system** — fires on load and on every click anywhere on the page
- **Responsive typography** — Amiri (Arabic serif) + Cinzel Decorative, served via Google Fonts
- **OpenGraph meta tags** — link previews work out of the box on WhatsApp, Twitter, etc.

---

## 🚀 Usage

Just open `index.html` in any modern browser — no server required.

```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

Or drop it on any static host (GitHub Pages, Netlify, Vercel) and share the URL.

---

## 🛠️ Customization

All personalization lives in one file. Key spots to edit:

| What | Where in `index.html` |
|---|---|
| Sender name | `.name-line` div — change `Nida Farooq Rana` |
| Blessing message | `.blessing` div |
| Year / Hijri date | `.badge` and `.year-tag` divs |
| Color palette | CSS vars / inline gradient strings |
| Confetti colors | `COLORS` array in the `<script>` block |
| Number of stars | `for(let i=0;i<90;i++)` loop |
| Number of grass blades | `for(let i=0;i<80;i++)` loop |

---

## 🏗️ Technical Notes

- **Canvas-based confetti** — particles support three shapes (circle, square, triangle), gravity, rotation, and alpha fade. Click anywhere to trigger a burst at the cursor position.
- **SVG animals** — fully inline, no external assets. The goat and cow are built from ellipses, paths, and rects with layered fills to simulate shading.
- **CSS animations only** — twinkling, swinging, swaying, and idle animal bobbing are all pure `@keyframes`; no JS animation loop touches the DOM elements.
- **Fixed-position layering** — z-index stack from back to front: sky → stars → rope → lanterns → grass → card content → confetti canvas.

---

## 📁 File Structure

```
.
└── index.html     # Everything — markup, styles, scripts, SVGs
```

Single-file by design, making it trivial to share as an email attachment or host anywhere.

---

## 📜 License

Feel free to fork, remix, and send to your own friends and family. Attribution appreciated but not required. 

---

*عيد الأضحى مبارك — May Allah accept your sacrifices and prayers.* 🌙
