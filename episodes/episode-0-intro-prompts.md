# Episode 0 — "Meet the Friends of Whisperwood Forest"

28 clips × 15 seconds = ~7 minutes. Model: Seedance 2.0. Aspect ratio 16:9.

Each clip below has two parts for the decoupled audio workflow (see concept doc §3):
- **video_prompt** → send to `generate_video` (Seedance 2.0, 15s, visuals + ambient sfx only)
- **lines** → send to `generate_audio` separately, one call per speaker, using the locked voice_id from the character table

> **Lip-sync fix:** for any clip where a character speaks directly to camera, use the **video_prompt (lip-sync)** version below instead of the plain one — it has the actual dialogue baked into the prompt so the mouth movement matches the words. Always set **`generate_audio: false`** on these (mute native audio) — the real voice gets dubbed in separately at the locked voice_id in assembly. Clips 1, 2, and 27 have no close-up speaker on screen, so the plain video_prompt is fine as-is.

---

### Clip 1 — 0:00–0:15 — Forest establishing shot

**video_prompt:**
Pixar/Disney 3D animation style. Establishing shot of magical Whisperwood Forest at golden morning hour. Camera glides slowly through tall trees, sunlight streaming through leaves, colorful wildflowers, a sparkling stream, birds and butterflies drifting through the air. Peaceful, warm, inviting atmosphere. No characters yet. Ambient forest sound only, no background music or score. This is Narrator voice-over only — no character is on screen to lip-sync.

**lines:**
- Narrator (voice: Emily): "Welcome to Whisperwood Forest — a magical place where the sun always finds a way through the leaves, and where eight very good friends call home. Today, we'd like you to meet them all."

---

### Clip 2 — 0:15–0:30 — Group gathering, distant

**video_prompt:**
Pixar/Disney 3D animation style. Wide shot of a sunny forest clearing. In the distance, eight small silhouetted animal figures are visible gathering and waving to each other excitedly under the golden light. Camera slowly pushes forward toward them. Warm, joyful, anticipatory mood. Each of the eight silhouettes appears only once — no duplicate figures. Ambient forest sound only, no background music or score. This is Narrator voice-over only — none of the distant figures' mouths move.

**lines:**
- Narrator (voice: Emily): "Ready? Let's start with the one who's probably already running toward you."

---

### Clip 3 — 0:30–0:45 — Coco intro 1

**video_prompt:**
@Coco bounds energetically into frame through the sunlit forest, skids to a stop, spins once with excitement, big grin, tail wagging fast. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Coco bounds energetically into frame through the sunlit forest, skids to a stop, spins once with excitement, big grin, tail wagging fast. She turns to face the camera directly and speaks clearly, mouth moving in sync with her words: "Hi! Hi hi hi! My name's Coco — I'm a fox, in case the tail and the ears didn't already give it away!" Only Coco's voice plays; her mouth moves only while she speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Coco (voice: Simone): "Hi! Hi hi hi! My name's Coco — I'm a fox, in case the tail and the ears didn't already give it away!"

---

### Clip 4 — 0:45–1:00 — Coco intro 2

**video_prompt:**
@Coco talking animatedly, gesturing with her paws, eyes wide with enthusiasm, standing among flowers. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Coco talking animatedly, gesturing with her paws, eyes wide with enthusiasm, standing among flowers, facing camera and speaking clearly, mouth moving in sync with her words: "I love finding new things — bugs, berries, butterflies, weird noises coming from the bushes, all of it! If something exciting is happening anywhere in this forest, I'm probably already there — usually before I've finished thinking it through." Only Coco's voice plays; her mouth moves only while she speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Coco (voice: Simone): "I love finding new things — bugs, berries, butterflies, weird noises coming from the bushes, all of it! If something exciting is happening anywhere in this forest, I'm probably already there — usually before I've finished thinking it through."

---

### Clip 5 — 1:00–1:15 — Coco intro 3

**video_prompt:**
@Coco's ears perk up suddenly at a rustling sound offscreen. Her eyes go wide with delight, and she dashes off toward it without hesitation, disappearing into the bushes mid-sentence. Pixar/Disney 3D animation style, playful energetic motion.

**video_prompt (lip-sync, generate_audio: false):**
@Coco's ears perk up suddenly at a rustling sound offscreen. Her eyes go wide with delight. Facing camera, she speaks quickly, mouth moving in sync with her words: "Ooh, wait — did you hear that?! I have to go check — nice meeting you, bye!" — then dashes off toward the sound without hesitation, disappearing into the bushes mid-sentence. Only Coco's voice plays; her mouth moves only while she speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, playful energetic motion.

