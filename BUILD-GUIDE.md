# Pure Harmony Choir — Wix Classic Editor Build Guide

Companion to `mockup.html` (open it in a browser; click the nav to see all four pages; resize the window to see the mobile layout).
All original photos are saved in `images/` under readable names. **All copy below is verbatim from the live site — nothing was added or rewritten.**

---

## 0. Decisions to confirm before you build

| # | Item | What I did | Your call |
|---|------|-----------|-----------|
| 1 | **Hero treatment** | The hero photo is shot on a pure-white (`#FFFFFF`) studio backdrop. A dark overlay would turn it muddy grey, so the hero is a **light, seamless editorial hero** (white strip, charcoal type, photo melting into the page). Dark is used for the band beneath and the footer. | Say so if you'd rather have a dark hero; it would need a different crop. |
| 2 | **Typo on live site** | Home shows "FLORDIA \| GEORGIA". Your brief says FLORIDA, so the mockup uses **FLORIDA \| GEORGIA**. | Confirm. |
| 3 | **Home page is thin** | Live Home has only: logo, title, tagline, location, an "About Us" link and 3 gallery photos. To avoid a sparse page I **reused the first sentence of the About page verbatim** (the "Based in West Palm Beach…" line) in the Home "About Us" band. | Delete that sentence if you want Home to carry zero reused copy; the band still works with just the photo + button. |
| 4 | **"Search" in the menu** | About/Services/Contact have a Search item in the menu. It isn't a page, and it clutters the nav. Mockup omits it. | Keep it if you use it. |
| 5 | **Contact details** | The live Contact page has **no phone, email or address** — only the Booking Inquiry form. I added none. | If you want direct contact info shown, supply it. |
| 6 | **Wix ad banner** | "This website was built on Wix" bar at the top of every page. Only removable by upgrading to a paid Premium plan + connecting a domain. It will break the premium look until removed. | — |
| 7 | **Tab titles** | Live tab titles are "HOME \| My Site 29" etc. Set real ones: Pages → ⋯ → SEO basics (e.g. "Home \| Pure Harmony Choir"). | — |

---

## 1. Classic Editor reality check (read first)

- Classic Editor is **not fluid**. Desktop = a fixed **980 px grid**; strips stretch edge-to-edge, content stays on the grid. Phones get a **separate Mobile Editor layout** (section 9). Tablets/laptops simply see the desktop layout scaled to fit — so design the desktop at 980 and it holds everywhere above phone size.
- Grid used below: **content x = 40 → 940 (900 wide)**. All X/Y values are measured inside the 980 canvas; Y is from the top of the strip.
- Full-width photography is done with **Strip backgrounds** (Strip → Change Strip Background → Image → Scaling *Fill* or *Fit* + Position). That is the one reliable way to get edge-to-edge images with controlled crops in Classic.
- Rectangles with **0 corner radius, transparent fill, 1 px border** (Add → Shapes → Box, or Boxes & Strips → Box) make the gold keyline frames.

---

## 2. Site Design (do this first — everything inherits it)

### Colors (Site Design → Colors → Customize)
| Role | Hex | Use |
|------|-----|-----|
| Ivory | `#F6F1E7` | Main page/strip background |
| White | `#FFFFFF` | Header, hero strips |
| Charcoal | `#1E1C1A` | Headings, button fill, text |
| Soft black | `#0B0A09` | Dark bands, footer |
| Gold (decor) | `#B8935A` | Rules, keylines, frames, button hover |
| Gold deep | `#8A6A36` | Small gold text on ivory (passes contrast) |
| Gold light | `#D2B27A` | Gold text on dark |
| Muted text | `#5E574E` | Body copy |
| Hairline | `#DCD2BF` | Divider lines on ivory |
| Hairline dark | `#2E2A25` | Divider lines on dark |

Gold is **never** used for small text on ivory (too low contrast) — use Gold deep there.

