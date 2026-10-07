# Pure Harmony Choir — Wix Classic Build Guide **v3** (reference-style)

Matches `mockup-v3.html` — open it, use the nav, and tap the round **PALETTE** button (bottom-right) to flip between the **Brand** palette (black + gold, from your crest) and the **Reference** palette (wine / terracotta / sage from the screenshot).
v1 and v2 are untouched. Unchanged and still authoritative from v1/v2: all copy (verbatim, v1 §4–7), alt text (v1 §11), animation rules (v1 §10), QA checklist (v1 §12), and the open decisions (v1 §0: FLORIDA spelling, About sentence reused on Home, Search removed, no invented contact info, Wix ad bar, SEO titles).

## 0. What I took from the reference, and what I changed

**Taken as-is (structure & feel):** header that sits on the dark hero · eyebrow + big serif headline + CTA hero with a photo in an **arch** · curved ("wave") divider into the ivory page · **floating white info bar** that overlaps the divider · photo tiles with a caption bar and round arrow button · wide featured banner · dark curved closing band · **pill buttons**, ~16 px rounded images/cards, soft shadows.

**Replaced with your real content (the reference's text is invented, so I did not copy it):**
| Reference | Pure Harmony version |
|---|---|
| "250K+ Attendees / 40+ countries / Global Speaker" stats bar | Your four **service categories** with their sub-service names (all existing text) → links to Our Services |
| "Programs Built for Real Change" tiles (Students, Educators…) | Tiles: **About Us · Our Services · Florida · Georgia** (existing page/location names, your photos) |
| "Turn Insight Into Action" video banner | **Booking Inquiry** banner (existing Contact heading) with the live-performance photo and a Contact Us button |
| "Listen on" podcast pills | **Dropped** — you have no podcast/audio |
| "Stories From People…" mountain band | Closing band with two of your gallery photos, crest, tagline and links |
| Handwritten script notes, vertical "PEOPLE IDEAS PROGRESS" | **Dropped** — they are invented copy, and script text conflicts with your brief |
| Line icons (globe, book…) | **Dropped** — replaced by a short gold rule above each title |
| Search icon in header | Dropped (no search needed) |

**Deviates from your original brief (because you chose this reference):** pill buttons, rounded corners and soft shadows, a wave divider, an arch shape. Everything else from the brief still holds: no gradients, glassmorphism or stock imagery; real photography; subtle animation only; gold used sparingly.

Palette choice is yours: **Brand** (default; ties to the crest) or **Reference** (wine/terracotta/sage). Sections 1–8 give both values.

---

## 1. Site Design

### Fonts
Headings **Playfair Display** · body/nav **Lato** (same as v2 — see v2 §1 for the size table). H1 on hero 62 px (Wix 980 canvas); inner-page H1 72 px; tile / card titles 28–32 px; body Lato 16 px.

### Colors
| Role | Brand | Reference |
|---|---|---|
| Dark (header, hero, closing band) | `#15110E` | `#4A1E2B` |
| Accent (hero word "Choir", eyebrows on dark) | `#D8BC88` | `#D9805A` |
| Button / round arrow | `#B8935A`, text `#0B0A09` | `#C4694A`, text `#FFFFFF` |
| Button hover | `#F3ECDD` | `#A9553A` |
| Arch behind photo | gold **outline** | **sage fill** `#8FA48B` |
| Ivory page | `#F6F1E7` (both) | |
| Ivory deep | `#ECE4D4` | |
| White (bar, cards, form) | `#FFFFFF` | |
| Ink / muted | `#1A1816` / `#5C554B` | |
| Gold deep (small text on ivory) | `#80622F` | `#A9553A` |

### Buttons (Classic → Button → Design)
- **Pill:** corner radius 50 (max), no border (Primary) or 1 px border (Ghost).
- *Primary (on dark):* fill button color, text per table, Lato Bold 12 px caps, spacing ≈ 200, label ends with " →". Hover → hover color.
- *Ghost (on dark):* transparent, 1 px `#F3ECDD` at 50 %, text cream → hover fill cream, text black.
- *Dark (on ivory):* fill `#1A1816`, text cream → hover = button color.
- Size 170 × 46 (hero buttons), header button 160 × 40.
- **Round arrow** (tiles): 42 × 42 button/shape, radius 50, fill button color, text "→".

### Shapes & shadows
- Images / banners: **corner radius 16**. Shadow only on the floating bar and the page-top banners: x 0, y 14, blur 44, 14 % `#140F0A`.
- Gold rule (decor): 48 × 2 (28 × 2 inside the info bar).
- **Use a Classic "Strip Divider" (wave/curve) if offered** (Strip → Divider). If not, place the supplied SVGs (below) as full-width images at the strip edge.

---

## 2. Supplied assets (`assets/` folder)
| File | Use |
|---|---|
| `hero-arch.png` (1080×720, transparent corners) | Your hero photo, **uncropped**, already clipped into the arch shape. Upload and place — no Wix mask needed. |
| `arch-gold-outline.svg` / `arch-sage-fill.svg` | Arch shape behind the hero photo (Brand = outline, Reference = sage fill). |
| `wave-ivory.svg` (1440×110) | Place at the **bottom** of each dark strip: ivory wave into the page. |
| `wave-ivory-flipped.svg` | Place at the **top** of the closing band. |

(SVG waves are the fallback if the strip divider isn't available. Set wave images to *stretch to full width*, height 110, no shadow. Make sure the strip underneath is exactly the dark color so the join is seamless.)

---

## 3. Header (shared, sits on the dark hero)

- Header strip: height **96**, fill = **dark** color, no border. Hero strip right below uses the same fill, so they read as one block.
- **Wordmark** "PURE HARMONY CHOIR": Playfair Display 21 px, caps, character spacing ≈ 200, cream. x 40, y 34. Link → Home. (Text only; the crest moves to the closing band because its black square can't blend into a non-black header.)
- **Menu:** x 350, y 28, w 400, h 40: HOME · ABOUT US · OUR SERVICES · CONTACT US. Lato 12 px, color `#E3DACB`, hover accent, **selected = cream + 1 px accent underline** (menu skin underline, or color only).
- **Button** "CONTACT US →" (Primary pill), x 780, y 28, 160 × 40 → Contact page.

---

## 4. HOME (strip order)
**Hero (dark) → Info bar → About lede → Tiles → Booking banner → Closing band/footer.**

### 4.1 Hero — height 640, fill dark (+ `wave-ivory.svg` at the bottom, y 530–640)
| Element | x | y | w × h | Spec |
|---|---|---|---|---|
| Eyebrow "FLORIDA • GEORGIA" | 40 | 30 | 300 × 18 | Lato Bold 11.5, spacing ≈ 340, accent |
| H1 "Pure Harmony **Choir**" (Choir in accent color) | 40 | 62 | 400 × 140 | Playfair 62, cream, line-height 1.05 → 2 lines |
| Tagline "THE LUXURY SOUND YOU DESERVE" | 40 | 228 | 400 × 20 | Lato Bold 13, spacing ≈ 340, cream |
| Button "ABOUT US →" → About | 40 | 282 | 160 × 46 | Primary |
| Button "OUR SERVICES" → Services | 214 | 282 | 160 × 46 | Ghost |
| Arch shape (svg, see §2) | 471 | 22 | 493 × 337 | **behind** the photo |
| Photo `hero-arch.png` | 440 | 50 | 500 × 333 | already arch-shaped, no crop |

Fade-in H1, tagline and photo. No overlay anywhere.

### 4.2 Info bar — white box x 40, y 560, w 900, h 120 (radius 16, shadow) 
It straddles the wave: **if Classic lets you drop it across the strip boundary, do** (it overflows into the ivory strip); **otherwise** keep the bar fully inside the ivory strip below and give that strip 60 px extra top padding.
Four equal columns (225 px) separated by 1 px `#D8CDB8` lines. Each: gold rule 28 × 2 (y +26) → title Playfair 21 px (y +42) → sub-line Lato 13 px `#5C554B` (y +90). Whole column links → Our Services.
1. **Artistic Performance** — *Live Vocalists & Music Curation · Musical Direction*
2. **Ceremonial Elegance** — *Wedding Officiants · Memorial Ceremony Leadership*
3. **Cinematic Capture** — *Photography · Videography*
4. **Custom Event Design** — *Luxury Event Stationery · Visual Branding & Monograms*

### 4.3 About lede — ivory, height 500 (starts below the bar)
Eyebrow "ABOUT US" (gold deep) · lede (verbatim, v1 §4.3) in Playfair *Italic* 36, centered, w 780 · rule · "ABOUT US →" Dark pill.

### 4.4 Tiles — ivory, height 760
2 × 2 grid, tiles **440 × 330** (4:3), gap 20, x 40 / 500, y 40 / 390. Each = image (radius 16) + caption bar (box 440 × 74 at the bottom, fill `#0C0907` at 62 % opacity, flat — no gradient) + title (Playfair 28, cream, x +24) + round arrow (42 × 42, right aligned). Whole tile links.
| Tile | Photo | Crop | Links to |
|---|---|---|---|
| About Us | `about-banner.jpg` | focus right-center (singer) | About |
| Our Services | `services-main.jpg` | focus top-center | Services |
| Florida | `about-florida.jpg` | none | About |
| Georgia | `about-georgia.jpg` | none | About |

### 4.5 Booking banner — ivory, height 460
One rounded (16) container x 40, y 20, w 900, h 420, split in two:
- **Left 2/5 (x 40–400):** solid dark-color panel. Eyebrow "CONTACT US" (accent) · H2 "Booking Inquiry" (Playfair 54, cream, 2 lines) · "CONTACT US →" Primary pill · small "FLORIDA • GEORGIA" (accent, spacing ≈ 300).
- **Right 3/5 (x 400–940):** `contact-main.jpg`, focus right (shows the three right-hand singers; the text never covers a face).

### 4.6 Closing band = footer (shared, all pages) — height ≈ 760, fill dark (+ `wave-ivory-flipped.svg` at the top)
| Element | y | Spec |
|---|---|---|
| `gallery-2.jpg` (x 40, 440 × 330) and `gallery-3.jpg` (x 500, 440 × 330), radius 16 | 150 | 4:3, no crop |
| Crest `home-about.jpg`, 124 × 124, **radius 50 (circle)**, 1 px gold border, centered x 428 | 410 | The circle crop hides its black square on any dark color |
| "THE LUXURY SOUND YOU DESERVE" | 560 | Lato Bold 12, spacing ≈ 380, accent, centered |
| Rule 48 × 2, centered | 592 | gold |
| Links HOME · ABOUT US · OUR SERVICES · CONTACT US | 622 | Lato Bold 11.5 caps, `#CFC6B4`, ~40 px apart |
| Hairline 1 px `#FFFFFF` at 12 % | 686 | x 40–940 |
| **© Pure Harmony Choir, LLC 2024-2026** | 708 | Lato 13, `#8F8777` |

---

## 5. ABOUT US — **Dark title block → floating banner → Manager → Locations → Description → Closing band**
- **Title block** (header + this strip share the dark fill): strip height 230 + wave. Eyebrow "FLORIDA • GEORGIA", H1 "About Us" (Playfair 72, cream, centered, y 40).
- **Floating banner:** `about-banner.jpg` x 40, w 900, **h 420**, radius 16, soft shadow, focus right-center; overlaps the wave by ~110 px (same fallback as §4.2).
- **Manager** (ivory, h 560): portrait `about-manager.png` x 40, y 80, 380 × 351, radius 16 · "Leolen Newsome" Playfair 48 (x 480) · "MANAGER" eyebrow · rule · paragraph (v1 §5.3).
- **Locations** (ivory deep, h 480): `about-florida.jpg` x 40, 436 × 291; `about-georgia.jpg` x 504, 436 × 291; radius 16; each with a caption bar (62 % dark, flat) at the bottom: "FLORIDA" / "GEORGIA" in Playfair 28, cream, spacing ≈ 200.
- **Description** (ivory, ≈ 700): column x 130, w 720. Opening sentence Playfair 29 in **ink** (not grey) → rule → two Lato paragraphs `#5C554B` (text in v1 §5.5).

## 6. OUR SERVICES — **Dark title block → floating banner → 2×2 cards → Contact button → Closing band**
- Title block as §5 ("Our Services").
- Floating banner: `services-main.jpg`, w 900, h 420, radius 16, shadow, focus top-center.
- **Cards** (ivory, h ≈ 900): 2 × 2, each **437 × ~380**, x 40 / 503, gap 26; fill `#FFFFFF`, radius 16, soft shadow (y 10, blur 34, 8 %), **3 px gold top border** (add a 437 × 3 gold box on the card's top edge), inner padding 40. Category title Playfair *Italic* 32 → rule → two entries (title Playfair SemiBold 19, body Lato 15 `#5C554B`; 28 px between). All text verbatim, v1 §6.3. Order: Artistic (TL), Ceremonial (TR), Cinematic (BL), Custom (BR).
- **"CONTACT US →"** Dark pill, centered, 56 px below the cards.

## 7. CONTACT US — **Dark title block → floating banner → Inquiry + form → Closing band**
- Title block as §5 ("Contact Us").
- Floating banner: `contact-main.jpg`, w 900, h 420, radius 16, focus center (all five faces in frame).
- **Left column** x 40, w 310: H2 "Booking Inquiry" Playfair *Italic* 34 · rule · intro paragraph (v1 §7.3, verbatim).
- **Right column** x 410, w 530: white panel (radius 16, soft shadow, padding 48) behind the **existing form — restyle, don't rebuild.** Inputs: transparent, bottom border 1 px `#B9AD94` (focus gold deep), text area 1 px border radius 10, labels Lato Bold 13, options Lato 14.5 `#5C554B`, checkboxes/radios in the button color. Submit = Dark pill "SUBMIT".

---

## 8. Mobile Editor (390 px)
Follow v1 §9 plus:
- Header: wordmark 17 px left, hamburger right; header button hidden (CTA lives in the hero).
- Hero: eyebrow, H1 **44 px** centered, tagline 10 px, buttons stacked (230 × 46); photo `hero-arch.png` full width 350 × 233 (shrink the arch outline to match, or drop it); wave 60 px tall.
- Info bar: **2 × 2** grid (each 175 wide), no overflow onto the wave — keep it inside the ivory strip.
- Tiles: single column, 350 × 262; caption bar 60 px high; title 24 px.
- Booking banner: stack — photo on top (350 × 220), dark panel below (title 38 px).
- Closing band: photos stacked; wave 60 px.
- Cards, locations, manager: single column; floating banners 240 px high.
- Body 16 px; nothing under 14 px.

## 9. v3-specific QA
- [ ] Hero strip and header strip are the identical dark color (no seam).
- [ ] Wave joins show no gap or color band (zoom to 200 % on the join).
- [ ] The arch outline sits behind the photo, not on top of it.
- [ ] Crest in closing band is circular, no black square visible.
- [ ] No text is placed over a person's face (Booking banner uses a solid panel).
- [ ] Lede on Home and About are ink-colored (not grey).
- [ ] Palette used consistently: pick Brand **or** Reference, don't mix.
- Plus v1 §12.
