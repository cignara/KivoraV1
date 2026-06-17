# Kivora – Site Map
### Version 4.0 · Aligned with `Kivora_Master_Activity_Plan.md` (v4, corrected) · June 2026
### Single Launch · All 9 Worlds · Ages 2–11 · English Only · Worldwide Audience

> **Changelog from v3.0:**
> - Audience reframed from "USA · UK" to **worldwide**. Curriculum-alignment language now presents Common Core (USA) and the UK National Curriculum as named reference frameworks *within* a broader international-standards alignment, rather than as the platform's market boundary. Compliance frameworks tied to specific jurisdictions (COPPA, GDPR-K, UK GDPR, FERPA, Ofsted-ready reporting) are retained as-is, since these are actual regulations rather than audience markers — a platform serving worldwide families can still offer region-specific compliance for the families who need it.
>
> **Changelog from v2.0 (carried forward):**
> - Activity total corrected from 900 → **840** (sum of per-world activity counts as specified in the Master Activity Plan body: 110+130+80+65+120+90+100+80+65). The 900 figure was a stale summary-table value that did not match the per-world breakdown; Special Needs' 145 items remain a separate cross-world bucket and are not part of the 840.
> - Per-world activity counts corrected to match Master Activity Plan world headers: Math Mountain 110→**130**, Story Cove 100→**80**, Creativity Kingdom 100→**65**, Brain Game Galaxy 90→**100**, Life Skills Village 85→**80**, Coding City 105→**65**.
> - All Sinhala/Tamil language routes, bilingual learning paths, and language-selector references removed. English is the sole working language at launch. Sri Lankan-themed *content* (festivals, folk tales, coloring categories) is retained as content variety, not as a language feature.
> - `/bilingual/*` routes removed. `PATH-024`, `PATH-025` (Sinhala/Tamil language learning paths) and `LP-049`, `LP-050` (bilingual lesson plans) removed from learning paths and lesson plan listings — reducing Learning Paths from 26 to **24** and Lesson Plans from 60 to **58**.

---

## 1. Home (`/`)
- Hero section — 9 worlds, all at launch
- Grade explorer (Toddler → Grade 5 + Special Needs)
- Trust bar (partner logos)
- Stats: 840 Activities · 280 Games · 300 Stories · 160 Videos · 280 Quizzes · 600 Coloring Pages · 550 Printables · 140 Crafts

---

## 2. Learning Worlds (`/worlds`)

All 9 worlds open at launch — no locks, no phases.

| World | Slug | Subject Focus | Activities |
|---|---|---|---|
| 🏝️ Alphabet Island | `/worlds/alphabet-island` | Literacy · Phonics · Vocabulary · Grammar | 110 |
| ⛰️ Math Mountain | `/worlds/math-mountain` | Numeracy · Problem-Solving · Algebra · Geometry | 130 |
| 🌊 Story Cove | `/worlds/story-cove` | Reading · Comprehension · Creative Writing | 80 |
| 🎨 Creativity Kingdom | `/worlds/creativity-kingdom` | Art · Fine Motor · Creative Expression | 65 |
| 🔬 Science Safari | `/worlds/science-safari` | STEM · Life Science · Earth Science · Physics | 120 |
| 🎵 Music Meadow | `/worlds/music-meadow` | Music Theory · Rhythm · Instruments · Songwriting | 90 |
| 🧠 Brain Game Galaxy | `/worlds/brain-game-galaxy` | Logic · Critical Thinking · Puzzles · Strategy | 100 |
| 🏘️ Life Skills Village | `/worlds/life-skills-village` | Social-Emotional · Financial · Digital Citizenship | 80 |
| 💻 Coding City | `/worlds/coding-city` | Block Coding · Text Coding · Debugging · Digital Literacy | 65 |
| | | **Total** | **840** |

### Each World Page (`/worlds/{slug}`) contains:
- World overview and Kivi intro (narrated)
- Grade-tier selector (Toddler → Grade 5)
- Activities for this world
- Games for this world
- Quizzes for this world
- Stories linked to this world
- Videos linked to this world
- Coloring pages for this world
- Learning paths through this world
- Printables and crafts for this world

---

## 3. Activities (`/activities`)

### 3.1 Browse All Activities (`/activities`)
- Filter by World (all 9)
- Filter by Grade (Toddler · Pre-K · K · Grade 1–5 · Special Needs)
- Filter by Difficulty (Pre-Easy · Easy · Intermediate · Advanced · Master)
- Total: **840 activities** (plus 145 Special Needs items, browsable separately)

