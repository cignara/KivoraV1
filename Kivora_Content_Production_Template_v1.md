# Kivora — Content Production Template
### v1.0 · Single Phase · All 9 Worlds · June 2026
### Source of truth: `Kivora_Master_Activity_Plan_v4.md`

> **How to use this file**
> One row / block per content item. Fill every mandatory field before the item enters build.
> Items missing `speakLoad`, `speakOk`, or `speakNo` are **blocked from build** — no exceptions.
> Colour-code status in your tracker: 🔴 Empty · 🟡 Draft · 🟢 Ready · ✅ Built

---

## 1. ACTIVITY TEMPLATE

### Mandatory fields (every activity)

| Field | Rule |
|---|---|
| `code` | From Master Plan (e.g. `AI-T-001`) |
| `world` | World slug (e.g. `alphabet-island`) |
| `title` | From Master Plan — do not rename |
| `grade` | Toddler / Pre-K / K / G1 / G2 / G3 / G4 / G5 |
| `difficulty` | Pre-Easy / Easy / Intermediate / Advanced / Master |
| `skill` | From Master Plan skill column |
| `xp` | 5 / 10 / 20 / 35 / 50 |
| `coins` | 3 / 5 / 10 / 15 / 25 |
| `type` | tap / drag / trace / build / listen / sing / read / colour |
| `kiviAsset` | KV-002 through KV-012 (see asset map) |
| `speakLoad` | Kivi reads the prompt when activity loads |
| `speakOk` | Kivi celebrates correct answer + reinforces learning |
| `speakNo` | Kivi explains WHY wrong + demonstrates correct answer |
| `question` | The activity prompt shown on screen |
| `answers` | Array — correct answer first, then distractors |
| `correctIndex` | 0 (always keep correct answer at index 0 pre-shuffle) |
| `hint` | Optional — shown after 2 wrong attempts |
| `tags` | grade, world, skill cluster, music:true/false |
| `status` | 🔴 / 🟡 / 🟢 / ✅ |

---

### Activity Block Format (copy-paste for each item)

```
CODE:         AI-T-001
WORLD:        alphabet-island
TITLE:        Tap the Letter A
GRADE:        Toddler
DIFFICULTY:   Pre-Easy
SKILL:        Visual letter recognition
TYPE:         tap
XP:           5
COINS:        3
KIVI_ASSET:   KV-005  (thinking face — loads with question)

QUESTION:
  "Can you find the letter A? Tap it!"

ANSWERS:
  [0] A  ← CORRECT
  [1] B
  [2] D
  [3] O

SPEAK_LOAD:
  "Hello! I'm Kivi! Can you find the letter A for me?
   Look carefully — tap the letter A!"

SPEAK_OK:
  "Yes! That's the letter A! A says /a/ — like in Apple! 🍎
   You are so clever! A is for amazing — just like you!"

SPEAK_NO:
  "Oops! That's not the letter A. The letter A has two
   tall lines that meet at the top, like a little tent! ⛺
   See this one? [points] THIS is the letter A. Can you
   tap it now? I know you can!"

HINT:
  "The letter A looks like a little tent — two lines
   going up and meeting at the top!"

TAGS:         toddler, alphabet-island, letter-recognition, music:false
STATUS:       🔴
```

---

### Kivi Voice Script Rules (apply to every speakLoad / speakOk / speakNo)

| Script | Length | Tone | Must include |
|---|---|---|---|
| `speakLoad` | 1–2 sentences | Warm, inviting | The task instruction in child language |
| `speakOk` | 2–3 sentences | Celebratory + educational | Correct answer reinforcement + the learning point |
| `speakNo` | 3–4 sentences | Gentle, never shaming | Why wrong · What correct looks like · Invite retry |

**Hard rules:**
- `speakNo` must NEVER say "Try again!" or "Wrong!" alone
- `speakNo` must COUNT, DEMONSTRATE, or SHOW the correct answer
- `speakOk` must reinforce the SKILL, not just celebrate
- All scripts written at the reading level one grade BELOW the activity grade
- Song activities (🎵): `speakLoad` introduces the song; `speakOk` references a lyric

