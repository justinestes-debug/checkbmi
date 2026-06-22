# HealthClaw — BMI Calculator

> A clean, medical-grade BMI Calculator web app built by HealthClaw.
> Single-file, zero dependencies (except Tailwind CDN), fully accessible.

---

## 🚀 Quick Start

Open `index.html` directly in any modern browser — no build step, no server required.

```bash
open index.html
# or serve it:
python3 -m http.server 8080
```

---

## 📐 Formula

**WHO Standard BMI formula:**

```
BMI = weight (kg) ÷ height (m)²
```

Unit conversions applied automatically:
- Pounds → kg: `lbs × 0.45359237`
- Feet + Inches → m: `(feet × 12 + inches) × 0.0254`

---

## 🎯 Features

| Feature | Details |
|---|---|
| **Unit Toggle** | Standard (ft + in / lbs) or Metric (cm / kg) |
| **Real-time calculation** | Updates on every keystroke |
| **SVG Gauge** | Animated needle, 4 colour zones |
| **BMI Category** | Underweight / Normal / Overweight / Obese |
| **Healthy Weight Range** | Computed from your height for BMI 18.5–24.9 |
| **Reset Button** | Clears all fields and gauge |
| **Accessibility** | ARIA labels, live region, keyboard nav |
| **Monetisation** | 2× AdSense placeholders + 3 affiliate card slots |
| **SEO** | Title, description, keywords, canonical, OG tags |

---

## 🎨 Gauge Colour Zones

| Zone | BMI Range | Colour |
|---|---|---|
| Underweight | < 18.5 | 🔵 Blue |
| Normal | 18.5–24.9 | 🟢 Green |
| Overweight | 25–29.9 | 🟡 Amber/Yellow |
| Obese | ≥ 30 | 🔴 Red |

---

## ♿ Accessibility

- All inputs have `<label>` tags + `aria-label` + `aria-describedby`
- Unit toggle buttons use `aria-pressed`
- Gauge SVG has `role="img"`, `aria-label`, `aria-valuenow/min/max/text`, and a `<desc>` tag
- Results wrapped in `aria-live="polite"` + `aria-atomic="true"` region
- Category conveyed by **text label** (not colour alone)
- Focus indicators on all interactive elements
- Respects `prefers-reduced-motion`

---

## 💰 Monetisation Setup

### Google AdSense
Search for `ADSENSE PLACEHOLDER` in `index.html`. Uncomment the two `<ins>` blocks and replace:
- `ca-pub-XXXXXXXXXXXXXXXXXX` → your AdSense publisher ID
- `1111111111` / `2222222222` → your ad slot IDs

### Affiliate Links
Search for `affiliate-placeholder` in `index.html`. Replace the `href="#...placeholder"` values with your tracked affiliate URLs for:
1. **MyFitnessPal Premium** — `#myfitnesspal-affiliate-placeholder`
2. **Noom** — `#noom-affiliate-placeholder`
3. **Home Gym Equipment** — `#fitness-equipment-affiliate-placeholder`

---

## 🌐 Domain Suggestions

| Domain | Rationale |
|---|---|
| `bmicalculator.health` | Premium health TLD, exact match |
| `checkbmi.com` | Short, action-oriented |
| `mybmicalc.com` | Personal, memorable |
| `bmicheck.io` | Modern, techy |
| `healthybmi.net` | Clear intent |
| `calcbmi.com` | Short verb form |
| `freebmicalculator.org` | Matches SEO keyword |

---

## 🗂️ File Structure

```
healthclaw/
├── index.html   ← Complete app (HTML + CSS + JS in one file)
└── README.md    ← This file
```

---

## 🛠️ Tech Stack

- **HTML5** — semantic elements, ARIA
- **Tailwind CSS** v3 via CDN — utility classes, no build step
- **Vanilla JavaScript** — no frameworks, no dependencies
- **SVG** — gauge arcs computed with `polarToXY()` math helpers
- **requestAnimationFrame** — smooth needle animation via lerp

---

## 📄 Licence

MIT — use freely for personal or commercial projects.

---

*Built by HealthClaw · Powered by OpenClaw*
