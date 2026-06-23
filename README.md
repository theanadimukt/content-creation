# Content Creation Workspace

A Claude Code–powered production system for a micro-SaaS building-in-public series. One episode folder holds everything: scripts, footage, exports. Claude Code skills handle scripting, video editing, captions, motion graphics, and production direction.

**Creator:** Indian software developer, London. Building a micro-SaaS in public.
**Formats:** YouTube (10–12 min) + Instagram Reel (45–60 sec standalone)
**Audience:** Developers, indie hackers, people building with AI.

---

## Prerequisites

| Tool | Version | Check |
|------|---------|-------|
| Claude Code | latest | `claude --version` |
| Node.js | 22+ | `node --version` |
| FFmpeg + ffprobe | any recent | `ffmpeg -version` |

---

## Project Structure

```
episodes/
  YYYY-MM-DD-slug/
    notes.md              ← YOU fill this first (7 fields — the story source)
    youtube.md            ← full recording script + YouTube hooks
    instagram.md          ← standalone reel script + reel cut guide + hooks
    thumbnail.md          ← YouTube thumbnail + Instagram reel cover briefs
    x-post.md             ← single tweet + 3-tweet thread
    production-guide.md   ← scene-by-scene visual direction, VO cues, music
    video/                ← raw footage (gitignored)
    audio/                ← raw audio (gitignored)
    images/               ← screenshots, thumbnail assets (git tracked)
    export/
      youtube.mp4         ← final YouTube cut (gitignored)
      instagram.mp4       ← final Reel cut (gitignored)

_templates/
  notes.md               ← scaffolded into every new episode automatically

.claude/skills/           ← Claude Code skills (content + editing)
.agents/skills/           ← HyperFrames skills (rendering engine)
```

---

## End-to-End Production Flow

```
Fill notes.md (7 fields)
       ↓
write-script → youtube.md + instagram.md + thumbnail.md + x-post.md
       ↓
write-production-guide → production-guide.md
       ↓
Record using youtube.md + production-guide.md side by side
       ↓
Edit reel → video-editing skill → export/instagram.mp4
       ↓
Add captions → embedded-captions skill
       ↓
Add overlays / motion graphics (optional) → graphic-overlays / motion-graphics
       ↓
Publish
```

---

## Step-by-Step Guide

### Step 1 — Create the episode folder

Run write-script with the episode slug and date. It scaffolds the full folder automatically:

```
Tell Claude: "Run write-script for episode 2026-06-28-day-three"
```

This creates:
```
episodes/2026-06-28-day-three/
  notes.md    ← scaffolded from _templates/notes.md
  video/
  audio/
  images/
  export/
```

---

### Step 2 — Fill notes.md

Open `episodes/YYYY-MM-DD-slug/notes.md` and fill all 7 fields **before running the script skill**. The AI reads your exact words — the more specific, the better the script. It does not invent story details.

```markdown
## 1. The moment
I was at my desk at 11pm, the terminal showed an error I had never seen before.

## 2. What I was building or trying
Setting up Stripe webhooks for the first time on my SaaS.

## 3. The obstacle
The webhook kept failing silently — no error in logs, no 200, nothing.

## 4. The fix or decision
Turned out the endpoint URL in Stripe dashboard had a trailing slash. One character.

## 5. The lesson
Always check the obvious things first. A one-character mistake wasted three hours.

## 6. The reel moment
The moment I found the trailing slash after three hours of debugging.

## 7. Next episode teaser
Next I am wiring up the payment confirmation email.
```

Tips for filling notes.md:
- Use voice-to-text and paste — raw is fine, skill cleans it up
- Fill it while coding, not after — details are sharper in the moment
- Field 6 (reel moment) is the Instagram story — it must stand alone, zero YouTube context needed

---

### Step 3 — Generate all scripts

With notes.md filled, run the write-script skill:

```
Tell Claude: "/write-script" or "Run write-script for this episode"
```

Generates four files:
- `youtube.md` — 1,500–1,800 word spoken script, progress-obstacle-lesson arc, 3 hook variants
- `instagram.md` — standalone 45–60s reel script (from notes field 6) + reel cut guide + 3 hooks
- `thumbnail.md` — 2 YouTube thumbnail briefs + 2 Instagram reel cover briefs, Canva-ready
- `x-post.md` — single tweet + 3-tweet thread

Script structure (YouTube):
1. Hook — personal story opening (from notes field 1)
2. Who this is for — 15 seconds
3. Progress — what you were building (notes field 2)
4. Obstacle — what broke or surprised you (notes field 3)
5. Fix or decision — what resolved it (notes field 4)
6. Lesson — one takeaway for developers watching (notes field 5)
7. CTA — "follow the journey" + next episode teaser (notes field 7)

---

### Step 4 — Iterate scripts (optional)

Rewrite hooks without regenerating the full script:

```
Tell Claude: "/write-hook youtube" or "/write-hook instagram"
```

Rewrite thumbnail briefs:

```
Tell Claude: "/thumbnail-brief"
```

Rewrite the Instagram reel cut guide:

```
Tell Claude: "/adapt-for-reel"
```

---

### Step 5 — Generate production guide

Run after youtube.md is final. Reads the script and produces scene-by-scene visual direction:

```
Tell Claude: "/write-production-guide"
```

Generates `production-guide.md` with:
- Scene breakdown matched to script sections
- Camera direction (talking head / screen recording / B-roll cues)
- On-screen text and overlay timing
- Music mood and chapter markers
- Caption and hashtag suggestions per platform

Use youtube.md and production-guide.md side by side during recording.

---

### Step 6 — Record

Record your YouTube video using youtube.md as the script and production-guide.md for visual cues.