**lines:**
- Coco (voice: Simone): "Ooh, wait — did you hear that?! I have to go check — nice meeting you, bye!"

---

### Clip 6 — 1:15–1:30 — Oliver intro 1

**video_prompt:**
@Oliver perched calmly on a low branch where Coco just disappeared, watching her go with a small knowing smile, adjusting his round glasses. Pixar/Disney 3D animation style, warm dappled light.

**video_prompt (lip-sync, generate_audio: false):**
@Oliver perched calmly on a low branch where Coco just disappeared, adjusting his round glasses, then turns to face camera and speaks warmly, mouth moving in sync with his words: "That was Coco. And I'm Oliver — I've lived in this forest a long time, and I've learned that most problems get smaller once you stop and actually think about them." Only Oliver's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, warm dappled light.

**lines:**
- Oliver (voice: Arthur): "That was Coco. And I'm Oliver — I've lived in this forest a long time, and I've learned that most problems get smaller once you stop and actually think about them."

---

### Clip 7 — 1:30–1:45 — Oliver intro 2

**video_prompt:**
@Oliver tilts his head thoughtfully, wings folded, wise gentle expression, warm afternoon forest light behind him. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Oliver tilts his head thoughtfully, wings folded, wise gentle expression, facing camera and speaking, mouth moving in sync with his words: "Whenever Coco needs... gentle redirecting, I'm usually not far away. Someone has to ask the second question before everyone runs off after the first exciting thing." Only Oliver's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Warm afternoon forest light behind him. Pixar/Disney 3D animation style.

**lines:**
- Oliver (voice: Arthur): "Whenever Coco needs... gentle redirecting, I'm usually not far away. Someone has to ask the second question before everyone runs off after the first exciting thing."

---

### Clip 8 — 1:45–2:00 — Oliver intro 3

**video_prompt:**
@Oliver spreads his wings and glides gracefully off his branch, soaring low and smooth over the treetops toward the next clearing, calm and dignified in flight. Pixar/Disney 3D animation style, golden light through canopy.

**video_prompt (lip-sync, generate_audio: false):**
@Oliver, still perched, faces camera and speaks calmly first, mouth moving in sync with his words: "Now — let's go find someone who could use a bit of quiet company." Then he spreads his wings and glides gracefully off his branch, soaring low and smooth over the treetops toward the next clearing, calm and dignified in flight. Only Oliver's voice plays; his mouth moves only while he speaks his line, not while gliding silently. No other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, golden light through canopy.

**lines:**
- Oliver (voice: Arthur): "Now — let's go find someone who could use a bit of quiet company."

---

### Clip 9 — 2:00–2:15 — Benny intro 1

**video_prompt:**
@Benny peeks out shyly from behind a large flower, ears twitching nervously, small and gray, big cautious eyes. Pixar/Disney 3D animation style, soft dappled light.

**video_prompt (lip-sync, generate_audio: false):**
@Benny peeks out shyly from behind a large flower, ears twitching nervously, looking toward camera and speaking softly, mouth moving in sync with his words: "Um. Hello. I'm... I'm Benny. I'm a bunny. I'm a little bit shy — you probably already noticed that." Only Benny's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Small and gray, big cautious eyes. Pixar/Disney 3D animation style, soft dappled light.

**lines:**
- Benny (voice: Chloe): "Um. Hello. I'm... I'm Benny. I'm a bunny. I'm a little bit shy — you probably already noticed that."

---

### Clip 10 — 2:15–2:30 — Benny intro 2

**video_prompt:**
@Benny slowly steps out fully from behind the flower, still nervous but standing a little taller, ears slowly relaxing. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Benny slowly steps out fully from behind the flower, still nervous but standing a little taller, ears slowly relaxing, facing camera and speaking, mouth moving in sync with his words: "My friends say I'm braver than I think I am. I'm... still not totally sure about that. But I'm working on it. Every day, a little bit." Only Benny's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Benny (voice: Chloe): "My friends say I'm braver than I think I am. I'm... still not totally sure about that. But I'm working on it. Every day, a little bit."

---

### Clip 11 — 2:30–2:45 — Benny intro 3

**video_prompt:**
@Benny takes a deep breath, closes his eyes, then hops forward bravely over a small log he was clearly nervous about, landing safely and opening his eyes with surprised pride. Pixar/Disney 3D animation style, warm encouraging light.

