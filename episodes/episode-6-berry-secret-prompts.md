# Episode 6 — "A bogyós titok" ("The Berry Secret")

15 clips × 15 seconds = ~3.75 minutes. Model: Seedance 2.0. Aspect ratio 16:9.

**Story:** Bruno stumbles on a hidden clearing overflowing with the best berries he's
ever tasted — and decides to keep it secret so there's "enough for him." He spends the
whole morning feasting alone... and it's delicious, but strangely quiet. When Coco
follows the smell and finds him mid-bite, Bruno has to admit what he did. Instead of
being upset, Coco just points out that eating something amazing all by yourself sounds
a little lonely. Bruno shares a berry with her — and discovers that eating together,
laughing together, is even better than having it all to himself.

**Lesson:** Good things don't get smaller when you share them — they get better.

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
> **Narrator-only clips (1, 4, 13) and the no-dialogue beat (6) get a pure scene
> description in `video_prompt` — no mention of narration, voice-over, or speech at
> all**, not even a line like "no character speaks on camera." Any reference to
> narration or speech in the prompt, even to say there isn't any, makes Seedance invent
> its own random spoken audio for the clip. Just describe what's on screen; the narrator
> line only ever goes in the `lines` section below, generated separately.

---

### Clip 1 — 0:00–0:15 — Cold open, forest morning

**video_prompt:**
Pixar/Disney 3D animation style. Establishing shot of Whisperwood Forest in soft morning
light, mist still clinging low between the trees. Camera drifts toward a dense, tangled
thicket at the edge of the frame, sunlight catching on dew. Peaceful, quietly curious
mood. No characters visible yet. Ambient forest sound only, no background music or score.

**lines:**
- Narrator (voice: Liza): "Some mornings in Whisperwood Forest hide a little secret — if you know exactly where to look."

---

### Clip 2 — 0:15–0:30 — Bruno finds the berries

**video_prompt:**
@Bruno pushes through thick bushes and freezes mid-step, eyes going wide with delight.
Ahead of him, a hidden clearing overflows with plump, glistening berries catching the
morning light. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno pushes through thick bushes and freezes mid-step, eyes going wide with delight at
a hidden clearing overflowing with plump, glistening berries catching the morning light,
speaking, mouth moving in sync with his words: "Whoa... whoa whoa whoa. Would you look at
THAT." Only Bruno's voice plays; his mouth moves only while he speaks these words, no
other character is on screen. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "Whoa... whoa whoa whoa. Would you look at THAT."

---

### Clip 3 — 0:30–0:45 — Bruno's plan

**video_prompt:**
@Bruno glances over both shoulders, checking no one is watching, then carefully drags
branches and leaves across the narrow gap in the bushes to hide the entrance to the
clearing. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno glances over both shoulders, checking no one is watching, then carefully drags
branches and leaves across the narrow gap in the bushes to hide the entrance, muttering
to himself, mouth moving in sync with his words: "If I tell anybody about this, there
won't be enough left for me. Better keep this one just... mine." Only Bruno's voice
plays; his mouth moves only while he speaks these words, no other character is on
screen. No background music or score, ambient forest sound only. Pixar/Disney 3D
animation style.

**lines:**
- Bruno (voice: Marcus): "If I tell anybody about this, there won't be enough left for me. Better keep this one just... mine."

---

### Clip 4 — 0:45–1:00 — A quiet feast

**video_prompt:**
Pixar/Disney 3D animation style. Inside the hidden clearing, @Bruno sits alone surrounded
by berries, eating happily at first, berry juice on his muzzle — but as the light shifts
from morning to midday, his chewing slows, his eyes drifting toward the empty space
beside him. Warm but quietly wistful mood. Ambient forest sound only, no background music
or score.

**lines:**
- Narrator (voice: Liza): "So Bruno feasted, and feasted, and feasted some more. It was delicious. It was also... a little quiet."

---

### Clip 5 — 1:00–1:15 — Coco catches the scent

**video_prompt:**
@Coco bounds through the forest, then stops abruptly, nose twitching, sniffing the air
with growing excitement. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Coco bounds through the forest, then stops abruptly, nose twitching, sniffing the air
with growing excitement, speaking, mouth moving in sync with her words: "Ooh — what IS
that smell? That is a very, very good smell." Only Coco's voice plays; her mouth moves
only while she speaks these words, no other character is on screen. No background music
or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Coco (voice: Simone): "Ooh — what IS that smell? That is a very, very good smell."

---

### Clip 6 — 1:15–1:30 — Following the trail

**video_prompt:**
Pixar/Disney 3D animation style. @Coco follows her nose through the forest, weaving
between trees and ducking under branches, getting closer and closer to the hidden
thicket, tail wagging with anticipation. Ambient forest sound only, no background music
or score.

**lines:**
*(none — visual-only beat, no dialogue or narration)*

---

### Clip 7 — 1:30–1:45 — Coco finds Bruno

