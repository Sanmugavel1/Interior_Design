# Sri Sankalp Interio — Website Demo

A premium static demo website for **Sri Sankalp Interio**, an interior design
studio in Mogalrajapuram, Vijayawada, Andhra Pradesh.

This is a single self-contained `index.html` (all CSS/JS inline, images
embedded as data URIs) — no build step, no backend. It's a visual/UX demo
built for a client presentation, not a production site.

## Structure

- Hero, **Walkthrough** (cinematic scroll-through-the-home), About, Services,
  Project Gallery (filterable), Design Collection, Before/After, Process,
  Why Us, Instagram showcase, Testimonial placeholder, Contact, Footer.

### Walkthrough section

A scroll-pinned sequence (`#walkthrough`) that dolly-zooms and cross-fades
through five rooms (Foyer → Living Room → Kitchen → Bedroom → Study) as the
visitor scrolls, giving the feel of walking through a finished space. It's
plain CSS `position:sticky` + a `requestAnimationFrame` scroll listener —
no animation library, nothing external. It reuses the studio's own project
photography already embedded in the page (via the `projects` array in the
script), so the room sequence is real Sri Sankalp work, not stand-in stock.

Replace it with a true single-project tour once the client supplies a
room-by-room shoot of one finished home: swap the five `projects[n]`
references in the `rooms` array (search for "walkthrough: scroll-through-
the-home" in the script) for images from that one project, in walking
order. Respects `prefers-reduced-motion` (falls back to a plain crossfade,
no zoom).
- Project names, gallery imagery, and contact details are placeholders —
  search the file for `REPLACE:` comments marking where real client content
  (project photography, phone/email, testimonials) should go.
- Stock photography sourced from Unsplash (free-to-use license) stands in
  for real project photos until the client supplies their own portfolio.

## Local preview

Just open `index.html` in a browser — no server required.

## Deploy

Static hosting only. Works as-is on Vercel, Netlify, GitHub Pages, etc.
