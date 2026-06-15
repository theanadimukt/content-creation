# Skill: thumbnail-brief

## Purpose
Iterate or fully redesign the thumbnail brief for an episode.
Covers YouTube thumbnail AND Instagram Reel cover frame.
Use when the brief from write-script needs a different visual direction or more Canva detail.

## Input required
- Path to episode directory
- Optional: specific direction or constraint (e.g. "text-only variant", "use my face", "darker palette")

## Output
Update thumbnail.md in the episode directory in place.
Do not touch youtube.md, instagram.md, or x-post.md.

## Brief structure to output

### YouTube Thumbnail

Generate 2 variants. User picks one.

**Variant A**
- **Main text:** 5 words max, punchy, high contrast — left side placement
- **Sub text:** optional, smaller font, right side, max 6 words
- **Emotion:** face expression if appearing (e.g. "surprised", "pointing left", "serious / deadpan")
- **Background:** simple suggestion (solid colour, blurred desk, dark gradient, split panel)
- **Palette:** 3 hex values — dominant / accent / text
- **Layout note:** brief call-out if face + text split, or text-only, or face-only
- **Mobile legibility check:** all text must be readable at 120px wide (mobile feed)
- **Canva start:** template category to start from + font pairing (e.g. "YouTube Thumbnail — Dark Modern" / "Bebas Neue headline / Inter body")

**Variant B**
- Same fields, different visual approach — vary layout or emotion, not just colour

---

### Instagram Reel Cover

Instagram Reel cover is a static frame shown in the grid before play.
Treat like a mini-poster: must work as standalone image, no motion context.
Keep all key elements in top 70% of frame — grid preview crops to 1080×1350.

Generate 2 variants. User picks one.

**Cover Variant A**
- **Headline text:** max 6 words, large, centre or top — this is the grid hook
- **Sub text:** optional, 1 line, smaller — adds context (e.g. "EP 01", series label, topic tag)
- **Visual treatment:** [e.g. solid colour bg + bold type / face photo + text overlay / screenshot crop + overlay]
- **Palette:** 3 hex values — dominant / accent / text — can inherit from YouTube or differ
- **Text placement:** keep all text within centre 80% of frame (edges clip in grid)
- **Grid coherence note:** how this fits with other episode covers — consistent series look?
- **Canva start:** template category + font pairing

**Cover Variant B**
- Same fields, different visual energy — try text-only vs face-forward contrast

---

## Platform size specs (reference)
- YouTube thumbnail: 1280 × 720px (16:9), text safe area: inner 1120 × 580px
- Instagram Reel cover: 1080 × 1920px (9:16), grid crops to 1080 × 1350px

## Style rules (both platforms)
- Developer-adjacent aesthetic: clean, minimal, no noise
- High contrast text over simple backgrounds
- Never mislead — thumbnail must match what the video delivers
- Maximum 2 font sizes per design
- No busy backgrounds — isolate the signal
- Canva-friendly: suggest shapes, text blocks, background colours buildable without custom assets
- If face appears: expression must match episode emotional tone (don't smile on a "I made a mistake" episode)
