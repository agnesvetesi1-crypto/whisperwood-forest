# Episode 5 — "A titkos ösvény" ("The Secret Shortcut")

14 clips × 15 seconds = ~3.5 minutes. Model: Seedance 2.0. Aspect ratio 16:9.

**Story:** Pip is sure he's found a shortcut through Old Hollow that will get the group
to Bramble Pond in half the time. Coco is thrilled by the adventure and doesn't
hesitate for a second. Benny isn't so sure — but doesn't want to be left behind, so he
follows anyway. The "shortcut" turns out to be more overgrown and confusing than Pip
remembered, and the group ends up properly lost. The whole time, quiet Benny has been
noticing the little things — moss, the sound of a stream — that the other two rushed
right past. When he finally speaks up, it's Benny who leads them home.

**Lesson:** Being sure of yourself isn't the same as being right — and the quietest
voice in the group is often the one worth listening to.

Each clip below has two parts for the decoupled audio workflow (see concept doc §3):
- **video_prompt** → send to `generate_video` (Seedance 2.0, 15s, visuals + ambient sfx only)
- **lines** → send to `generate_audio` separately, one call per speaker, using the locked voice_id from the character table

> **Lip-sync fix:** for any clip where a character speaks directly to camera, use the
> **video_prompt (lip-sync)** version below instead of the plain one — it has the actual
> dialogue baked into the prompt so the mouth movement matches the words. Set
> **`generate_audio: true`** on these. Don't upload the locked-voice line as an audio
> reference — the correct voice gets layered in at final assembly, native ambience stays
> underneath. No duplicate characters in frame; when two characters share a clip, only the
> speaking one's mouth moves, the other stays silent (except where a clip explicitly
> alternates between two speakers, in which case only whoever is currently talking has
> mouth movement).
>
> **Narrator-only clips (1 and 13) and the no-dialogue beat (6) get a pure scene
> description in `video_prompt` — no mention of narration, voice-over, or speech at
> all**, not even a line like "no character speaks on camera." Any reference to
> narration or speech in the prompt, even to say there isn't any, makes Seedance invent
> its own random spoken audio for the clip. Just describe what's on screen; the narrator
> line only ever goes in the `lines` section below, generated separately.

---

### Clip 1 — 0:00–0:15 — Cold open, forest establishing shot

**video_prompt:**
Pixar/Disney 3D animation style. Establishing shot of Whisperwood Forest in bright
mid-morning light. Camera drifts across a sunny trail winding toward the deeper woods,
dew still sparkling on the ferns, a woodpecker tapping somewhere in the distance. Warm,
everyday, adventurous mood. No characters visible yet. Ambient forest sound only, no
background music or score.

**lines:**
- Narrator (voice: Liza): "Some days in Whisperwood Forest call for a little adventure — especially when someone thinks they've found a shortcut."

---

### Clip 2 — 0:15–0:30 — Pip announces the shortcut

**video_prompt:**
@Pip bursts into a sunny clearing where @Coco and @Benny are waiting, practically
vibrating with excitement, arms waving. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip bursts into a sunny clearing where @Coco and @Benny are waiting, practically
vibrating with excitement, speaking fast, mouth moving in sync with his words: "I found
it! A shortcut through Old Hollow — cuts the whole walk to Bramble Pond in HALF! Trust
me, trust me, come ON!" Coco and Benny are present but their mouths do not move. Only
Pip's voice plays. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "I found it! A shortcut through Old Hollow — cuts the whole walk to Bramble Pond in HALF! Trust me, trust me, come ON!"

---

### Clip 3 — 0:30–0:45 — Coco is instantly in

**video_prompt:**
@Coco's eyes light up, bouncing on her paws, already half-turned toward the trees.
Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Coco's eyes light up, bouncing on her paws, already half-turned toward the trees,
speaking with bright excitement, mouth moving in sync with her words: "A SECRET
shortcut?! Yes! I love this already — let's go, let's go!" Only Coco's voice plays; her
mouth moves only while she speaks these words, no other character is on screen. No
background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Coco (voice: Simone): "A secret shortcut?! Yes! I love this already — let's go, let's go!"

---

### Clip 4 — 0:45–1:00 — Benny hesitates

**video_prompt:**
@Benny stays rooted in place, ears drooping slightly with worry, glancing after @Pip
and @Coco who are already dashing toward the trees. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Benny stays rooted in place, ears drooping slightly with worry, calling after @Pip and
@Coco who are already dashing toward the trees, speaking, mouth moving in sync with his
words: "Wait — has anyone actually BEEN through Old Hollow before? It doesn't sound
like a place we know..." Pip and Coco are present but their mouths do not move, already
half-gone. Only Benny's voice plays. No background music or score, ambient forest sound
only. Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "Wait — has anyone actually BEEN through Old Hollow before? It doesn't sound like a place we know..."

---

### Clip 5 — 1:00–1:15 — Setting off

**video_prompt:**
@Pip leads the way into a narrower trail at the edge of Old Hollow, @Coco right behind
him, @Benny trailing a little further back, glancing around uncertainly. Pixar/Disney
3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip leads the way into a narrower trail at the edge of Old Hollow, walking backward to
face his friends as he talks, mouth moving in sync with his words: "This way, this way!
I remember it... mostly!" Coco and Benny are present but their mouths do not move. Only
Pip's voice plays. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "This way, this way! I remember it... mostly!"

---

### Clip 6 — 1:15–1:30 — The path disappears

**video_prompt:**
Pixar/Disney 3D animation style. @Pip, @Coco, and @Benny push through a stretch of Old
Hollow where the trail has all but vanished under overgrown brambles and tangled
roots, ducking under low branches, the canopy overhead thickening and dimming the
light. A little uncertain, a little wilder than before. Ambient rustling leaves and
snapping twigs only, no background music or score.

