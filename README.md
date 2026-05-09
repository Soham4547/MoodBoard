# ✦ Moodboard Generator

A beautiful, single-file HTML app that turns any text vibe into a full aesthetic universe — color palette, mood description, keywords, and typography direction. No install, no login, no API key needed.

---
Website Available : [moodboard01.netlify.app](https://moodboard01.netlify.app/)

## ✨ Features

- 🎨 **5-color palette** — curated per vibe, hover to expand each swatch
- 💬 **Mood description** — poetic, evocative copy matched to your input
- 🏷️ **Aesthetic keywords** — design language for your vibe
- ✍️ **Typography direction** — font personality and pairing suggestions
- 🖼️ **Live type preview** — see your vibe rendered in editorial Playfair Display
- 📋 **Click to copy hex** — click any swatch to copy the color code instantly
- 🔁 **Seeded generation** — same input always produces the same palette
- 🌐 **Unlimited vibes** — 8 handcrafted aesthetics + algorithmic fallback for anything else
- ⚡ **Zero dependencies** — pure HTML, CSS, and JavaScript
- 📱 **Fully responsive** — works on desktop, tablet, and mobile

---

## 🎨 Design & Animations

- Dark editorial theme with film grain noise texture overlay
- Staggered fade-up animations on palette, cards, keywords, and type preview
- Swatch hover-expand — hovered color stretches wide to reveal name and hex
- Smooth button transitions with full invert on hover
- Playfair Display editorial serif for type preview
- DM Mono for all UI text — clean, minimal, techy
- Glassmorphism-free — intentionally flat and raw

---

## 🌈 Built-in Vibes

| Vibe | Palette | Mood |
|------|---------|------|
| `rainy tokyo cafe` | Midnight blues, foggy grays | Melancholic & Intimate |
| `desert sunset` | Burnt sienna → golden ochre | Expansive & Raw |
| `90s nostalgia` | Bubblegum, grape soda, aqua | Chaotic & Joyful |
| `deep sea` | Abyss black → bioluminescent teal | Mysterious & Ancient |
| `cottage core` | Parchment, sage, bark | Gentle & Grounded |
| `brutalist architecture` | Carbon → bone white | Severe & Honest |
| `cherry blossom` | Petal blush → twilight plum | Fleeting & Beautiful |
| `industrial warehouse` | Soot, iron, rust, hazard yellow | Gritty & Authentic |
| *anything else* | Algorithmically generated ✨ | Unique to your input |

---

## 🔧 How It Works

1. User types a vibe and hits **Generate** (or presses Enter)
2. App checks for an **exact match** in the curated vibe library
3. Falls back to **partial keyword matching** across vibe names
4. If no match, runs a **seeded LCG color algorithm** using a hash of your input
5. Palette, mood, keywords, and type preview are rendered with staggered animations
6. Click any swatch to copy its hex code to clipboard

---

## 🧠 The Seeded Algorithm

For vibes outside the library, the app generates a deterministic palette using:

| Step | What Happens |
|------|-------------|
| Hash | Input string → integer seed via polynomial rolling hash |
| RNG | Seeded linear congruential generator (LCG) |
| Colors | 5 HSL values across complementary hues |
| Keywords | Adjective pool shuffled by seed, top 6 selected |

Same input = same palette. Every time. Forever.

---

## 🚀 How to Use

### Option 1 — Open Locally

Just download `moodboard-generator.html` and open it in any browser. Done.

### Option 2 — GitHub Pages (Live Website)

1. Fork or clone this repo
2. Go to **Settings → Pages → Source → main branch**
3. GitHub gives you a live link: `https://yourusername.github.io/moodboard-generator`

---

## 🛠️ Tech Stack

- **HTML5** — single file, no build step
- **Pure CSS3** — animations, custom properties, flexbox, grid
- **Vanilla JavaScript** — DOM manipulation, seeded RNG, HSL color math, Clipboard API
- **Google Fonts** — Playfair Display + DM Mono (loaded via CDN)

---

## 📊 Output Breakdown

| Section | What You Get |
|---------|-------------|
| 🎨 Palette Row | 5 color swatches with name + hex, hover to expand, click to copy |
| 💬 Mood Card | Label + poetic 1–2 sentence description |
| 🎛️ Palette Card | Typography direction + top 3 palette colors with dots |
| 🏷️ Keywords | 7–9 aesthetic tags for the vibe |
| ✍️ Type Preview | Your input rendered large in Playfair Display + italic mood label |

---

## 🎛️ Add Your Own Vibes

Open `moodboard-generator.html`, find the `VIBES` object, and add an entry:

```javascript
"your vibe here": {
  palette: [
    { hex: "#RRGGBB", name: "color name" },
    { hex: "#RRGGBB", name: "color name" },
    { hex: "#RRGGBB", name: "color name" },
    { hex: "#RRGGBB", name: "color name" },
    { hex: "#RRGGBB", name: "color name" },
  ],
  mood: "Mood Label",
  description: "One or two evocative sentences about the feeling.",
  keywords: ["word", "word", "word", "word", "word", "word", "word"],
  fontMood: "Typography personality in a few words",
},
```

---

## 📁 Project Structure

```
moodboard-generator.html   ← entire app in one file (HTML + CSS + JS)
README.md                  ← this file
```

---

## 📱 Responsive Breakpoints

| Screen | Layout |
|--------|--------|
| Desktop | Full-width palette, 2-column info grid, expanded keyword row |
| Tablet ≤ 768px | Stacked input zone, single-column cards |
| Mobile ≤ 480px | Compact padding, full-width button |

---

## 📄 License

MIT — free to use, modify, and distribute.
