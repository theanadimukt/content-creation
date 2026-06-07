# Skill: write-script

## Purpose
Generate a complete script.md for one episode — recording script, hooks,
thumbnail brief, and reel cut guide — all in one file.

## Input required
- Episode topic (e.g. "how I validated the idea")
- Raw notes or paste from notes.md
- Episode number and where it sits in the series

## Output
Save to: episodes/YYYY-MM-DD-[slug]/script.md
Create the episode directory if it does not exist.

## script.md structure to output

```
# Episode [N]: [Title]
Date: YYYY-MM-DD

---

## Script

[Full 1,500–1,800 word recording script]

---

## Hooks

**YouTube hook — Option A** (max 75 words):
[hook]

**YouTube hook — Option B** (max 75 words):
[hook]

**YouTube hook — Option C** (max 75 words):
[hook]

---

**Instagram hook — Option A** (max 15 words, silent-video safe):
[hook]

**Instagram hook — Option B** (max 15 words, silent-video safe):
[hook]

**Instagram hook — Option C** (max 15 words, silent-video safe):
[hook]

---

## Thumbnail brief

- **Main text:** [5 words max, punchy]
- **Sub text:** [optional, max 6 words]
- **Emotion:** [face expression if I appear]
- **Background:** [simple suggestion]
- **Palette:** #XXXXXX (dominant) / #XXXXXX (accent) / #XXXXXX (text)

---

## Reel cut guide

- **Clip:** [scene description — which moment, what's happening]
- **Why this moment:** [one sentence]
- **Opening line on screen:** [matches Instagram hook]
- **CTA:** "Full video linked in bio"

---

## X post

**Single tweet** (280 chars max):
[tweet]

**Thread** (3 tweets):
1/ [opening — hook, same energy as YouTube hook]
2/ [the key insight or moment from the episode]
3/ [lesson + link placeholder: "Full video → [link]"]
```

## Script structure (## Script section)
1. Hook — first 30 seconds, spoken version of YouTube hook
2. Who this is for — 15 seconds
3. Main content — 3 to 5 clearly named sections
4. Lesson / what I learned
5. CTA — subscribe and tease next episode

## Tone rules
- First person. Past tense for what happened, present tense for lessons
- No corporate language, no filler phrases
- Short sentences. One idea per paragraph
- Technical terms are fine — briefly explain each one once
- Sound like a developer talking to another developer, not a YouTuber performing

## Word count targets
- Script section: 1,500 to 1,800 words
- YouTube hook: 75 words max
- Instagram hook: 15 words max, must work as silent text overlay

## Hook formulas — rotate, pick strongest fit
1. Contradiction: "Most developers think X. I did Y. Here is what happened."
2. Stakes: "I had [time] to decide if this idea was worth building."
3. Curiosity gap: "There was one thing nobody told me about building in public."
4. Result first: "I shipped my first micro-SaaS feature using only AI. Here is the exact process."
5. Mistake: "I made a mistake most solo developers make on day one. Here is how I caught it."

## Rules
- Generate 3 variants for each hook (YouTube and Instagram) — user picks
- Use a different formula for each variant — no two hooks same approach
- Never start hook with "In this video..." or "Hey guys" or "Welcome back"
- No question hooks — statements perform better for this niche
- Thumbnail text must be readable at 120px wide (mobile feed size)
- Reel cut guide picks ONE moment only — the single strongest beat
- X single tweet: punchy, no hashtags, no emojis unless natural, ends with value not hype
- X thread: tweet 1 hooks, tweet 2 delivers insight, tweet 3 closes with lesson + video link placeholder
- Both X formats written every run — user picks single or thread