**lines:**
*(none — visual-only beat, no dialogue or narration)*

---

### Clip 7 — 1:30–1:45 — Pip admits it's different

**video_prompt:**
@Pip stops at a fork in the brambles, scratching his head, looking around at
unfamiliar trees. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip stops at a fork in the brambles, scratching his head, looking around at
unfamiliar trees, speaking, mouth moving in sync with his words: "Okay, okay, it's a
LITTLE different than I remember. But it's fine! Probably!" Only Pip's voice plays; his
mouth moves only while he speaks these words, no other character is on screen. No
background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "Okay, okay, it's a LITTLE different than I remember. But it's fine! Probably!"

---

### Clip 8 — 1:45–2:00 — Coco's doubt flickers

**video_prompt:**
@Coco glances between the tangled trees, her earlier bounce fading into a more
uncertain expression. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Coco glances between the tangled trees, her earlier bounce fading into a more
uncertain expression, speaking, mouth moving in sync with her words: "Pip... 'probably'
isn't super reassuring right now." Only Coco's voice plays; her mouth moves only while
she speaks these words, no other character is on screen. No background music or score,
ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Coco (voice: Simone): "Pip... 'probably' isn't super reassuring right now."

---

### Clip 9 — 2:00–2:15 — Benny notices something

**video_prompt:**
@Benny lags a step behind, crouching briefly to look at thick moss growing on a tree
root, tilting his head to listen to a faint sound in the distance. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Benny lags a step behind, crouching briefly to look at thick moss growing on a tree
root, tilting his head to listen to a faint sound in the distance, murmuring quietly to
himself, mouth moving in sync with his words: "The moss only grows this thick near the
stream... we're closer to the old bridge than they think." Only Benny's voice plays,
soft and almost to himself; his mouth moves only while he speaks these words, no other
character is on screen. No background music or score, ambient forest sound only,
including a faint distant stream trickle. Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "The moss only grows this thick near the stream... we're closer to the old bridge than they think."

---

### Clip 10 — 2:15–2:30 — Properly lost

**video_prompt:**
@Pip turns in a slow circle, ears drooping, while @Coco stands with her paws on her
hips, staring at him. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip turns in a slow circle, ears drooping, speaking sheepishly, mouth moving in sync
with his words: "Okay, I— I don't actually know where we are." Then @Coco's mouth moves
as she stares at him, paws on her hips, replying, mouth moving in sync with her words:
"WHAT? You said you knew this place!" Only whoever is speaking has their mouth move;
the other listens with mouth closed. No background music or score, ambient forest
sound only. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "Okay, I— I don't actually know where we are."
- Coco (voice: Simone): "WHAT? You said you knew this place!"

---

### Clip 11 — 2:30–2:45 — Benny speaks up

**video_prompt:**
@Benny steps forward between @Pip and @Coco, a little nervous but standing his ground,
pointing off toward a cluster of ferns. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Benny steps forward between @Pip and @Coco, a little nervous but standing his ground,
pointing off toward a cluster of ferns, speaking, mouth moving in sync with his words:
"Um... I think I know a way. The stream's just past those ferns — I noticed the moss
earlier." Pip and Coco are present but their mouths do not move, turning to listen.
Only Benny's voice plays. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "Um... I think I know a way. The stream's just past those ferns — I noticed the moss earlier."

---

### Clip 12 — 2:45–3:00 — Pip listens, finally

**video_prompt:**
@Pip looks at @Benny with surprise, then something softer. Pixar/Disney 3D animation
style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip looks at @Benny with surprise, mouth moving in sync with his words: "Wait, you
knew this whole time and didn't say anything?" Then @Benny's mouth moves, glancing down
shyly, replying, mouth moving in sync with his words: "I wasn't sure anyone would
listen." Only whoever is speaking has their mouth move; the other listens with mouth
closed. No background music or score, ambient forest sound only. Pixar/Disney 3D
animation style.

**lines:**
- Pip (voice: Zane): "Wait, you knew this whole time and didn't say anything?"
- Benny (voice: Chloe): "I wasn't sure anyone would listen."

---

### Clip 13 — 3:00–3:15 — Resolution

**video_prompt:**
Pixar/Disney 3D animation style. @Pip, @Coco, and @Benny step out of the tangled
brambles onto the familiar sunlit trail by Bramble Pond, @Benny leading the way with a
small proud smile, the other two following close behind him for once. Warm, relieved,
grateful mood. Ambient forest sound only, no background music or score.

**lines:**
- Narrator (voice: Liza): "Pip learned that being sure isn't the same as being right. And Benny learned that his quiet voice was worth speaking up — the moment someone finally listened."

---

### Clip 14 — 3:15–3:30 — Generic outro invite

**video_prompt:**
@Benny stands together with @Pip and @Coco at the edge of Bramble Pond, warm and happy,
a little more sure of himself than before. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Benny turns to face the camera, warm and a little proud of himself, still standing
close with @Pip and @Coco, speaking, mouth moving in sync with his words: "There's
always something new happening here in Whisperwood Forest — come back soon and see
what we get up to next!" Pip and Coco are visible beside him, smiling, mouths not
moving. Only Benny's voice plays. No background music or score, ambient forest sound
only. Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "There's always something new happening here in Whisperwood Forest — come back soon and see what we get up to next!"

---

## Music

One continuous track for the full 3:30, generated once (2-3 mood sections crossfaded
together, same approach as the earlier episodes). Suggested arc: bright and eager for
the opening (clips 1-5, the shortcut idea and setting off), tense and a little
uncertain as the trail vanishes and doubt creeps in (6-10), warm and settling once
Benny speaks up and leads the way (11-13), then bright and warm again for the close
(14).