### Fonts (Site Design → Text → edit each style)
| Style | Font | Spec |
|-------|------|------|
| Page title (H1) | **Cormorant Garamond** Light (Regular if Light isn't listed) | 80–96 px, charcoal, centered, line-height 1.05 |
| Section / category title (H2) | Cormorant Garamond Regular | 42–54 px |
| Item title (H3) | Cormorant Garamond Medium | 26 px |
| Lede / pull text | Cormorant Garamond Regular or *Light Italic* | 30–34 px, line-height 1.3 |
| Body | **Montserrat** Regular | 15 px, line-height 1.85, `#5E574E` |
| Eyebrow / labels | Montserrat Medium, caps | 12 px, **character spacing ≈ 280**, Gold deep |
| Nav, buttons | Montserrat Medium, caps | 12 px, character spacing ≈ 200 |

Cormorant is thin — **never below 24 px**. Body copy is always Montserrat.

### Buttons (Site Design → Buttons, or per button → Design)
- **Square corners (radius 0).** No shadows, no pills, no gradients.
- *Primary:* fill `#1E1C1A`, text `#F6F1E7`, no border. Hover: fill `#B8935A`, text `#0B0A09`. Transition ~0.35 s.
- *Secondary:* transparent fill, 1 px border `#1E1C1A`, text `#1E1C1A`. Hover: fill charcoal, text ivory.
- *On dark:* transparent, 1 px border `#B8935A`, text `#D2B27A`. Hover: fill gold, text `#0B0A09`.
- Standard size: 170 × 50 px, 12 px Montserrat Medium caps.

### Frame recipe (used on several photos)
Photo at (x, y, w, h) → add a transparent 1 px `#B8935A` box at **(x+16, y+16, w, h)** and send it **behind** the photo. Result: a gold keyline offset down-right.

---

## 3. Header (shared, all pages)

- Header strip: height **88**, fill `#FFFFFF`, bottom border 1 px `#DCD2BF` (Header → Design → Border bottom). Show on all pages. Fixed position is fine at this height.
- **Logo** `images/logo.jpg` (gold crest on white — the white matches the header, so it is seamless): 62 × 62 at x 40, y 13. Link → Home.
- **Wordmark** text "PURE HARMONY CHOIR": Cormorant Garamond Medium 20 px, caps, character spacing ≈ 240, charcoal. x 118, y 31. Link → Home.
- **Menu**: one Horizontal Menu, x 540, y 24, w 400, h 40, **no background, no borders**. Items exactly: HOME · ABOUT US · OUR SERVICES · CONTACT US (remove Search). Montserrat Medium 12 px, charcoal; hover text Gold deep. **Active page:** use the menu skin's selected-state underline/line in `#B8935A` if your skin offers one; otherwise set the selected state text to Gold deep + a 1 px bottom border. *(Wix menus have no letter-spacing control — if the nav looks tight, bump the font to 12.5 and increase item spacing/padding; do not replace the menu with text links, or the mobile hamburger breaks.)*

---

## 4. HOME

Strip order: **Hero title → Hero photo → About band → Dark gallery band → Footer.**

### 4.1 Hero title strip — height 430, fill `#FFFFFF`
| Element | x | y | w × h | Spec |
|---------|---|---|-------|------|
| H1 "Pure Harmony Choir" | 40 | 70 | 900 × 110 | H1 style, ~96 px, centered |
| Line (horizontal) | 462 | 206 | 56 × 1 | `#B8935A` |
| Tagline "THE LUXURY SOUND YOU DESERVE" | 40 | 232 | 900 × 24 | Montserrat Medium 14 px caps, char. spacing ≈ 320, charcoal, centered |
| Location "FLORIDA \| GEORGIA" | 40 | 268 | 900 × 20 | Montserrat Medium 12 px, spacing ≈ 300, `#5E574E`, centered |
| Button "ABOUT US" → About Us page | 305 | 330 | 170 × 50 | Primary |
| Button "CONTACT US" → Contact Us page | 505 | 330 | 170 × 50 | Secondary |

### 4.2 Hero photo strip — height 780, fill `#FFFFFF`
- Background image `images/hero.jpg` (1920×1280), **Scaling: Fit**, position **bottom center**. Parallax off.
- Because the photo's backdrop is pure white and the strip is pure white, the picture appears to float on the page with **no crop and no visible edges**. (If your Fit option isn't available, use a stretched-full-width image element with Display = Fit on a white strip.)
- Combined with 4.1 the hero is ~1210 px tall; the title, tagline, CTAs and all four faces are visible on a standard laptop screen.
- **Do not add an overlay.**

