# Noize Beatz — Personal Website

Animated single-file personal website for **Noize Beatz — Music Producer**.
Open `index.html` in any browser, or drop it on any static host (Netlify, Vercel,
GitHub Pages, Squarespace code injection, cPanel). No dependencies, no build step.

## Design direction

Built from the official one-sheet: black + gold foil + cream, "Beats That Move
Culture." Inspired by tpain.com-style artist sites and the Squarespace music
template structure (hero → work → about → connect).

- **Palette** — ink black `#0C0906`, animated gold-foil gradient
  (`#F0D283 → #C9992E → #8A6516`), cream `#F0EBE1` for the pillars section
  (mirroring the one-sheet's light lower half). The hero uses the logo banner's
  world instead: chrome silver + signal red `#E8192C` on black, drawn live on
  canvas (red equalizer waveform, city skyline with twinkling windows, floor
  reflection) with the chrome/red beveled wordmark and headphone N|B mark.
- **Type** — massive gold-foil display with a continuous shimmer sweep, script
  face for taglines ("Beats That Move Culture.", "It's time to Create."),
  letterspaced caps for labels.
- **Motion** — hero wordmark rises in on load, drifting gold-dust canvas,
  two scrolling marquees, scroll-triggered section reveals, hover states on the
  singles grid. All motion respects `prefers-reduced-motion`.

## Content (from the one-sheet)

- Full bio, verbatim
- Three pillars: Proven Hitmaker / Sonic Versatility / Global Impact
- Produced singles: Pick A Side (Too $hort), Kinda Love (Teamarrr & D Smoke),
  Lemon & Lime (Elijah Connor), American Gold (TLC), Ah! Ah! (Jaydon & 310babii)
- Instagram @noizebeatz · Hi Rize Management

## SEO built in

- Semantic HTML5, keyword-rich H1/H2s, full meta description, canonical,
  Open Graph + Twitter cards, theme-color
- `Person` JSON-LD (music producer, worksFor Hi Rize Management, sameAs Instagram)
- `ItemList` of `MusicRecording` entries for all five produced singles

## AEO built in

- `FAQPage` JSON-LD plus a visible "Quick Answers" block written answer-first —
  the format AI answer engines (ChatGPT, Perplexity, Google AI Overviews) cite
- Quotable facts: credits list, Billboard №1 plaque, how-to-work-with steps

## Before going live — swap the placeholders

1. Drop `portrait.jpg` into `assets/` — the About frame displays it
   automatically (see `assets/README.md`)
2. `https://noizebeatz.com` → your real domain (canonical, OG, JSON-LD)
3. Singles grid: CSS-art covers → official artwork; link each card to
   Spotify / Apple Music / YouTube
4. `og-cover.jpg` → a 1200×630 share image (the banner art crops well)
5. Footer streaming links (Spotify / Apple Music / YouTube profiles)
6. `bookings@noizebeatz.com` → your real booking email