---

### TTS Settings (Web Speech API)

```js
rate:  0.86
pitch: 1.1
voice priority: Samantha (iOS) → Google US English → Aria/Zira (Edge) → en-US → en
```

---

## 2. QUIZ TEMPLATE

### Mandatory fields

| Field | Rule |
|---|---|
| `code` | Format: `QZ-[WORLD]-[NUMBER]` e.g. `QZ-AI-001` |
| `world` | World slug |
| `title` | Short quiz title |
| `grade` | Grade tier |
| `skill` | Skill being assessed |
| `questionText` | The question shown on screen |
| `questionType` | mc4 / mc2 / truefalse / fillblank / matchpair |
| `answers[0]` | CORRECT answer |
| `answers[1–3]` | Distractors (for mc4) |
| `speakLoad` | Kivi reads the question aloud |
| `speakOk` | Kivi confirms + explains WHY it is correct |
| `speakNo` | Kivi explains the correct answer — teaches, never shames |
| `explanation` | 1-sentence written explanation shown after answer |
| `xp` | Same as activity difficulty tier |
| `coins` | Same as activity difficulty tier |
| `status` | 🔴 / 🟡 / 🟢 / ✅ |

---

### Quiz Block Format

```
CODE:           QZ-AI-001
WORLD:          alphabet-island
TITLE:          What Sound Does B Make?
GRADE:          Pre-K
SKILL:          Letter-sound correspondence
QUESTION_TYPE:  mc4
XP:             10
COINS:          5

QUESTION_TEXT:
  "What sound does the letter B make?"

ANSWERS:
  [0] /b/ as in Ball   ← CORRECT
  [1] /d/ as in Dog
  [2] /p/ as in Pig
  [3] /m/ as in Moon

EXPLANATION:
  "The letter B makes the /b/ sound — like the beginning of Ball, Bee, and Bear!"

SPEAK_LOAD:
  "Quiz time! Look at the letter B. What sound does B make?
   Choose the right answer!"

SPEAK_OK:
  "That's right! B says /b/! B is for Ball, B is for Bear,
   B is for Butterfly! Great job remembering that!"

SPEAK_NO:
  "Not quite! The letter B makes the /b/ sound — say it
   with me: /b/ /b/ /b/! Like Ball! /b/ Ball!
   Now you try — which answer shows the /b/ sound?"

STATUS:         🔴
```

---

## 3. STORY TEMPLATE

### Mandatory fields

| Field | Rule |
|---|---|
| `code` | From Master Plan (STR-001 etc.) |
| `title` | From Master Plan |
| `type` | original-fiction / kivi-adventure / folk-tale / science / social / song-story |
| `theme` | From Master Plan theme column |
| `grade` | Target grade tier |
| `pages` | Target page count (per Master Plan range) |
| `wordCount` | Per page: Toddler 20–40w · Pre-K 40–80w · K 80–120w · G1–2 120–200w · G3–5 200–350w |
| `hasReadAloud` | true (ALL stories — Web Speech API narration) |
| `hasSong` | true/false (song-stories only — marked 🎵 in Master Plan) |
| `kiviNarrates` | true (always) |
| `coverEmoji` | Representative emoji for story card |
| `coverColor` | Tailwind gradient class for story card bg |
| `pages[]` | Array of page objects (see page format below) |
| `comprehensionQ` | 1–3 questions after the story ends |
| `status` | 🔴 / 🟡 / 🟢 / ✅ |

---

### Page Object Format