### 4.3 About band — height 620, fill `#F6F1E7`
| Element | x | y | w × h | Spec |
|---------|---|---|-------|------|
| Frame box (see recipe) | 56 | 166 | 540 × 405 | gold keyline, behind photo |
| Photo `gallery-1.jpg` (4:3, no crop) | 40 | 150 | 540 × 405 | |
| Eyebrow "ABOUT US" | 640 | 178 | 300 × 18 | Eyebrow style, Gold deep |
| Lede (see decision #3): *Based in West Palm Beach, FL, Pure Harmony Choir is the ultimate choice for those seeking an unforgettable, luxury musical experience for their special occasion.* | 640 | 210 | 300 × ~270 | Cormorant Garamond Light Italic 30 px, line-height 1.3, charcoal |
| Button "ABOUT US" → About Us | 640 | 505 | 170 × 50 | Primary |

### 4.4 Dark gallery band — height 830, fill `#0B0A09`
| Element | x | y | w × h | Spec |
|---------|---|---|-------|------|
| Frame box | 385 | 80 | 210 × 210 | 1 px `#B8935A`, transparent |
| Crest `home-about.jpg` (the black-background logo — it is **only 400 px**, keep ≤ 190) | 395 | 90 | 190 × 190 | |
| "FLORIDA \| GEORGIA" | 40 | 316 | 900 × 20 | Montserrat Medium 12 px, spacing ≈ 340, `#D2B27A`, centered |
| Photo `gallery-2.jpg` (3 women, garden rail) | 40 | 440 | 360 × 270 | |
| Photo `gallery-3.jpg` (5 men, bridge) | 436 | 356 | 504 × 378 | |

The left photo sits 84 px lower than the right — that deliberate stagger is what keeps this from reading as a generic 2-up gallery. Use plain image elements (not a Pro Gallery) so the positions stay exact; set click action to *None* (or *Zoom* if you want enlargement).

---

## 5. ABOUT US

Strip order: **Title → Banner photo → Manager → Locations (dark) → Description → Footer.** (Same order as the live page.)

### 5.1 Title strip — height 250, fill ivory
H1 "About Us" (x 40, y 90, w 900, ~80 px, centered) · gold line 56 × 1 at x 462, y 200.

### 5.2 Banner strip — height 560
Strip background `images/about-banner.jpg` (vocalist singing), Scaling **Fill**, position **Center**. The singer's face and microphone stay in frame at all desktop widths. No overlay, no text.

### 5.3 Manager strip — height 640, fill ivory
| Element | x | y | w × h | Spec |
|---------|---|---|-------|------|
| Frame box | 56 | 126 | 400 × 369 | gold keyline |
| Portrait `about-manager.png` | 40 | 110 | 400 × 369 | The amber backdrop echoes the gold palette |
| H2 "Leolen Newsome" | 520 | 130 | 420 × 60 | Cormorant Garamond Regular 50 px |
| Eyebrow "MANAGER" | 520 | 200 | 300 × 18 | Gold deep |
| Line | 520 | 238 | 56 × 1 | gold, left aligned |
| Body (below) | 520 | 262 | 420 × ~230 | Montserrat 15 px, `#5E574E` |

Body, verbatim: *Passionate about music and leadership, our manager is dedicated to keeping every performance and event organized, professional, and impactful. From coordinating rehearsals and planning, she helps create meaningful experiences that inspire audiences and strengthen community through music. Her commitment to excellence, creativity, and teamwork helps ensure every event leaves a lasting impression.*

### 5.4 Locations strip — height 520, fill `#0B0A09`
| Element | x | y | w × h |
|---------|---|---|-------|
| `about-florida.jpg` | 40 | 80 | 440 × 280 |
| Line `#2E2A25`, 1 px | 40 | 396 | 440 × 1 |
| "FLORIDA" caption | 40 | 412 | 440 × 40 |
| `about-georgia.jpg` | 500 | 80 | 440 × 280 |
| Line | 500 | 396 | 440 × 1 |
| "GEORGIA" caption | 500 | 412 | 440 × 40 |

Captions: Cormorant Garamond 30 px, caps, character spacing ≈ 300, `#F3ECDD`, centered. No overlays on the photos.

### 5.5 Description strip — fill ivory, height ≈ 760
One text column, x 140, w 700:
1. *Based in West Palm Beach, FL, Pure Harmony Choir is the ultimate choice for those seeking an unforgettable, luxury musical experience for their special occasion.* — Cormorant Garamond Regular 30 px, line-height 1.38, charcoal.
2. Gold line (56 × 1, left) 30 px below.
3. *Pure Harmony Choir delivers a sophisticated and professional blend of soulful vocals and uplifting harmonies, designed to inspire and delight your guests. While originally comprised of family members united by a deep musical bond, the choir has gracefully expanded to include a hand-selected circle of extended family, and close friends—each bringing their own excellence, heart, and experience to the stage. This thoughtful growth allows Pure Harmony Choir to provide outstanding vocalists and musicians throughout both Florida and Georgia.*
4. *Whether you're hosting an intimate wedding or a grand celebration, Pure Harmony Choir offers a refined ensemble of five singers with a pianist to a dynamic choir of 10 singers, a pianist, and a drummer.*

Paragraphs 3–4: Montserrat 15 px, `#5E574E`, 26 px between paragraphs. If you'd rather keep the manager *after* the description, swapping 5.3 and 5.5 works equally well.

---

## 6. OUR SERVICES

### 6.1 Title strip — height 250, ivory
H1 "Our Services" + gold line (same as 5.1).

### 6.2 Photo strip — height 560
Background `images/services-main.jpg`, Scaling **Fill**, position **Top center**. (Its backdrop isn't pure white — it has a soft vignette — so it must run edge-to-edge as a crop, not float like the hero.)

### 6.3 Services strip — fill ivory
Four rows, **no cards, no icons, no rounded boxes** — editorial two-column rows separated by hairlines.

Each row (height ≈ 350–390): hairline `#DCD2BF` across x 40 → 940 at the row top; **category title** left (x 40, y +64, w 300; Cormorant Garamond Regular 42 px, charcoal); **two service entries** right (x 380, w 560): title in Cormorant Garamond Medium 26 px, body in Montserrat 15 px `#5E574E`, with a hairline between the two entries (x 380 → 940). Add a closing hairline under the last row.

| Category (left) | Entry title | Body (verbatim) |
|---|---|---|
| **Artistic Performance** | Live Vocalists & Music Curation | Whether you're walking down the aisle or honoring a life well-lived, the right music transforms the moment. Our carefully selected vocalists and musicians deliver live, soul-stirring performances tailored to your event's tone and vision. |
| | Musical Direction | From intimate weddings to elegant gatherings, we offer custom arrangements, vocal blends, and curated sound experiences that enhance the emotional journey of your event. |
| **Ceremonial Elegance** | Wedding Officiants | Your ceremony should feel as personal as your love story. Our officiants specialize in crafting and delivering beautiful, tailored ceremonies that honor your unique journey with warmth, style, and grace. |
| | Memorial Ceremony Leadership | In times of remembrance, we offer more than words—we offer presence, poetry, and peace. Our team creates and delivers personalized tribute services that honor the life and legacy of your loved ones with heartfelt dignity. |
| **Cinematic Capture** | Photography | Our photographers specialize in timeless, editorial-style captures with an eye for authentic emotion, luxurious detail, and natural beauty. |
| | Videography | More than a recap—our films tell your story. We deliver cinematic, emotionally rich highlight reels and full-length features for weddings, memorials, and special occasions. |
| **Custom Event Design** | Luxury Event Stationery | Our design team creates sophisticated printed pieces including invitations, programs, signage, and menus. Each design is crafted to reflect your vision with elegance and intention. |
| | Visual Branding & Monograms | Add a signature touch to your event with custom monograms, logos, or cohesive visual design across all your printed and digital elements. |

### 6.4 CTA strip — height 280, fill `#0B0A09`
Button "CONTACT US" → Contact Us page, *on-dark* style, 170 × 50, centered (x 405, y 115).

---

## 7. CONTACT US

### 7.1 Title strip — height 250, ivory
H1 "Contact Us" + gold line.

### 7.2 Banner strip — height 520
Background `images/contact-main.jpg` (five singers performing), Scaling **Fill**, position **Center**. All five faces and microphones stay in frame.

### 7.3 Form strip — fill ivory, height set by form (≈ 2,300–2,500)
- **Do not rebuild the form** — open the existing one and restyle it, so every field, option and its logic stays exactly as is.
- Form panel: a box at x 90, w 800, fill `#FFFFFF`, 1 px border `#DCD2BF`, radius 0, behind the form.
- Heading "Booking Inquiry": H2, ~44 px, centered, + gold line below.
- Intro, verbatim: *Thank you for your interest in booking with Pure Harmony Choir for your upcoming event. Please kindly fill out the form below (be as detailed as you can) and we'll be in touch with a quote within 24-48 hours.* — Montserrat 15 px, `#5E574E`, centered, w 600.
- **Form styling (Design):** transparent input fill, **bottom border only** 1 px `#BFB39C` (focus `#8A6A36`), radius 0; text areas get a full 1 px border. Labels Montserrat Medium 12 px, charcoal. Checkbox/radio labels Montserrat 14 px `#5E574E`. Required asterisks stay. Submit button = Primary style, centered, 170 × 50 (live label "Submit").
- Keep every field/label exactly as on the live form (Name, Email, Phone Number, Type of Event, Date and Time of Event, hours, venue, reception place, indoor/outdoor, guest count, choir/instrument options, sound equipment, vision, Rosarrio Entertainment partner options, budget, accommodations, how did you hear). The mockup reproduces them all for visual reference.

---

## 8. Footer (shared) — height 380, fill `#0B0A09`
| Element | y | Spec |
|---------|---|------|
| "PURE HARMONY CHOIR" | 84 | Cormorant Garamond 28 px, caps, spacing ≈ 300, `#F3ECDD`, centered |
| "THE LUXURY SOUND YOU DESERVE" | 134 | Montserrat Medium 11 px, spacing ≈ 320, `#D2B27A`, centered |
| Links: HOME · ABOUT US · OUR SERVICES · CONTACT US (text elements linked to each page, ~40 px apart, centered) | 190 | Montserrat Medium 11 px caps, `#CFC6B4`; hover `#D2B27A` |
| Hairline `#2E2A25`, x 40 → 940 | 290 | |
| **© Pure Harmony Choir, LLC 2024-2026** | 316 | Montserrat 12 px, `#8E8676`, centered |

Nothing else — no invented company details.

---

## 9. Mobile Editor (390 px layout — build after desktop is final)

Open Mobile Editor and work top to bottom; Classic does not auto-adapt.
- **Header:** logo 40 px + wordmark at 14 px; hamburger menu on the right, menu panel fill `#FFFFFF`, items Montserrat 13 px.
- **Margins:** 20 px each side. Single column everywhere. Nothing overlaps; stack in this order: image, then text.
- **Hero:** H1 **44 px** (two lines is fine); tagline 11 px, spacing ≈ 260; location 11 px; buttons stacked, each ~230 × 48, 12 px apart. Photo strip: height **260**, Fit, so all four faces show.
- **Photos:** full content width (350), 4:3 or 3:2, height 262 / 233; frames offset by 8 px instead of 16 (or drop them if cramped). Home dark band: seal 150 px, then gallery-2 and gallery-3 stacked at 350 wide, no stagger.
- **Banner strips (About/Services/Contact):** height 280–300; Fill; same focal position.
- **Headings:** H1 46 px; lede 24 px; category titles 34 px; item titles 24 px. Body stays **15 px**, never smaller.
- **Services:** category title above its entries; hairline between entries.
- **Form:** fields full width, ≥ 44 px tall tap targets; form panel padding 20 px; submit 48 px high.
- **Footer:** stack centered; links in two rows; wordmark 22 px.
- Delete (hide) decorative-only elements that hurt mobile; never hide content.

---

## 10. Animation (sparing)
Animations panel (Classic): **Fade In, 0.8 s, once** on the H1s, hero photo and the major photos. Nothing else — no Reveal sweeps, parallax, zoom, spin or scroll-jacking. Hover effects: buttons (colour change, 0.35 s) and footer/nav link colour only. No image hover effects.

---

## 11. Images — placement, crops, alt text

| File (`images/`) | Live source | Size | Used for | Treatment | Alt text to set |
|---|---|---|---|---|---|
| `logo.jpg` | logo, all pages | 400² | Header | 62 px on white header | "Pure Harmony Choir crest" |
| `hero.jpg` | Home hero | 1920×1280 | Home hero strip | Fit, white, uncropped | "Four members of Pure Harmony Choir standing in a line, each with a hand on the shoulder of the singer in front" |
| `home-about.jpg` | Home (black logo version) | 400² | Home dark band | ≤ 190 px in gold keyline | "Pure Harmony Choir crest — The Luxury Sound You Deserve" |
| `gallery-1.jpg` | Home gallery | 1280×963 | Home About band | 4:3, uncropped, framed | "Four members of Pure Harmony Choir in black and white attire" |
| `gallery-2.jpg` | Home gallery | 1280×962 | Home dark band | 4:3, uncropped | "Three members of Pure Harmony Choir in black beside a garden railing" |
| `gallery-3.jpg` | Home gallery | 1280×962 | Home dark band | 4:3, uncropped | "Five members of Pure Harmony Choir in black on a garden bridge" |
| `about-banner.jpg` | About banner | 2048×1365 | About banner strip | Fill, center | "A Pure Harmony Choir vocalist singing into a microphone" |
| `about-manager.png` | About, manager | 1108×1023 | Manager portrait | ~400×369, framed | "Leolen Newsome, Manager" |
| `about-florida.jpg` | About location card | 1280×814 | Locations strip | 440×280 | "Four members of Pure Harmony Choir, Florida" |
| `about-georgia.jpg` | About location card | 1280×814 | Locations strip | 440×280 | "Members of Pure Harmony Choir at a garden gazebo, Georgia" |
| `services-main.jpg` | Services, below title | 1920×1280 | Services photo strip | Fill, top center | "A member of Pure Harmony Choir in a white shirt" |
| `contact-main.jpg` | Contact | 2048×1365 | Contact banner strip | Fill, center | "Five members of Pure Harmony Choir performing" |

Live alt text is currently "unnamed (4).jpg" etc.; replace as above (helps accessibility and SEO).
Re-upload the files from `images/` (they are the originals pulled from the Wix media URLs) or simply keep using the ones already in your Wix Media Manager — same files.

---

## 12. QA checklist

- [ ] Fonts set in Site Design, not per element (so new text inherits).
- [ ] No rounded corners, shadows, gradients or overlays anywhere.
- [ ] Gold only on lines, frames, button hovers; small gold text is always `#8A6A36` on ivory.
- [ ] Hero strips 4.1 and 4.2 both exactly `#FFFFFF` (use the eyedropper on the photo's backdrop to confirm no seam).
- [ ] Every paragraph matches the live site word-for-word (compare against section tables above).
- [ ] Footer reads exactly "© Pure Harmony Choir, LLC 2024-2026".
- [ ] Preview at 1920, 1440, 1280 and 1024 widths; then the Mobile Editor at 390 and 360 — no overlap, no clipped words.
- [ ] Button links: Home → About Us, Contact Us; Services → Contact Us.
- [ ] Submit a test inquiry through the restyled form.
- [ ] Premium plan + domain connected so the Wix ad bar is gone.
- [ ] Page SEO titles and alt text set.
