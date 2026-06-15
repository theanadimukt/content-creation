# Skill: write-script

## Purpose
Generate all four platform content files for one episode from raw notes.
Outputs: youtube.md, instagram.md, thumbnail.md, x-post.md

## Input required
- Episode topic
- Raw notes or paste from notes.md
- Episode number and where it sits in the series

## Output
Save four files to: episodes/YYYY-MM-DD-[slug]/
Create the episode directory if it does not exist.
Never output only to terminal — always write all four files.

---

## File 1: youtube.md

```
# Episode [N]: [Title]
Date: YYYY-MM-DD
Format: YouTube (~10–12 min)

---

## Script

> **Production note:** [Mix of talking head / text overlays / screen recording as relevant. Pace note.]

---

[Script body — 1,500–1,800 words. Structure below.]

---

## Hooks

**Hook — Option A** ([formula name] — max 75 words):
[hook]

**Hook — Option B** ([formula name] — max 75 words):
[hook]

**Hook — Option C** ([formula name] — max 75 words):
[hook]
```

### Script body structure
1. **Hook** — first 30 seconds, spoken version of the strongest YouTube hook
2. **Who this is for** — 15 seconds, direct address
3. **Main content** — 3 to 5 clearly named sections with `**[SECTION N: Name]**` headers
4. **Lesson / what I learned** — single key takeaway
5. **CTA** — subscribe + tease next episode by name

Include production cues inline:
- `**[CAMERA — description]**` for talking head moments
- `**[TEXT OVERLAY — description]**` with overlay copy in quotes
- `**[SCREEN RECORDING — description]**` for screen moments

### YouTube hook rules
- 3 variants, each using a different formula — no two hooks same approach
- Max 75 words each
- Never start with "In this video..." or "Hey guys" or "Welcome back"
- No question hooks — statements perform better for this niche
- End with clear reason to keep watching

### Hook formulas — rotate, pick strongest fit
1. Contradiction: "Most developers think X. I did Y. Here is what happened."
2. Stakes: "I had [time] to decide if this idea was worth building."
3. Curiosity gap: "There was one thing nobody told me about building in public."
4. Result first: "I shipped my first micro-SaaS feature using only AI. Here is the exact process."
5. Mistake: "I made a mistake most solo developers make on day one. Here is how I caught it."

---

## File 2: instagram.md

```
# Episode [N]: [Title] — Instagram
Date: YYYY-MM-DD
Format: Instagram Reel (45–90 sec cut)

---

## Hooks

**Hook — Option A** (max 15 words, silent-video safe):
[hook]

**Hook — Option B** (max 15 words, silent-video safe):
[hook]

**Hook — Option C** (max 15 words, silent-video safe):
[hook]

---

## Reel cut guide

- **Clip:** [scene description — which moment from youtube.md, what's happening]
- **Why this moment:** [one sentence — why this is the strongest standalone beat]
- **Opening line on screen:** [text overlay, must match or derive directly from chosen hook]
- **Reel structure:** [beat-by-beat: e.g. "hook overlay (3s) → talking head from Section 5 (~30s) → punchline overlay (2.5s) → CTA (~10s)"]
- **Target length:** [45–90 seconds]
- **CTA at end:** [spoken line — "Follow if you want to watch this in real time" for ep 1; "Full video linked in bio" for later episodes]
```

### Instagram hook rules
- 3 variants, each a different approach
- Max 15 words — must work as silent text overlay on first frame
- No question hooks
- Must make sense with zero context from the full video

### Reel cut guide rules
- Pick ONE moment only — the single most surprising or emotionally punchy beat
- The clip must work without context from earlier in the video
- Opening line on screen must match or directly derive from the Instagram hook
- No chapter structure — one continuous narrative beat

---

## File 3: thumbnail.md

```
# Thumbnail Brief: [Episode Title]
Date: YYYY-MM-DD

---

## YouTube Thumbnail

### Variant A

- **Main text:** [5 words max, punchy, high contrast]
- **Sub text:** [optional, max 6 words]
- **Emotion:** [face expression if appearing — e.g. "deadpan", "surprised", "pointing left"]
- **Background:** [simple suggestion — solid colour, dark gradient, blurred desk]
- **Palette:** #XXXXXX (dominant) / #XXXXXX (accent) / #XXXXXX (text)
- **Layout note:** [face + text split / text-only / face-only — brief call-out]
- **Mobile legibility check:** all text readable at 120px wide
- **Canva start:** [template category + font pairing suggestion]

### Variant B

- **Main text:** [different approach — vary layout or emotion, not just colour]
- **Sub text:** [optional]
- **Emotion:** [different from Variant A]
- **Background:** [different treatment]
- **Palette:** #XXXXXX / #XXXXXX / #XXXXXX
- **Layout note:** [how it differs from A]
- **Mobile legibility check:** all text readable at 120px wide
- **Canva start:** [template category + font pairing]

---

## Instagram Reel Cover

> Static frame shown in grid before play. Must work as standalone image with no motion context.
> Keep all key elements in top 70% of frame — grid preview crops to 1080×1350.

### Cover Variant A

- **Headline text:** [max 6 words, large — this is the grid hook]
- **Sub text:** [optional, 1 line — e.g. episode tag, series label]
- **Visual treatment:** [e.g. solid colour bg + bold type / face photo + overlay / screenshot crop]
- **Palette:** #XXXXXX / #XXXXXX / #XXXXXX
- **Text placement:** [keep within centre 80% — edges clip in grid]
- **Grid coherence note:** [how this fits series visual consistency]
- **Canva start:** [template category + font pairing]

### Cover Variant B

- Same fields, different visual energy — text-only vs face-forward contrast

---

## Platform specs (reference)
- YouTube thumbnail: 1280 × 720px (16:9), text safe area: inner 1120 × 580px
- Instagram Reel cover: 1080 × 1920px (9:16), grid crops to 1080 × 1350px — key elements in top 70%
```

### Thumbnail style rules
- Developer-adjacent aesthetic: clean, minimal, no noise
- High contrast text over simple backgrounds
- Never mislead — thumbnail must match what the video delivers
- Max 2 font sizes per design
- No busy backgrounds — isolate the signal
- Canva-friendly: no custom assets required
- If face appears: expression must match episode emotional tone

---

## File 4: x-post.md

```
# X Post: [Episode Title]
Date: YYYY-MM-DD

---

## Single Tweet

[tweet — 280 chars max. Punchy, no hashtags, no emojis unless natural, ends with value not hype.]

---

## Thread

1/ [hook — same energy as YouTube hook option A]

2/ [key insight or moment from the episode]

3/ [lesson + link placeholder → [link]]
```

### X post rules
- Single tweet: punchy, no hashtags, no emojis unless natural, ends with value not hype
- Thread tweet 1: hooks with same energy as the YouTube hook
- Thread tweet 2: delivers the core insight from the episode
- Thread tweet 3: closes with lesson + video link placeholder
- Both formats written every run — user picks single or thread

---

## Tone rules (all files)
- First person. Past tense for what happened, present tense for lessons
- No corporate language, no filler phrases
- Short sentences. One idea per paragraph
- Technical terms are fine — briefly explain each once
- Sound like a developer talking to another developer, not a YouTuber performing
