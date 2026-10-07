# Pure Harmony Choir — Wix Classic Build Guide **v2** ("Concert Program")

Matches `mockup-v2.html`. v1 (`mockup.html` + `BUILD-GUIDE.md`) is untouched.
**What changed from v1:** new font pairing, black header with centered crest, black hero with the photo shown as a framed print, centered lede + mosaic on Home, masthead-style two-column layouts on About and Contact, a 2×2 hairline "menu" on Services.
**Unchanged from v1:** all copy (verbatim), all photos, the decisions list (section 0 of v1 — FLORIDA typo, reused About sentence on Home, Search removed, no invented contact info, Wix ad bar, SEO titles), image alt text (v1 §11), mobile principles (v1 §9), animation rules (v1 §10), and the QA checklist (v1 §12). Copy text for each section is in v1 — paste from there.

The same Classic rules apply: 980 grid, content x = 40 → 940 (900 wide), Y measured from the top of each strip, Mobile Editor built separately.

---

## 1. Site Design

### Fonts (Site Design → Text)
| Style | Font | Spec |
|---|---|---|
| H1 | **Playfair Display** Regular | 72–88 px, line-height 1.05–1.12 |
| H2 / H3 | Playfair Display Regular, **or Italic** for category names, location names, "Booking Inquiry" | 26–48 px |
| Entry titles (Services) | Playfair Display **SemiBold** | 19 px |
| Lede / pull quote | Playfair Display *Italic* | 36–38 px (Home), Regular 30 px (About) |
| Body | **Lato** Regular | 16 px, line-height 1.8, `#5C554B` (on black: `#CFC6B4`) |
| Eyebrow / nav / buttons | Lato **Bold**, caps | 12 px, character spacing ≈ 240–300 |

Playfair is high-contrast — keep it ≥ 26 px. All body copy is Lato.
**Wix fallback:** if "Playfair Display SemiBold" isn't listed, use Bold for entry titles.

### Colors
| Role | Hex | Use |
|---|---|---|
| **Black** | `#000000` | Header, hero, footer, CTA band — **must be pure black** so the crest (black-background JPG) is seamless |
| Ivory | `#F6F1E7` | Main page background |
| Ivory deep | `#ECE4D4` | Gallery / locations bands |
| White | `#FFFFFF` | Manager band, form panel |
| Ink | `#1A1816` | Headings, button fill |
| Gold | `#B8935A` | Rules, frames, hover |
| Gold deep | `#80622F` | Small gold text on ivory |
| Gold light | `#D8BC88` | Gold text on black, italic "Choir" |
| Cream | `#F3ECDD` | Text on black |
| Muted | `#5C554B` | Body text on ivory |
| Hair | `#D8CDB8` / `#2A2621` | Divider lines on ivory / on black |

### Buttons
Square, no shadow. Sizes 170 × 50, Lato Bold 12 px caps.
- **On ivory — Primary:** fill `#1A1816`, text cream → hover fill `#B8935A`, text black.
- **On black — Primary:** fill `#B8935A`, text black → hover fill cream.
- **On black — Outline:** 1 px `#B8935A`, text `#D8BC88` → hover fill gold, text black.
- **Rule (decor):** 48 × 2 px line, `#B8935A`.

---

## 2. Header (shared) — black, centered