```
PAGE 1:
  text: |
    Kivi the fox woke up one bright morning.
    The forest was full of golden sunlight.
    "Today," said Kivi, "I will find something wonderful!"
  illustration_prompt: |
    Kivi the fox (small orange fox with big eyes, friendly)
    waking up inside a cosy tree hollow. Morning light
    streaming through leaves. Warm golden palette.
    Style: flat children's illustration, no text in image.
  kivi_reads: |
    "Kivi the fox woke up one bright morning.
     The forest was full of golden sunlight.
     Today, said Kivi — I will find something wonderful!"
  interaction: tap_to_next  [tap / highlight_word / fill_blank / none]
```

---

### Comprehension Questions Format (post-story)

```
Q1:
  question:  "What did Kivi want to find?"
  type:      mc2
  answers:   ["Something wonderful", "Something scary"]
  correct:   0
  speakOk:   "Yes! Kivi wanted to find something wonderful — just like you!"
  speakNo:   "Let's check! Kivi said: I will find something WONDERFUL!
               Can you find the right answer now?"

Q2:
  question:  "How did the forest feel in the morning?"
  type:      mc2
  answers:   ["Bright and sunny", "Dark and cold"]
  correct:   0
  speakOk:   "That's right! The forest was full of golden sunlight — beautiful!"
  speakNo:   "Remember — the story said the forest was full of golden SUNLIGHT.
               Which answer means sunny?"
```

---

## 4. COLORING PAGE TEMPLATE

### Mandatory fields

| Field | Rule |
|---|---|
| `code` | Format: `CP-[CATEGORY]-[NUMBER]` e.g. `CP-AI-001` |
| `category` | alphabet / numbers / animals-srilanka / animals-world / fantasy / festivals-srilanka / festivals-world / science / coding / kivi / mandalas / seasonal / geography / art / certificates |
| `title` | Descriptive title e.g. "Letter A — Apple Tree Scene" |
| `world` | Linked world slug (or `cross-world`) |
| `grade` | Target age range |
| `illustration_prompt` | Detailed SVG/illustration brief (see format below) |
| `printSize` | A4 / Letter |
| `onScreenTool` | color-by-number / free-paint / both |
| `colorPalette` | Suggested colours for color-by-number mode |
| `downloadable` | true |
| `status` | 🔴 / 🟡 / 🟢 / ✅ |

---

### Illustration Brief Format

```
CODE:       CP-AI-001
CATEGORY:   alphabet
TITLE:      Letter A — Apple Tree Scene
WORLD:      alphabet-island
GRADE:      Pre-K–K
PRINT_SIZE: A4

ILLUSTRATION_PROMPT:
  A large capital letter A in the centre of the page,
  formed by the trunk and branches of an apple tree.
  Apples hang from the branches (6–8 apples, round,
  with leaves and stems). A friendly Kivi fox sits
  at the base of the tree, waving. Rolling hills in
  background. Style: thick black outlines, white fill,
  child-friendly, suitable for colouring. No shading.
  No text in image. Portrait A4 orientation.

COLOUR_PALETTE (for color-by-number):
  1 = Red (apples)
  2 = Brown (trunk)
  3 = Green (leaves, hills)
  4 = Orange (Kivi)
  5 = Blue (sky)
  6 = Yellow (sun)

ON_SCREEN_TOOL: both
STATUS:         🔴
```

---

## 5. PRINTABLE TEMPLATE

### Mandatory fields

| Field | Rule |
|---|---|
| `code` | Format: `PR-[TYPE]-[NUMBER]` e.g. `PR-WS-001` |
| `type` | worksheet / activity-sheet / flashcard / certificate / lesson-plan / poster |
| `title` | Descriptive title |
| `world` | Linked world slug |
| `grade` | Target grade |
| `skill` | Skill practised |
| `pages` | Number of print pages |
| `printSize` | A4 / Letter |
| `content_brief` | Full description of what the printable contains |
| `answer_key` | true/false (worksheets need answer keys) |
| `status` | 🔴 / 🟡 / 🟢 / ✅ |

---

### Printable Brief Format

