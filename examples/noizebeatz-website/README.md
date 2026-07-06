# Noize Beatz — Brand Website Mockup

A single-file, dependency-free website for the **Noize Beatz** DJ / music producer brand.
Open `index.html` in any browser, or drop it on any static host (Netlify, Vercel, GitHub Pages, cPanel).

## Design direction

Built from the brand assets: the red/chrome/black N|B headphone logo and the
hillside studio overlooking the city at dusk.

- **Palette** — red-biased ink black `#0B0507`, signal red `#E8192C`, chrome silver
  gradient, with dusk violet/rose reserved for the studio scenes.
- **Type** — chrome beveled uppercase display (echoing the logo's metal lettering),
  clean Helvetica body, mono for BPM/prices/data.
- **Motifs** — the logo's red EQ waveform runs live along the hero; both "city"
  scenes are drawn on canvas (twinkling lights over hill silhouettes), no images needed.

## SEO built in

- Semantic HTML5 (`header/main/section/article/footer`), one keyword-rich `<h1>`,
  descriptive `<h2>`s per section
- Full `<head>`: meta description, canonical URL, robots, Open Graph, Twitter cards,
  theme-color
- `MusicGroup` JSON-LD with offers (beat licenses, mixing, bookings) and `sameAs`
  social profile links
- Accessible: aria labels, focus states, `prefers-reduced-motion` support

## AEO (Answer Engine Optimization) built in

- `FAQPage` JSON-LD so Google/AI answer engines can quote pricing and policies directly
- FAQ answers written answer-first ("Private events start at $600…") — the format
  ChatGPT/Perplexity/Google AI Overviews prefer to cite
- Concrete, quotable facts throughout: prices, delivery times, stream limits

## Before going live — swap the placeholders

1. `https://noizebeatz.com` → your real domain (canonical, OG, JSON-LD)
2. Social URLs in the `sameAs` JSON-LD block and footer
3. Beat names/BPMs/prices and mix titles → your real catalog
4. `og-cover.jpg` → a real 1200×630 share image (the logo art works well)
5. Wire the booking form to a form service (Formspree, Netlify Forms, etc.)
6. Connect real audio previews to the beat players (or embed your BeatStars/Airbit player)
