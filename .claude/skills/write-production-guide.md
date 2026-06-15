# Skill: write-production-guide

## Purpose
Generate a production-guide.md for an episode — scene-by-scene visual direction,
voiceover cues, on-screen text, music mood, pacing, and platform captions with hashtags.
Runs after script.md exists. Reads script, outputs separate production file.

## Input required
- Path to episode's youtube.md (primary source for script and scene structure)

## Output
Save to: same episode directory → production-guide.md
Do not modify youtube.md, instagram.md, thumbnail.md, or x-post.md.

## production-guide.md structure to output

```
# Production Guide: [Episode Title]
Date: YYYY-MM-DD

---

## Music & Pacing

- **Mood:** [e.g. focused, tense, curious, understated — match episode tone]
- **Energy arc:** [e.g. "low at open → builds at insight → resolves at CTA"]
- **BPM feel:** [e.g. "~90 BPM lo-fi for talking sections, no beat under key reveal"]
- **Drop point:** [scene name where energy peaks — usually the main insight moment]
- **Track type:** [e.g. lo-fi instrumental, ambient electronic, none for serious moments]
- **Silence rule:** [e.g. "cut music entirely during the [scene] reveal for impact"]

---

## Scenes

[Repeat block below for every scene in the script. Break script into 6–10 scenes max.]

### Scene [N]: [Scene Name]

- **Voiceover:** [exact spoken lines pulled verbatim from ## Script section]
- **On-screen text:** [short overlay copy — max 8 words — that amplifies VO, not repeats it]
- **Visual:** [what appears on screen: face-cam, screen recording, B-roll, static graphic, text-only]
- **Duration:** [estimated seconds, e.g. "~25s"]
- **Transition in:** [cut / fade / zoom-in / none]
- **Transition out:** [cut / fade / slide / freeze-frame]
- **Text placement:** [e.g. bottom-third, top-left, centre — avoid covering face]
- **Text style note:** [e.g. bold white sans, highlight key word in accent colour]

---

## Platform Captions

### YouTube Description

[2–3 sentence hook paragraph — first 125 chars must be compelling, visible before "show more"]

**Timestamps:**
[Generate placeholder timestamps based on scene breakdown, e.g.]
0:00 — [scene 1 name]
[N]:00 — [scene name]
...

**Links:**
- Subscribe: [placeholder]
- GitHub / project: [placeholder]

**Tags:** [10–15 comma-separated YouTube search tags, no #, match dev/indie hacker audience]

---

### Instagram Caption

[3–5 short punchy lines. First line = hook — visible before "more". No full stops mid-paragraph.
Sound human, not broadcast. End with a soft CTA: "Full video linked in bio"]

[blank line]

**Hashtags (first comment block):**
[30 hashtags, grouped by tier:]
Tier 1 — niche (5): [e.g. #indiehacker #solofounder #buildinpublic #microsaas #devjourney]
Tier 2 — mid (10): [e.g. #sideproject #solodev #startuplife #makerlog #shipfast]
Tier 3 — broad (15): [e.g. #developer #coding #startup #tech #entrepreneurship ...]

---

### TikTok Caption (optional, same footage)

[2 punchy lines max. End with question to drive comments.]
[5–8 hashtags only — TikTok penalises hashtag stuffing]
```

---

## Scene breakdown rules

- Map scenes directly to the 5-part script structure from youtube.md:
  1. Hook scene (~30s)
  2. Who this is for (~15s)
  3. Main content scenes (split into 3–5 sub-scenes)
  4. Lesson scene
  5. CTA scene

- VO pulls exact lines from ## Script — do not paraphrase
- On-screen text is DIFFERENT from VO — it adds context or emphasis, never repeats word-for-word
- Keep on-screen text to 8 words max — must be readable in 1.5 seconds
- Visual column picks the most natural format: face-cam for personal moments,
  screen recording for code/product, B-roll suggestion for abstract ideas
- Transitions: default to hard cuts. Use fades only for scene 1 open and scene 5 CTA close
- Text placement: never block the speaker's face. Bottom-third is default safe zone

## Music rules
- Lo-fi / ambient instrumental is default for developer content
- Never suggest licensed tracks — suggest mood/genre only
- Silence is a valid production choice — call it out explicitly when it adds impact
- Music should duck under VO (not compete). Note this in Silence rule field

## Caption rules
- YouTube: first 125 chars are what shows before "show more" — make them count
- YouTube tags: mix [specific topic] + [broader category] + [format] (e.g. "indie hacker", "solo developer", "day in the life coding")
- Instagram hashtags: 30 total, post in first comment not caption body — keeps caption clean
  Tier 1 = niche audience (high relevance, lower volume)
  Tier 2 = mid-size communities
  Tier 3 = broad reach (use sparingly — avoid pure vanity tags like #love)
- TikTok: algorithm is interest-graph not hashtag-graph — fewer, more precise tags win
