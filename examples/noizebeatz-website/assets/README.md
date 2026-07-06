# Assets

Drop your files here — the site picks them up automatically:

| File | Where it appears | Notes |
|---|---|---|
| `hero-loop.mp4` | Landing hero, full-bleed background | The console knob-twist orbit clip (job `11964653…` / 4K master `3ee0a030…`). When present, it plays behind the NOIZE BEATZ wordmark and CTAs (the headphone mark and drawn skyline hide automatically); until then the 3D banner scene shows. A hosted preview URL is wired as a second source until you drop the file in. |
| `portrait-loop.mp4` | About section, gold-cornered frame (video) | The console knob-twist orbit clip (job `11964653…`) or any portrait clip. Takes priority over `portrait.jpg`. |
| `portrait.jpg` | About section, gold-cornered frame (still) | The studio portrait (mixing console shot). Portrait orientation, ~1200px wide. Until a file exists, the N\|B monogram placeholder shows instead. |
| `og-cover.jpg` | Social link previews (not on the page) | 1200×630. The red NOIZE BEATZ banner art crops well. Also update the `og:image` URLs in `index.html` to your live domain. |

Tip: for web backgrounds, re-encode the mp4s to ~2–4 Mbps H.264 (the 4K
masters are for socials/press; a 1080p web copy keeps the page fast).

The hero banner itself (headphones, waveform, skyline) is drawn in code —
no image file needed — but you can swap in the real banner art as a CSS
`background-image` on `.hero` if you prefer the original render.
