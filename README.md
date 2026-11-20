# CRAFT platform - UPDATE 171 (compact deploy build)

Same 6-file layout as before:

| File | Purpose |
|---|---|
| `package.json` | dependencies + `npm start` |
| `start.js` | launcher: unpacks `app.pack` into `app/` and starts the platform |
| `app.pack` | the entire platform (50 games, compressed) |
| `.env.example` | environment variable reference |
| `.gitignore` | keeps `app/`, `node_modules/`, runtime data out of git |
| `README.md` | this file |

## Deploy (Render)
1. Upload these files to GitHub (replace the previous files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged.
3. The first start prints `[launcher] unpacked N files`, then `[TEAMARENA] Mounted at /teamarena` and one `[HANGMAN] Mounted at /hangman` style line per new game. Saved settings under `app/data/` are never overwritten.

## What's new in 171
Full details are in `CHANGES_UPDATE_171.md` (inside the pack, at `app/CHANGES_UPDATE_171.md` after the first start).

1. **TEAM ARENA - one version above Platform 8, 9 and 10** (26 -> 45 formats). Restored the word duels that only existed in the older versions (Codedle, Shapedle, Colorblindle, Colordle, Structle, Comparable, Linedle) and Category Rush; Flagle Showdown now also shows distance + direction clues; world trivia grew from 235 to 427 questions. Nothing was removed.
2. **11 new Arena formats** ("Arcade clashes"): Hangman Showdown, Missing Vowels Rush, Odd One Out Rush, Emoji Decoder Duel, Secret Code Duel, Number Hunt Duel, Speed Typist Duel, Chain Reaction Clash, Word Rain Battle, Pattern Memory Duel and Connect Four Clash.
3. **HANGMAN LIVE** (`/hangman/`) - unlimited tries, answers from the Word Shuffle categories.
4. **16 new games**: Missing Vowels, Odd One Out, Emoji Decoder, Capital Quest, Math Blitz, Number Hunt, Speed Typist, Chain Reaction, Quiz Rush, Pick a Side, Higher or Lower, Ladder Climb, Word Rain, Simon Chat, Secret Code, Name 'Em All. Each has a home card, its own colours, the standard settings drawer, Test / Offline / Live modes, TikTok auto-chat, AFK Autopilot support and Customize.
