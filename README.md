# CRAFT platform - UPDATE 172 (compact deploy build)

Same 6-file layout as before:

| File | Purpose |
|---|---|
| `package.json` | dependencies + `npm start` |
| `start.js` | launcher: unpacks `app.pack` into `app/` and starts the platform |
| `app.pack` | the entire platform (80 games, compressed) |
| `.env.example` | environment variable reference |
| `.gitignore` | keeps `app/`, `node_modules/`, runtime data out of git |
| `README.md` | this file |

## Deploy (Render)
1. Upload these files to GitHub (replace the previous files).
2. Render: Build Command `npm install`, Start Command `npm start`. Environment variables are unchanged.
3. The first start prints `[launcher] unpacked N files`, then `[TEAMARENA] Mounted at /teamarena` and one `[HANGMAN] Mounted at /hangman` style line for each of the 47 arcade games. Saved settings under `app/data/` are never overwritten.

## What's new in 172
Full details: `CHANGES_UPDATE_172.md` (also inside the pack at `app/CHANGES_UPDATE_172.md` after the first start).

1. **80 games** on the platform (33 earlier games including Team Arena + 47 arcade games).
2. **No "whole chat is one player" games.** Voting, shared-chain, shared-rain and shared-ladder games were removed or reworked; every viewer now answers on their own.
3. **Built for TikTok chat delay.** Default scoring is "everyone who answers correctly before the clock stops scores"; answers stay hidden in the chat window until the round ends; windows are generous.
4. **35 new games** in word, maths, geography, quiz, estimation and visual categories - see the changelog.
5. **Team Arena: 59 formats**, including 25 "Arcade clashes" in which each player answers on their own.
