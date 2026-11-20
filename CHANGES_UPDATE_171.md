# UPDATE 171 - TEAM ARENA merged + HANGMAN LIVE + 16 NEW GAMES

Built on the most advanced of the three update-170 versions (Platform10) and enriched with everything the other two (Platform8, Platform9) had and Platform10 did not. No game was removed.

## 1. TEAM ARENA - one version above all three (26 -> 45 formats)

**What each version had** (all three share the 12 base games: Tug of War, Territory, Relay, Boss, Capture the Word, Team Memory, Team Sudoku, Geo Showdown, Duels, Bracket, Last Letter Standing, Team Blossom).

| Game / feature | P8 | P9 | P10 | In 171 |
|---|---|---|---|---|
| Blindle, Oracle, Shiftle, Forbackle, Rangedle, Fixle, Betweendle, Number Blindle | partly | partly | yes | kept (P10 engine) |
| Codedle, Shapedle, Colorblindle, Colordle, Structle, Comparable | yes | yes | - | **restored**, rebuilt on the P10 engine with a header above each team board |
| Linedle | - | yes | - | **restored** (wave line per team) |
| PIN Breaker | yes | - | - | merged into Number Blindle Duel (same game: bulls & cows with digits) |
| Category Rush | yes | - | - | **restored + upgraded** (uses all Word Shuffle categories, points per answer) |
| Word Hunt / Boxdle Hunt, Expandle, Findle | yes | yes | yes | kept P10's (richest: bonus words, Findle, Boxdle) |
| Flag Showdown / Flagle Showdown | sharpening + distance | simple | blurred | P10's blur + **version 8's distance & direction clues** (km / mi) |
| Shuffle Showdown / Travle Race | - | - | yes | kept |
| Trivia pool | 138 local | 235+ | 235 | **427 world questions** (P9's extra pack merged) |
| Series Rounds, join words, per-game options, 14 Tug types | partly | partly | yes | kept |

**New in Team Arena (11 formats, group "Arcade clashes")** - the new interactive games of the platform rebuilt for teams, same puzzles and answer databases:
Hangman Showdown (unlimited tries), Missing Vowels Rush, Odd One Out Rush, Emoji Decoder Duel, Secret Code Duel, Number Hunt Duel, Speed Typist Duel, Chain Reaction Clash, Word Rain Battle, Pattern Memory Duel and **Connect Four Clash** (team vs team; each team votes a column 1-7 every turn).
They run through `games-arcade.js` ("ArcadeBridge"), so any future arcade game can be added to the Arena in a few lines.

New / changed files: `server/teamarena/games-dle2.js`, `games-more.js`, `games-arcade.js`, `arena-trivia2.js`; `games-flag.js`, `games-dle.js`, `formats.js`, `arena-content.js`, `arena-quizgen.js`, `public/arena.js`, `public/arena.css`, `public/index.html`.

## 2. HANGMAN LIVE (new platform game, /hangman/)
Unlimited tries, built for audiences: a category and blanks, viewers type letters or the whole word. Every revealed letter scores; the rope friend is rescued after 7 wrong letters and the rope resets, so nobody ever loses. Answers come from the 89 themed **Word Shuffle categories** (plus the host's own "My puzzles"). Settings: category choice, word length, number of words, whole-word guessing, optional no-time-limit, pre-revealed letters, points per letter / finish / rescue, hints.

## 3. SIXTEEN NEW GAMES
2. **Missing Vowels** (`/vowels/`) - The vowels ran away! Type the word they left behind.
3. **Odd One Out** (`/oddone/`) - Three belong together. One doesn't. Find the intruder!
4. **Emoji Decoder** (`/emoji/`) - A few emojis. One answer. Can the chat crack the code?
5. **Capital Quest** (`/capital/`) - Flags, countries and capitals from all over the world. How far can the chat travel?
6. **Math Blitz** (`/math/`) - Quick sums, quicker fingers - first correct number wins!
7. **Number Hunt** (`/numhunt/`) - A secret number is hiding. The chat narrows it down together - who lands on it?
8. **Speed Typist** (`/typist/`) - A phrase flashes up - the fastest, cleanest typist in the chat wins.
9. **Chain Reaction** (`/chain/`) - Every word must start with the LAST letter of the one before. How long can the chat keep the chain alive?
10. **Quiz Rush** (`/quiz/`) - Four answers, one winner... or everyone! Type A, B, C or D and watch the votes climb.
11. **Pick a Side** (`/pickside/`) - This or that? The whole chat votes - and the crowd decides!
12. **Higher or Lower** (`/hilo/`) - One number is shown, one is hidden. Is the hidden one higher or lower? The chat decides!
13. **Ladder Climb** (`/ladder/`) - Change ONE letter at a time to climb from the start word to the target. The whole chat builds the ladder!
14. **Word Rain** (`/rain/`) - Words fall from the sky - type them before they hit the ground!
15. **Simon Chat** (`/simon/`) - Watch the colours flash, then type them back in order. Each win makes the pattern longer!
16. **Secret Code** (`/cipher/`) - A secret message in code - crack it before the chat does!
17. **Name 'Em All** (`/nameall/`) - A category. Everybody types answers. Every answer counts once - how many can the chat find?

Every game has the same organised settings drawer as WORD SHUFFLE (tabs: Play / Hints / Scores / Connect / Look), a Test / Offline / Live mode, TikTok auto-chat, host controls, AFK Autopilot support, a home card, themed colours, a floating chat window, winner and leaderboard windows, a final screen and a Customize list. All 17 run on one shared engine (`server/arcade/`).

## Files
`server/arcade/` (engine, mount, data, content, games-a.js, games-b.js, public/arcade.js, boards.js, arcade.css, boards.css) and the registrations in `server.js`, `home-cards-store.js`, `engagement-hub.js`, `autopilot-config.js`, `public/index.html`, `home.js`, `home-views.js`, `platform-sync.js`, `records-ui.js`, `theme.js`, `game-chrome.css`, `ng-cards.css`, `game-customize.js`.
