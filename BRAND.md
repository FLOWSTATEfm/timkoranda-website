# FLOWSTATE RECORDS — Brand Reference

> Living document. Update whenever new standards are established.

---

## Identity

**Artist:** Tim Koranda  
**Label:** FLOWSTATE Records  
**Based:** Los Angeles, CA  
**Web:** timkoranda.com · flowstaterecords.fm  
**Voice:** Underground. Precise. Forward-moving. Los Angeles.

---

## Logo & Wordmark

The primary wordmark is **FLOWSTATE** written as a single word, always uppercase, split by color:

| Part | Color | Hex |
|------|-------|-----|
| FLOW | White | `#ffffff` |
| STATE | Cyan | `#00d4ff` |

**Never** separate FLOW and STATE with a space in the primary mark (they are one word). The color split carries the visual separation.

### Secondary Mark
`FLOWSTATE RECORDS` — same color rules, RECORDS in small caps or reduced weight below.

### Tagline
`UNDERGROUND · LOS ANGELES` — used beneath the wordmark in caps with a center dot separator.

---

## Typography

### Display / Headings
- **Family:** Barlow Condensed
- **Weight:** 800 (ExtraBold) for FLOWSTATE wordmark; 700 (Bold) for section headers
- **Transform:** Uppercase
- **Letter-spacing:** ~0.25–0.28em (wide tracking for impact)
- **Usage:** Hero headings, merch logos, section titles, product cards

### Monospace / Code / Tags
- **Family:** Space Mono
- **Weight:** Regular / Bold
- **Transform:** Uppercase
- **Letter-spacing:** 0.3–0.45em
- **Usage:** Section numbers (01–07), subtitles, labels, taglines, tech specs

### Body / UI
- **Family:** Barlow (non-condensed), system sans as fallback
- **Usage:** Body copy, descriptions, nav items

### Web Import
```html
<link href="https://fonts.googleapis.com/css2?family=Barlow+Condensed:wght@700;800&family=Barlow:wght@300;400;500&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
```

### PIL / Image Compositing
- Use `fonts/BarlowCondensed-Bold.ttf` (in repo) for FLOWSTATE wordmarks baked into product images
- Letter-spacing simulation: add 2–4px per character gap depending on size

---

## Color Palette

| Name | Hex | RGB | Usage |
|------|-----|-----|-------|
| Cyan (brand) | `#00d4ff` | 0, 212, 255 | STATE wordmark, accents, borders, glows |
| White | `#ffffff` | 255, 255, 255 | FLOW wordmark, body text |
| Off-white | `#e8e8e8` | 232, 232, 232 | Subdued white text on dark backgrounds |
| Near-black (bg) | `#030303` | 3, 3, 3 | Primary site background |
| Dark surface | `#0a0a0f` | 10, 10, 15 | Card backgrounds, elevated surfaces |
| Mid-grey | `rgba(255,255,255,0.25)` | — | Subtext, metadata |
| Cyan glow | `rgba(0,212,255,0.15–0.4)` | — | Text shadows, ambient glow effects |

### Do Not Use
- Warm whites or creams (too approachable)
- Saturated colors outside cyan (dilutes the monochrome-with-cyan identity)
- Pure grey backgrounds (use near-black)

---

## Image Treatment

### Photography
- **Monochrome + high contrast** is the default for merch and editorial imagery
- Darks go very dark, highlights stay crisp — avoid flat grey tones
- PIL pipeline: `grayscale → Contrast ×1.9 → Brightness ×0.82 → Sharpness ×1.4`
- Unsplash CDN params for monochrome: `&sat=-100&con=55&bri=-15`

### Aesthetic References
- Underground club photography
- Parking garage / urban environment
- Ferrofluid / physics visualizations
- Dark record store / vinyl culture
- Los Angeles at night

### Product Images
- Dark backgrounds only (near-black)
- Brand cyan as the primary accent/glow color
- FLOWSTATE wordmark composited in Barlow Condensed Bold when branding physical products
- Ferrofluid Visualizer Speaker: FLOWSTATE horizontal on device bottom bezel in white+cyan
- Hoodie: FLOWSTATE on chest, baked into image pixels (not CSS overlay)

---

## Site Architecture

| # | Section | Notes |
|---|---------|-------|
| 01 | Hero | Full-bleed, artist photo, FLOWSTATE Records wordmark |
| 02 | About | Bio + press photo (currently SoundCloud avatar — update needed) |
| 03 | Music | Releases grid with streaming links |
| 04 | Mixes | Mix archive (Transmissions series) |
| 05 | Events | Upcoming / past shows |
| 06 | Merch | Product cards — all "Soon" at launch |
| 07 | Contact | Booking email + social links + contact form |

---

## Merch Cards (current)

| Product | Image | Status |
|---------|-------|--------|
| Digital Release | Live concert photo (confetti, crowd) | Soon |
| FLOWSTATE Hoodie | Monochrome parking garage photo, FLOWSTATE on chest | Soon |
| Ferrofluid Visualizer Speaker | 3D product render, FLOWSTATE on device | Soon |
| Vinyl · Ltd. | Monochrome turntable close-up | Soon |

---

## Contact & Booking

- **Booking / General:** Bookings@TimKoranda.com
- **Label site:** flowstaterecords.fm
- **Formspree form ID:** `xvzjvwdy` (restricted to timkoranda.com)

---

## Social Links

| Platform | URL |
|----------|-----|
| SoundCloud | soundcloud.com/timkoranda |
| Instagram | instagram.com/timkoranda |
| TikTok | tiktok.com/@timkoranda |
| YouTube | youtube.com/@timkoranda |
| Facebook | facebook.com/tim.koranda |
| X / Twitter | x.com/timkoranda |
| Spotify | open.spotify.com/user/31bh2en3tt2nfdpfhdtxschl6uba |
| Apple Music | *coming soon* |
| Mixcloud | *coming soon* |

---

## Deployment

- **Repo:** github.com/FLOWSTATEfm/timkoranda-website
- **Host:** Netlify (auto-deploy on push to `main`)
- **Domain:** timkoranda.com
- **Push workflow:** `rm -f .git/HEAD.lock && git push origin main`
- **Local font for PIL:** `fonts/BarlowCondensed-Bold.ttf`

---

*Last updated: July 2026*
