# 🎓 Graduation Quest: The Memory Lane Arcade

A four-year side-scrolling arcade journey — **Freshman → Senior** — built as a single,
self-contained `index.html`. No build step, no external files, no internet required.

*For Klaire Ann Alvanza, from Christopher John Raagas (cyocyo).*

## ▶ How to play / run it

Just open **`index.html`** in any modern browser (double-click it, or drag it into a
browser tab). To send it to her, you can email the single file or host it anywhere
static (GitHub Pages, Netlify drop, etc.).

**Controls**
- Desktop: `Space` / `↑` / `W` to jump — press again in the air to **double-jump**.
- Mobile: **tap** anywhere on the play area to jump.

## 🕹️ What's in it

- **4 levels** with rising difficulty: Quad (Freshman) → Environmental Sciences hall
  (Sophomore) → midnight Library (Junior) → Graduation Stage boss rush (Senior).
- **GPA bar** as health (starts at 4.0, friendly "Retake Exam" retry, never a hard wall).
- **Power-ups**: ☕ speed, 🛡️ Study Group shield, ⭐ All-Nighter invincibility,
  and the one-time 👓 **Adviser's Guidance** from Sir A in the final boss.
- **The Spark** ✨ — a one-time golden beat late in Freshman year referencing the
  Tigpanuki Debate Society meeting where you two met.
- **Sir A arc** — a feared spotlight/pop-quiz obstacle who returns in Senior year as
  her supportive thesis adviser.
- 🍕 **Shakey's slice** running joke, once per level.
- **Multi-phase Capstone boss** (Literature Review → Field Data Collection → Defense).
- **Finale**: procedural fireworks, a typed diploma reading
  *"Klaire Ann Alvanza — Bachelor of Science in Environmental Science,"* an 8-tile
  scrapbook grid, and a typewriter scroll letter.
- **Procedural chiptune** (Web Audio API) — a per-year motif, no audio files.
- **Reduced-motion toggle** and **mute** button (top-right).
- **Best score + best time** saved in `localStorage`.

## ✏️ Customizing it (the personal touches)

Open `index.html` and look for these spots near the bottom of the `<script>`:

1. **The closing letter** — find `const NOTES = [`. Edit the text, and add more
   authors (parents, siblings, friends) by adding objects:
   ```js
   const NOTES = [
     { author:'Christopher John Raagas (cyocyo)', text:'...', color:'#8B5E3C' },
     { author:'Mom & Dad', text:'We are so proud of you.', color:'#E08B8B' },
   ];
   ```

2. **The Spark line** — find `const SPARK_LINE =` to reword the meeting moment.

3. **The scrapbook photos** — find `const PHOTO_TILES = [`. Each tile currently shows
   an emoji + caption. To drop in real photos, replace the emoji rendering with an
   `<img>` (the tiles and modal are plain DOM in the finale section).

4. **Difficulty / pacing** — each level's `speed`, `spawnMin/Max`, and `goal` live in
   the `LEVELS` array near the top of the script.

Everything is heavily commented and grouped into clear sections (setup, audio,
level data, entities, rendering, game loop, finale).
