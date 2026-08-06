# Episode 3 — "Benny és a Nagy Zivatar" ("Benny and the Big Storm")

14 clips × 15 seconds = ~3.5 minutes. Model: Seedance 2.0. Aspect ratio 16:9.

**Story:** A storm rolls in over Whisperwood Forest and Benny, already the most anxious of
the group, bolts for his burrow in a panic. Bruno finds him there — and while trying to
comfort Benny, a huge thunderclap makes even big, steady Bruno jump. Benny realizes his
brave friend gets scared too; being scared isn't the opposite of being brave, it's just
part of it.

**Lesson:** Courage isn't not being scared — it's staying anyway, and it's easier together.

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
> **Narrator-only clips (1, 4, 11, 13) and any no-dialogue beat get a pure scene
> description in `video_prompt` — no mention of narration, voice-over, or speech at
> all**, not even a line like "no character speaks on camera." Any reference to
> narration or speech in the prompt, even to say there isn't any, makes Seedance invent
> its own random spoken audio for the clip. Just describe what's on screen; the narrator
> line only ever goes in the `lines` section below, generated separately.

---

### Clip 1 — 0:00–0:15 — Cold open, storm approaching

**video_prompt:**
Pixar/Disney 3D animation style. Establishing shot of Whisperwood Forest in the late
afternoon, sky shifting from gold to a heavy grey-blue, wind picking up and bending the
treetops, leaves swirling off branches, distant thunder rumbling low. Warm but uneasy
mood. No characters visible yet. Ambient wind and distant thunder only, no background
music or score.

**lines:**
- Narrator (voice: Liza): "Some afternoons in Whisperwood Forest turn without warning. Today, the wind had a different kind of whisper — one that meant a storm was coming."

---

### Clip 2 — 0:15–0:30 — Benny notices

**video_prompt:**
@Benny hops along a mossy path, ears twitching, then suddenly freezes as a gust of wind
rustles hard through the bushes around him, looking up nervously at the darkening sky.
Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Benny hops along a mossy path, ears twitching, then suddenly freezes as a gust of wind
rustles hard through the bushes around him, looking up nervously at the darkening sky,
speaking to himself, mouth moving in sync with his words: "Oh no. Oh no no no. That sky
does NOT look friendly." Only Benny's voice plays; his mouth moves only while he speaks
these words, no other character is on screen. No background music or score, ambient wind
sound only. Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "Oh no. Oh no no no. That sky does NOT look friendly."

---

### Clip 3 — 0:30–0:45 — Thunder, Benny bolts

**video_prompt:**
A low rumble of thunder rolls across the sky. @Benny's whole body flinches, ears pinning
back flat, and he bolts across the clearing in a blur toward his burrow, small paws
kicking up leaves behind him. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
A low rumble of thunder rolls across the sky. @Benny's whole body flinches, ears pinning
back flat, and he bolts across the clearing toward his burrow, calling out as he runs,
mouth moving in sync with his words: "Nope! Nope, I am OUT, see you after the storm,
bye!" Only Benny's voice plays; his mouth moves only while he speaks these words, no
other character is on screen. No background music or score, ambient wind and thunder
only. Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "Nope! Nope, I am OUT, see you after the storm, bye!"

---

### Clip 4 — 0:45–1:00 — Alone in the burrow

**video_prompt:**
Pixar/Disney 3D animation style. Inside @Benny's cozy burrow, dim and root-lined. Benny is
curled into the smallest possible ball in the corner, ears pressed down over his head,
eyes squeezed shut, trembling slightly as muffled thunder rumbles outside. Ambient muffled
wind and thunder only, no background music or score.

**lines:**
- Narrator (voice: Liza): "Deep underground, Benny was safe. But safe didn't feel very brave. It just felt very, very alone."

---

### Clip 5 — 1:00–1:15 — Bruno on the move

**video_prompt:**
@Bruno lumbers calmly through the forest as the first fat raindrops begin to fall, humming
to himself, seemingly unbothered by the wind, heading toward the burrows for shelter. He
glances toward Benny's usual spot near the big oak and notices it's empty. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno lumbers calmly through the forest as the first fat raindrops begin to fall, humming
to himself, then slows and glances toward Benny's usual spot near the big oak, noticing
it's empty, speaking to himself, mouth moving in sync with his words: "Hm. No Benny by the
oak today. Wonder where that little guy got to." Only Bruno's voice plays; his mouth moves
only while he speaks these words, no other character is on screen. No background music or
score, ambient wind and rain only. Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "Hm. No Benny by the oak today. Wonder where that little guy got to."

---

### Clip 6 — 1:15–1:30 — Bruno finds the burrow

**video_prompt:**
@Bruno crouches down at the small entrance of @Benny's burrow, rain dripping off his fur,
peering in gently. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno crouches down at the small entrance of @Benny's burrow, rain dripping off his fur,
peering in gently and speaking softly, mouth moving in sync with his words: "Benny? It's
just me. Mind if a big wet bear squeezes in?" Benny is heard from inside, his mouth moving
in sync with his words, small and shaky: "I— I'm okay. I just don't like the loud parts."
Only whoever is speaking has their mouth move; the other stays still. No background music
or score, ambient rain only. Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "Benny? It's just me. Mind if a big wet bear squeezes in?"
- Benny (voice: Chloe): "I— I'm okay. I just don't like the loud parts."

---

### Clip 7 — 1:30–1:45 — Bruno flinches too

