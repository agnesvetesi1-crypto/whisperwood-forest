# Episode 2 — "Pip Bocsánatot Kér" ("Pip Says Sorry")

14 clips × 15 seconds = ~3.5 minutes. Model: Seedance 2.0. Aspect ratio 16:9.

**Story:** In his usual rush, Pip crashes straight through Milo's carefully built leaf
house without even noticing — and keeps running. When Milo finds the wreckage, Pip has
to go back, own up to what he did, and help rebuild it. Saying "sorry" isn't the end of
it — making it right is.

**Lesson:** Apologizing means fixing what you broke, not just saying the word.

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
> **Narrator-only clips (1 and 13) never get the narration text written into the
> `video_prompt` itself** — only a plain scene description plus a note that no character
> speaks on camera. Putting narration words into the video prompt makes Seedance invent
> its own random spoken audio for the clip, which we don't want; the narrator line only
> ever goes in the `lines` section below, generated separately.

---

### Clip 1 — 0:00–0:15 — Cold open, forest establishing shot

**video_prompt:**
Pixar/Disney 3D animation style. Establishing shot of Whisperwood Forest in the golden
late-afternoon light. Camera drifts slowly across a quiet clearing near a stream, sunlight
filtering through the canopy, a light breeze rustling the leaves, birds calling softly in
the distance. Warm, peaceful, everyday mood. No characters visible yet. Ambient forest
sound only, no background music or score. No character speaks on camera — this is
Narrator voice-over only.

**lines:**
- Narrator (voice: Liza): "Every day in Whisperwood Forest is a little different — today starts with someone in an awfully big hurry."

---

### Clip 2 — 0:15–0:30 — Pip's whirlwind intro

**video_prompt:**
@Pip zips through the clearing in a blur of red fur, skidding around a tree root, full of
restless energy. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip zips through the clearing in a blur of red fur, skids to a brief stop around a tree
root, eyes darting everywhere with excitement, and turns to camera, speaking quickly,
mouth moving in sync with his words: "Morning, morning, MORNING! So much to do, so little
time — can't stop, gotta go, catch you later!" Only Pip's voice plays; his mouth moves
only while he speaks these words, no other character is on screen. No background music or
score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "Morning, morning, MORNING! So much to do, so little time — can't stop, gotta go, catch you later!"

---

### Clip 3 — 0:30–0:45 — Milo's leaf house

**video_prompt:**
@Milo carefully places a final leaf on top of a small, intricately built leaf-and-twig
house nestled between tree roots, humming softly to himself with delicate, focused
movements. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Milo carefully places a final leaf on top of a small, intricately built leaf-and-twig
house nestled between tree roots, then leans back to admire it, turning slightly to
camera and speaking softly, mouth moving in sync with his words: "There... almost
perfect. Just needed one more leaf for the roof." Only Milo's voice plays; his mouth moves
only while he speaks these words, no other character is on screen. No background music or
score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Milo (voice: Leo): "There... almost perfect. Just needed one more leaf for the roof."

---

### Clip 4 — 0:45–1:00 — The crash

**video_prompt:**
Pixar/Disney 3D animation style. @Pip bursts through the same clearing at full speed,
completely focused on the horizon ahead, and barrels straight through Milo's little leaf
house without looking down — leaves and twigs scatter into the air behind him. He is
already gone before the last leaf settles. No character speaks on camera — this is a
visual-only comedic beat, nobody is present to react yet. Ambient forest sound plus a
soft scattering/crunching sound only, no background music or score.

**lines:**
*(none — visual-only beat, no dialogue or narration)*

---

### Clip 5 — 1:00–1:15 — Pip, oblivious

**video_prompt:**
@Pip keeps bounding through the forest, glancing back over his shoulder with a proud
grin, completely unaware of what just happened behind him. Pixar/Disney 3D animation
style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip keeps bounding through the forest, glances back over his shoulder with a proud grin,
then briefly faces camera mid-stride, speaking, mouth moving in sync with his words:
"Fastest squirrel in the whole forest — that's me, no contest!" Only Pip's voice plays;
his mouth moves only while he speaks these words, no other character is on screen. No
background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "Fastest squirrel in the whole forest — that's me, no contest!"

---

### Clip 6 — 1:15–1:30 — Milo discovers the wreckage

**video_prompt:**
@Milo returns to find his little leaf house completely flattened, scattered leaves and
broken twigs where it used to stand, his ears drooping. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Milo returns to find his little leaf house completely flattened, scattered leaves and
broken twigs where it used to stand. His ears droop, eyes wide with sadness, he kneels
down beside the wreckage and speaks quietly, mouth moving in sync with his words: "My...
my house. It's all broken." Only Milo's voice plays; his mouth moves only while he speaks
these words, no other character is on screen. No background music or score, ambient
forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Milo (voice: Leo): "My... my house. It's all broken."

