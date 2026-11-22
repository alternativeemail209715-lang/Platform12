# CRAFT platform - UPDATE 173 (compact deploy build)

Same 6-file layout as before:

| File | Purpose |
|---|---|
| `package.json` | dependencies + `npm start` |
| `start.js` | launcher: unpacks `app.pack` into `app/` and starts the platform |
| `app.pack` | the entire platform (100 games, compressed) |
| `.env.example` | environment variable reference |
| `.gitignore` | keeps `app/`, `node_modules/`, runtime data out of git |
| `README.md` | this file |

## Deploy (Render)
1. Upload these files to GitHub (replace the previous files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged.
3. The first start prints `[launcher] unpacked N files`, then `[TEAMARENA] Mounted at /teamarena` and one `[HANGMAN] Mounted at /hangman` style line for each of the 67 arcade games. Saved settings under `app/data/` are never overwritten.

## What's new in 173 (details: `CHANGES_UPDATE_173.md`)
1. **100 games**: 20 new learning games (vocabulary, idioms, grammar, irregular verbs, English-Melayu-Indonesia translation, animal words, algebra, geometry, number sense, money maths, fractions, chart reading, state capitals, time zones, dial codes, food origins, inventors, sports, Morse code, calendar maths).
2. **Design pass on all 67 arcade games**: board layouts that fit each game, no scrolling on Android phone sizes, long words/options auto-shrink, medium default difficulty.
3. **Settings audit**: 6,300+ setting variants tested with real rounds - all working; 4 edge-case bugs fixed.
4. **Test mode**: fake viewers on by default in every arcade game; human typing verified in all 67.
5. **Team Arena (75 formats)**: fair bots with 4 teams (6 per team), smarter word-duel bots, 16 new formats, and Boss Battle now shows which team is attacking which boss.
