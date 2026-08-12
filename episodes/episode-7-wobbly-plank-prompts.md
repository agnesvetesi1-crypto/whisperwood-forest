# Episode 7 — "Az ingó palló" ("The Wobbly Plank")

16 clips × 15 seconds = ~4 minutes (15s episode-intro pre-roll + 15 story/CTA clips).
Model: Seedance 2.0. Aspect ratio 16:9.

**Story:** Luna and Milo set off together to Bramble Pond to gather what's needed for
the autumn gathering. The path crosses a narrow, weathered log over a small ravine.
Milo is nervous but tries anyway, stepping carefully — until a gust of wind rocks the
log and he loses his footing. Luna, steady and quick, catches him instantly and guides
him the rest of the way across, calm and sure. They finish the errand together, and
Milo walks home a little taller, having done the scary thing anyway — because Luna was
right there beside him.

**Lesson:** Having someone steady beside you can make even the scariest step feel
possible.

Each clip below has two parts for the decoupled audio workflow (see concept doc §3):
- **video_prompt** → send to `generate_video` (Seedance 2.0, 15s, visuals + ambient sfx only)
- **lines** → send to `generate_audio` separately, one call per speaker, using the locked voice_id from the character table

> **Lip-sync fix:** for any clip where a character speaks directly to camera, use the
> **video_prompt (lip-sync)** version below instead of the plain one — it has the actual
> dialogue baked into the prompt so the mouth movement matches the words. Set
> **`generate_audio: true`** on these. Don't upload the locked-voice line as an audio
> reference — the correct voice gets layered in at final assembly, native ambience stays
> underneath. No duplicate characters in frame; when two characters share a clip, only the
> speaking one's mouth moves, the other stays silent.
>
> **Narrator-only clips (1, 13) and no-dialogue beats (6, 12) get a pure scene
> description in `video_prompt` — no mention of narration, voice-over, or speech at
> all**, not even a line like "no character speaks on camera." Any reference to
> narration or speech in the prompt, even to say there isn't any, makes Seedance invent
> its own random spoken audio for the clip. Just describe what's on screen; the narrator
> line only ever goes in the `lines` section below, generated separately.

---

### Clip 0 — Pre-roll (before 0:00) — Episode intro (Milo)

**video_prompt:**
@Milo stands in a sunny spot at the edge of Whisperwood Forest, facing the camera
directly, ears twitching, a little nervous but trying to smile. Pixar/Disney 3D
animation style, warm morning light.

**video_prompt (lip-sync, generate_audio: true):**
@Milo stands in a sunny spot at the edge of Whisperwood Forest, facing the camera
directly, ears twitching, a little nervous but trying to smile, speaking, mouth moving
in sync with his words: "H-hi, it's Milo! Today's story is called 'The Wobbly Plank.'
It's a LOT to worry about, but also — you should really watch!" Only Milo's voice
plays; his mouth moves only while he speaks these words, no other character is on
screen. No background music or score, ambient forest sound only. Pixar/Disney 3D
animation style, warm morning light.

**lines:**
- Milo (voice: Leo): "H-hi, it's Milo! Today's story is called 'The Wobbly Plank.' It's a LOT to worry about, but also — you should really watch!"

---

### Clip 1 — 0:00–0:15 — Cold open, forest morning

**video_prompt:**
Pixar/Disney 3D animation style. Establishing shot of Whisperwood Forest in bright
morning light. Camera drifts along a trail leading away from the clearing, toward
denser trees and the sound of a small stream somewhere ahead. Warm, everyday,
adventurous mood. No characters visible yet. Ambient forest sound only, no background
music or score.

**lines:**
- Narrator (voice: Liza): "Some errands in Whisperwood Forest take you somewhere new — especially when the path gets a little tricky."

---

### Clip 2 — 0:15–0:30 — Luna and Milo set off

**video_prompt:**
@Luna walks confidently along a forest trail, @Milo trailing a little behind with a
small woven basket, both heading away from the clearing. Pixar/Disney 3D animation
style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna walks confidently along a forest trail, glancing back at @Milo who trails a
little behind with a small woven basket, speaking, mouth moving in sync with her
words: "Bramble Pond has exactly what we need for the gathering, Milo. Ready?" Milo's
mouth then moves as he replies, mouth moving in sync with his words: "Ready. ...Mostly
ready." Only whoever is speaking has their mouth move; the other listens with mouth
closed. No background music or score, ambient forest sound only. Pixar/Disney 3D
animation style.