```
CODE:         PR-WS-001
TYPE:         worksheet
TITLE:        Alphabet Tracing — A to E
WORLD:        alphabet-island
GRADE:        Pre-K–K
SKILL:        Letter formation (uppercase + lowercase)
PAGES:        2
PRINT_SIZE:   A4
ANSWER_KEY:   false (tracing — no answer key needed)

CONTENT_BRIEF:
  Page 1: Uppercase letters A, B, C, D, E
    - Each letter: dotted tracing guide × 3 rows
    - One illustration per letter (apple, ball, cat, dog, egg)
    - Kivi character in corner with speech bubble: "Trace me!"
  Page 2: Lowercase letters a, b, c, d, e
    - Same structure as page 1
    - Bottom row: free writing practice line
  Font: Print Clearly (or similar manuscript font)
  Style: Clean, minimal, 14pt+ all text, high contrast

STATUS:       🔴
```

---

## 6. CRAFT TEMPLATE

### Mandatory fields

| Field | Rule |
|---|---|
| `code` | Format: `CR-[TYPE]-[NUMBER]` e.g. `CR-PA-001` |
| `type` | paper / nature / seasonal / science / recycled |
| `title` | Craft title |
| `world` | Linked world slug |
| `grade` | Target age range |
| `duration` | Estimated time in minutes |
| `materials` | Array of materials needed |
| `steps[]` | Numbered step-by-step instructions |
| `kiviTip` | Kivi's tip shown on screen |
| `safetyNote` | Any scissors / glue / adult-required flags |
| `illustration_prompt` | Brief for the finished-craft illustration |
| `status` | 🔴 / 🟡 / 🟢 / ✅ |

---

### Craft Block Format

```
CODE:       CR-PA-001
TYPE:       paper
TITLE:      Kivi the Fox Paper Puppet
WORLD:      creativity-kingdom
GRADE:      Ages 3–7
DURATION:   20 minutes
SAFETY:     Child-safe scissors recommended · Adult help for step 4

MATERIALS:
  - Orange card stock or thick paper
  - Child-safe scissors
  - Glue stick
  - Black marker
  - Popsicle stick or pencil (for handle)
  - Optional: googly eyes

STEPS:
  1. Print the Kivi template (or draw a fox shape on orange card)
  2. Carefully cut out the fox shape along the dotted lines
  3. Draw Kivi's face — two big eyes, a small triangle nose, a smile
  4. [ADULT HELP] Glue the popsicle stick to the back of Kivi
  5. Let the glue dry for 5 minutes
  6. Your Kivi puppet is ready — put on a show!

KIVI_TIP:
  "You made ME! Give me a name — maybe I'll be your
   learning buddy all week! 🦊"

ILLUSTRATION_PROMPT:
  A cheerful completed fox paper puppet held by a child's hand.
  Orange fox face with big eyes and a smile on a popsicle stick.
  Simple, bright, welcoming style. White background.

STATUS:     🔴
```

---

## 7. SPECIAL NEEDS ITEM TEMPLATE

### Additional mandatory fields (beyond standard activity fields)

| Field | Rule |
|---|---|
| `snProfile` | autism / dyslexia / adhd / fine-motor / gifted |
| `accommodation` | Specific accessibility feature(s) |
| `maxDuration` | ADHD: 5 min max · others: standard |
| `fontOverride` | dyslexia: OpenDyslexic · others: Nunito |
| `targetSize` | fine-motor: 80px min tap target · others: standard |
| `predictableStructure` | autism: true (no sudden changes, no auto-play surprises) |
| `audioFirst` | dyslexia: true · others: false |
| `movementBreak` | adhd: true if SN-AD-006/011/016/021/026 type |

---

### Special Needs Block Format (example — Autism Social Story)