**video_prompt (lip-sync, generate_audio: false):**
@Benny takes a deep breath, closes his eyes, then hops forward bravely over a small log he was clearly nervous about, landing safely and opening his eyes with surprised pride, turning to camera and speaking, mouth moving in sync with his words: "See? A little bit braver already." Only Benny's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, warm encouraging light.

**lines:**
- Benny (voice: Chloe): "See? A little bit braver already."

---

### Clip 12 — 2:45–3:00 — Bruno intro 1

**video_prompt:**
@Bruno lumbers warmly into frame, big and friendly, holding a berry between two claws, warm chuckle. Pixar/Disney 3D animation style, golden forest light.

**video_prompt (lip-sync, generate_audio: false):**
@Bruno lumbers warmly into frame, big and friendly, holding a berry between two claws, facing camera and speaking with a warm chuckle, mouth moving in sync with his words: "Name's Bruno. I'm a bear, in case that wasn't obvious. Big, a little slow, hungry pretty much all the time." Only Bruno's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, golden forest light.

**lines:**
- Bruno (voice: Marcus): "Name's Bruno. I'm a bear, in case that wasn't obvious. Big, a little slow, hungry pretty much all the time."

---

### Clip 13 — 3:00–3:15 — Bruno intro 2

**video_prompt:**
@Bruno sits down heavily but gently on a soft patch of moss, offering the berry outward toward camera with a warm smile. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Bruno sits down heavily but gently on a soft patch of moss, offering the berry outward toward camera with a warm smile, speaking, mouth moving in sync with his words: "But I give the best hugs in this whole forest — ask anybody. Well. Ask Benny. Gently. He startles easy." Only Bruno's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Bruno (voice: Marcus): "But I give the best hugs in this whole forest — ask anybody. Well. Ask Benny. Gently. He startles easy."

---

### Clip 14 — 3:15–3:30 — Bruno + Benny hug

**video_prompt:**
@Bruno spots @Benny nearby, opens his arms wide for a gentle hug. Benny hesitates, then steps into it happily, completely enveloped in the big gentle embrace. Pixar/Disney 3D animation style, warm heartwarming light.

**video_prompt (lip-sync, generate_audio: false):**
@Bruno spots @Benny nearby, opens his arms wide for a gentle hug, glancing at camera and speaking first, mouth moving in sync with his words: "See? Perfectly safe." Benny hesitates, then steps into the embrace happily, and once enveloped in the hug, also turns slightly toward camera and speaks, mouth moving in sync with his words: "Okay, this part I like." Only Bruno and Benny's voices play, one at a time — each one's mouth moves only during his own line, staying still during the other's. Bruno and Benny each appear only once in frame, no duplicates. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, warm heartwarming light.

**lines:**
- Bruno (voice: Marcus): "See? Perfectly safe."
- Benny (voice: Chloe): "Okay, this part I like."

---

### Clip 15 — 3:30–3:45 — Luna intro 1

**video_prompt:**
@Luna stands tall and calm at the edge of the clearing, alert posture, gray fur catching the light, scanning the forest protectively before her expression softens. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Luna stands tall and calm at the edge of the clearing, alert posture, gray fur catching the light, scanning the forest protectively before her expression softens and she faces camera, speaking, mouth moving in sync with her words: "I'm Luna. Wolf. I keep an eye on everyone out here." Only Luna's voice plays; her mouth moves only while she speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Luna (voice: Remy): "I'm Luna. Wolf. I keep an eye on everyone out here."

---

### Clip 16 — 3:45–4:00 — Luna intro 2

**video_prompt:**
@Luna walks calmly along a ridge overlooking the forest, watching over the distant clearing where the other friends are gathered. Pixar/Disney 3D animation style, warm late-afternoon light.

**video_prompt (lip-sync, generate_audio: false):**
@Luna walks calmly along a ridge overlooking the forest, watching over the distant clearing where the other friends are gathered, then turns to camera and speaks, mouth moving in sync with her words: "Not because they need it, exactly. Just because that's what friends do for each other. If you're ever lost in Whisperwood Forest, just call out. I'll hear you." Only Luna's voice plays; her mouth moves only while she speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, warm late-afternoon light.

**lines:**
- Luna (voice: Remy): "Not because they need it, exactly. Just because that's what friends do for each other. If you're ever lost in Whisperwood Forest, just call out. I'll hear you."

---

### Clip 17 — 4:00–4:15 — Luna intro 3

**video_prompt:**
@Luna's ears perk toward a faint sound in the distance. She turns her head sharply, then relaxes and softens into a small warm smile toward camera. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Luna's ears perk toward a faint sound in the distance. She turns her head sharply, then relaxes and softens into a small warm smile toward camera, speaking, mouth moving in sync with her words: "Come on. I think you'll like the next one." Only Luna's voice plays; her mouth moves only while she speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Luna (voice: Remy): "Come on. I think you'll like the next one."