**video_prompt:**
@Coco pushes through the leaves at the edge of the clearing and freezes, spotting
@Bruno mid-bite, surrounded by berries. Both go still, staring at each other.
Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Coco pushes through the leaves at the edge of the clearing and freezes, spotting
@Bruno mid-bite, surrounded by berries, speaking with wide-eyed surprise, mouth moving
in sync with her words: "Bruno?! You found a WHOLE secret berry patch and didn't tell
anyone?" Bruno is present but his mouth does not move in this clip, frozen mid-bite.
Only Coco's voice plays. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Coco (voice: Simone): "Bruno?! You found a WHOLE secret berry patch and didn't tell anyone?"

---

### Clip 8 — 1:45–2:00 — Bruno's guilty admission

**video_prompt:**
@Bruno freezes, a berry still in one paw, ears drooping with guilt. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno freezes, a berry still in one paw, ears drooping with guilt, speaking slowly,
mouth moving in sync with his words: "I— okay, yes. I found it yesterday. I didn't
want it to run out." Only Bruno's voice plays; his mouth moves only while he speaks
these words, no other character is on screen. No background music or score, ambient
forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "I— okay, yes. I found it yesterday. I didn't want it to run out."

---

### Clip 9 — 2:00–2:15 — Coco, more curious than upset

**video_prompt:**
@Coco tilts her head, studying @Bruno, more thoughtful than angry. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Coco tilts her head, studying @Bruno, more thoughtful than angry, speaking gently,
mouth moving in sync with her words: "But... eating all these amazing berries all by
yourself? That sounds kind of lonely, actually." Bruno is present but his mouth does
not move in this clip. Only Coco's voice plays. No background music or score, ambient
forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Coco (voice: Simone): "But... eating all these amazing berries all by yourself? That sounds kind of lonely, actually."

---

### Clip 10 — 2:15–2:30 — Bruno reconsiders

**video_prompt:**
@Bruno looks down at the berry in his paw, then up at @Coco, something shifting in his
expression. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno looks down at the berry in his paw, then up at @Coco, something shifting in his
expression, speaking quietly, mouth moving in sync with his words: "Huh. I guess... I
didn't think about that part." Coco is present but her mouth does not move in this
clip. Only Bruno's voice plays. No background music or score, ambient forest sound
only. Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "Huh. I guess... I didn't think about that part."

---

### Clip 11 — 2:30–2:45 — Bruno shares

**video_prompt:**
@Bruno picks the biggest, juiciest berry from the bush and holds it out toward @Coco.
Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno picks the biggest, juiciest berry from the bush and holds it out toward @Coco,
speaking warmly, mouth moving in sync with his words: "Here. Try this one — it's the
best one I've found all day." Coco is present but her mouth does not move in this
clip, reaching out eagerly. Only Bruno's voice plays. No background music or score,
ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "Here. Try this one — it's the best one I've found all day."

---

### Clip 12 — 2:45–3:00 — Sharing the feast

**video_prompt:**
@Bruno and @Coco sit together in the berry clearing, eating and laughing, berry juice
on both their faces, warm golden light. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno and @Coco sit together in the berry clearing, eating and laughing, berry juice
on both their faces, warm golden light. Bruno pauses mid-laugh, speaking with quiet
realization, mouth moving in sync with his words: "Huh... this is way better with
someone to share it with." Coco is present but her mouth does not move in this clip,
grinning beside him. Only Bruno's voice plays. No background music or score, ambient
forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "Huh... this is way better with someone to share it with."

---

### Clip 13 — 3:00–3:15 — Resolution

**video_prompt:**
Pixar/Disney 3D animation style. Wide, warm shot of the berry clearing in golden
afternoon light. @Bruno and @Coco sit together, content and full, surrounded by
berries that seem to gleam even brighter now. Peaceful, warm, satisfied mood. Ambient
forest sound only, no background music or score.

**lines:**
- Narrator (voice: Liza): "Bruno learned something sweet that day: good things don't get smaller when you share them. Somehow, they just get better."

---

### Clip 14 — 3:15–3:30 — Generic outro invite

**video_prompt:**
@Bruno and @Coco stand together at the edge of the berry clearing, warm and happy,
berry-stained smiles. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno turns to face the camera, warm and happy, berry-stained smile, speaking, mouth
moving in sync with his words: "There's always something new happening here in
Whisperwood Forest — come back soon and see what we get up to next!" Coco is visible
beside him, smiling proudly, mouth not moving. Only Bruno's voice plays. No background
music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "There's always something new happening here in Whisperwood Forest — come back soon and see what we get up to next!"

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

One continuous track for the full 3:45, generated once (2-3 mood sections crossfaded
together, same approach as the earlier episodes). Suggested arc: playful and curious
for the discovery (clips 1-3), warm but quietly wistful during the solo feast (4),
light and eager as Coco follows the scent (5-6), a little awkward and tense through the
discovery and confession (7-10), warm and joyful once they share and laugh together
(11-12), settled and content for the resolution (13), then bright and warm through the
close and subscribe CTA (14-15).
