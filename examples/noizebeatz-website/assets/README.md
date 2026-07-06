# Assets

Drop your files here — the site picks them up automatically:

| File | Where it appears | Notes |
|---|---|---|
| `studio-loop.mp4` | "The Studio Above The City" section, full-bleed background | The city-overlook loop (Higgsfield job `52d35e9c…`, or its 4K upscale). Autoplays muted and loops; a dusk gradient shows until the file exists. |
| `portrait-loop.mp4` | About section, gold-cornered frame (video) | The console knob-twist orbit clip (job `11964653…`) or any portrait clip. Takes priority over `portrait.jpg`. |
| `portrait.jpg` | About section, gold-cornered frame (still) | The studio portrait (mixing console shot). Portrait orientation, ~1200px wide. Until a file exists, the N\|B monogram placeholder shows instead. |
| `og-cover.jpg` | Social link previews (not on the page) | 1200×630. The red NOIZE BEATZ banner art crops well. Also update the `og:image` URLs in `index.html` to your live domain. |

Tip: for web backgrounds, re-encode the mp4s to ~2–4 Mbps H.264 (the 4K
masters are for socials/press; a 1080p web copy keeps the page fast).

The hero banner itself (headphones, waveform, skyline) is drawn in code —
no image file needed — but you can swap in the real banner art as a CSS
`background-image` on `.hero` if you prefer the original render.
