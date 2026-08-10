# Episode 4 — "Luna sosem áll meg" ("Luna Never Stops")

14 clips × 15 seconds = ~3.5 minutes. Model: Seedance 2.0. Aspect ratio 16:9.

**Story:** Luna always keeps watch over the group — steady, alert, standing a little apart
from the fun. Hazel notices that Luna never joins in, never rests. Instead of arguing with
her about it, Hazel quietly makes her a flower crown and asks her to just sit for five
minutes and let someone else do the watching for once.

**Lesson:** Whoever always looks after everyone else deserves to be looked after too.

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
> **Narrator-only clips (1, 2, 7, 13) get a pure scene description in `video_prompt`** —
> no mention of narration, voice-over, or speech at all, not even a line like "no
> character speaks on camera." Any reference to narration or speech in the prompt, even
> to say there isn't any, makes Seedance invent its own random spoken audio for the clip.
> Just describe what's on screen; the narrator line only ever goes in the `lines` section
> below, generated separately.

---

### Clip 1 — 0:00–0:15 — Cold open, forest establishing shot

**video_prompt:**
Pixar/Disney 3D animation style. Establishing shot of Whisperwood Forest in warm
late-afternoon light. Camera drifts toward a lively clearing in the distance — faint
sounds of laughter and playful chatter drift on the breeze, wildflowers swaying. Warm,
joyful, everyday mood. No characters visible yet. Ambient forest sound and distant
laughter only, no background music or score.

**lines:**
- Narrator (voice: Liza): "Some afternoons in Whisperwood Forest are just for playing. But even on the happiest days... someone is always keeping watch."

---

### Clip 2 — 0:15–0:30 — Luna at the tree line

**video_prompt:**
@Luna stands at the edge of a sunlit clearing, alert and still, ears turned outward
toward the forest rather than toward the clearing behind her. Behind her, soft
out-of-focus movement and color hints at friends laughing and playing in the meadow.
Luna's posture is steady, watchful, apart from the fun. Pixar/Disney 3D animation style,
warm afternoon light.

**lines:**
- Narrator (voice: Liza): "Luna always stood a little apart. Watching the paths. Listening to the wind. Just in case."

---

### Clip 3 — 0:30–0:45 — Hazel notices

**video_prompt:**
@Hazel pauses mid-step in the sunny clearing, a half-finished flower crown in her hooves,
glancing back over her shoulder toward Luna at the tree line, head tilted thoughtfully.
Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Hazel pauses mid-step in the sunny clearing, a half-finished flower crown in her hooves,
and glances back over her shoulder at @Luna standing alone at the tree line. Hazel tilts
her head thoughtfully, speaking softly to herself, mouth moving in sync with her words:
"She's not dancing again. She never dances." Only Hazel's voice plays; her mouth moves
only while she speaks these words, no other character is on screen. No background music
or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Hazel (voice: Hana): "She's not dancing again. She never dances."

---

### Clip 4 — 0:45–1:00 — Hazel comes over

**video_prompt:**
@Hazel crosses the clearing and comes to stand beside @Luna at the tree line, offering a
warm, gentle smile. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Hazel crosses the clearing and comes to stand beside @Luna at the tree line, offering a
warm, gentle smile, speaking, mouth moving in sync with her words: "Come dance with us,
Luna. Just for a little while?" Luna's mouth then moves as she glances at Hazel, then back
out at the forest, replying, mouth moving in sync with her words: "Someone has to keep
watch, Hazel. That's just... what I do." Only whoever is speaking has their mouth move;
the other listens with mouth closed. No background music or score, ambient forest sound
only. Pixar/Disney 3D animation style.

**lines:**
- Hazel (voice: Hana): "Come dance with us, Luna. Just for a little while?"
- Luna (voice: Gia): "Someone has to keep watch, Hazel. That's just... what I do."

---

### Clip 5 — 1:00–1:15 — Hazel presses gently

**video_prompt:**
@Hazel studies @Luna's face for a moment, gentle and curious. Pixar/Disney 3D animation
style.

**video_prompt (lip-sync, generate_audio: true):**
@Hazel studies @Luna's face for a moment, gentle and curious, then speaks quietly, mouth
moving in sync with her words: "But who keeps watch over you?" Luna blinks, caught off
guard, her mouth staying still, clearly not having an answer. Only Hazel's voice plays.
No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Hazel (voice: Hana): "But who keeps watch over you?"

---

### Clip 6 — 1:15–1:30 — Luna deflects

**video_prompt:**
@Luna looks away, a little uncomfortable, then turns her gaze firmly back out toward the
trees. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna looks away, a little uncomfortable, then speaks, mouth moving in sync with her
words: "I don't need watching. I'm fine right here." She turns her gaze firmly back out
toward the trees. Only Luna's voice plays; her mouth moves only while she speaks these
words, no other character is on screen. No background music or score, ambient forest
sound only. Pixar/Disney 3D animation style.

**lines:**
- Luna (voice: Gia): "I don't need watching. I'm fine right here."

---

### Clip 7 — 1:30–1:45 — Hazel quietly makes something