**lines:**
- Luna (voice: Gia): "Bramble Pond has exactly what we need for the gathering, Milo. Ready?"
- Milo (voice: Leo): "Ready. ...Mostly ready."

---

### Clip 3 — 0:30–0:45 — The wobbly plank appears

**video_prompt:**
@Luna and @Milo arrive at the edge of a small ravine, crossed by a narrow, weathered
wooden log worn smooth with age. Milo's steps slow, ears drooping as he looks down at
the drop. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna and @Milo arrive at the edge of a small ravine, crossed by a narrow, weathered
wooden log worn smooth with age. Milo's steps slow, ears drooping as he looks down at
the drop, speaking, mouth moving in sync with his words: "Oh. Oh, that's... that's
higher than I thought it'd be." Only Milo's voice plays; his mouth moves only while he
speaks these words, no other character is on screen. No background music or score,
ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Milo (voice: Leo): "Oh. Oh, that's... that's higher than I thought it'd be."

---

### Clip 4 — 0:45–1:00 — Luna reassures

**video_prompt:**
@Luna turns back to face @Milo, calm and warm, steady posture. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna turns back to face @Milo, calm and warm, steady posture, speaking gently, mouth
moving in sync with her words: "I'll go first, and I'll stay right where you can see
me the whole way. One step at a time, okay?" Milo is present but his mouth does not
move in this clip, nodding uncertainly. Only Luna's voice plays. No background music or
score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Luna (voice: Gia): "I'll go first, and I'll stay right where you can see me the whole way. One step at a time, okay?"

---

### Clip 5 — 1:00–1:15 — Milo starts crossing

**video_prompt:**
@Milo steps onto the log, gripping tightly with each paw, moving carefully one small
step at a time, @Luna already steady on the far side watching him. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Milo steps onto the log, gripping tightly with each paw, moving carefully one small
step at a time, murmuring to himself, mouth moving in sync with his words: "One step...
just one step. I can do one step." Luna is present on the far side but her mouth does
not move in this clip. Only Milo's voice plays. No background music or score, ambient
forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Milo (voice: Leo): "One step... just one step. I can do one step."

---

### Clip 6 — 1:15–1:30 — The wind gusts

**video_prompt:**
Pixar/Disney 3D animation style. Midway across the log, a sudden gust of wind sweeps
through the ravine — leaves swirl, the log creaks and sways slightly under @Milo's
paws. Tense but brief, no real danger, just an unsteady moment. Ambient wind and
creaking wood only, no background music or score.

**lines:**
*(none — visual-only beat, no dialogue or narration)*

---

### Clip 7 — 1:30–1:45 — Milo slips, Luna catches him

**video_prompt:**
@Milo's footing slips on the log, one paw sliding off the edge. @Luna, already close
on the far side, lunges and grabs his paw firmly, steady and sure. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Milo's footing slips on the log, one paw sliding off the edge. @Luna, already close
on the far side, lunges and grabs his paw firmly, speaking calmly and quickly, mouth
moving in sync with her words: "I've got you. I've got you — look at me, not down."
Milo is present but his mouth does not move in this clip, wide-eyed and gripping her
paw. Only Luna's voice plays. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Luna (voice: Gia): "I've got you. I've got you — look at me, not down."

---

### Clip 8 — 1:45–2:00 — Steadying, crossing together

**video_prompt:**
@Luna guides @Milo step by step, steady and calm, the two of them moving together
across the rest of the log toward solid ground. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna guides @Milo step by step, steady and calm, the two of them moving together
across the rest of the log toward solid ground, speaking warmly, mouth moving in sync
with her words: "That's it. Just like that. Almost there." Milo is present but his
mouth does not move in this clip, focused and determined. Only Luna's voice plays. No
background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Luna (voice: Gia): "That's it. Just like that. Almost there."

---

### Clip 9 — 2:00–2:15 — Safe on the other side

**video_prompt:**
@Luna and @Milo step off the log onto solid ground together. Milo breathes hard,
shaky but safe, while Luna keeps a steady paw on his shoulder. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna and @Milo step off the log onto solid ground together. Milo breathes hard, shaky
but safe, speaking, mouth moving in sync with his words: "You... you caught me. I
really thought I was going to fall." Luna is present but her mouth does not move in
this clip, keeping a steady paw on his shoulder. Only Milo's voice plays. No background
music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Milo (voice: Leo): "You... you caught me. I really thought I was going to fall."

