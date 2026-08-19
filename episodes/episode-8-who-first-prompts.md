# Episode 8 — "Ki ér előbb?" ("Who Gets There First?")

16 clips × 15 seconds = ~4 minutes (15s episode-intro pre-roll + 15 story/CTA clips).
Model: Seedance 2.0. Aspect ratio 16:9.

**Story:** From opposite sides of the clearing, Pip and Coco spot the same thing at the
same moment — a perfectly round, opal-shimmering stone throwing little rainbows of
light across the grass. Both declare it theirs and take off in an all-out race across
the forest, each trying wilder shortcuts than the other, crashing through Hazel's
flower tower and leaping clean over a sleeping Bruno along the way. When they finally
both dive for the stone at once, they collide in a heap — and the stone pops loose,
rolling away down the slope and straight into the stream. One more frantic splashy
chase later, soaked and out of breath, they realize that now that they actually have
the thing... there's nothing to do with it alone. So instead, they start tossing it
back and forth, laughing.

**Lesson:** It was never about who got there first — it's about having someone
ridiculous to run wild with.

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
> **Narrator-only clips (1, 13) and no-dialogue beats (4, 7, 8, 11) get a pure scene
> description in `video_prompt` — no mention of narration, voice-over, or speech at
> all**, not even a line like "no character speaks on camera." Any reference to
> narration or speech in the prompt, even to say there isn't any, makes Seedance invent
> its own random spoken audio for the clip. Just describe what's on screen; the narrator
> line only ever goes in the `lines` section below, generated separately.

---

### Clip 0 — Pre-roll (before 0:00) — Episode intro (Pip)

**video_prompt:**
@Pip zips into frame at the edge of Whisperwood Forest and skids to a stop facing the
camera directly, eyes bright, tail flicking with energy. Pixar/Disney 3D animation
style, warm morning light.

**video_prompt (lip-sync, generate_audio: true):**
@Pip zips into frame at the edge of Whisperwood Forest and skids to a stop facing the
camera directly, eyes bright, tail flicking with energy, speaking rapidly, mouth
moving in sync with his words: "PipPipPip, it's me, Pip! Today's story is called 'Who
Gets There First?' Trust me, you don't want to blink!" Only Pip's voice plays; his
mouth moves only while he speaks these words, no other character is on screen. No
background music or score, ambient forest sound only. Pixar/Disney 3D animation style,
warm morning light.

**lines:**
- Pip (voice: Zane): "PipPipPip, it's me, Pip! Today's story is called 'Who Gets There First?' Trust me, you don't want to blink!"

---

### Clip 1 — 0:00–0:15 — Cold open, forest morning

**video_prompt:**
Pixar/Disney 3D animation style. Establishing shot of a wide, sunny forest clearing
at bright morning hour, dew still sparkling on the grass. Camera drifts slowly across
the open space, birds calling, a light breeze moving the wildflowers. No characters
visible yet. Ambient forest sound only, no background music or score.

**lines:**
- Narrator (voice: Liza): "Some mornings in Whisperwood Forest start quietly. This one didn't stay quiet for long."

---

### Clip 2 — 0:15–0:30 — Pip spots the sparkle

**video_prompt:**
@Pip is mid-climb on a tree trunk at one edge of the clearing when something catches
his eye across the grass — a perfectly round, opal-shimmering stone in a patch of
sunlight, throwing little rainbows of light. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip is mid-climb on a tree trunk at one edge of the clearing when something catches
his eye across the grass — a perfectly round, opal-shimmering stone in a patch of
sunlight, throwing little rainbows of light. Pip's eyes go wide, and he speaks,
mouth moving in sync with his words: "Whoa — whoa whoa whoa, is that... that's MINE,
calling it, mine!" Only Pip's voice plays; his mouth moves only while he speaks these
words, no other character is on screen. No background music or score, ambient forest
sound only. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "Whoa — whoa whoa whoa, is that... that's MINE, calling it, mine!"

---

### Clip 3 — 0:30–0:45 — Coco spots the sparkle

