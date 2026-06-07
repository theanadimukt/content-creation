# Content Creation Workspace

## Who I am
Solo developer building a micro-SaaS in public. My content documents
my real journey — idea → requirements → AI-assisted build → launch.
Audience: developers, indie hackers, people curious about building with AI.
Tone: honest, direct, no fluff, slightly technical but accessible.

## Workflow
One recording per episode. Same raw footage → YouTube full cut + Instagram Reel cut.
No separate platform scripts — one script.md per episode covers everything.

## Content formats
- YouTube: 10-12 minute video, full narrative journey
- Instagram Reel: 60-90 second cut from same footage
- Both exports live in episodes/[slug]/export/

## Directory layout
```
episodes/
  YYYY-MM-DD-slug/
    notes.md        → raw ideas, research, braindump
    script.md       → recording script + hooks + thumbnail brief + reel cut guide
    video/          → raw footage files
    audio/          → raw audio if recorded separately
    images/         → screenshots, thumbnail assets
    export/
      youtube.mp4   → full cut
      instagram.mp4 → reel cut
_templates/         → reusable skill templates
```

## script.md sections
Every script.md has these five H2 sections in order:
1. `## Script` — full 1,500–1,800 word recording script
2. `## Hooks` — 3 YouTube hook variants + 3 Instagram hook variants
3. `## Thumbnail brief` — Canva spec
4. `## Reel cut guide` — which moment to clip + editing notes
5. `## X post` — single tweet + 3-tweet thread

## Skills
See .claude/skills/ for available skills.
Always load the relevant skill before starting any content task.

## Tools
Manual for now. No external API calls.

## Output rules
- Save to: episodes/YYYY-MM-DD-slug/script.md
- Create episode directory if it does not exist
- Never output only to terminal — always write the file

## Available skills
- .claude/skills/write-script.md    → generate full script.md from notes
- .claude/skills/write-hook.md      → rewrite/strengthen ## Hooks section
- .claude/skills/thumbnail-brief.md → rewrite ## Thumbnail brief section
- .claude/skills/adapt-for-reel.md  → rewrite ## Reel cut guide section