---

### Clip 18 — 4:15–4:30 — Hazel intro 1

**video_prompt:**
@Hazel twirls gracefully through tall grass in a sunlit meadow, petals drifting around her, elegant and light on her feet. Pixar/Disney 3D animation style, dreamy golden light.

**video_prompt (lip-sync, generate_audio: false):**
@Hazel twirls gracefully through tall grass in a sunlit meadow, petals drifting around her, elegant and light on her feet, then faces camera and speaks brightly, mouth moving in sync with her words: "I'm Hazel! Doesn't the wind sound like music today?" Only Hazel's voice plays; her mouth moves only while she speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, dreamy golden light.

**lines:**
- Hazel (voice: Hana): "I'm Hazel! Doesn't the wind sound like music today?"

---

### Clip 19 — 4:30–4:45 — Hazel intro 2

**video_prompt:**
@Hazel pauses mid-dance to gently touch a dewdrop resting on a leaf, watching it sparkle with delight. Pixar/Disney 3D animation style, soft magical light.

**video_prompt (lip-sync, generate_audio: false):**
@Hazel pauses mid-dance to gently touch a dewdrop resting on a leaf, watching it sparkle with delight, then turns to camera and speaks dreamily, mouth moving in sync with her words: "I love to dance, I love to sing, and I love finding beauty in the smallest things — a dewdrop, a leaf falling just right. This forest is full of it, if you just slow down and look." Only Hazel's voice plays; her mouth moves only while she speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, soft magical light.

**lines:**
- Hazel (voice: Hana): "I love to dance, I love to sing, and I love finding beauty in the smallest things — a dewdrop, a leaf falling just right. This forest is full of it, if you just slow down and look."

---

### Clip 20 — 4:45–5:00 — Hazel intro 3

**video_prompt:**
@Hazel spins one final graceful turn, arms open, flower petals swirling around her in the golden light, then comes to a gentle stop facing the camera with a warm smile. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Hazel spins one final graceful turn, arms open, flower petals swirling around her in the golden light, then comes to a gentle stop facing the camera with a warm smile, speaking, mouth moving in sync with her words: "Come dance along with us — there's still so much forest left to see." Only Hazel's voice plays; her mouth moves only while she speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Hazel (voice: Hana): "Come dance along with us — there's still so much forest left to see."

---

### Clip 21 — 5:00–5:15 — Milo intro 1

**video_prompt:**
@Milo fidgets nervously in place, small spiky brown hedgehog, glancing around anxiously before straightening up with effort. Pixar/Disney 3D animation style, soft forest light.

**video_prompt (lip-sync, generate_audio: false):**
@Milo fidgets nervously in place, small spiky brown hedgehog, glancing around anxiously before straightening up with effort, facing camera and speaking nervously, mouth moving in sync with his words: "M-Milo. Hedgehog. I like rules, I like plans, and I like knowing exactly what's going to happen before it happens." Only Milo's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, soft forest light.

**lines:**
- Milo (voice: Leo): "M-Milo. Hedgehog. I like rules, I like plans, and I like knowing exactly what's going to happen before it happens."

---

### Clip 22 — 5:15–5:30 — Milo intro 2

**video_prompt:**
@Milo curls slightly into a small worried ball for a moment, then slowly uncurls, taking a deep breath, standing a bit taller with a small proud smile. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Milo curls slightly into a small worried ball for a moment, then slowly uncurls, taking a deep breath, standing a bit taller with a small proud smile, facing camera and speaking, mouth moving in sync with his words: "Which, living with this group, almost never happens. But... I wouldn't trade them for anything. Probably. Okay — definitely." Only Milo's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style.

**lines:**
- Milo (voice: Leo): "Which, living with this group, almost never happens. But... I wouldn't trade them for anything. Probably. Okay — definitely."

---

### Clip 23 — 5:30–5:45 — Milo intro 3

**video_prompt:**
@Milo checks over his shoulder nervously, then musters courage and takes a small determined step forward toward camera. Pixar/Disney 3D animation style, warm encouraging light.

**video_prompt (lip-sync, generate_audio: false):**
@Milo checks over his shoulder nervously, then musters courage and takes a small determined step forward toward camera, speaking, mouth moving in sync with his words: "Okay. Okay, let's keep going. One more friend to meet — the fast one. Very fast." Only Milo's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, warm encouraging light.