- Header strip: height **152**, fill `#000000`, bottom border 1 px `#2A2621`. Fixed on scroll is fine.
- **Crest** `images/home-about.jpg` (the gold-on-black logo; its background is exactly `#000000`): **92 × 92**, centered at x 444, y 12. Link → Home. *(It is a 400 px file — don't exceed ~120 px.)*
- **Menu** (single Horizontal Menu): x 240, y 108, w 500, h 34, centered, no background or borders. Items: HOME · ABOUT US · OUR SERVICES · CONTACT US. Lato Bold 12 px; normal `#CFC6B4`, hover `#D8BC88`, **selected `#F3ECDD` with a 1 px `#B8935A` underline** (use the menu skin's line/underline option; if your skin lacks one, selected = `#F3ECDD` only).
- `logo.jpg` (gold on white) is no longer in the header — keep it for the favicon / social share image.

---

## 3. HOME

Order: **Hero (black) → Lede (ivory) → Mosaic (ivory deep) → Footer (black).**

### 3.1 Hero — height 1010, fill `#000000`
| Element | x | y | w × h | Spec |
|---|---|---|---|---|
| "FLORIDA \| GEORGIA" | 40 | 60 | 900 × 20 | Lato Bold 12, spacing ≈ 420, `#D8BC88`, centered |
| H1 "Pure Harmony *Choir*" | 40 | 92 | 900 × 100 | Playfair 88 px, cream; the word **Choir** in *italic* `#D8BC88` |
| Line (left) | 258 | 232 | 64 × 1 | `#B8935A` |
| "THE LUXURY SOUND YOU DESERVE" | 340 | 222 | 300 × 22 | Lato Bold 13, spacing ≈ 380, cream |
| Line (right) | 658 | 232 | 64 × 1 | `#B8935A` |
| Button "ABOUT US" → About Us | 301 | 280 | 170 × 50 | On-black Primary |
| Button "CONTACT US" → Contact Us | 509 | 280 | 170 × 50 | On-black Outline |
| Photo `hero.jpg` — **uncropped 3:2** | 40 | 392 | 900 × 600 | the framed "print" |
| Frame box | 24 | 376 | 932 × 632 | 1 px `#B8935A`, transparent, **behind** the photo (16 px all round) |

The white studio backdrop becomes the print's own white mat against the black — no overlay, no crop. Fade-in the H1 and the photo.

### 3.2 Lede — height 520, fill `#F6F1E7`
| Element | x | y | w × h | Spec |
|---|---|---|---|---|
| Eyebrow "ABOUT US" | 40 | 110 | 900 × 18 | Gold deep, centered |
| Lede (verbatim: *Based in West Palm Beach, FL, Pure Harmony Choir is the ultimate choice for those seeking an unforgettable, luxury musical experience for their special occasion.*) | 100 | 150 | 780 × ~190 | Playfair *Italic* 38 px, line-height 1.32, ink, centered |
| Rule | 466 | 372 | 48 × 2 | gold |
| Button "ABOUT US" | 405 | 410 | 170 × 50 | On-ivory Primary |

### 3.3 Mosaic — height 560, fill `#ECE4D4`
All images 4:3, **no cropping needed**, no frames.
| Element | x | y | w × h |
|---|---|---|---|
| `gallery-3.jpg` (5 men, bridge) | 40 | 90 | 595 × 446 |
| `gallery-1.jpg` (4 women, studio) | 655 | 90 | 285 × 213 |
| `gallery-2.jpg` (3 women, garden) | 655 | 323 | 285 × 213 |

Set image click action to *None*. (Use plain image elements, not a Pro Gallery, to keep positions exact.)

---

## 4. ABOUT US

Order: **Banner → Masthead + Manager (white) → Locations (ivory deep) → Description (ivory) → Footer.**

### 4.1 Banner — height 540
Strip background `about-banner.jpg`, **Fill**, position **Center**. No title strip above it — the page title lives in the masthead below.

### 4.2 Masthead + Manager — height 700, fill `#FFFFFF`
Two columns, left 4/11, right 7/11.
| Element | x | y | w × h | Spec |
|---|---|---|---|---|
| H1 "About Us" | 40 | 90 | 340 × 80 | Playfair 72, left aligned |
| Rule | 40 | 188 | 48 × 2 | gold |
| Frame box | 54 | 258 | 300 × 277 | gold keyline, behind portrait |
| Portrait `about-manager.png` | 40 | 244 | 300 × 277 | |
| H2 "Leolen Newsome" | 440 | 100 | 500 × 60 | Playfair 48, ink |
| Eyebrow "MANAGER" | 440 | 172 | 300 × 18 | Gold deep |
| Rule | 440 | 212 | 48 × 2 | gold |
| Body (v1 §5.3 paragraph, verbatim) | 440 | 240 | 500 × ~230 | Lato 16, `#5C554B` |

### 4.3 Locations — height 560, fill `#ECE4D4`
| Element | x | y | w × h | Spec |
|---|---|---|---|---|
| "FLORIDA" | 40 | 90 | 430 × 44 | Playfair *Italic* 34, ink |
| Rule | 40 | 148 | 48 × 2 | gold |
| `about-florida.jpg` | 40 | 176 | 430 × 287 | 3:2 |
| "GEORGIA" | 510 | 90 | 430 × 44 | same |
| Rule | 510 | 148 | 48 × 2 | gold |
| `about-georgia.jpg` | 510 | 176 | 430 × 287 | 3:2 |

(Captions sit **above** the photos in v2, flush left.)

### 4.4 Description — fill ivory, height ≈ 760
Text column x 130, w 720. Paragraph 1 (the "Based in West Palm Beach…" sentence): Playfair Regular 30, line-height 1.42, ink. Then a gold rule 34 px below. Paragraphs 2–3: Lato 16, `#5C554B`, 26 px apart. Text is in v1 §5.5.

---

## 5. OUR SERVICES

Order: **Photo banner → Title (ivory) → 2×2 menu → CTA (black) → Footer.**

### 5.1 Photo banner — height 500
Strip background `services-main.jpg`, **Fill**, position **Top center**.

### 5.2 Title — height 230, fill ivory
H1 "Our Services" centered, Playfair 76 (x 40, y 80, w 900) + centered rule at y 190.

### 5.3 The 2×2 menu — fill ivory, height ≈ 780
No cards, no icons. Two columns separated by a **vertical 1 px `#D8CDB8` line at x 490**, two rows separated by a horizontal line; plus lines on the top and bottom edges (x 40 → 940).
- **Left cells** text at x 40, w 410. **Right cells** text at x 530, w 410.
- Row 1 top y 0 · Row 2 top ≈ y 390 (each cell ≈ 390 tall; the longest entries — Ceremonial / Artistic — set the height).
- In each cell: category (Playfair *Italic* 34, ink) → rule (48 × 2 gold, 16 px below) → entry 1 title (Playfair SemiBold 19) + body (Lato 15, `#5C554B`) → 30 px gap → entry 2.
- Cell order: **Artistic Performance** (TL), **Ceremonial Elegance** (TR), **Cinematic Capture** (BL), **Custom Event Design** (BR). All entry text verbatim from v1 §6.3.

### 5.4 CTA — height 260, fill `#000000`
Button "CONTACT US" → Contact page, On-black Outline, 170 × 50, centered (x 405, y 105).

---

## 6. CONTACT US

Order: **Banner → Masthead + Form → Footer.**

### 6.1 Banner — height 480
Strip background `contact-main.jpg`, **Fill**, position **Center** (all five singers' faces stay in frame).

### 6.2 Masthead + Form — fill ivory, height set by the form (≈ 2,500)
Left column (sticks to the top of the form — Classic can't make it sticky, so just top-align):
| Element | x | y | w × h | Spec |
|---|---|---|---|---|
| H1 "Contact Us" | 40 | 96 | 330 × 70 | Playfair **58** (72 wraps in this column), left aligned |
| Rule | 40 | 182 | 48 × 2 | gold |
| "Booking Inquiry" | 40 | 220 | 330 × 34 | Playfair *Italic* 26 |
| Intro (verbatim, v1 §7.3) | 40 | 268 | 330 × ~150 | Lato 16, `#5C554B` |

Right column — **restyle the existing form, don't rebuild it:**
- White panel box x 430, y 96, w 510 (fill `#FFFFFF`, 1 px `#D8CDB8`, radius 0) sitting behind the form; form inset 48 px.
- Inputs: transparent, bottom border only 1 px `#B9AD94` (focus `#80622F`), radius 0; text area full 1 px border. Labels Lato Bold 13 px, ink. Option labels Lato 14.5 px `#5C554B`. Submit = On-ivory Primary, 170 × 50, left aligned.
- Keep every field and option exactly as live (list in v1 §7.3).

---

## 7. Footer (shared) — height 360, fill `#000000`
| Element | y | Spec |
|---|---|---|
| Crest `home-about.jpg`, 120 × 120, centered (x 430) | 70 | Link → Home |
| "THE LUXURY SOUND YOU DESERVE" | 212 | Lato Bold 12, spacing ≈ 360, `#D8BC88`, centered |
| Links HOME · ABOUT US · OUR SERVICES · CONTACT US (text elements, ~44 px apart) | 256 | Lato Bold 12 caps, `#CFC6B4`; hover `#D8BC88` |
| Hairline `#2A2621`, x 40 → 940 | 300 | |
| **© Pure Harmony Choir, LLC 2024-2026** | 322 | Lato 13, `#8A8272`, centered |

---

## 8. Mobile (Mobile Editor)
Follow v1 §9, plus v2 specifics:
- Header: crest 64 px, centered; menu as hamburger below/beside it; header stays black.
- Hero: "FLORIDA | GEORGIA" 10 px; H1 **44 px** (breaks to 2 lines); tagline 10 px with the two flanking lines shortened to 22 px; buttons stacked 230 × 48; photo full content width (350 × 233), frame offset 8 px.
- Home mosaic: `gallery-3` full width (350 × 262), then `gallery-1` and `gallery-2` side by side (167 × 125 each, 16 px gap).
- About: banner 280; "About Us" 46 px, then portrait (full width ≤ 350), then name/role/body; Florida and Georgia stacked; description lede 23 px.
- Services: banner 280; the 2×2 menu becomes a single column, hairline between cells, no vertical line.
- Contact: banner 280; title block above the form; form full width, panel padding 20.
- Body text stays 16 px; nothing smaller than 14 px.

---

## 9. v2-specific QA
- [ ] Header, hero, CTA band and footer all exactly `#000000`; zoom in on the crest — no visible box edge.
- [ ] Hero photo is the full uncropped 3:2 image (all four faces + hands visible).
- [ ] H1 on Contact is 58 px and does not wrap.
- [ ] 2×2 menu lines align; no cell text touches a divider.
- [ ] Playfair never below 26 px; Lato body 16 px.
- [ ] Contact banner: all five faces visible at 1920, 1440 and 1280 widths.
- Plus v1 §12 checklist.