```
CODE:           SN-AU-001
SN_PROFILE:     autism
WORLD:          cross-world
TITLE:          My Morning Routine with Kivi
GRADE:          All ages
DIFFICULTY:     Pre-Easy
TYPE:           social-story / read-along
ACCOMMODATION:  Predictable structure · No sudden sound/visual changes
                · Progress bar visible always · Skip button always visible
PREDICTABLE:    true
AUDIO_FIRST:    false
TARGET_SIZE:    standard
MAX_DURATION:   No limit (child-paced)
FONT:           Nunito (standard — no dyslexia font for this profile)
XP:             5
COINS:          3

PAGES: (social stories use page format — see Story Template)
  Page 1: "In the morning, I wake up."
           Illustration: Kivi waking up peacefully in bed, morning light.
  Page 2: "First, I wash my face."
           Illustration: Kivi at a sink, step shown clearly.
  [... continue for all steps of morning routine ...]

SPEAK_LOAD:    "Good morning! Let's follow our morning routine with Kivi.
                We'll go step by step. Take your time."
SPEAK_OK:      "Well done! You read the whole story. Morning routines
                help our day feel calm and happy."
SPEAK_NO:      n/a (social stories have no wrong answer)

STATUS:         🔴
```

---

## 8. PRODUCTION STATUS TRACKER

Use this table in your Google Sheet — one row per content item:

| code | world | type | title | grade | speakLoad | speakOk | speakNo | content | illustration | audio | built | status |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| AI-T-001 | alphabet-island | activity | Tap the Letter A | Toddler | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 | 🔴 |

**Status key:** 🔴 Empty · 🟡 Draft · 🟢 Approved · ✅ Built into platform

---

## 9. PRODUCTION PRIORITY ORDER

Follow the v4 Master Activity Plan sequence exactly:

| Week | Focus | Items | Blocking? |
|---|---|---|---|
| 1–2 | AI-T-001→015 + MM-T-001→010 | 25 activities | None |
| 3–4 | SN-AU-001→020 + SN-AD-001→010 | 30 SN items | NEVER deprioritise |
| 5–6 | AI-PK-001→025 + MM-PK-001→025 | 50 activities | Week 1–2 complete |
| 7–8 | SS-K-001→020 + MM Music Toddler | 40 activities | Week 5–6 complete |
| 9–10 | Story Cove Pre-K + STR-001→025 | 45 items | |
| 11–12 | Creativity Kingdom Toddler→Pre-K + Coloring batch 1 | 65 items | |
| Month 2 | Kindergarten tier all worlds | 120+ items | |
| Month 3 | Grade 1–2 tier all worlds | 200+ items | |
| Month 4–5 | Grade 3–5 tier all worlds | 300+ items | |
| Ongoing | Games · Quizzes · Videos · Printables | All counts | Alongside tiers |

---

## 10. CONTENT QUALITY CHECKLIST

Before marking any item 🟢 Approved:

**Activities**
- [ ] All 3 Kivi Voice scripts written and reviewed
- [ ] `speakNo` teaches — does NOT say "Try again!" alone
- [ ] Question text at correct reading level for grade
- [ ] Distractors are plausible (not obviously wrong)
- [ ] XP and Coins match difficulty tier exactly
- [ ] Correct answer is at index 0 (shuffle handles display order)
- [ ] Tags include world, grade, skill, music:true/false

**Stories**
- [ ] Word count per page within range for grade tier
- [ ] Kivi narration script matches page text exactly
- [ ] All illustrations fully briefed (prompt + style + palette)
- [ ] Comprehension questions cover literal + inferential
- [ ] Song stories have melody brief + lyric draft

**Coloring Pages**
- [ ] Illustration prompt includes: style / outline weight / orientation / "no text in image"
- [ ] Color-by-number palette defined if applicable
- [ ] Linked to correct world and curriculum skill

**Special Needs**
- [ ] Accommodation field filled for every SN item
- [ ] ADHD items timed — max 5 minutes
- [ ] Fine motor items have 80px+ target note
- [ ] Dyslexia items have audio-first flag
- [ ] Autism items have predictable-structure flag

---

*Kivora Content Production Template v1.0 · June 2026*
*Cross-reference: `Kivora_Master_Activity_Plan_v4.md` · `kivora-platform-structure-v4.md`*
