# Adding YouTube clips ("Sample Our Music") — Wix Classic

Works with any of the three designs. The v3 mockup (`mockup-v3.html`, Home page, "Sample Our Music") shows the look; the slides there are **placeholders**.

## Where it goes
A section on the **Home page**, between the photo tiles and the Booking Inquiry banner — so no new page and no change to your page names. If you later want a page of its own, add one called whatever you like; the same section drops straight in. The heading words "Listen" / "Sample Our Music" are my suggestion, taken from how you described it — change freely.

## Which method? (pick one)

| | Method | Visitors can scroll through | When you add new clips | Look |
|---|---|---|---|---|
| **A — recommended** | **YouTube playlist embed** (HTML iframe) | Yes — YouTube's own next/previous + playlist list | **Just add the video to your YouTube playlist. Nothing to edit in Wix.** | YouTube player (red/black controls), framed in our rounded container |
| **B** | **Wix Pro Gallery, Slider layout, with video items** | Yes — arrows + swipe, one clip per slide | Open Manage Media → add the new YouTube link | Most on-brand (custom arrows, captions) |
| **C** | **Slideshow strip** (Add → Strip → Slideshow), one Video Player per slide | Yes — arrows | Add a slide, change its video link | Fully custom, most manual |

### Method A — playlist embed (easiest to maintain)
1. On YouTube, create a **playlist** of your clips (YouTube Studio → Content → Playlists). Set it to *Public* (or *Unlisted*). Make sure each video has **Allow embedding** on (Studio → video → Show more).
2. Copy the playlist ID: it's the part after `list=` in the playlist URL.
3. In Wix: **Add (+) → Embed Code → Embed HTML → "Code" → paste:**
   ```html
   <iframe width="100%" height="100%"
     src="https://www.youtube-nocookie.com/embed/videoseries?list=YOUR_PLAYLIST_ID"
     title="Pure Harmony Choir — sample our music"
     frameborder="0" loading="lazy"
     allow="accelerometer; clipboard-write; encrypted-media; gyroscope; picture-in-picture"
     allowfullscreen></iframe>
   ```
4. Size the embed **900 × 506** (16:9) at x 40 on the grid, inside the ivory-deep strip, under the heading. Round the corners: wrap it in a box with corner radius 16 (embeds themselves can't round — set the box to the same size, send the embed in front, and give the box a 16 px radius + shadow; or leave the embed square).
5. Set the strip height to ≈ 760. Remove the placeholder reel/arrows from your Wix layout (they exist only in the mockup).

### Method B — Pro Gallery slider
1. **Add → Gallery → Pro Gallery** → pick the **Slider** layout.
2. **Manage Media → Add Media → Video** → add your YouTube link (YouTube/Vimeo links are supported; if your editor version only lists "Upload video", use Method A).
3. Layout settings: item size ≈ **400 × 225 (16:9)**, spacing 22, corner radius 16, arrows ON (style: round, button color, 46 px), swipe ON, *Autoplay off*, *Item click → plays video / expands*.
4. Titles: add a title under each item if you want "Song title" captions (Playfair 22 px).
5. Place at x 40, w 900; leave the right edge to bleed so the next clip peeks in (that's what tells visitors it scrolls).

### Method C — Slideshow strip
Add → Strip → Slideshow → in each slide add **Add → Video & Music → Video Player (YouTube)** and paste the link. Style the slideshow arrows round, 46 px, button color. Use only if A and B don't suit; it's the most work per new clip.

## Good practice
- **Never autoplay.** Set autoplay OFF everywhere.
- Mobile: re-check in the **Mobile Editor** — the player should be full content width (350 × 197), and gallery slides ≈ 84 % wide so the next clip peeks in.
- Use clean video titles/thumbnails on YouTube — they show in the embed.
- Uploading to your own YouTube channel means the clips also work elsewhere (social, email).
- Embeds load a third-party player; if you serve EU visitors, make sure your cookie/consent banner (Wix Settings → Cookie consent) is on. Using `youtube-nocookie.com` (as above) limits tracking until a clip is played.
- Don't put the section on a page that doesn't need it — Home is enough.

## Using the section in v1 / v2
Copy the same build onto the Home page of the chosen design. Colors: ivory-deep strip `#ECE4D4`, heading Playfair 44 px, eyebrow Lato Bold 11.5 px gold-deep. (v1/v2: square corners if you keep their style — set radius 0 and arrows square.)
