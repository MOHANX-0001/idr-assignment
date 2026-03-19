<div align="center">

# 🧊 Institute of Digital Risk — Website

[![Status](https://img.shields.io/badge/Status-Live-F05A1A?style=for-the-badge)](https://instituteofdigitalrisk.com)
[![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/HTML)
[![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)](https://developer.mozilla.org/en-US/docs/Web/CSS)
[![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)](https://developer.mozilla.org/en-US/docs/Web/JavaScript)
[![License](https://img.shields.io/badge/License-Private-555555?style=for-the-badge)](#)

<br/>

> **Professional marketing website** for the Institute of Digital Risk (IDR) —  
> an industry-led training and deployment institute for digital, cyber and AI risk practitioners.  
> Built with pure HTML · CSS · Vanilla JS. Zero frameworks. Zero dependencies.

</div>

---

## 📌 Table of Contents

- [Overview](#-overview)
- [Live Preview](#-live-preview)
- [Features](#-features)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Page Sections](#-page-sections)
- [Design System](#-design-system)
- [Logo & Brand Identity](#-logo--brand-identity)
- [Local Setup](#-local-setup)
- [Deployment](#-deployment)
- [Contributing](#-contributing)

---

## 🏛️ Overview

The IDR website is the primary public-facing platform for the **Institute of Digital Risk** — a UK-based organisation sitting at the intersection of a leading university partnership and live industry engagement.

The site is built to:
- Communicate IDR's mission, model, and value proposition to prospective students, employers, and institutional partners
- Convert visitors into registered-interest leads via a structured, categorised contact form
- Reflect the professional authority of a regulated-sector training institution
- Deliver a fast, polished experience across all devices with no runtime overhead

---

## 🌐 Live Preview

> 🔗 **[https://instituteofdigitalrisk.com](https://instituteofdigitalrisk.com)**

---

## ✨ Features

| Feature | Details |
|---|---|
| **Sticky Glassmorphic Nav** | Frosted-glass header using `backdrop-filter: blur` — stays fixed at top while scrolling |
| **3D Animated Hero Cube** | CSS 3D rotating cube in the hero section — directly tied to brand identity |
| **Scroll Reveal Animations** | Staggered element entrance on scroll via `IntersectionObserver` with `reveal-d1/d2/d3` delay classes |
| **Active Nav Highlighting** | Current section link highlights dynamically as the user scrolls through the page |
| **Responsive Hamburger Menu** | Full-screen mobile overlay with animated hamburger → X icon transition |
| **Body Scroll Lock** | Background scroll is locked while the mobile menu is open |
| **Interest Registration Form** | Role-based dropdown (Student · Professional · Organisation · University · Industry Partner · Other) |
| **Form Confirmation UX** | Inline orange success message on submit, auto-clears after 5 seconds |
| **Semantic & Accessible HTML** | Correct use of `<article>`, `aria-labelledby`, `aria-label`, `aria-hidden`, and `role` throughout |
| **Custom Scrollbar** | Orange-branded 4px scrollbar matching brand accent colour |
| **CSS Design Token System** | All colours, fonts, and spacing live in `:root` custom properties |
| **Fluid Typography** | Section titles scale via `clamp()` — responsive without breakpoints |
| **Fully Responsive** | Mobile-first layout, tested at all common breakpoints |
| **Zero Dependencies** | No npm, no frameworks — Google Fonts is the only external resource |

---

## 🛠️ Tech Stack

```
Markup      →  HTML5 (semantic, ARIA-annotated)
Styling     →  CSS3 (custom properties, grid, flexbox, 3D transforms, clamp())
Scripting   →  Vanilla JavaScript ES6+
Fonts       →  Google Fonts — Syne (display) · DM Sans (body) · DM Mono (mono/labels)
Animations  →  CSS keyframe transitions + IntersectionObserver API
Hosting     →  Static — deployable to any CDN or static host
```

**Design philosophy:** No build tools. No bundlers. No runtime dependencies. Fast by default, maintainable by design.

---

## 📁 Project Structure

```
idr-website/
│
├── index.html              # Primary HTML — all page sections and structure
├── style.css               # Full stylesheet — layout, components, animations, tokens
├── main.js                 # All JS — nav toggle, scroll reveal, form handling, nav highlight
├── idr-logo-icon.svg       # Standalone SVG logo asset (geometric cube, reusable)
└── idr-homepage.html       # Self-contained single-file version (styles + JS inline)
```

> The project is intentionally flat — no subdirectories or asset pipelines needed.

---

## 📄 Page Sections

### 🔝 Navigation
Sticky header with glassmorphic background. Contains the IDR cube SVG logo, full wordmark in Syne + DM Mono, desktop nav links with animated orange underline on hover, a "Register Interest" CTA button, and a hamburger for mobile.

### 🦸 Hero
Full-viewport opening section featuring the headline *"Advancing the Future of Digital Risk"*, a supporting paragraph, dual CTAs (Explore Programs / Learn More), and the 3D CSS cube visual with floating stats callouts: **4+ Industry Partners** and **AI/ML Risk Focused**.

### 🏢 About
Two-column layout presenting IDR's founding purpose. The left carries the main narrative copy; the right shows three highlight cards:

| Card | Summary |
|---|---|
| **University Partnership** | Research-backed methodology, analytical depth alongside vocational skills |
| **Industry-Led Design** | Curriculum co-designed with partners to reflect current threats and AI governance |
| **Deployment Focus** | Practitioners placed directly into organisations — not just trained, but deployed |

### ⚙️ Services — Three Pillars
Grid of three service cards with numbered pillar labels, SVG icons, and descriptions:

| # | Pillar | Focus |
|---|---|---|
| 01 | **Education & Training** | Academically grounded programmes in digital, cyber and AI risk |
| 02 | **Industry Deployment** | Placing trained practitioners directly into real-world regulated roles |
| 03 | **Research & Innovation** | Applied research into emerging threat models and AI governance frameworks |

Followed by the **pipeline strip**: `Train → Hire → Innovate → Deploy`

### 👥 Community — Who We Serve
Split layout with audience segments and sector coverage:

**Audiences:** Students & Graduates · Early-Career Professionals · Experienced Practitioners  
**Sectors:** Financial Services · Critical Infrastructure · Insurance · Public Sector · Healthcare · Energy · Legal & Professional

### 📬 Contact / Register Interest
Two-column section. Left: IDR contact details (email + UK location). Right: structured interest form with fields for First Name, Last Name, Email, Interest Category (dropdown), and Message. On submission, an inline orange confirmation message appears and the form resets automatically after 5 seconds.

### 🦶 Footer
Three-element minimal footer: IDR logo (cube + wordmark), copyright notice, and quick-nav links.

---

## 🎨 Design System

All design tokens are declared as CSS custom properties in `:root`:

```css
:root {
  /* Brand */
  --orange:    #F05A1A;   /* Primary — CTA buttons, accents, highlights, scrollbar */
  --orange-lt: #FF7A3D;   /* Hover states, lighter variant */

  /* Surfaces */
  --black:     #080808;   /* Page background */
  --ink:       #111111;   /* Alt dark surface */
  --grey-dk:   #1C1C1C;   /* Cards, elevated containers */
  --grey-md:   #2E2E2E;   /* Borders, dividers, form inputs */
  --grey-lt:   #9A9A9A;   /* Muted text, labels, secondary copy */
  --white:     #F8F6F2;   /* Primary text (warm off-white — avoids harsh pure white) */

  /* Typography */
  --font-display: 'Syne', sans-serif;      /* Headlines, nav, buttons */
  --font-body:    'DM Sans', sans-serif;   /* Body copy, paragraphs */
  --font-mono:    'DM Mono', monospace;    /* Tags, stat labels, section markers */

  /* Layout */
  --nav-h: 70px;      /* Nav height used for mobile menu offset */
  --max-w: 1160px;    /* Max content width */
}
```

**Typography** uses `clamp()` for fluid scaling — section titles respond from `2rem` to `3rem` without requiring breakpoints.

**Selection colour** is overridden to `--orange` for a consistent branded feel on text highlight.

---

## 🧊 Logo & Brand Identity

The IDR logo is a **geometric cube** constructed entirely from inline SVG polygons — no raster images, infinitely scalable, zero loading overhead.

```
Top face    →  #F8F6F2  (off-white)   — clarity, openness
Left face   →  #1C1C1C  (dark grey)   — depth, professionalism
Right face  →  #F05A1A  (orange)      — innovation, energy
```

> *"The cube structure symbolises stability and protection within complex digital environments. Orange highlights innovation and energy, while black and white provide a professional and trustworthy technology-focused appearance."*

The cube appears in **three contexts** across the site:

| Context | Size | Notes |
|---|---|---|
| Navigation header | 42×42px | Includes dashed construction line for detail |
| Hero section | ~260px scene | CSS 3D animated, continuously rotating |
| Footer | 32×32px | Simplified, static |

---

## ⚙️ Local Setup

No build step required. Clone and open directly.

```bash
# 1. Clone the repository
git clone https://github.com/<your-org>/idr-website.git

# 2. Move into the project folder
cd idr-website

# 3. Open in browser
open index.html

# — OR — use VS Code Live Server for hot-reload
```

> 💡 **Recommended:** Install the [Live Server](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer) extension in VS Code. Right-click `index.html` → *Open with Live Server* for instant browser refresh on file save.

---

## 🚀 Deployment

Fully static — deploys to any host with no configuration or build step.

### GitHub Pages
```bash
# Push to main → Settings → Pages → Source: main / root
# Accessible at: https://<org>.github.io/idr-website
```

### Netlify (Drag & Drop)
1. Go to [app.netlify.com](https://app.netlify.com)
2. Drag the project folder into the deploy zone
3. Live instantly — auto-deploys on every future push

### Cloudflare Pages
```
Build command:    (leave empty)
Publish directory: /
```

### Any Static Host (Vercel, S3, etc.)
Upload `index.html`, `style.css`, `main.js`, and `idr-logo-icon.svg` — that's the entire deployment.

---

## 🤝 Contributing

This is a private institutional codebase. For internal contributors:

1. **Branch naming:** `feature/section-name` or `fix/brief-description`
2. **Keep the vanilla stack** — no frameworks, no build tools, no npm packages
3. **Always use CSS custom properties** — never hardcode hex values directly in rules
4. **Preserve accessibility** — maintain all `aria-label`, `aria-labelledby`, `aria-hidden`, and `role` attributes
5. **Mobile-first** — test on small screens before raising a pull request
6. **Form backend** — the contact form currently uses a frontend-only stub; integrate with a backend service (e.g. Formspree, EmailJS, or a custom API) before going live

---

<div align="center">

**© 2025 Institute of Digital Risk. All rights reserved.**  
*United Kingdom*

</div>
