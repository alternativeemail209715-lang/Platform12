# UPDATE 172 - 80 GAMES, NO "ONE-PLAYER CHAT" GAMES

## What changed and why
You asked for games where the whole chat is NOT one single player, that tolerate the delay of TikTok comments, and a platform total of **80 games including Team Arena**.

**Platform total: 33 earlier games (incl. Team Arena) + 47 arcade games = 80.**

### 1. Collective games removed or reworked
| Game (update 171) | Problem | Now |
|---|---|---|
| Pick a Side, Higher or Lower | the chat votes as one | **removed** |
| Number Hunt | the chat narrows one number together | **replaced** by *Closest Wins* (everyone gives ONE hidden estimate) |
| Chain Reaction | one shared chain | **removed** |
| Word Rain | one shared city and hearts, needs fast typing | **removed** |
| Ladder Climb | one shared ladder | **reworked** into *Ladder Link* (find the one middle word; every viewer answers alone) |
| Quiz Rush | live vote bars | bars **removed** - every viewer's choice is private, everyone who is right scores |
| Team Arena: Number Hunt Duel, Chain Reaction Clash, Word Rain Battle, Connect Four Clash | whole team acts as one player | **removed**, replaced by 25 individual-answer team formats (below) |

Kept on purpose: **Hangman Live** (you asked for it; letters are shared on one board but every viewer scores for their own letters and guesses) and **Name 'Em All** (a shared answer board, but viewers compete - each answer scores for the viewer who found it).

### 2. Built for TikTok chat delay
- Every "race" game now has a **Who scores** setting. Default = **everyone who answers correctly before the clock stops scores** (small early-bird bonus for the first three, optional "end the round after N correct viewers"). The typed answer is hidden in the chat window until the round ends, so nobody can copy it. "Only the first correct answer" is still available.
- Answer windows are generous (20-90 seconds); nothing needs split-second control.
- Estimation games (Closest Wins, Distance Duel, Target Number) collect one answer per viewer and decide when the clock stops.
- Multiple-choice games (Quiz Rush, Spell Check, Survivor Quiz) lock each viewer's first answer and score everyone who is right.

### 3. The 47 arcade games (all share one engine: `server/arcade/`)
**From update 171 (12, reworked where noted)**
- **Hangman Live** (`/hangman/`) - Type a letter - or the whole word! Unlimited tries, so the whole chat can play together.
- **Missing Vowels** (`/vowels/`) - The vowels ran away! Type the word they left behind.
- **Odd One Out** (`/oddone/`) - Three belong together. One doesn't. Find the intruder!
- **Emoji Decoder** (`/emoji/`) - A few emojis. One answer. Can the chat crack the code?
- **Capital Quest** (`/capital/`) - Flags, countries and capitals from all over the world. How far can the chat travel?
- **Math Blitz** (`/math/`) - Quick sums, quicker fingers - first correct number wins!
- **Speed Typist** (`/typist/`) - A phrase flashes up - the fastest, cleanest typist in the chat wins.
- **Quiz Rush** (`/quiz/`) - Four answers - type A, B, C or D. Everybody who is right when the clock stops scores.
- **Simon Chat** (`/simon/`) - Watch the colours flash, then type them back in order. Each win makes the pattern longer!
- **Secret Code** (`/cipher/`) - A secret message in code - crack it before the chat does!
- **Name 'Em All** (`/nameall/`) - A category. Everybody types answers. Every answer counts once - how many can the chat find?
- **Ladder Link** (`/ladder/`) - COLD → ? → CORD. Find the word that is ONE letter away from both!

