# Anniversary Scrapbook

A single-page, responsive "digital scrapbook" anniversary gift. Plain HTML, CSS and JavaScript. No build step, no dependencies.

## Files
- `index.html` - the whole site (markup, styles, script)
- `audio/song.mp3` - the song (128 kbps)
- `images/photo-01.jpg ... photo-16.jpg` - compressed photos (max 860px)
- `anniversary-standalone.html` - same site with photos embedded, works as one file

## Run locally
Open `index.html` in a browser, or run `python3 -m http.server` in this folder.

## Customize (all in the `<script>` at the bottom of index.html)
- `CAP` - captions under each polaroid (same order as the photos)
- `NOTES` - title and text of the three story cards
- `CARDPIC` - which photo each story card shows (index into the photo list)
- `N` - the day counter value (currently 371)
- Song: replace `audio/song.mp3` (or change the path in `au.src`) and edit the title in `.player .n`
- Love letter: edit the text inside `#ltr`
- Hero photos: the three `data-i` values in `.stack`
- Colors: the CSS variables at the top of the `<style>` block (dark mode values included)

## Add or swap photos
Drop a new JPG in `images/`, add its path to the `IM` array in the script, and add a caption to `CAP`.

## Sections
Home (title, counter, illustration, photo stack), Our Story (3 cards), The Gallery, Love Letter (envelope reveal), plus a sticky music player at the bottom.

## Notes
- Fonts (Caveat, Patrick Hand) load from Google Fonts, with cursive fallbacks.
- Respects dark mode, reduced motion and phone safe areas.
- The sticky player plays `audio/song.mp3` (tap play; browsers block autoplay). Tap the progress bar to seek.
- Hosting: any static host works (GitHub Pages, Netlify, etc.).