### 3.2 By Grade
- `/activities/toddler` — Ages 2–3
- `/activities/pre-k` — Ages 3–4
- `/activities/kindergarten` — Age 5
- `/activities/grade-1` — Age 6
- `/activities/grade-2` — Age 7
- `/activities/grade-3` — Age 8
- `/activities/grade-4` — Age 9
- `/activities/grade-5` — Ages 10–11
- `/activities/special-needs` — All ages

### 3.3 By World (each world has its activity subsection)
`/activities/alphabet-island` · `/activities/math-mountain` · `/activities/story-cove` ·
`/activities/creativity-kingdom` · `/activities/science-safari` · `/activities/music-meadow` ·
`/activities/brain-game-galaxy` · `/activities/life-skills-village` · `/activities/coding-city`

---

## 4. Games (`/games`)

Total: **280 games**

| Route | Games | World |
|---|---|---|
| `/games` | 280 | All games |
| `/games/alphabet-island` | 30 | Alphabet Island |
| `/games/math-mountain` | 40 | Math Mountain |
| `/games/story-cove` | 20 | Story Cove |
| `/games/creativity-kingdom` | 10 | Creativity Kingdom |
| `/games/science-safari` | 40 | Science Safari |
| `/games/music-meadow` | 25 | Music Meadow |
| `/games/brain-game-galaxy` | 40 | Brain Game Galaxy |
| `/games/life-skills-village` | 20 | Life Skills Village |
| `/games/coding-city` | 20 | Coding City |
| `/games/special-needs` | 15 | Inclusive / cross-world |

Filter tabs: All · Alphabet Island · Math Mountain · Science Safari · Brain Game Galaxy · Music Meadow · Life Skills Village · Coding City · Creativity Kingdom · Story Cove

---

## 5. Quizzes (`/quizzes`)

Total: **280 quizzes**

| Route | Quizzes | World |
|---|---|---|
| `/quizzes` | 280 | All quizzes |
| `/quizzes/alphabet-island` | 30 | Alphabet Island |
| `/quizzes/math-mountain` | 40 | Math Mountain |
| `/quizzes/story-cove` | 30 | Story Cove |
| `/quizzes/creativity-kingdom` | 10 | Creativity Kingdom |
| `/quizzes/science-safari` | 40 | Science Safari |
| `/quizzes/music-meadow` | 25 | Music Meadow |
| `/quizzes/brain-game-galaxy` | 40 | Brain Game Galaxy |
| `/quizzes/life-skills-village` | 20 | Life Skills Village |
| `/quizzes/coding-city` | 20 | Coding City |
| `/quizzes/special-needs` | 25 | Inclusive / cross-world |

---

## 6. Stories (`/stories`)

Total: **300 stories**

- `/stories` — All stories
- `/stories/by-age` — Filter by age (2–3 · 3–4 · 5 · 6 · 7 · 8 · 9 · 10–11)
- `/stories/by-grade` — Filter by grade
- `/stories/by-theme` — Adventure · Nature · Friendship · Festivals · Science · Coding
- `/stories/by-world` — Linked to Story Cove and other worlds
- `/stories/bedtime` — Bedtime Stories Pack (20 stories)

---

## 7. Videos (`/videos`)

Total: **160 videos**

- `/videos` — All videos
- `/videos/by-subject` — Literacy · Maths · Science · Music · Creativity · Life Skills · Coding
- `/videos/by-grade` — All grade tiers
- `/videos/by-world` — All 9 worlds

---

## 8. Coloring Pages (`/coloring`)

Total: **600 pages**

- `/coloring` — All coloring pages (browse by category)
- `/coloring/alphabet` — Alphabet & Letters A–Z (52 pages)
- `/coloring/numbers` — Numbers & Math Scenes (20 pages)
- `/coloring/animals` — Animals — Sri Lanka & World (78 pages)
- `/coloring/nature` — Fantasy & Nature Scenes (60 pages)
- `/coloring/festivals-srilanka` — Sri Lankan Festivals (20 pages)
- `/coloring/festivals-world` — World Festivals (30 pages)
- `/coloring/science` — Science Safari Scenes (40 pages)
- `/coloring/coding` — Coding City Scenes (20 pages)
- `/coloring/kivi` — Kivi Character Poses (40 pages)
- `/coloring/mandalas` — Mandalas & Patterns (40 pages)
- `/coloring/seasonal` — Seasonal (4 seasons) (20 pages)
- `/coloring/geography` — Geography & World Maps (20 pages)
- `/coloring/art` — Creative Kingdom Art (60 pages)
- `/coloring/certificates` — Printable Certificates (60 pages)
- `/coloring/crafts-sheets` — Crafts & Activity Sheets (110 pages)

### Coloring Tool
- `/coloring/play/{id}` — On-screen coloring tool (Color-by-Number or Free Paint)
  - Save to gallery
  - Download as PNG
  - Print