**video_prompt:**
@Coco is sniffing around a bush at the opposite edge of the same clearing when the
same glimmer of light catches her eye — the round, opal-shimmering stone sparkling in
the sunlight across the grass. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Coco is sniffing around a bush at the opposite edge of the same clearing when the
same glimmer of light catches her eye — the round, opal-shimmering stone sparkling in
the sunlight across the grass. Coco's ears perk straight up, and she speaks, mouth
moving in sync with her words: "Ooh! Shiny! That's going in MY collection!" Only
Coco's voice plays; her mouth moves only while she speaks these words, no other
character is on screen. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Coco (voice: Simone): "Ooh! Shiny! That's going in MY collection!"

---

### Clip 4 — 0:45–1:00 — The race begins

**video_prompt:**
Pixar/Disney 3D animation style. Wide shot of the clearing: @Pip and @Coco launch
into a full sprint from opposite sides, straight toward the shimmering stone in the
middle, both a blur of motion, dust and grass kicking up behind them. Playful,
frantic energy. Ambient forest sound only, no background music or score.

**lines:**
*(none — visual-only beat, no dialogue or narration)*

---

### Clip 5 — 1:00–1:15 — Pip's shortcut

**video_prompt:**
@Pip springs up into the trees, leaping branch to branch at high speed, taking a wild
shortcut above the forest floor. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip springs up into the trees, leaping branch to branch at high speed, taking a wild
shortcut above the forest floor, calling out gleefully, mouth moving in sync with his
words: "Trees are basically just very tall shortcuts — watch this!" Only Pip's voice
plays; his mouth moves only while he speaks these words, no other character is on
screen. No background music or score, ambient forest sound only. Pixar/Disney 3D
animation style.

**lines:**
- Pip (voice: Zane): "Trees are basically just very tall shortcuts — watch this!"

---

### Clip 6 — 1:15–1:30 — Coco's shortcut

**video_prompt:**
@Coco spots a muddy slope and takes it at full speed, sliding downhill on her belly,
mud splattering everywhere, completely losing control. Pixar/Disney 3D animation
style.

**video_prompt (lip-sync, generate_audio: true):**
@Coco spots a muddy slope and takes it at full speed, sliding downhill on her belly,
mud splattering everywhere, completely losing control, yelping, mouth moving in sync
with her words: "Mud is basically just a very fast floor — wait, why am I sliding—"
Only Coco's voice plays; her mouth moves only while she speaks these words, no other
character is on screen. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Coco (voice: Simone): "Mud is basically just a very fast floor — wait, why am I sliding—"

---

### Clip 7 — 1:30–1:45 — Crashing through Hazel's flower tower

**video_prompt:**
Pixar/Disney 3D animation style. @Pip leaps down from the trees right as @Coco, still
muddy, comes barreling past — both crash straight through a tall, carefully stacked
tower of flowers @Hazel had been building nearby, petals exploding into the air in
every direction. Neither one slows down. Hazel is visible only in the background,
frozen mid-stack, watching them go. Ambient forest sound plus a soft scattering
sound only, no background music or score.

**lines:**
*(none — visual-only beat, no dialogue or narration)*

---

### Clip 8 — 1:45–2:00 — Leaping over sleeping Bruno

**video_prompt:**
Pixar/Disney 3D animation style. @Pip and @Coco, still sprinting neck and neck, both
leap clean over @Bruno's huge sleeping shape sprawled across the path, petals and mud
still flying off them. Bruno barely stirs, one eye cracking open just enough to
notice, then closing again. Ambient forest sound only, no background music or score.

**lines:**
*(none — visual-only beat, no dialogue or narration)*

---

### Clip 9 — 2:00–2:15 — Neck and neck, trash-talking

**video_prompt:**
@Pip and @Coco run side by side now, both breathless but grinning, glancing sideways
at each other competitively as the stone comes into view just ahead. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip and @Coco run side by side now, both breathless but grinning, glancing sideways
at each other competitively as the stone comes into view just ahead. Pip calls out,
mouth moving in sync with his words: "Slow down, slowpoke, I've basically already
won!" Coco's mouth then moves as she fires back, mouth moving in sync with her words:
"You're literally still behind me, Pip!" Only whoever is speaking has their mouth
move; the other stays focused ahead. No background music or score, ambient forest
sound only. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "Slow down, slowpoke, I've basically already won!"
- Coco (voice: Simone): "You're literally still behind me, Pip!"

