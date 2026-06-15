# Content Creation Workspace

## Who I am
Solo developer building a micro-SaaS in public. My content documents
my real journey — idea → requirements → AI-assisted build → launch.
Audience: developers, indie hackers, people curious about building with AI.
Tone: honest, direct, no fluff, slightly technical but accessible.

## Workflow
One recording per episode. Same raw footage → YouTube full cut + Instagram Reel cut.
Each platform has its own output file. No single monolithic script file.

## Content formats
- YouTube: 10-12 minute video, full narrative journey
- Instagram Reel: 45-90 second cut from same footage
- Both exports live in episodes/[slug]/export/

## Directory layout
```
episodes/
  YYYY-MM-DD-slug/
    notes.md            → raw ideas, research, braindump
    youtube.md          → full recording script + YouTube hooks
    instagram.md        → reel cut guide + Instagram hooks
    thumbnail.md        → YouTube thumbnail brief + Instagram reel cover brief
    x-post.md           → single tweet + 3-tweet thread
    production-guide.md → scene-by-scene visual direction, VO cues, music, captions
    video/              → raw footage files
    audio/              → raw audio if recorded separately
    images/             → screenshots, thumbnail assets
    export/
      youtube.mp4       → full cut
      instagram.mp4     → reel cut
_templates/             → reusable skill templates
```

## File specs

### youtube.md
Two H2 sections in order:
1. `## Script` — full 1,500–1,800 word recording script with scene directions
2. `## Hooks` — 3 YouTube hook variants (75 words max each)

### instagram.md
Two H2 sections in order:
1. `## Hooks` — 3 Instagram hook variants (15 words max, silent-video safe)
2. `## Reel cut guide` — which moment to clip + reel structure + CTA

### thumbnail.md
Two H2 sections in order:
1. `## YouTube Thumbnail` — 2 Canva-ready variants (1280×720)
2. `## Instagram Reel Cover` — 2 Canva-ready variants (1080×1920)

### x-post.md
Two H2 sections in order:
1. `## Single Tweet` — 280 chars max
2. `## Thread` — 3 tweets

## Skills
See .claude/skills/ for available skills.
Always load the relevant skill before starting any content task.

## Tools
Manual for now. No external API calls.

## Output rules
- write-script generates all four files: youtube.md, instagram.md, thumbnail.md, x-post.md
- Create episode directory if it does not exist
- Never output only to terminal — always write the files

## Available skills
- .claude/skills/write-script.md           → generates youtube.md + instagram.md + thumbnail.md + x-post.md from notes
- .claude/skills/write-hook.md             → rewrite YouTube hooks in youtube.md OR Instagram hooks in instagram.md
- .claude/skills/thumbnail-brief.md        → iterate thumbnail.md (YouTube + Reel cover, 2 variants each)
- .claude/skills/adapt-for-reel.md         → rewrite reel cut guide in instagram.md
- .claude/skills/write-production-guide.md → scene-by-scene visual direction, VO cues, on-screen text, music mood, platform captions + hashtags

## Episode production order
1. Run write-script → youtube.md + instagram.md + thumbnail.md + x-post.md
2. Run write-production-guide → production-guide.md (reads youtube.md)
3. Iterate any file independently: write-hook / thumbnail-brief / adapt-for-reel as needed
4. Record using youtube.md + production-guide.md side by side
5. Edit using production-guide.md scene breakdown