Drop footage into `episodes/YYYY-MM-DD-slug/video/` (gitignored — safe to dump SD card here).

For the Instagram Reel, you have two options:
- Record a fresh 60-second standalone take using the `## Reel Script` section in instagram.md
- Clip the exact matching section from your YouTube footage using the `## Reel cut guide`

---

### Step 7 — Edit the Instagram Reel

With footage in `video/`, use the video-editing skill to produce a polished 9:16 reel:

```
Tell Claude: "Using the video-editing skill, edit my Instagram reel.
Script: instagram.md. Footage: video/raw.mp4. Output: export/instagram.mp4"
```

The skill handles:
- Engineered hook frame (first 1–3 seconds)
- A-roll / B-roll cutting
- Eased camera moves (no jitter)
- Captions and fonts from your brand style
- Rights-free SFX synthesis + audio mix
- 9:16 verification gate (ffprobe checks dimensions, duration, codec, audio)
- Auto-generates `edit-report.md` with beat-by-beat decisions

To use your brand style (fonts, colours, motion):

```bash
cd .claude/skills/video-editing/styles
cp -r _template your-brand
# edit your-brand/FRAME.md
```

Then tell Claude: `"theme from styles/your-brand/FRAME.md"`

---

### Step 8 — Add captions (optional)

Burn styled captions into the reel or YouTube cut:

```
Tell Claude: "Using the embedded-captions skill, add captions to export/instagram.mp4"
```

Choose a caption identity (32 available): `anchor` (clean default), `editorial`, `neon`, `documentary`, `velocity`, etc.

---

### Step 9 — Add motion graphics or overlays (optional)

Add animated lower-thirds, stat callouts, or title cards to the YouTube video:

```
Tell Claude: "Using the graphic-overlays skill, add a lower-third with my name and title at 0:32"
```

Create a short standalone motion graphic (number counter, stat, quote card):

```
Tell Claude: "Using the motion-graphics skill, create a 5-second stat card: '3 hours lost to a trailing slash'"
```

---

## Skill Reference

### Content Skills (`.claude/skills/`)

| Skill | When to use | Trigger |
|-------|-------------|---------|
| `write-script` | Generate all 4 platform files from notes.md | Start of every episode |
| `write-hook` | Rewrite YouTube or Instagram hooks only | Hooks feel weak after review |
| `thumbnail-brief` | Iterate thumbnail.md variants | Not happy with thumbnail direction |
| `adapt-for-reel` | Rewrite reel cut guide in instagram.md | Reel structure needs rework |
| `write-production-guide` | Generate production-guide.md from youtube.md | After script is finalised |

### Video Editing Skills (`.claude/skills/`)

| Skill | When to use |
|-------|-------------|
| `video-editing` | Turn script + talking-head footage into a polished 9:16 reel |
| `embedded-captions` | Burn styled captions into any video |
| `graphic-overlays` | Layer timed title cards, lower-thirds, data callouts onto existing footage |
| `motion-graphics` | Standalone short motion graphics — stat cards, quote cards, logo stings |
| `faceless-explainer` | Text/topic → narrated faceless explainer video (no talking head) |
| `general-video` | Custom multi-scene video composition (longer/freeform) |
| `music-to-video` | Music-driven visual video |
| `slideshow` | Photo/image slideshow video |
| `website-to-video` | Capture and animate a website into a video |
| `product-launch-video` | Marketing/launch video for a product |

### HyperFrames Engine Skills (`.agents/skills/`)

These power the rendering underneath. You rarely invoke these directly — the editing skills above call them. Reference if you need low-level control.

| Skill | What it covers |
|-------|---------------|
| `hyperframes` | Full composition authoring, timing, media, production workflow |
| `hyperframes-core` | Composition structure, data attributes, clips, tracks, validation |
| `hyperframes-animation` | Atomic motion rules, scene blueprints, transitions, GSAP/Lottie/Three.js |
| `hyperframes-creative` | Design spec, palettes, typography, brand/style decisions |
| `hyperframes-media` | TTS voiceover, BGM, SFX, transcription, captions |
| `hyperframes-cli` | CLI commands: init, lint, preview, render, doctor |
| `hyperframes-registry` | Install catalog blocks (transitions, overlays, social widgets) |

---

## notes.md Field Reference

| Field | Maps to | What to write |
|-------|---------|--------------|
| The moment | YouTube hook | One scene. Where were you, what happened. |
| What I was building | Progress section | Episode context and goal. |
| The obstacle | Obstacle section | What broke, surprised, or stopped you. Be specific. |
| The fix or decision | Fix section | What resolved it or what you chose. Include uncertainty. |
| The lesson | Lesson section | One sentence. Developer takeaway. |
| The reel moment | Instagram Reel Script | One insight that stands alone without YouTube context. |
| Next episode teaser | CTA | One line. What is coming next. |

---

## Adding a New Episode (Quick Reference)

```
1. Tell Claude: "Create episode 2026-XX-XX-[slug]" → notes.md + folders scaffolded
2. Fill notes.md (7 fields) — voice memo → paste is fine
3. Tell Claude: "Run write-script" → 4 files generated
4. Tell Claude: "Run write-production-guide" → production-guide.md generated
5. Record using youtube.md + production-guide.md
6. Drop footage in video/
7. Tell Claude: "Edit my reel using video-editing skill"
8. Optional: add captions, overlays, motion graphics
9. Export lives in export/
```

---

## Git Tracking Policy

Tracked (committed):
- All `.md` files (scripts, notes, guides, briefs)
- `images/.gitkeep` (keeps folder in git, images added manually)

Ignored (never committed):
- `video/` — raw footage
- `audio/` — raw audio
- `export/*.mp4` — rendered video files

This keeps the repo fast and script-focused. Raw media lives on disk only.
