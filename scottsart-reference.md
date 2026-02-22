# Scott's Art — Website Reference
**scottsart.com · Prepared by Chris Carle · 2025**

---

## 1. Project Overview

The goal is to modernize ScottsArt.com — the portfolio and sales website for botanical artist Scott Carle, M.D. The redesign was built by Chris Carle to improve usability on mobile, better showcase Scott's work to collectors, commissioners, and Bitcoin art enthusiasts, and simplify the browsing experience by splitting the site into focused pages.

> **Design goal:** Warm & personal — like meeting the artist — with a focus on the live webcam, better gallery browsing, and a clear path to commission or purchase art.

### About Scott Carle

| | |
|---|---|
| **Location** | Little Rock, Arkansas 72223 |
| **Phone** | 501-960-4137 |
| **Email** | Scott@ScottsArt.com |
| **Website** | scottsart.com |
| **Webcam** | scottswebcam.com |
| **Painting since** | Age 9 (inspired by grandfather A.P. Finken) |
| **Day job** | Occupational Medicine physician, 35+ years at Concentra |
| **Specialty** | Large-scale botanical oil paintings on black canvas |
| **Total paintings** | 200+ originals spanning 1998–2025 (catalog codes C00–C25) |

---

## 2. Site Structure (Multi-Page)

The site is split into 6 standalone HTML pages, each with shared nav, footer, and design system (inline CSS, no build tools).

### Pages

| Page | File | Description |
|------|------|-------------|
| **Homepage** | `index.html` | Hero section, 8 featured paintings, commission form |
| **Full Gallery** | `gallery.html` | ~100 paintings from MOREPieces archive, filterable by flower type |
| **About Scott** | `about.html` | Portrait, bio, quote, credentials grid |
| **The Process** | `process.html` | 5-step painting process strip, studio photos |
| **Watch Live** | `live.html` | Webcam preview, painting schedule, link to scottswebcam.com |
| **Digital Art** | `digital.html` | Bitcoin Ordinals, SatoshiHouseArt auction, Bitcoin Museum |

### Navigation (shared across all pages)
- Fixed top nav: Logo → Gallery, Watch Live, About Scott, Digital Art, Commission a Piece (CTA)
- Mobile: hamburger menu opens full-screen overlay
- Commission CTA links to `index.html#commission` from sub-pages

---

## 3. Image Assets

### Source Folders

| Folder | Contents | Count |
|--------|----------|-------|
| `images/hero/` | Hero section images (anemone, poppy, passionflower, tulip) | 4 |
| `images/gallery/` | Web-optimized gallery images + thumbnails | ~21 + 19 thumbs |
| `images/process/` | 5-step tulip process photos | 5 |
| `images/studio/` | Work-in-progress studio shots | 4 |
| `images/about/` | Portrait + signature | 2 |
| `images/scottsordinal.png` | Bitcoin Ordinal artwork | 1 |
| `MOREPieces/ART all images/` | Full catalog archive (C00–C25) | 228+ |
| `MOREPieces/MARKETING PIECES BIO ETC/` | Marketing materials, .pub files | 264 |
| `Scotts Photos of Physical Art and misc Projects/` | Phone photos, raw files, archives | 244+ |

### Catalog Code System
Images in `MOREPieces/ART all images/` follow the pattern `CXX-### Description.jpg` where XX = approximate year:
- C00 = 2000, C02 = 2002, C03 = 2003 ... C25 = 2025
- Filenames contain: flower type, dimensions, framing status, and variant info

### Gallery Page — Flower Type Categories
The gallery page (`gallery.html`) organizes paintings into these filter categories:
- **Roses** (~15 paintings) — C05, C08, C11, C12, C14, C15, C25
- **Lilies** (~25 paintings) — C08, C10, C11, C12, C15, C18, C20, C23, C25
- **Tulips** (~9 paintings) — C10, C12, C13, C14, C21, C23
- **Peonies** (~6 paintings) — C15, C18, C21, C23, C25
- **Sunflowers** (~5 paintings) — C08, C10, C12, C15, C18
- **Dahlias** (~3 paintings) — C07, C11, C23
- **Orchids** (~3 paintings) — C06, C20, C25
- **Irises** (~3 paintings) — C15, C21
- **Poppies** (~3 paintings) — C08, C18
- **Passionflowers** (~4 paintings) — C10, C13, C14, C19
- **Hibiscus** (~4 paintings) — C07, C14, C25
- **Other** (~20 paintings) — zinnia, gladiolus, daisy, daffodil, poinsettia, dogwood, anemone, ranunculus, magnolia, chrysanthemum, bird of paradise, apple blossom, night blooming cereus, honeysuckle, hydrangeas, borg, etc.

---

## 4. Design System

### Color Palette

| Variable | Hex | Use |
|---|---|---|
| `--black` | `#0E0C0A` | Primary background — echoes the black canvas technique |
| `--dark` | `#1A1612` | Section backgrounds (gallery, commission) |
| `--warm-brown` | `#2E2119` | Cards, form backgrounds, footer |
| `--amber` | `#C8873A` | Primary accent — labels, CTAs, borders |
| `--amber-light` | `#E8A85A` | Hover states |
| `--cream` | `#F5EFE6` | Headings, strong text |
| `--text` | `#F0E8DC` | Primary body text |
| `--text-muted` | `#A09080` | Secondary text, meta info |
| `--sage` | `#7A8C6E` | "Available" indicators |
| `--border` | `rgba(200,135,58,0.2)` | Subtle amber borders |

### Typography