---

### Clip 7 — 1:30–1:45 — Milo sits with the loss

**video_prompt:**
@Milo sits alone among the scattered leaves, picking up a small broken twig and turning
it over in his paws, quietly upset. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Milo sits alone among the scattered leaves, picks up a small broken twig and turns it
over in his paws, and speaks softly to himself, mouth moving in sync with his words: "I
picked every one of these leaves myself. Found just the right twigs." Only Milo's voice
plays; his mouth moves only while he speaks these words, no other character is on screen.
No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Milo (voice: Leo): "I picked every one of these leaves myself. Found just the right twigs."

---

### Clip 8 — 1:45–2:00 — Milo tries alone, and stops

**video_prompt:**
@Milo starts stacking a couple of leaves back into place, half-hearted, then sets them
down again, discouraged. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Milo starts stacking a couple of leaves back into place, half-hearted, then sets them
down again, discouraged, and speaks quietly, mouth moving in sync with his words: "It's no
use starting over all by myself. It won't be the same." Only Milo's voice plays; his mouth
moves only while he speaks these words, no other character is on screen. No background
music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Milo (voice: Leo): "It's no use starting over all by myself. It won't be the same."

---

### Clip 9 — 2:00–2:15 — Pip notices something's wrong

**video_prompt:**
@Pip finally slows to a stop on a sunny branch, catching his breath, then glances down at
himself, puzzled. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip finally slows to a stop on a sunny branch, catching his breath, then glances down and
notices bits of leaf and twig stuck in his fur. He frowns, puzzled, speaking to himself,
mouth moving in sync with his words: "Huh... why do I have leaves stuck all over me?"
Only Pip's voice plays; his mouth moves only while he speaks these words, no other
character is on screen. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "Huh... why do I have leaves stuck all over me?"

---

### Clip 10 — 2:15–2:30 — Pip races back and realizes

**video_prompt:**
@Pip dashes back along his own trail and skids to a stop at the sight of @Milo sitting
beside the ruined leaf house, his excited expression dropping into horror. Pixar/Disney
3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip dashes back along his own trail and skids to a stop at the sight of @Milo sitting
beside the ruined leaf house. His excited expression drops into horror, and he speaks
slowly, mouth moving in sync with his words: "Oh no... Milo, I— I did this, didn't I?"
Milo is present but his mouth does not move in this clip. Only Pip's voice plays. No
background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "Oh no... Milo, I— I did this, didn't I?"

---

### Clip 11 — 2:30–2:45 — Milo's honest response

**video_prompt:**
@Milo looks up at @Pip, sad but calm, not angry. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Milo looks up at @Pip, sad but calm, not angry, and speaks quietly, mouth moving in sync
with his words: "Saying sorry doesn't fix my house, Pip." Pip is present but his mouth
does not move in this clip. Only Milo's voice plays. No background music or score,
ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Milo (voice: Leo): "Saying sorry doesn't fix my house, Pip."

---

### Clip 12 — 2:45–3:00 — Pip commits to fixing it

**video_prompt:**
@Pip kneels down to @Milo's level, slow and steady this time instead of rushing.
Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip kneels down to @Milo's level, slow and steady this time instead of rushing, and
speaks earnestly, mouth moving in sync with his words: "Then let's fix it. Together. I'll
gather the leaves — you just tell me exactly how you want them." Milo is present but his
mouth does not move in this clip. Only Pip's voice plays. No background music or score,
ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "Then let's fix it. Together. I'll gather the leaves — you just tell me exactly how you want them."

---

### Clip 13 — 3:00–3:15 — Rebuilding, together

**video_prompt:**
Pixar/Disney 3D animation style. @Pip and @Milo work side by side in the golden
late-afternoon light — Pip carefully carrying one leaf at a time instead of rushing, Milo
directing and placing them, the little house slowly rising again, a little sturdier than
before. Warm, satisfied mood. No character speaks on camera — this is Narrator
voice-over only. Ambient forest sound only, no background music or score.

**lines:**
- Narrator (voice: Liza): "Pip learned that sorry is just the beginning — the rest is showing up, and helping put things right."

---

### Clip 14 — 3:15–3:30 — Outro

**video_prompt:**
@Pip and @Milo stand together in front of the finished, sturdier leaf house, warm and
happy. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Pip and @Milo stand together in front of the finished, sturdier leaf house. Pip turns to
camera, warm and happy, speaking, mouth moving in sync with his words: "There's always
something new happening here in Whisperwood Forest — come back soon and see what we get
up to next!" Milo is present but his mouth does not move in this clip, smiling proudly at
the house beside Pip. Only Pip's voice plays. No background music or score, ambient
forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "There's always something new happening here in Whisperwood Forest — come back soon and see what we get up to next!"
