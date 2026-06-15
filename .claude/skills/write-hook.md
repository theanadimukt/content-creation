# Skill: write-hook

## Purpose
Generate a new batch of hook variants when all three from write-script missed.
Use only when none of the current hooks are usable.

## Input required
- Path to episode directory
- Platform: YouTube or Instagram (or both)
- Which variant was closest and why it didn't land

## Output
- YouTube hooks → update `## Hooks` section in youtube.md in place
- Instagram hooks → update `## Hooks` section in instagram.md in place
- Do not touch any other section or file

## Hook formulas — rotate, pick strongest fit
1. Contradiction: "Most developers think X. I did Y. Here is what happened."
2. Stakes: "I had [time] to decide if this idea was worth building."
3. Curiosity gap: "There was one thing nobody told me about building in public."
4. Result first: "I shipped my first micro-SaaS feature using only AI. Here is the exact process."
5. Mistake: "I made a mistake most solo developers make on day one. Here is how I caught it."

## Rules
- YouTube hook: max 75 words, ends with clear reason to keep watching
- Instagram hook: max 15 words, must work as silent text overlay
- Never start with "In this video..." or "Hey guys" or "Welcome back"
- No question hooks — statements perform better for this niche
- Generate 3 variants, let user pick
- Use a different formula for each variant — no two hooks same approach