**video_prompt:**
@Bruno squeezes into the burrow entrance beside @Benny, settling down warm and close.
Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno squeezes into the burrow entrance beside @Benny, settling down warm and close,
speaking gently, mouth moving in sync with his words: "It's just noise, Benny, that's all
thund—" A HUGE crack of thunder booms directly overhead. Bruno's whole massive body
flinches hard, ears back, eyes wide, cutting himself off mid-word. Only Bruno's voice
plays; his mouth moves only while he speaks these words, no other character is on screen.
No background music or score, one loud thunder crack, ambient rain otherwise.
Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "It's just noise, Benny, that's all thund—"

---

### Clip 8 — 1:45–2:00 — Benny notices

**video_prompt:**
@Benny blinks up at @Bruno, surprised, having clearly seen him flinch. Pixar/Disney 3D
animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Benny blinks up at @Bruno, surprised, having clearly seen him flinch, speaking with wide
eyes, mouth moving in sync with his words: "Wait... are YOU scared too?" Bruno rubs the
back of his neck sheepishly, his mouth moving in sync with his words: "...A little. Every
single time. Never really goes away." Only whoever is speaking has their mouth move; the
other listens with mouth closed. No background music or score, ambient rain only.
Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "Wait... are YOU scared too?"
- Bruno (voice: Marcus): "...A little. Every single time. Never really goes away."

---

### Clip 9 — 2:00–2:15 — Bruno explains

**video_prompt:**
@Bruno and @Benny sit close together in the burrow entrance, rain falling steadily beyond
it. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Bruno and @Benny sit close together in the burrow entrance, rain falling steadily beyond
it. Bruno speaks warmly, mouth moving in sync with his words: "Being big doesn't make the
scared part go away, Benny. It just means I've had more practice sitting with it." Benny's
mouth stays still, listening, ears slowly relaxing. Only Bruno's voice plays. No
background music or score, ambient rain only. Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "Being big doesn't make the scared part go away, Benny. It just means I've had more practice sitting with it."

---

### Clip 10 — 2:15–2:30 — Flinching together, then laughing

**video_prompt:**
A bright flash of lightning lights up the burrow entrance, followed instantly by a sharp
crack of thunder. Both @Benny and @Bruno flinch hard at the exact same moment — then catch
each other's eye and both start giggling. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
A bright flash of lightning lights up the burrow entrance, followed instantly by a sharp
crack of thunder. Both @Benny and @Bruno flinch hard at the exact same moment, then catch
each other's eye, and Benny bursts into giggles, speaking, mouth moving in sync with his
words: "Okay that one got you too, I SAW it!" Bruno's mouth then moves as he chuckles his
reply, mouth moving in sync with his words: "Caught red-pawed." Only whoever is speaking
has their mouth move. No background music or score, one thunder crack, ambient rain
otherwise. Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "Okay that one got you too, I SAW it!"
- Bruno (voice: Marcus): "Caught red-pawed."

---

### Clip 11 — 2:30–2:45 — Riding it out together

**video_prompt:**
Pixar/Disney 3D animation style. @Benny and @Bruno sit huddled together in the burrow
entrance, Benny leaning into Bruno's warm fur, both watching the rain fall, calm now
despite the ongoing storm outside. Ambient steady rain only, no background music or score.

**lines:**
- Narrator (voice: Liza): "So they sat, and they waited, and every time the sky rumbled, they flinched together instead of alone. Somehow, that made all the difference."

---

### Clip 12 — 2:45–3:00 — Storm passing

**video_prompt:**
Pixar/Disney 3D animation style. The rain outside the burrow entrance softens to a light
drizzle, then stops. Sunlight breaks weakly through the clearing clouds. @Benny peeks his
head out first, blinking in surprise at the calm. Ambient dripping water and returning
birdsong, no background music or score.

**video_prompt (lip-sync, generate_audio: true):**
The rain outside the burrow entrance softens to a light drizzle, then stops. Sunlight
breaks weakly through the clearing clouds. @Benny peeks his head out first, blinking in
surprise at the calm, speaking, mouth moving in sync with his words: "Hey... hey, it's
over! We made it!" Only Benny's voice plays; his mouth moves only while he speaks these
words. No background music or score, ambient dripping water and returning birdsong.
Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "Hey... hey, it's over! We made it!"

---

### Clip 13 — 3:00–3:15 — Resolution

**video_prompt:**
Pixar/Disney 3D animation style. @Benny and @Bruno step out of the burrow together into
the rain-washed forest, puddles sparkling in the returning sunlight, droplets glittering
on every leaf, a faint rainbow arcing over the trees. Warm, peaceful, relieved mood.
Ambient birdsong and dripping water only, no background music or score.

**lines:**
- Narrator (voice: Liza): "Benny learned something that day that even Bruno needed reminding of sometimes: being brave was never about not being scared. It was about staying — and it was always a little easier together."

---

### Clip 14 — 3:15–3:30 — Generic outro invite

**video_prompt:**
@Benny stands in the sparkling, rain-washed clearing, warm and happy, @Bruno beside him.
Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: true):**
@Benny stands in the sparkling, rain-washed clearing, turning to face the camera, warm and
happy, speaking, mouth moving in sync with his words: "There's always something new
happening here in Whisperwood Forest — come back soon and see what we get up to next!"
Bruno is visible beside him, smiling proudly, mouth not moving. Only Benny's voice plays.
No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "There's always something new happening here in Whisperwood Forest — come back soon and see what we get up to next!"

---

## Music

One continuous track for the full 3:30, generated once (e.g. via vidIQ's music tool, in
2-3 mood sections crossfaded together, same approach as Episodes 0-2). Suggested arc:
uneasy/anticipatory as the storm builds (clips 1-4), tense but warm during Bruno's search
and the reveal (5-9), a lighter comedic lift for the flinch-and-laugh beat (10), settling
to calm and tender while they wait it out (11), then bright and warm for the resolution
and close (12-14).