---

### Clip 10 — 2:15–2:30 — Luna's humble response

**video_prompt:**
@Luna gives @Milo a warm, matter-of-fact look, no fuss, steady as ever. Pixar/Disney
3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna gives @Milo a warm, matter-of-fact look, no fuss, steady as ever, speaking,
mouth moving in sync with her words: "That's what I'm here for. You did the hard part
— you kept going." Milo is present but his mouth does not move in this clip. Only
Luna's voice plays. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Luna (voice: Gia): "That's what I'm here for. You did the hard part — you kept going."

---

### Clip 11 — 2:30–2:45 — Gathering at Bramble Pond

**video_prompt:**
@Luna and @Milo kneel together at the edge of Bramble Pond, gathering herbs and
berries into the woven basket, warm and light mood. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna and @Milo kneel together at the edge of Bramble Pond, gathering herbs and
berries into the woven basket, warm and light mood. Milo sits back, looking at the
full basket, speaking, mouth moving in sync with his words: "We actually made it. And
I only panicked a *little* bit." Luna is present but her mouth does not move in this
clip, smiling beside him. Only Milo's voice plays. No background music or score,
ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Milo (voice: Leo): "We actually made it. And I only panicked a little bit."

---

### Clip 12 — 2:45–3:00 — Walking back

**video_prompt:**
Pixar/Disney 3D animation style. @Luna and @Milo walk back along the same trail in
warm late-afternoon light, passing the log bridge in the distance — Milo glances at it
and keeps walking, a little taller than before, no longer flinching. Ambient forest
sound only, no background music or score.

**lines:**
*(none — visual-only beat, no dialogue or narration)*

---

### Clip 13 — 3:00–3:15 — Resolution

**video_prompt:**
Pixar/Disney 3D animation style. @Luna and @Milo walk together into the golden
sunset light back toward the clearing, basket full, calm and content. Warm, peaceful,
proud mood. Ambient forest sound only, no background music or score.

**lines:**
- Narrator (voice: Liza): "Milo learned that day that being scared doesn't mean you can't be brave. Having someone steady beside you can make even the scariest step feel possible."

---

### Clip 14 — 3:15–3:30 — Generic outro invite

**video_prompt:**
@Luna stands with @Milo at the edge of the clearing, warm and happy, evening light.
Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna turns to face the camera, warm and happy, speaking, mouth moving in sync with
her words: "There's always something new happening here in Whisperwood Forest — come
back soon and see what we get up to next!" Milo is visible beside her, smiling proudly,
mouth not moving. Only Luna's voice plays. No background music or score, ambient
forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Luna (voice: Gia): "There's always something new happening here in Whisperwood Forest — come back soon and see what we get up to next!"

---

### Clip 15 — 3:30–3:45 — Subscribe CTA

**video_prompt:**
@Coco stands facing the camera directly in a warm, sunny spot in Whisperwood Forest, tail
wagging happily, big friendly smile, ears perked. Pixar/Disney 3D animation style, warm
inviting light.

**video_prompt (lip-sync, generate_audio: true):**
@Coco stands facing the camera directly in a warm, sunny spot in Whisperwood Forest, tail
wagging happily, speaking warmly and directly to the viewer, mouth moving in sync with her
words: "If you had fun with us today, ask a grown-up to help you hit that subscribe
button, so you never miss our next adventure here in Whisperwood Forest!" Only Coco's
voice plays; her mouth moves only while she speaks these words, no other character is on
screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation
style, warm inviting light.

**lines:**
- Coco (voice: Simone): "If you had fun with us today, ask a grown-up to help you hit that subscribe button, so you never miss our next adventure here in Whisperwood Forest!"

---

## Music

One continuous track for the full 4:00, generated once (2-3 mood sections crossfaded
together, same approach as the earlier episodes). Suggested arc: warm and everyday for
the setup (clips 1-3), gentle and encouraging through Luna's reassurance and the first
steps (4-5), tense but brief through the wind gust and the slip (6-7), warm and
steadying through the rescue and crossing (8-9), settled and proud for the gathering
and walk home (10-12), then bright and warm through the resolution, close, and
subscribe CTA (13-15).