---

## 9. Printables (`/printables`)

Total: **550 printables**

- `/printables` — All printables
- `/printables/worksheets` — 180 worksheets (all subjects, all grades)
- `/printables/activity-sheets` — 120 activity sheets
- `/printables/flashcards` — 80 flashcard sets
- `/printables/certificates` — 60 achievement certificates
- `/printables/lesson-plans` — 58 lesson plans (teacher access)
- `/printables/posters` — 50 classroom posters & displays

---

## 10. Crafts (`/crafts`)

Total: **140 crafts**

- `/crafts` — All crafts
- `/crafts/paper` — 40 paper crafts (origami, cut & fold, pop-ups)
- `/crafts/nature` — 25 nature crafts
- `/crafts/seasonal` — 30 seasonal crafts (festivals & calendar)
- `/crafts/science` — 25 science crafts
- `/crafts/recycled` — 20 recycled material crafts

---

## 11. Creativity Kingdom Hub (`/creativity-kingdom`)

Part of World 4 — accessible via `/worlds/creativity-kingdom` and `/creativity-kingdom`

- `/creativity-kingdom` — Hub overview
- `/creativity-kingdom/coloring` — → redirects to `/coloring`
- `/creativity-kingdom/drawing-studio` — 50 guided drawing projects
- `/creativity-kingdom/build-and-design` — 20 construction challenges
- `/creativity-kingdom/crafts` — → redirects to `/crafts`

---

## 12. Special Needs Hub (`/special-needs`)

Total: **145 items**

- `/special-needs` — Hub overview
- `/special-needs/autism` — 40 autism-friendly activities & social stories
- `/special-needs/dyslexia` — 35 dyslexia support activities
- `/special-needs/adhd` — 30 ADHD sprint-set activities
- `/special-needs/fine-motor` — 20 fine motor development activities
- `/special-needs/gifted` — 20 gifted & advanced enrichment activities
- `/special-needs/gentle-start` — Learning path: Gentle Start (PATH-023)

---

## 13. Learning Paths (`/paths`)

Total: **24 guided paths**

- `/paths` — All learning paths
- `/paths/{code}` — Individual path (e.g. `/paths/path-001`)

### Key Paths
- `PATH-001` Pre-K Literacy Foundations
- `PATH-002` Pre-K Numeracy Foundations
- `PATH-003` Kindergarten Phonics
- `PATH-004` Kindergarten Maths
- `PATH-005` Grade 1 Reading & Phonics
- `PATH-018` Coding City: Block Coding
- `PATH-019` Coding City: Text Coding
- `PATH-020` Music Meadow: Complete Journey
- `PATH-021` Life Skills Complete Path
- `PATH-022` Brain Game Galaxy: Logic Path
- `PATH-023` Special Needs: Gentle Start
- `PATH-026` Full Kivora Journey (all 9 worlds)

---

## 14. Parents (`/parents`)

### 14.1 Parent Overview (`/parents`)
- What Kivora offers for parents
- Feature highlights
- Curriculum alignment (international standards, with Common Core USA and UK National Curriculum as named reference frameworks)
- CTA to dashboard

### 14.2 Parent Dashboard (`/parents/dashboard`) — In-App
- Child profiles & progress across all 9 worlds
- Curriculum alignment view (Common Core, UK National Curriculum, and general international skill benchmarks)
- Screen time management
- Bedtime lock (default: 20:00)
- Weekly progress report preferences

### 14.3 Resources for Parents (`/parents/resources`)
- Blog & learning tips
- Curriculum guides (international, with USA and UK guides available)
- Newsletter sign-up

---

## 15. Teachers (`/teachers`)

### 15.1 Teacher Overview (`/teachers`)
- What Kivora offers for teachers
- Curriculum alignment (Common Core USA / UK National Curriculum / Ofsted-ready, plus general international primary curriculum benchmarks)
- Free classroom access sign-up

### 15.2 Teacher Hub — Dashboard (`/teachers/dashboard`) — In-App
- Class management (grade, student list, XP leaderboard)
- Student progress analytics per world and per curriculum standard
- Learning path assignment (per student or whole class)
- Activity assignment
- Skill gap detection
- Reports (Ofsted-ready for UK teachers; standard progress reports for all other regions)

### 15.3 Teacher Resources (`/teachers/resources`)
- 58 curriculum-aligned lesson plans
- Printables: worksheets, homework, tests, certificates
- Free classroom access sign-up

---

## 16. Featured Collections (`/collections`)

