# Coco's Adventures in Whisperwood Forest — Production Bible

This document is the reference file for Claude Code. It should be read before writing any generation or assembly script for this channel.

---

## 1. Concept

A heartwarming animated children's series for ages 3–7, set in the magical **Whisperwood Forest**. Each episode follows Coco the Fox and her woodland friends discovering a gentle life lesson through a small adventure. Pixar/Disney 3D animation style, warm colors, soft lighting, big expressive eyes, no scares, no real danger — only wonder, mild mishaps, and kindness.

- **Target platform:** Higgsfield.ai, model **Seedance 2.0**
- **Max clip length:** 15 seconds per generation (hard limit)
- **Target episode length:** 3–4 minutes for story episodes, up to 7–8 minutes for the introduction episode
- **Aspect ratio:** 16:9, 1080p or higher for YouTube
- **Narration language:** English

---

## 2. Characters

Each character has a fixed visual description (used with Higgsfield's `@Element` reference system) and now also a **fixed voice_id** for narration/dialogue generation. Voice IDs must never change between episodes — this is the fix for the voice-consistency problem.

| Character | Role / personality | Visual reference (for @Element upload) | Voice (Higgsfield preset) | voice_id |
|---|---|---|---|---|
| **Coco the Fox** | Curious, energetic, acts before thinking. Series lead. | Small young female fox, bright orange fur, white chest patch, white tail tip, oversized amber eyes, fluffy tail | Pixie | `0178ef57-ada4-43d9-992b-8d9221045bb4` |
| **Oliver the Owl** | Wise, calm, gently teaches lessons | Medium barn owl, warm brown/cream feathers, small round wire glasses, dignified posture | Arthur | `30fc8796-ceb6-4a66-b3a7-4a145ef7f346` |
| **Benny the Bunny** | Shy, kind, braver than he thinks | Small gray rabbit, big cautious eyes, twitchy ears | Quinn | `80914268-dfae-4f76-8306-36f2d55f58f8` |
| **Bruno the Bear** | Big, warm, always hungry, gentle | Large brown bear, soft rounded shape, warm chuckle | Marcus | `6f98d3dd-324f-4845-8c28-c1d1647a06cd` |
| **Luna the Wolf** | Protective, steady, quiet leader | Gray wolf, alert but warm posture | Simone | `d3b201aa-086c-4d54-8568-a6bb9f4a0b63` |
| **Hazel the Deer** | Graceful, artistic, loves beauty | Tan deer, small antlers, elegant movement | Tallulah | `f32c8f51-449e-4ddf-bdf7-1527e11df917` |
| **Milo the Hedgehog** | Anxious, rule-following, secretly brave | Small brown spiky hedgehog | Gideon | `1ad38ba4-9cc4-4f2f-9fde-b0fefdf67ae5` |
| **Pip the Squirrel** | Fast-talking, hyper, always half a step ahead | Red squirrel, quick movements | Remy | `b9c5c5db-4eb7-468a-a0b7-d06423af0335` |
| **Narrator** | Warm, calm, gentle storyteller — not a character in-world | — | Emily | `6b3e3642-f7b7-4cb8-9688-51e233c4b92f` |

> Note: these voice assignments are a reasonable starting guess based on name/tone only — Ági should preview each in the Higgsfield voice picker before locking them in. Once chosen, the ID goes in this table and never changes.

---

## 3. THE AUDIO PROBLEM — root cause and fix

**Symptom:** character voices sound different from clip to clip, and background music does not carry across clips.

**Root cause:** Seedance 2.0's *native* audio (voice + music) is generated independently for every single 15-second clip. There is no memory between generations — every clip gets a fresh, randomly-flavored voice and a fresh, unrelated music cue, even with the same text prompt.

**Fix — decouple video from audio:**

1. **Generate video clips with Seedance 2.0 as visuals only.** Either mute native audio in post, or set the model's audio generation off if the parameter allows it — ambient sound effects (footsteps, wind, splashes) can stay if desired, since those don't need cross-clip consistency.
2. **Generate all spoken lines separately** with `Higgsfield:generate_audio`, always passing the **same voice_id** for the same character (see table above). This guarantees Coco always sounds like Coco, Oliver always sounds like Oliver, across every episode.
3. **Generate ONE continuous music bed per episode** (not per clip) with `Higgsfield:generate_music`, sized to the full episode duration, so the score doesn't restart or clash every 15 seconds. Optionally generate 2–3 mood variants (calm / playful / emotional) and crossfade between them at scene changes rather than cutting.
4. **Assemble in Claude Code**, not in Higgsfield: concatenate the muted video clips in order, lay the single continuous music track underneath at low volume for the whole runtime, and place each character's dialogue clip at its correct timestamp on top. `ffmpeg` or `moviepy` can do this; Higgsfield's `explainer_video` tool can also stitch ordered video + audio blocks automatically and is worth trying as a shortcut before building a custom script.

This is the piece to build first in Claude Code: a script that (a) calls `generate_video` for each clip prompt, (b) calls `generate_audio` for each line using the locked voice_id, (c) calls `generate_music` once per episode, and (d) assembles everything with consistent timing.

---

## 4. Episode structure template

Every episode (after Episode 0) follows this shape:

1. Cold open — Whisperwood Forest establishing shot, same visual style every time
2. Story scenes — 1–2 lead characters, a small conflict or discovery, 15-sec segments
3. Resolution — the day's gentle lesson, spoken by the Narrator
4. **Generic outro invite** (15 sec) — the episode's lead character turns to camera and invites the viewer back, WITHOUT naming the next episode's content (so it never goes stale or requires the child to hunt for a specific title). Reusable line pattern:

> "[Character], warm and happy, turning to camera: 'There's always something new happening here in Whisperwood Forest — come back soon and see what we get up to next!'"

---

## 5. Character voice-and-tone notes (for writing new dialogue)

- **Coco:** enthusiastic, fast, a little breathless — "you HAVE to see this"
- **Oliver:** calm, wise, a little mysterious — "I have a feeling you'll want to see that"
- **Benny:** timid but trying — "I— I think you should watch. I mean, I hope you will."
- **Bruno:** warm, easygoing — "Come hang out with us again, yeah?"
- **Luna:** short, confident — "Trust me. You won't want to miss this one."
- **Hazel:** poetic, dreamy — "The next chapter is already dancing on the wind..."
- **Milo:** anxious but excited — "It's a LOT to worry about, but also — you should really watch."
- **Pip:** rapid, energetic — "next time next time NEXT TIME you have to see—"

---

## 6. Files in this handoff

- `episode-0-intro-prompts.md` — 28 clips × 15s (~7 min), introduces all 8 characters by name
- `episode-1-butterfly-prompts.md` — 14 clips × 15s (~3.5 min), "Coco and the Little Butterfly," the first story episode
