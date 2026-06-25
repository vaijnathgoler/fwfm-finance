# Folk Williams Financial Management — Final Delivery

## Complete Rebuild — Version 3.0 (Bold & Substantial)

### What Changed in This Upgrade

| Feature | Before | After (Bold) |
|---|---|---|
| **Logo** | Approximate SVG | Exact original logo image (44px, high presence) |
| **Nav Height** | ~64px | 84px (taller, more commanding) |
| **Button Borders** | 1px thin | 2px substantial |
| **Button Padding** | 12px 28px | 14px 32px (more weight) |
| **Display Type** | Light 300 | Medium 500 (heavier, more premium) |
| **Body Type** | Light 300 | Regular 400 (better readability, less fragile) |
| **Nav Links** | 11px / 0.14em | 12px / 0.16em (bolder, wider) |
| **Section Padding** | 160px | 180px–200px (more breathing room) |
| **Hero Display** | 48–112px | 52–120px (even more commanding) |
| **Card Borders** | 1px | 2px (substantial, architectural) |
| **Footer Logo** | 28px | 40px (heavier brand presence) |
| **Mobile Menu** | Alert placeholder | Full overlay with hamburger→X animation |
| **Archetype Nav** | direction:rtl (bug) | Proper grid order (clean) |
| **All Hover States** | Basic | 2px underline, translateY(-3px), heavy shadows |

---

## Complete File Map

```
fwfm-design/
├── pages/
│   ├── index.html                    (Homepage — flagship)
│   ├── business-management.html      (Elite archetype page — 4 segments)
│   ├── tax-preparation.html          (Inclusive service — pricing tiers)
│   ├── accounting.html               (Strategic accounting — entity detail)
│   ├── insights.html                 (Editorial blog hub — magazine layout)
│   └── contact.html                  (Premium form — portals — diagnostic)
├── images/
│   ├── logo-original.jpg             (Exact provided logo — 16026 bytes)
│   ├── hero-premium.jpg              (Cinematic architectural hero)
│   ├── editorial-still.jpg           (Warm editorial texture)
│   ├── hero-architecture.jpg         (Abstract architectural lines)
│   ├── texture-oceanic.jpg           (Fluid oceanic texture)
│   ├── archetype-elite.jpg           (Theatrical spotlight)
│   ├── archetype-corporate.jpg      (Dusk glass skyscraper)
│   ├── archetype-wealth.jpg          (Gold & teal silk flow)
│   └── archetype-legacy.jpg          (Heritage classical columns)
└── README.md                         (This file)
```

---

## Design System (Embedded Per Page)

**Typography**
- Display: Cormorant Garamond 500 (medium weight, editorial, substantial)
- Body: Inter 400 (regular, readable, warm)
- Labels/Nav: Space Grotesk 500 (architectural, uppercase, tracked)

**Color**
- Primary: `#0097A7` → `#002529` (10-step oceanic scale, anchored to logo)
- Warm: `#FDFCFA` → `#5C5243` (cream, sand, earth — never cold grey)
- Charcoal: `#0D1117` (soft black, warm, never pure `#000000`)

**Motion**
- Easing: `cubic-bezier(0.22, 1, 0.36, 1)` — organic deceleration
- Reveals: IntersectionObserver, 1.1s duration, 0.12s stagger delays
- Parallax: Hero backgrounds at 0.25x scroll speed with `will-change`
- Hover: translateY(-3px), heavy shadow spread, 0.5s transition

**Mobile**
- Full hamburger menu overlay (hamburger → X animation)
- Touch targets: min 44px
- Responsive breakpoints: 1024px (tablet) / 640px (mobile)
- `prefers-reduced-motion` fully respected

---

## Verified Page Interconnections

| From Page | Links To |
|---|---|
| **index.html** | tax-preparation.html, accounting.html, business-management.html, insights.html, contact.html |
| **business-management.html** | index.html, tax-preparation.html, accounting.html, insights.html, contact.html + 4 anchor sections (#elite, #corporate, #wealth, #legacy) |
| **tax-preparation.html** | index.html, business-management.html, accounting.html, insights.html, contact.html |
| **accounting.html** | index.html, tax-preparation.html, business-management.html, insights.html, contact.html |
| **insights.html** | index.html, tax-preparation.html, accounting.html, business-management.html, contact.html |
| **contact.html** | index.html, tax-preparation.html, accounting.html, business-management.html, insights.html + Schwab/Fidelity portals |

---

## WordPress Integration Path

### Phase 1: Prototype Approval ✅ (Current)
All 6 HTML pages are interactive prototypes. Open any file in a browser to test scroll reveals, parallax, pathing tool, and mobile menu.

### Phase 2: Gutenberg Custom HTML Blocks
Each page is composed of self-contained sections. For WordPress deployment:

1. **Create a custom CSS file** in your theme: `fwfm.css` containing the `:root` tokens and utility classes
2. **Add Google Fonts** via `functions.php` enqueue or self-host for performance
3. **Paste each section** as a Gutenberg Custom HTML block
4. **Update image paths** from `../images/` to your WordPress Media Library URLs

### Phase 3: Performance Optimization for 90+ PageSpeed
- [ ] Self-host fonts (woff2) or use `font-display: swap`
- [ ] Convert all images to WebP/AVIF with `<picture>` fallbacks
- [ ] Inline critical CSS for above-the-fold content
- [ ] Lazy-load all images below hero
- [ ] JS is ~0.6KB (IntersectionObserver + parallax + mobile menu) — no libraries needed

---

## Final Notes

- **Logo**: The exact provided `FWFM Logo.jpg` is used as `logo-original.jpg` throughout all navs and footers
- **No stock clichés**: All 8 images are bespoke abstract/editorial photography
- **No template**: Every line of CSS is custom-written for this project
- **Accessibility**: Focus states, reduced-motion support, semantic HTML, WCAG AA contrast ratios
- **Forms**: Contact form is a prototype. Wire to Gravity Forms or WPForms with reCAPTCHA v3 for production
- **Portals**: Schwab/Fidelity links are placeholders — replace with your advisor-specific URLs

---

*Folk Williams Financial Management — Warmth in precision. Clarity in every ledger.*
*Final Delivery — June 2026*