- `/collections` — All collections
- `/collections/bedtime-stories` — 🌙 Bedtime Stories Pack (20 stories · Ages 3–8)
- `/collections/number-ninja` — 🔢 Number Ninja Pack (25 games · Ages 5–10)
- `/collections/science-explorer` — 🔬 Science Explorer Pack (35 items · Ages 6–11)
- `/collections/creativity-starter` — 🎨 Creativity Kingdom Starter (30 items · Ages 3–8)
- `/collections/coding-launchpad` — 💻 Coding City Launchpad (20 activities · Ages 6–10)

---

## 17. Pricing (`/pricing`)

- Free plan
- Explorer plan ($9.99/month — all 9 worlds, full library)
- Family plan ($14.99/month — up to 4 children, Special Needs profiles)
- Schools & Enterprise (custom — teacher portal, lesson plans, FERPA/GDPR-K, Ofsted reports)
- Monthly / Annual toggle (Annual saves 17%)
- Full feature comparison table

---

## 18. Blog (`/blog`)

- `/blog` — All posts
- `/blog/learning-tips` — Learning tips for parents
- `/blog/teacher-resources` — Resources and ideas for teachers
- `/blog/curriculum` — Curriculum guides for families worldwide, including USA &amp; UK deep-dives

---

## 19. Company

- `/about` — About Kivora
- `/careers` — Careers
- `/privacy` — Privacy Policy (COPPA · GDPR-K · UK GDPR)
- `/terms` — Terms of Service
- `/compliance` — COPPA · GDPR-K · WCAG 2.1 · Ofsted details

---

## 20. Auth (Modals / Overlays)

- `#login` — Login
  - Email & password
  - SSO: Google · Apple · Microsoft
- `#register` — Register
  - Multi-step: Account type → Email → Child profile(s) → Grade → Curriculum preference (optional — Common Core USA, UK National Curriculum, or General International)

---

## 21. Child Dashboard (In-App, `#child-dashboard`)

- Continue Learning (resume in-progress activities)
- Today's Challenges (daily goals with XP)
- Explore All 9 Worlds (full world grid — all accessible)
- My Rewards (Stars · XP · Gems · Coins · Badges · Certificates)
- Kivi's Message (personalised narrated greeting)
- My Gallery (saved coloring artworks)
- Avatar & profile customisation

---

## 22. Parent Dashboard (In-App, `#parent-dashboard`)

- Child profiles overview
- Per-child progress across all 9 worlds
- Curriculum standard view (Common Core, UK National Curriculum, or General International — selectable per child)
- Screen time controls
- Bedtime lock (default: 20:00)
- Weekly report settings

---

## 23. Teacher Dashboard (In-App, `#teacher-dashboard`)

- Class management (add classes, add students)
- Student progress list with XP and activity count
- Skill gap analytics per curriculum standard
- Activity and learning path assignment
- Leaderboard view
- Ofsted-ready progress reports (UK)
- FERPA-compliant data handling (USA)

---

## URL Structure Summary

```
/                                    Home
/worlds                              All 9 Worlds
/worlds/{slug}                       Individual World
/activities                          All 840 Activities
/activities/{grade}                  By Grade
/activities/{world-slug}             By World
/games                               All 280 Games
/games/{world-slug}                  By World
/quizzes                             All 280 Quizzes
/quizzes/{world-slug}                By World
/stories                             All 300 Stories
/stories/{filter}                    By Age / Grade / Theme
/videos                              All 160 Videos
/videos/{filter}                     By Subject / Grade / World
/coloring                            All 600 Coloring Pages
/coloring/{category}                 By Category
/coloring/play/{id}                  On-screen Coloring Tool
/printables                          All 550 Printables
/printables/{category}               By Category
/crafts                              All 140 Crafts
/crafts/{category}                   By Category
/creativity-kingdom                  Creativity Kingdom Hub
/special-needs                       Special Needs Hub (145 items)
/special-needs/{area}                By Need Area
/paths                               All 24 Learning Paths
/paths/{code}                        Individual Path
/collections                         Featured Collections
/collections/{slug}                  Individual Collection
/parents                             Parent Overview
/parents/dashboard                   Parent Dashboard (in-app)
/parents/resources                   Parent Resources
/teachers                            Teacher Overview
/teachers/dashboard                  Teacher Hub (in-app)
/teachers/resources                  Teacher Resources & Lesson Plans
/pricing                             Pricing
/blog                                Blog & Tips
/about                               About Us
/careers                             Careers
/privacy                             Privacy Policy
/terms                               Terms of Service
/compliance                          Compliance Details
```

---

*Kivora Site Map v4.0 · Single Launch · All 9 Worlds · English Only · Worldwide Audience · June 2026*
*Source of truth: `Kivora_Master_Activity_Plan.md` (v4, corrected) · Supersedes: `kivora-sitemap-v3.md`*
