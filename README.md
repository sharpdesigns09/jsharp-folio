<div align="center">

# J.D. Sharp — Portfolio
### Biomedical Engineer · Medical Device Design · Fabrication

[![Live Site](https://img.shields.io/badge/Live_Site-jdsharp.org-6AAFE0?style=for-the-badge&logo=cloudflare&logoColor=white)](https://jdsharp.org)
[![PageSpeed Performance](https://img.shields.io/badge/PageSpeed-62%2F100-orange?style=for-the-badge&logo=pagespeed-insights&logoColor=white)](https://pagespeed.web.dev)
[![Accessibility](https://img.shields.io/badge/Accessibility-100%2F100-brightgreen?style=for-the-badge&logo=pagespeed-insights&logoColor=white)](https://pagespeed.web.dev)
[![SEO](https://img.shields.io/badge/SEO-100%2F100-brightgreen?style=for-the-badge&logo=pagespeed-insights&logoColor=white)](https://pagespeed.web.dev)
[![Best Practices](https://img.shields.io/badge/Best_Practices-100%2F100-brightgreen?style=for-the-badge&logo=pagespeed-insights&logoColor=white)](https://pagespeed.web.dev)

*Engineering at the intersection of clinical need and precision manufacturing —*
*from concept sketches to FDA-ready prototypes.*

</div>

---

## Overview

Single-page portfolio for **Joseph D. Sharp**, Fabrication Lab Manager and Subject Matter Expert in electro-mechanical engineering at UNC Chapel Hill and NC State. The site showcases fifteen years of engineering leadership across biomedical devices, fabrication systems, digital tooling, and industrial design.

Built as a lean, dependency-free HTML/CSS/JS site and deployed on **Cloudflare Pages** — no frameworks, no build step, no runtime dependencies.

---

## Live Projects

| # | Project | Discipline |
|---|---------|------------|
| 01 | **Endoscopic GI Surgical Actuator** — Novel steerable actuator developed with UNC Hospital's Advanced Endoscopy Fellowship. Documented to ISO 13485, 21 CFR 8xx, and IEC 60601-1. | Medical Device · Mechanical |
| 02 | **CNC Shielding — Wegstr PCB Mill** — Custom acrylic safety enclosure fabricated in-house with DCM solvent bonding and 3D-printed fixtures. | Mechanical · Operations |
| 03 | **Album Illustration — Commission** — Traditional media commission for recording artist Jose "MoneyBag$" Rios. Exhibited at Pancakes & Booze. | Illustration |
| 04 | **3D Printing Queue — UNC BME** — Department-wide queue management: Google Forms → App Script → Calendar → DakBoard on Raspberry Pi. Increased machine tracking from 0% to 40%+. | Digital · Operations |
| 05 | **Z-axis Manual Override — Universal Laser** — Emergency brass leadscrew adapter machined on lathe and mill to rescue a seized $50k laser cutter bed. | Mechanical |

---

## Technical Stack

```
Hosting     Cloudflare Pages
Language    HTML5 · CSS3 · Vanilla JS
Fonts       Self-hosted WOFF2 — Playfair Display · IBM Plex Mono · IBM Plex Sans
Images      AVIF (thumbnails 224×160px 2× retina) · PNG · JPEG
Forms       Web3Forms API
Captcha     Cloudflare Turnstile
CV Gate     Lead-capture modal before PDF download
Analytics   Cloudflare Web Analytics
```

---

## Performance

Tested on **Lighthouse 13.0.1** · Emulated Moto G Power · Slow 4G throttling.

| Metric | Score |
|--------|-------|
| Performance | 62 / 100 |
| Accessibility | **100 / 100** |
| Best Practices | **100 / 100** |
| SEO | **100 / 100** |

Active optimizations in place:

- Self-hosted WOFF2 fonts — zero Google Fonts dependency on critical path
- Three above-the-fold fonts preloaded (`playfair-display` 400/400i, `ibm-plex-mono` 400)
- Playfair Display 700 set to `font-display: optional` to prevent LCP blocking
- All images served as AVIF with explicit `width`/`height` to prevent CLS
- Thumbnail images at 224×160px (2× retina) via `loading="lazy"` + `decoding="async"`
- PDF iframe lazy-loaded
- `_headers` file sets 1-year immutable cache on all assets
- Security headers: `X-Content-Type-Options`, `X-Frame-Options`, `Referrer-Policy`

---

## SEO & Structured Data

- `<meta>` description, Open Graph, and Twitter Card tags
- JSON-LD `Person` schema with job title, skills, alma mater, and social profiles
- `robots.txt` at repo root
- `rel="canonical"` set to production URL
- All images include descriptive `alt` attributes
- `rel="noopener noreferrer"` on all external links

---

## Accessibility

- WCAG AA contrast compliant (`--dim: #999` on `#0c0c0c`)
- `<main>` landmark wrapping all page content
- `aria-label` on nav, sections, buttons, and all social links
- `aria-hidden="true"` on all decorative elements
- Keyboard-navigable modal (Escape to close, backdrop click to dismiss)
- Touch-device cursor fallback via `@media(hover:none)`

---

## CV Gate

Downloads of `cv.pdf` are gated behind a lead-capture modal requiring:

1. Name + Email
2. Cloudflare Turnstile captcha (Managed — invisible for verified visitors)

On submission, **Web3Forms** sends an email notification with the visitor's contact info and a download timestamp. The PDF then downloads automatically as `JD-Sharp-CV.pdf`.

---

## Repository Structure

```
/
├── index.html               # Single-page portfolio
├── cv.pdf                   # Curriculum Vitae (gated download)
├── robots.txt               # Crawler directives
├── _headers                 # Cloudflare Pages cache + security headers
├── fonts/                   # Self-hosted WOFF2 font files
│   ├── playfair-display-latin-400-normal.woff2
│   ├── playfair-display-latin-400-italic.woff2
│   ├── playfair-display-latin-700-normal.woff2
│   ├── ibm-plex-mono-latin-300-normal.woff2
│   ├── ibm-plex-mono-latin-400-normal.woff2
│   ├── ibm-plex-mono-latin-500-normal.woff2
│   ├── ibm-plex-sans-latin-300-normal.woff2
│   ├── ibm-plex-sans-latin-400-normal.woff2
│   └── ibm-plex-sans-latin-500-normal.woff2
├── gi-assy.png              # Project 01 — full res
├── gi-assy-thumb.avif       # Project 01 — thumbnail 224×160
└── ...                      # Additional project images
```

---

## Contact

**Joseph D. Sharp**
Fabrication Lab Manager · UNC Chapel Hill Biomedical Engineering

[![Email](https://img.shields.io/badge/Email-jd%40jdsharp.org-6AAFE0?style=flat-square&logo=gmail&logoColor=white)](mailto:jd@jdsharp.org)
[![LinkedIn](https://img.shields.io/badge/LinkedIn-j--d--sharp-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/j-d-sharp/)
[![GitHub](https://img.shields.io/badge/GitHub-sharpdesigns09-181717?style=flat-square&logo=github&logoColor=white)](https://github.com/sharpdesigns09)
[![Instagram](https://img.shields.io/badge/Instagram-sharpdesigns09-E4405F?style=flat-square&logo=instagram&logoColor=white)](https://www.instagram.com/sharpdesigns09/)
[![YouTube](https://img.shields.io/badge/YouTube-sharpdesigns09-FF0000?style=flat-square&logo=youtube&logoColor=white)](https://www.youtube.com/@sharpdesigns09/playlists)

---

<div align="center">
<sub>© 1989–2026 Joseph D. Sharp · All Rights Reserved</sub>
</div>