**video_prompt:**
Pixar/Disney 3D animation style. @Hazel sits a little apart, carefully weaving wildflowers
and soft leaves together into a small crown, glancing occasionally toward Luna with a
thoughtful, fond expression. Warm, patient mood. Ambient forest sound only, no background
music or score.

**lines:**
- Narrator (voice: Liza): "So Hazel didn't argue. She just... started making something."

---

### Clip 8 — 1:45–2:00 — The flower crown

**video_prompt:**
@Hazel walks back to @Luna and gently places a delicate flower crown over her ears,
stepping back to admire it. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Hazel walks back to @Luna and gently places a delicate flower crown over her ears,
stepping back to admire it, speaking warmly, mouth moving in sync with her words: "There.
Now you sit, and let me watch for a while. Just for five minutes." Only Hazel's voice
plays; her mouth moves only while she speaks these words, no other character is on
screen. No background music or score, ambient forest sound only. Pixar/Disney 3D
animation style.

**lines:**
- Hazel (voice: Hana): "There. Now you sit, and let me watch for a while. Just for five minutes."

---

### Clip 9 — 2:00–2:15 — Luna hesitates

**video_prompt:**
@Luna touches the flower crown gently with one paw, unsure, glancing between the crown
and the forest. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna touches the flower crown gently with one paw, unsure, glancing between the crown
and the forest, speaking, mouth moving in sync with her words: "I don't know how to
just... sit." Only Luna's voice plays; her mouth moves only while she speaks these words,
no other character is on screen. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Luna (voice: Gia): "I don't know how to just... sit."

---

### Clip 10 — 2:15–2:30 — Hazel reassures her

**video_prompt:**
@Hazel sits down beside @Luna, settling in close. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Hazel sits down beside @Luna, settling in close, speaking gently, mouth moving in sync
with her words: "Then just sit badly. Nothing's going to happen in five minutes, Luna. I
promise." Luna's mouth stays still as she looks at Hazel, a small uncertain smile
forming. Only Hazel's voice plays. No background music or score, ambient forest sound
only. Pixar/Disney 3D animation style.

**lines:**
- Hazel (voice: Hana): "Then just sit badly. Nothing's going to happen in five minutes, Luna. I promise."

---

### Clip 11 — 2:30–2:45 — Luna admits it's hard

**video_prompt:**
@Luna slowly lowers herself down onto the soft grass beside @Hazel, shoulders loosening
for the first time. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna slowly lowers herself down onto the soft grass beside @Hazel, shoulders loosening
for the first time, speaking quietly, mouth moving in sync with her words: "It's hard.
Always watching. I forget how to stop." Hazel's mouth stays still, listening warmly.
Only Luna's voice plays. No background music or score, ambient forest sound only.
Pixar/Disney 3D animation style.

**lines:**
- Luna (voice: Gia): "It's hard. Always watching. I forget how to stop."

---

### Clip 12 — 2:45–3:00 — Hazel's gentle response

**video_prompt:**
@Hazel leans her head gently against @Luna's shoulder. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Hazel leans her head gently against @Luna's shoulder, speaking softly, mouth moving in
sync with her words: "You don't have to stop forever. Just for right now." Luna's mouth
stays still, closing her eyes for a moment, soaking in the quiet. Only Hazel's voice
plays. No background music or score, ambient forest sound only. Pixar/Disney 3D
animation style.

**lines:**
- Hazel (voice: Hana): "You don't have to stop forever. Just for right now."

---

### Clip 13 — 3:00–3:15 — Resolution

**video_prompt:**
Pixar/Disney 3D animation style. @Luna and @Hazel sit together in the golden meadow as
the sun begins to set, the flower crown still resting on Luna's head, both watching the
sky in comfortable silence. Warm, peaceful, tender mood. Ambient forest sound only, no
background music or score.

**lines:**
- Narrator (voice: Liza): "That day, Luna learned something new: watching over everyone else didn't mean she couldn't be watched over too. And for five whole minutes, she let herself just... be."

---

### Clip 14 — 3:15–3:30 — Generic outro invite

**video_prompt:**
@Luna stands with @Hazel in the golden meadow, still wearing the flower crown, warm and
happy. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Luna turns to face the camera, warm and a little surprised at her own smile, still
wearing the flower crown, speaking, mouth moving in sync with her words: "There's always
something new happening here in Whisperwood Forest — come back soon and see what we get
up to next!" @Hazel is visible beside her, smiling proudly, mouth not moving. Only Luna's
voice plays. No background music or score, ambient forest sound only. Pixar/Disney 3D
animation style.

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

One continuous track for the full 3:45, generated once (2-3 mood sections crossfaded
together, same approach as the earlier episodes). Suggested arc: warm, playful and
slightly distant for the opening (clips 1-2, the fun happening elsewhere), steady and
watchful under Luna's stillness (2-3), gentle and curious through Hazel's questions
(4-6), soft and patient while the crown is made (7-8), tender and a little vulnerable
through Luna's admission (9-11), warm and settled for the resolution (12-13), then
bright and warm for the close (14), staying warm and bright through the subscribe CTA (15).
