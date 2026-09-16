# The Big Five-O — a birthday timeline site

A 6-page template: a cover page plus five "chapter" pages, one per era of your
dad's life. Every page is plain HTML/CSS, no build tools needed.

## Files

- `index.html` — cover page with links to all five chapters
- `01-childhood-teens.html` — 1976–1994, age 0–18
- `02-twenties.html` — 1996–2005
- `03-thirties.html` — 2006–2015
- `04-forties.html` — 2016–2025
- `05-turning-fifty.html` — 2026, the birthday finale (includes a
  "messages from family & friends" section)
- `style.css` — shared styles for every page. Each era has its own color
  palette (70s/80s harvest tones → Y2K brights → indie-blog warmth → modern
  bold → gold birthday finale) so the site visually travels through time as
  you click through chapters.

## To customize

1. **Find and replace `[Dad's Name]`** across all files with his actual name
   (it's in `index.html`'s title, hero, and footer).
2. **Look for ✏️** — every one marks a spot with placeholder text meant to be
   swapped for a real story, photo caption, or memory. The italic "Prompt:"
   lines are just idea-starters; delete them once you've written the real
   text.
3. **Adding real photos** — each photo placeholder looks like this:
   ```html
   <figure class="photo" style="--rotate:-3deg">
     <div class="photo__frame" style="--ratio:4/5">
       <svg>...</svg>
       <span class="photo__hint">Replace with ...</span>
     </div>
     <figcaption>Caption</figcaption>
   </figure>
   ```
   Replace the whole `<div class="photo__frame">...</div>` with:
   ```html
   <div class="photo__frame has-image" style="--ratio:4/5">
     <img src="photos/dad-1982.jpg" alt="Dad at the lake, 1982">
   </div>
   ```
   Put your image files in a `photos/` folder next to the HTML files.
   `--ratio` controls the frame's aspect ratio (`4/5` portrait, `1/1` square,
   `16/9` wide) — set it close to your photo's real shape so it isn't cropped
   awkwardly.
4. **Adjust the years** if 1976–2026 isn't quite right — search each page for
   the year ranges in the `hero__meta` line and the chapter cards on
   `index.html`.
5. **Add or remove photos** in the gallery grids by copying/deleting a
   `<figure class="photo">...</figure>` block. The grid re-flows
   automatically.
6. **Messages section** (chapter 5 only) — add one `.message-card` per person
   you want to include; copy the existing block and change the name and text.

## To view it

Just double-click `index.html` to open it in a browser — no server needed.

## To publish it

The easiest free options:
- **Netlify Drop** (netlify.com/drop) — drag the whole folder in, get a link
  instantly.
- **GitHub Pages** — push the folder to a GitHub repo and enable Pages in
  settings.

Both give you a shareable link you can text or email on the big day.