---

### Clip 10 — 2:15–2:30 — The collision

**video_prompt:**
@Pip and @Coco both dive for the shimmering stone at the exact same instant, colliding
head-on and tumbling into a tangled heap right on top of it. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip and @Coco both dive for the shimmering stone at the exact same instant. Pip
calls out mid-dive, mouth moving in sync with his words: "Wait, that's—" Coco's mouth
then moves as she dives too, mouth moving in sync with her words: "—MY rock—" and
then they collide head-on, tumbling into a tangled heap right where the stone was.
Only whoever is speaking has their mouth move, each cut off by the crash. No
background music or score, ambient forest sound only. Pixar/Disney 3D animation
style.

**lines:**
- Pip (voice: Zane): "Wait, that's—"
- Coco (voice: Simone): "—MY rock—"

---

### Clip 11 — 2:30–2:45 — The stone rolls away

**video_prompt:**
Pixar/Disney 3D animation style. From beneath the tangled heap of @Pip and @Coco, the
opal-shimmering stone pops loose and rolls free, picking up speed down a gentle slope
toward the sound of running water. Both scramble up, wide-eyed, and take off after
it. Ambient forest sound only, no background music or score.

**lines:**
*(none — visual-only beat, no dialogue or narration)*

---

### Clip 12 — 2:45–3:00 — Into the stream

**video_prompt:**
The stone rolls off the bank and plops into the forest stream with a splash. @Pip and
@Coco arrive right behind it and both dive in after it without hesitation, sending
water everywhere. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
The stone rolls off the bank and plops into the forest stream with a splash. @Pip and
@Coco arrive right behind it, and Pip calls out, mouth moving in sync with his words:
"It's getting away!" Coco's mouth then moves as she dives in right after him, mouth
moving in sync with her words: "Not on my watch!" Both dive into the water, sending
splashes everywhere. Only whoever is speaking has their mouth move. No background
music or score, ambient splashing water sound. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "It's getting away!"
- Coco (voice: Simone): "Not on my watch!"

---

### Clip 13 — 3:00–3:15 — Resolution

**video_prompt:**
Pixar/Disney 3D animation style. @Pip and @Coco sit dripping wet on the sunny
streambank, muddy, petal-covered, and completely out of breath — and now, instead of
reaching for the stone between them, they start gently tossing it back and forth to
each other, laughing. Warm, happy, silly mood. Ambient forest sound only, no
background music or score.

**lines:**
- Narrator (voice: Liza): "Turns out, once you actually catch the thing you're racing for... there's not much to do with it alone. So Pip and Coco found something better to do with it — together."

---

### Clip 14 — 3:15–3:30 — Generic outro invite

**video_prompt:**
@Pip and @Coco sit together on the streambank, soggy and happy, still tossing the
stone gently back and forth between them. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip turns to face the camera, soggy and grinning, catching the stone one more time,
speaking, mouth moving in sync with his words: "There's always something new
happening here in Whisperwood Forest — come back soon and see what we get up to
next!" Coco is visible beside him, laughing, mouth not moving. Only Pip's voice
plays. No background music or score, ambient forest sound only. Pixar/Disney 3D
animation style.

**lines:**
- Pip (voice: Zane): "There's always something new happening here in Whisperwood Forest — come back soon and see what we get up to next!"

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
together, same approach as the earlier episodes). Suggested arc: bright and playful
for the discovery and the start of the race (clips 1-4), fast and comedic/frantic
through the shortcuts, the flower tower, and jumping over Bruno (5-9), a big
percussive hit for the collision (10), a quick chase beat as the stone rolls away
(11), splashy and energetic for the stream dive (12), warm and silly for the
resolution (13), then bright and warm through the close and subscribe CTA (14-15).