**lines:**
- Milo (voice: Leo): "Okay. Okay, let's keep going. One more friend to meet — the fast one. Very fast."

---

### Clip 24 — 5:45–6:00 — Pip intro 1

**video_prompt:**
@Pip zips rapidly across tree branches in quick darting movements, skids to a sudden stop right in front of camera, wide excited grin, tail flicking fast. Pixar/Disney 3D animation style, energetic motion.

**video_prompt (lip-sync, generate_audio: false):**
@Pip zips rapidly across tree branches in quick darting movements, skids to a sudden stop right in front of camera, wide excited grin, tail flicking fast, speaking rapidly, mouth moving fast in sync with his words: "HiI'mPip! Squirrel! I collect acorns, I climb literally everything, and I already know what everyone else just said because I was listening while also doing three other things!" Only Pip's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, energetic motion.

**lines:**
- Pip (voice: Zane): "HiI'mPip! Squirrel! I collect acorns, I climb literally everything, and I already know what everyone else just said because I was listening while also doing three other things!"

---

### Clip 25 — 6:00–6:15 — Pip intro 2

**video_prompt:**
@Pip darts up a tree trunk in a spiral, grabs an acorn mid-motion, and leaps to the next branch without slowing down, energy never stopping. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Pip darts up a tree trunk in a spiral, grabs an acorn mid-motion, and leaps to the next branch without slowing down, talking the whole time toward camera, mouth moving fast in sync with his words: "I know every shortcut in this whole forest — this way's faster, that way's faster, honestly most ways are faster if you just commit—" Only Pip's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Energy never stopping. Pixar/Disney 3D animation style.

**lines:**
- Pip (voice: Zane): "I know every shortcut in this whole forest — this way's faster, that way's faster, honestly most ways are faster if you just commit—"

---

### Clip 26 — 6:15–6:30 — Pip intro 3

**video_prompt:**
@Pip suddenly freezes mid-motion, realizing something, then grins and points offscreen toward the group. Pixar/Disney 3D animation style, warm light.

**video_prompt (lip-sync, generate_audio: false):**
@Pip suddenly freezes mid-motion, realizing something, then grins and points offscreen toward the group, speaking quickly to camera, mouth moving in sync with his words: "Wait that's everybody! Okay bye — I mean hi — I mean, let's go find the others!" Only Pip's voice plays; his mouth moves only while he speaks these words, no other character is on screen. No background music or score, ambient forest sound only. Pixar/Disney 3D animation style, warm light.

**lines:**
- Pip (voice: Zane): "Wait that's everybody! Okay bye — I mean hi — I mean, let's go find the others!"

---

### Clip 27 — 6:30–6:45 — Group together

**video_prompt:**
Wide golden-hour shot: all eight characters — @Coco, @Oliver, @Benny, @Bruno, @Luna, @Hazel, @Milo, @Pip — standing together in the sunny forest clearing, warm and united, looking out at the forest together. Each of the eight characters appears only once in frame, no duplicates. Ambient forest sound only, no background music or score. This is Narrator voice-over only — none of the characters' mouths move. Pixar/Disney 3D animation style, soft warm sunset light.

**lines:**
- Narrator (voice: Emily): "Eight friends, one magical forest, and more adventures than anyone could count. Some days they'll chase butterflies. Some days they'll get a little lost. But they always find their way — together."

---

### Clip 28 — 6:45–7:00 — Generic outro invite

**video_prompt:**
@Coco steps forward from the group toward camera, big warm smile, waving. The other seven friends visible behind her still waving. Golden sunset light. Camera slowly pulls back to reveal the whole forest. Pixar/Disney 3D animation style.

**video_prompt (lip-sync, generate_audio: false):**
@Coco steps forward from the group toward camera, big warm smile, waving, then speaks directly to camera, mouth moving in sync with her words: "There's always something new happening here in Whisperwood Forest — come back soon and see what we get up to next!" Only Coco's voice plays; her mouth moves only while she speaks these words. The other seven friends are each visible only once behind her, still waving, mouths not moving. No background music or score, ambient forest sound only. Golden sunset light. Camera slowly pulls back to reveal the whole forest. Pixar/Disney 3D animation style.

**lines:**
- Coco (voice: Simone): "There's always something new happening here in Whisperwood Forest — come back soon and see what we get up to next!"

---

## Music

One continuous track for the full 7:00, generated once via `generate_music`. Suggested arc: warm/curious for clips 1–2, light and playful under Coco/Pip/Benny sections, calmer and warmer under Oliver/Luna/Hazel sections, swelling gently for the group finale (27–28).
