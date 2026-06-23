# Skill: write-script

## Purpose
Generate all four platform content files for one episode from raw notes.
Outputs: youtube.md, instagram.md, thumbnail.md, x-post.md

## Input required
Read `notes.md` in the episode folder. It contains 7 required fields:
1. **The moment** — the real scene the hook comes from
2. **What I was building or trying** — episode context
3. **The obstacle** — what broke, surprised, or stopped progress
4. **The fix or decision** — what resolved it or was chosen
5. **The lesson** — one sentence takeaway for a developer watching
6. **The reel moment** — single insight that works standalone in 60s (becomes the Instagram Reel)
7. **Next episode teaser** — one line on what's coming

If notes.md is missing or fields are blank, stop and ask the user to fill it in. Do not invent story details.

## Output
Save four files to: episodes/YYYY-MM-DD-[slug]/
Create the episode directory if it does not exist.
Never output only to terminal — always write all four files.

When creating a new episode directory, also scaffold all media subdirs so the folder is production-ready immediately:

```bash
mkdir -p episodes/YYYY-MM-DD-slug/video
mkdir -p episodes/YYYY-MM-DD-slug/audio
mkdir -p episodes/YYYY-MM-DD-slug/images
mkdir -p episodes/YYYY-MM-DD-slug/export
touch episodes/YYYY-MM-DD-slug/images/.gitkeep
cp _templates/notes.md episodes/YYYY-MM-DD-slug/notes.md
```

Files to generate every run:
1. youtube.md — spoken English script
2. instagram.md — hooks + full reel script + reel cut guide
3. thumbnail.md — YouTube thumbnail + Instagram reel cover briefs
4. x-post.md — single tweet + thread

---

## Script writing rules (apply to all scripts)

The creator is an Indian software developer living in the UK. English is their second language. They understand English well but sometimes struggle with fluency and vocabulary while speaking. They are building confidence on camera. The audience should feel like they are talking to a normal person, not an influencer.

1. Use simple British English
2. Use short sentences
3. Avoid advanced vocabulary
4. Avoid corporate jargon
5. Avoid motivational clichés
6. Write exactly how a normal person would speak
7. Include natural pauses (use "..." or `[pause]` inline)
8. Use conversational language
9. Make the script easy to remember
10. Keep grammar correct but not overly formal
11. Do not try to sound like a native speaker
12. Do not use words that most English learners wouldn't know
13. Keep the tone honest, reflective and personal
14. Use personal stories whenever possible
15. If a sentence is difficult to pronounce, simplify it
16. Explain like talking to a kid — if a 10-year-old wouldn't follow it, simplify further

### Script structure (every script)
1. Hook (5–10 seconds)
2. Personal story
3. Lesson learned
4. Practical takeaway
5. Simple ending

### Every script must include
- Full script
- Bullet point version
- Estimated speaking time

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
1. **Hook** — first 30 seconds. Personal story opening from notes field 1 "The moment". Drop the viewer into a real scene.
2. **Who this is for** — 15 seconds, direct address
3. **Progress** — what you were building or trying (notes field 2). Sets up the stakes.
4. **Obstacle** — what broke, surprised, or stopped you (notes field 3). This is the tension. Do not rush past it.
5. **Fix or decision** — what resolved it or what you chose (notes field 4). Keep honest — include uncertainty if it was there.
6. **Lesson** — one clear takeaway for a developer watching (notes field 5). One sentence, then expand briefly.
7. **CTA** — "follow the journey" (not "subscribe") + tease next episode by name (notes field 7). No hard sell.

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
- **Default to personal story opening** — drop viewer into the real scene from notes field 1

### Hook formulas — personal story opening is the recommended default
1. **Personal story** *(recommended)*: Drop into a real moment. "I was sitting at my desk at 11pm. The error made no sense. I had been staring at it for two hours." Then pivot to what this video is about.
2. Contradiction: "Most developers think X. I did Y. Here is what happened."
3. Stakes: "I had [time] to decide if this idea was worth building."
4. Curiosity gap: "There was one thing nobody told me about building in public."
5. Mistake: "I made a mistake most solo developers make on day one. Here is how I caught it."

---

## File 2: instagram.md

```
# Episode [N]: [Title] — Instagram
Date: YYYY-MM-DD
Format: Instagram Reel (45–60 sec, standalone)

---

## Hooks

**Hook — Option A** (max 15 words, silent-video safe):
[hook]

**Hook — Option B** (max 15 words, silent-video safe):
[hook]

**Hook — Option C** (max 15 words, silent-video safe):
[hook]

---

## Reel Script

> This is a fully standalone script. It does NOT summarise the YouTube video. It tells ONE story — the reel moment from notes field 6. Record this separately or clip the exact matching section from your talking-head footage.

[Full spoken script — 45–60 seconds. Structure: hook line (spoken) → set the scene in one sentence → the one insight/obstacle/surprise → lesson in one sentence → CTA]

**Estimated speaking time:** [X seconds]

---

## Reel cut guide

- **Source:** [record fresh OR clip from YouTube section — specify which]
- **The moment:** [which insight from notes field 6 this reel covers]
- **Opening line on screen:** [text overlay matching chosen hook — must appear in first 2 seconds]
- **Reel structure:** [beat-by-beat: e.g. "hook overlay (2s) → spoken hook (3s) → story (35s) → lesson (10s) → CTA (8s)"]
- **Target length:** 45–60 seconds
- **CTA at end:** [spoken — "Follow to watch this build in real time" or "Full story linked in bio"]
```

### Instagram hook rules
- 3 variants, each a different approach
- Max 15 words — must work as silent text overlay on first frame
- No question hooks
- Must make sense with zero context from the YouTube video

### Reel script rules
- Source: notes field 6 "The reel moment" — one insight, one story, start to finish
- Never summarise the YouTube video — that is a trailer and gets skipped
- Must work as a completely standalone piece of content
- Same simple English rules as YouTube script — short sentences, easy to say

### Reel cut guide rules
- One moment only — the single beat from notes field 6
- No chapter structure — one continuous narrative
- CTA never pushes a product — always "follow the journey" or "full story in bio"

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
- Simple British English. Short sentences. One idea per sentence
- No advanced vocabulary. No corporate jargon. No motivational clichés
- Technical terms are fine — briefly explain each once
- No essay transitions ("Furthermore", "In conclusion", "As we can see") — real people don't talk like that
- Honest, reflective, personal. Use personal stories whenever possible
- If a sentence would be hard to say out loud, simplify it