| Role | Font |
|---|---|
| Display / Headings | Playfair Display (serif) |
| Body / Quotes | Lora (serif, italic) |
| UI / Labels / Buttons | DM Sans (sans-serif) |

### Component Patterns
- `.section-label` — amber uppercase eyebrow with line prefix
- `.section-title` — Playfair Display heading
- `.section-body` — Lora italic description
- `.btn-primary` — amber background, dark text, uppercase
- `.btn-ghost` — text-only button with opacity hover
- `.gallery-card` — image with hover overlay + lift animation
- `.reveal` — scroll-triggered fade-in via IntersectionObserver
- Lightbox — full-screen image viewer with keyboard nav (gallery page)

### Responsive Breakpoints
- **768px** — nav collapses to hamburger, grids stack, sections go single-column
- **480px** — gallery goes single-column, footer stacks fully

---

## 5. Page Details

### Homepage (`index.html`)
- Hero: eyebrow label, headline ("Flowers painted with soul"), subtitle, two CTAs, live badge
- Hero right: 2x2 painting grid
- Gallery preview: 8 featured paintings linking to `gallery.html`
- Commission form: name, email, flower, size dropdown, vision textarea
- Footer with all page links

### Gallery (`gallery.html`)
- Page header with title and description
- Sticky filter bar (below nav) with 13 flower-type buttons
- 4-column grid of ~100 paintings sourced from `MOREPieces/ART all images/`
- Each card shows: painting name, dimensions, flower type tag
- Lightbox with keyboard navigation (arrows, escape)
- Filter count display

### About (`about.html`)
- Portrait section with `images/about/scott-portrait.jpg`
- Three bio paragraphs (grandfather, career, artistic approach)
- Quote: "Painting is an opportunity to create images without rules or timelines."
- Credentials grid: Location, Painting since, Specialty, Also a physician

### Process (`process.html`)
- 5-step horizontal scroll strip (sketch → early color → depth → detail → finished)
- Uses `images/process/01-05` tulip series
- Studio section with 4 in-progress photos from `images/studio/`

### Live (`live.html`)
- Webcam preview frame with blurred studio image
- Schedule: weekend mornings, random evenings, late nights
- CTA to scottswebcam.com
- "No login required" note

### Digital (`digital.html`)
- Bitcoin badge (₿ On Bitcoin)
- Ordinal card: `images/scottsordinal.png`, 4MB inscription, 1 of 1
- Links to ord.io, SatoshiHouseArt, Bitcoin Museum Nashville
- Partnership mentions: @SatoshiHouseArt, @BMAG_HQ

---

## 6. Bitcoin & Digital Art

### Background
Encouraged by Chris, Scott has begun inscribing select paintings onto the Bitcoin blockchain as "Ordinals" — a method of permanently storing art on individual satoshis. Unlike NFTs on Ethereum or Solana, Bitcoin Ordinals inherit Bitcoin's security and permanence.

### Current Status

| | |
|---|---|
| **First inscription** | Scott's first Ordinal — a 4MB inscription of a botanical painting |
| **Format** | Physical painting + digital inscription sold together as a pair |
| **Auction partner** | @SatoshiHouseArt |
| **Venue** | Bitcoin Museum Nashville (BMAG — opened January 2026) |
| **Twitter post** | x.com/ScottCarleArt/status/1935693589075345630 |

---

## 7. Next Steps & To-Do List

### Completed
- [x] Redesign prototype built (single-page)
- [x] Split site into 6 focused pages
- [x] Build full gallery page with ~100 paintings from MOREPieces archive
- [x] Flower-type filtering with lightbox viewer
- [x] Commission form connected to Scott's email
- [x] Mobile responsive across all pages
- [x] Consistent nav and footer on every page

### Remaining Priorities
- [ ] Populate Available Art section with current pieces and prices
- [ ] Embed live webcam iframe from scottswebcam.com into the Watch Live page
- [ ] Add remaining paintings from MOREPieces to gallery (early works C00–C06, more C09 variants)
- [ ] Add more paintings to homepage featured section as new work is completed

### Near-Term
- [ ] Build individual painting detail pages with larger images and full metadata
- [ ] Build out EVO slideshow galleries (painting evolution series)
- [ ] Expand Digital Offerings page with more Ordinals content and auction links
- [ ] Consolidate all sub-domains under one nav

### Nice to Have
- [ ] Year-by-year gallery browser with visual timeline
- [ ] Instagram feed embed for real-time social content
- [ ] Price inquiry system (structured contact, not full e-commerce)
- [ ] Generate proper thumbnails for gallery page performance

---

## 8. Files & Links

| | |
|---|---|
| **Site files** | `index.html`, `gallery.html`, `about.html`, `process.html`, `live.html`, `digital.html` |
| **Backup / reference** | `scottsart-mockup.html`, `scottsart-mockup-backup.html` |
| **Current site** | https://www.scottsart.com |
| **Webcam** | https://www.scottswebcam.com |
| **GitHub repo** | https://github.com/cchops89/scotts-art |
| **LinkedIn** | https://www.linkedin.com/in/scottsart |
| **Instagram** | https://instagram.com/scottsart |
| **Facebook** | https://facebook.com/scottsart |
| **Twitter / X** | @ScottCarleArt |
| **Bitcoin auction** | https://x.com/ScottCarleArt/status/1935693589075345630 |
| **Bitcoin Museum** | https://museum.b.tc |
| **SatoshiHouseArt** | https://satoshihouse.auction |
| **Ordinal on-chain** | https://www.ord.io/97602690 |

---

*This document and the site were created by Chris Carle to help modernize his dad's art website. All pages are static HTML — no backend or build tools required.*
