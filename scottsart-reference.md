# Scott's Art — Website Redesign Reference
**scottsart.com · Prepared by Chris Carle · 2025**

---

## 1. Project Overview

The goal is to modernize ScottsArt.com — the portfolio and sales website for botanical artist Scott Carle, M.D. The redesign prototype was built by Chris Carle to improve usability on mobile and better showcase Scott's work to collectors, commissioners, and Bitcoin art enthusiasts.

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
| **Galleries on site** | 1998–2025 (by year) + EVO series + Guitars |

---

## 2. Current Site Structure

### Main Navigation Pages
- **Home Page** — hero image, gallery links, tagline
- **Artist Bio** — full background, philosophy, digital art expansion
- **Digital Offerings** — Bitcoin / Ordinals section (newest addition)
- **Social Media & Contact** — Facebook, Twitter, LinkedIn, Instagram, email, phone
- **ScottsArt LIVE Studio Webcam** — links to scottswebcam.com

### Gallery Sections
- **Physical Art by Year** — galleries from 1998, 1999, 2000, 2002–2015, 2018–2025, plus Guitars
- **EVO Galleries** — slideshow series showing the evolution of individual paintings: Daffodil, Small Zinnia, Mary, Dogwood, Hope Ball 2011, Tabriz 2011, Zinnia, Red Rose, Lily, Gerber Daisy, Tulip, Passion Flower
- **Available Art** — sparse section showing pieces for sale (no prices listed)

### Problems with the Current Site
- No prices shown anywhere on available art
- No checkout or purchase flow — buyers must call or email
- Available Art section is hard to find and nearly empty
- Commission process is vague — no form or clear steps
- Digital Offerings page is thin — one post, no marketplace link
- WordPress blog lives on a separate domain — fragmented presence
- Multiple disconnected domains (scottswebcam.com, scottseasel.com, evosunflower.com, etc.)
- Site is not mobile-friendly

---

## 3. Redesign Concept

### Color Palette

| Variable | Hex | Use |
|---|---|---|
| Background (primary) | `#0E0C0A` | Near-black — echoes the black canvas technique |
| Background (section) | `#2E2119` | Warm dark brown |
| Accent (primary) | `#C8873A` | Amber / burnt orange |
| Accent (light) | `#E8A85A` | Lighter amber for hover states |
| Text (primary) | `#F0E8DC` | Warm cream |
| Text (muted) | `#A09080` | Warm gray for secondary text |
| Sage green | `#7A8C6E` | Used for "Available" indicators |

### Typography

| Role | Font |
|---|---|
| Display / Headings | Playfair Display (serif) — elegant, gallery feel |
| Body / Quotes | Lora (serif, italic) — warm, readable |
| UI / Labels / Buttons | DM Sans (sans-serif) — clean, modern |

### Key Design Choices
- Hero section splits text left / painting grid right on desktop, stacks on mobile
- Stats bar highlights: 27+ years, 200+ paintings, any commission, Bitcoin
- Dark background makes the vivid flower colors "pop" — just like on a real black canvas
- Live pulsing red dot on webcam badge signals real-time availability
- Scott's quote prominently featured: *"Painting is an opportunity to create without rules or timelines."*

---

## 4. Page Sections (Redesign)

### Navigation
- Fixed top nav with logo, links, and Commission CTA button
- On mobile: hamburger menu opens full-screen overlay with all links
- Links: Gallery, Watch Live, About Scott, Digital Art, Commission a Piece

### Hero
- Left side: eyebrow label, large headline ("Flowers painted with soul"), subtitle, two CTAs
- Right side: 2×2 grid of vivid painting color blocks (replace with real photos)
- Live badge below CTAs linking to webcam
- Mobile: stacks vertically, painting grid becomes a banner strip

### Gallery
- Filter buttons: All / Roses / Lilies / Daisies / Available
- 4-column grid on desktop, 2-column on tablet, 1-column on phone
- Each card shows: painting name, dimensions, medium, availability status
- Hover reveals "View painting →" overlay
- "View all 200+ paintings" CTA at bottom

### Live Webcam
- Two-column layout: left = text + schedule + button, right = webcam frame mockup
- Schedule shows typical painting times (weekend mornings, random evenings, late night)
- Links to scottswebcam.com
- "No login required" note for accessibility