**New in update 172 (35)**
- **Missing Letter** (`/missing/`) - Some letters have fallen out of a word. Put them back!
- **Pattern Match** (`/pattern/`) - “Name an ANIMAL that starts with B.” Everybody finds as many answers as they can - your list is yours alone!
- **Spell Check** (`/spellcheck/`) - Which spelling is right? One of the choices is the real word.
- **Hidden Word** (`/hidden/`) - A word is hiding inside a jumble of letters. Can you spot it?
- **Link Word** (`/linkword/`) - Which word goes before one and after the other? BIRTH ___ LIGHT → DAY!
- **Word Twins** (`/twins/`) - Type the OPPOSITE - or the word that means the SAME.
- **Finish the Proverb** (`/proverb/`) - A famous saying is missing its last words. Can you finish it?
- **Initials Game** (`/initials/`) - J.K.R.? A.E.? Only the initials are shown - who or what is it?
- **Riddle Me This** (`/riddle/`) - A classic riddle with a one-word answer. Think outside the box!
- **Roman Rush** (`/roman/`) - XLVII is…? Convert Roman numerals to numbers and back!
- **Next in Line** (`/sequence/`) - 2, 4, 8, 16, … what comes next? Find the pattern!
- **Missing Sign** (`/sign/`) - 7 ? 3 = 21 - which sign is missing?
- **Percent Power** (`/percent/`) - 25% of 80? 3/4 of 120? A jacket with 30% off? Quick mental maths with percentages.
- **Clock Maths** (`/clock/`) - It is 9:45. What time will it be in 2 h 30 min? Time maths on the 24-hour clock.
- **Binary Buzz** (`/binary/`) - 1011 in binary is…? Convert between binary, decimal and hex.
- **Make 24** (`/make24/`) - Use all four numbers once each, with + − × ÷ and brackets, to make exactly 24.
- **Target Number** (`/target/`) - Six numbers, one target. Combine them with + − × ÷ to reach it - or get as close as you can!
- **Closest Wins** (`/closest/`) - How tall? How long? How many? Everybody gives ONE estimate - the closest one wins!
- **Distance Duel** (`/distance/`) - How many kilometres between two cities? One estimate each - the closest wins!
- **Continent Check** (`/continent/`) - Which continent is this country on? Easy, until it isn't!
- **City Spotter** (`/cityspot/`) - A city from somewhere in the world - which country is it in?
- **Town Spotter** (`/townspot/`) - A town or city from Malaysia - which state is it in?
- **Landmark Hunt** (`/landmark/`) - Famous places and monuments - in which country do you find them?
- **Currency Quest** (`/currency/`) - Yen, ringgit, baht, rand… which money does this country use?
- **Flag Zoom** (`/flagzoom/`) - A tiny piece of a flag, hugely zoomed in. The longer you wait, the more you see - but the fewer points!
- **Periodic Pop** (`/element/`) - Au is gold. Fe is iron. How well do you know the periodic table?
- **Colour Clash** (`/stroop/`) - The word says one colour, the ink shows another. Which one are you asked for?
- **Count Up** (`/countup/`) - Count the hidden treasures in a crowd of look-alikes!
- **Odd Emoji Out** (`/oddemoji/`) - One emoji in the grid is slightly different. Find it and type its position!
- **Memory Tray** (`/tray/`) - Memorise the tray - then spot the one thing that vanished!
- **Emoji Equations** (`/emojimath/`) - 🍎 + 🍎 + 🍎 = 12 - so what's 🍌 worth? Solve the picture puzzle!
- **Mystery Country** (`/mystery/`) - Clues appear one by one. Guess the country early for the most points!
- **Trivia Time** (`/trivia/`) - General knowledge questions - type the answer, no multiple choice!
- **Kuiz Malaysia** (`/kuiz/`) - How well do you know Malaysia? Food, places, history and culture - type the answer!
- **Survivor Quiz** (`/survivor/`) - Answer wrong - and you're out! The last survivors win the crown.

Every arcade game has: the platform's tabbed settings window (Gameplay / Hints / Connection / Look & sound / Customize / Scores & feedback) with the same organised sections as WORD SHUFFLE, Test / Offline / Live modes, TikTok auto-chat, host controls, AFK Autopilot support, a home card, its own colours and banner emojis, a floating chat window, winner / leaderboard / final windows and a Customize list.

### 4. TEAM ARENA (59 formats)
Still contains every game from Platform 8, 9 and 10 (see CHANGES_UPDATE_171.md). The "Arcade clashes" group is now **25 formats** where every player answers on their own and the first team with a correct answer wins the round (or, for estimation games, the closest team): Hangman Showdown, Missing Vowels Rush, Odd One Out Rush, Emoji Decoder Duel, Secret Code Duel, Speed Typist Duel, Pattern Memory Duel, Make 24 Duel, Closest Wins Duel, Mystery Country Duel, Missing Letter Rush, Hidden Word Hunt, Link Word Duel, Riddle Duel, Landmark Duel, Periodic Pop Duel, Colour Clash Duel, Odd Emoji Out Duel, Count Up Duel, Next in Line Duel, Flag Zoom Duel, Memory Tray Duel, Emoji Equations Duel, Target Number Duel, Word Twins Duel. All support the Series Rounds option.

## Databases
Word Shuffle categories (89 themed, incl. "My puzzles"), the platform's flag / country list, 6,000-city and 2,500-place Malaysian databases, EN / MS / ID dictionaries, 427 world + 138 Malaysian trivia questions, and new hand-made banks: 119 emoji riddles, 36 link-word puzzles, 100+ opposite / synonym pairs, 39 riddles, 97 landmarks, 72 currencies, 41 elements, 50 proverbs (English + Malay), 41 memory-tray objects.

## Notes
- Flag pictures (Capital Quest, Continent Check, Currency Quest, Flag Zoom, Mystery Country) load from flagcdn.com, as in Flagle.
- Files: `server/arcade/` (engine, mount, data, content, games-a/b/c/d, public/arcade.js, boards.js, arcade.css, boards.css); `server/teamarena/games-arcade.js`; registrations in `server.js`, `home-cards-store.js`, `engagement-hub.js`, `autopilot-config.js`, `public/index.html`, `home.js`, `home-views.js`, `platform-sync.js`, `records-ui.js`, `theme.js`, `game-chrome.css`, `ng-cards.css`, `game-customize.js`.
