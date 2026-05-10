# Maserena — International Spirits Distribution

> *Refined spirits. Global reach.*

A premium, editorial-style website for **Maserena**, an international alcohol distribution business operating across Africa, Europe and Asia. Built with a warm, distinctive design language — deep sand tones, ember dark typography, and Cormorant Garamond editorial elegance.

---

## Project Status

| Section | Status | File |
|---------|--------|------|
| 01 — Hero | ✅ Complete | `maserena-hero.html` |
| 02 — About | ✅ Complete | `maserena-about.html` |
| 03 — Catalogue | ✅ Complete | `maserena-catalogue.html` |
| 04 — Order | ✅ Complete | `maserena-order.html` |
| 05 — Events | ⬜ In progress | — |
| 06 — Partners | ⬜ In progress | — |
| 07 — Contact | ✅ Complete | `maserena-contact.html` |

---

## Design System

### Colors
```css
--sand:       #EDE5D8   /* Primary background — deep sand */
--sand-mid:   #D9CBBA   /* Gradient mid tone */
--sand-deep:  #C9B49A   /* Gradient deep tone */
--ember:      #1F0C04   /* Primary type & UI — deep ember dark */
--ember-mid:  #3D1A0A   /* Hover states */
--ember-soft: #6B3420   /* Accents & labels */
```

### Typography
```
Display:  Cormorant Garamond — headings, brand name, editorial text
Body:     DM Sans — navigation, body copy, buttons, labels
```

### Philosophy
Two-color editorial system with warm gradient depth.
Inspired by Amour Liquide — bold simplicity over complex palettes.

---

## Tech Stack

### Frontend
| Tool | Purpose |
|------|---------|
| Next.js 14 | Framework — SSR, routing, performance |
| React Three Fiber | 3D bottle scenes, WebGL |
| GSAP + ScrollTrigger | Parallax, scroll animations |
| Lenis | Smooth inertia scrolling |
| Framer Motion | Page transitions |
| Tailwind CSS | Utility-first styling |

### Backend & Services
| Tool | Purpose |
|------|---------|
| Sanity CMS | Catalogue, events, content management |
| Resend | Transactional emails — confirmations, replies |
| Stripe | Payment infrastructure (future) |
| Vercel | Deployment — global edge hosting |

---

## Project Structure

```
maserena/
├── README.md
├── maserena-hero.html
├── maserena-about.html
├── maserena-catalogue.html
├── maserena-order.html
├── maserena-contact.html
└── assets/
    ├── images/
    └── fonts/
```

---

## Features Built

### Hero
- Age verification gate — legally required for alcohol sites
- Three-color gradient background with animated mesh blobs
- Canvas-drawn 3D bottle — floats, tilts toward cursor
- Staggered text reveal animations
- Custom ember-dark cursor with trailing ring

### About
- Founder photo placeholder + company story
- Animated stats strip — years, brands, markets, continents
- Six values cards reflecting founder personality
- Three regional reach cards with pulse indicators
- Parallax background word

### Catalogue
- 15 placeholder products across all categories
- Full filter system — category, origin, volume, price range, search
- Product detail modal with specs and quote CTA
- Sticky filter bar

### Order
- 4-step wholesale enquiry flow
- Product picker with live basket sidebar
- Company details + shipping + payment terms
- Full review step before submission
- Success screen with unique reference number

### Contact
- Three enquiry tabs — General, Wholesale, Press & Media
- Three regional office cards — Nairobi, Europe, Asia Pacific
- All contact channels — email, phone, WhatsApp
- Floating WhatsApp button
- Response times table

---

## Replacing Placeholder Data

All placeholders are marked `[REPLACE]` in the HTML. Key replacements:

```
[REPLACE-EMAIL]            → your real email address
[REPLACE-PHONE]            → your real phone number
[REPLACE-WHATSAPP-NUMBER]  → digits only e.g. 254700000000
[Founder Name]             → actual founder name
[Brand Name]               → actual product brand names
[XX]                       → actual wholesale prices
```

---

## Email Integration (Resend)

Wire up form submissions to Resend API:

```javascript
await fetch('/api/send', {
  method: 'POST',
  headers: { 'Content-Type': 'application/json' },
  body: JSON.stringify({
    to: 'your@maserena.com',
    replyTo: data.email,
    subject: `New enquiry — Maserena`,
  })
})
```

---

## Legal Compliance

- ✅ Age verification gate (18+)
- ✅ Responsible drinking disclaimers throughout
- ✅ Wholesale-only ordering — no direct consumer sales
- ✅ Human follow-up on all orders — no automated purchasing

---

## Brand

**Name:** Maserena
**Tagline:** *Refined spirits. Global reach.*
**Founded:** East Africa
**Reach:** Africa · Europe · Asia
**Categories:** Spirits · Wine · Beer · Champagne · Liqueur

---

## Build Roadmap

- [x] Design system
- [x] Hero
- [x] About
- [x] Catalogue
- [x] Order
- [ ] Events
- [ ] Partners
- [x] Contact
- [ ] Integrate into Next.js
- [ ] Connect Sanity CMS
- [ ] Wire Resend email
- [ ] Deploy to Vercel

---

*Built with care. Like everything Maserena does.*