### About Scott
- Two-column: portrait placeholder left, story text right
- Pull quote block overlapping the portrait frame
- Credentials grid: Based in, Painting since, Specialty, Also a (Physician)

### Commission a Piece
- Centered layout with intro text
- Form fields: Name, Email, Flower (if known), Approximate size (dropdown), Vision/description
- Submit button: "Send inquiry →"

### Digital Art / Bitcoin Ordinals
- Two-column: left = text about Ordinals, right = art card
- Mentions Nashville Bitcoin Museum and @SatoshiHouseArt auction partnership
- Credits Chris as the one who encouraged Scott to explore Bitcoin
- Bitcoin badge (₿ On Bitcoin) with orange accent color

### Footer
- 4-column grid: Brand info, Gallery links, Connect links, Digital links
- Contact info: 501-960-4137 · Scott@ScottsArt.com
- Bottom bar: copyright, location

---

## 5. Mobile Responsiveness

### Tablet / Small Desktop (≤ 768px)
- Nav collapses to hamburger menu with full-screen overlay
- Hero stacks: text on top, painting grid below (50vw tall)
- Stats bar wraps to 2×2 grid
- Gallery drops to 2-column grid
- All two-column sections (webcam, about, bitcoin) stack vertically
- Commission form: row pairs stack to single column
- Footer: 2-column grid, brand spans full width

### Phone (≤ 480px)
- Gallery becomes single column
- Stats bar goes fully vertical
- Footer goes fully single column
- Painting banner height increases to 60vw
- About credentials stack to single column

---

## 6. Bitcoin & Digital Art

### Background
Encouraged by Chris, Scott has begun inscribing select paintings onto the Bitcoin blockchain as "Ordinals" — a method of permanently storing art on individual satoshis (the smallest Bitcoin units). Unlike NFTs on Ethereum or Solana, Bitcoin Ordinals inherit Bitcoin's security and permanence.

### Current Status

| | |
|---|---|
| **First inscription** | Scott's first Ordinal — a 4MB inscription of a botanical painting |
| **Format** | Physical painting + digital inscription sold together as a pair |
| **Auction partner** | @SatoshiHouseArt |
| **Venue** | Bitcoin Museum Nashville (BMAG — opened January 2026) |
| **Twitter post** | x.com/ScottCarleArt/status/1935693589075345630 |

### Opportunity
- The Nashville Bitcoin Museum just opened in January 2026 — excellent timing for local exposure
- SatoshiHouseArt is a credible Bitcoin art auction platform
- Physical + digital paired sales are a compelling collector pitch
- Scott's large, vivid paintings are visually striking in digital form
- The Digital Offerings page needs to be expanded significantly

---

## 7. Next Steps & To-Do List

### Immediate Priorities
- [ ] Replace color swatches with real painting photos from scottsart.com galleries
- [ ] Connect commission form to Scott's email (Scott@ScottsArt.com)
- [ ] Populate Available Art section with current pieces and prices
- [ ] Embed live webcam iframe from scottswebcam.com into the Watch Live section

### Near-Term
- [ ] Add proper page routing (Gallery detail pages per painting)
- [ ] Build out EVO slideshow galleries in the new design
- [ ] Expand Digital Offerings page with more Ordinals content and auction links
- [ ] Consolidate all sub-domains under one nav

### Nice to Have
- [ ] Year-by-year gallery browser with visual timeline
- [ ] Lightbox / fullscreen viewer for paintings
- [ ] Instagram feed embed for real-time social content
- [ ] Price inquiry system (structured contact, not full e-commerce)

---

## 8. Files & Links

| | |
|---|---|
| **Prototype file** | scottsart-mockup.html — fully self-contained HTML/CSS/JS |
| **Current site** | https://www.scottsart.com |
| **Webcam** | https://www.scottswebcam.com |
| **LinkedIn** | https://www.linkedin.com/in/scottsart |
| **Instagram** | https://instagram.com/scottsart |
| **Facebook** | https://facebook.com/scottsart |
| **Twitter / X** | @ScottCarleArt |
| **Bitcoin auction** | https://x.com/ScottCarleArt/status/1935693589075345630 |
| **Bitcoin Museum** | https://museum.b.tc |
| **SatoshiHouseArt** | https://satoshihouse.auction |

---

*This document and the prototype HTML file were created by Chris Carle to help modernize his dad's art website. The prototype is a static mockup — no backend required for review.*
