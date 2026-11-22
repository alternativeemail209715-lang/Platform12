# UPDATE 173 - 100 GAMES, BOTS, FOUR-TEAM ARENA, BOSS ATTACK MAP

## Platform total: **100 games** (33 earlier games incl. Team Arena + 67 arcade games)

## 1. 20 new learning games (added value, none is a "lucky wheel")
Every game teaches or trains a real skill, every viewer answers on their own, everyone who is right in time scores, and the default difficulty is medium.

| Game | What it trains |
|---|---|
| **Vocabulary Builder** (`/vocab/`) | learn 54 useful English words by meaning |
| **Idiom Meaning** (`/idiom/`) | understand 40 English idioms native speakers use |
| **Confusing Words** (`/confuse/`) | fix the 43 most common grammar slips (their/there, its/it's, prepositions, tenses) |
| **Irregular Verbs** (`/verbs/`) | master 64 irregular verbs - the biggest stumbling block in English |
| **Terjemah** (`/terjemah/`) | practise English ↔ Melayu / Indonesia, including the words that differ between the two |
| **Animal Families** (`/animalfam/`) | learn baby, group, sound, home and gender words for animals |
| **Solve for X** (`/algebra/`) | practise solving linear equations step by step |
| **Geometry Bites** (`/geometry/`) | area, perimeter, angles and circles with the shape drawn |
| **Number Sense** (`/numsense/`) | GCD, LCM, remainders and prime factors - skills behind fractions |
| **Money Math** (`/money/`) | change, discounts, tax, tips and bill splitting - everyday money skills |
| **Fractions & Decimals** (`/fractions/`) | convert, simplify and add fractions |
| **Chart Reader** (`/chart/`) | data literacy: read a bar chart and answer questions |
| **State Capitals** (`/statecap/`) | know the capitals of Malaysian, US and Australian states |
| **Time Zone Hop** (`/timezone/`) | convert times between cities - useful for calls and travel |
| **Dial Code Dash** (`/dialcode/`) | know 60 international calling codes |
| **Food Origins** (`/foodorigin/`) | learn food culture across 64 dishes |
| **Inventors** (`/inventor/`) | learn who made the key inventions and discoveries |
| **Sports IQ** (`/sports/`) | rules, hosts and records of popular sports |
| **Morse Decoder** (`/morse/`) | learn Morse code by decoding words |
| **Calendar Quest** (`/calendar/`) | weekday / month arithmetic, date gaps and leap years |

Content bank: 54 vocabulary words, 40 idioms, 43 grammar sentences, 64 irregular verbs, 71 EN/MS/ID word triples, 58 animal questions, 70 state capitals, 25 time-zone cities, 60 dial codes, 64 dishes, 39 inventor questions, 40 sports questions.

## 2. Design, layout and defaults for all 67 arcade games
- **No scrolling and nothing clipped.** I measured every game on two Android sizes (360×700 and 412×892): no page scrolls, no board is clipped, nothing overflows sideways. The only intended clip is Flag Zoom's zoomed-in picture.
- **Board architecture fits each game:** letter tiles (Hangman, Missing Letter, Hidden Word), option buttons (Quiz Rush, Spell Check, Vocabulary, Idioms, Survivor), flag/geo cards, big equation cards (maths), drawn shapes (Geometry), bar charts (Chart Reader), dot-and-dash boxes (Morse), emoji grids with coordinates (Odd Emoji Out, Count Up, Memory Tray), picture equations, a zoom box (Flag Zoom). Long words and long options shrink automatically instead of wrapping mid-word.
- **Default difficulty = medium everywhere:** e.g. Next in Line starts at the squares/Fibonacci level, City Spotter and Town Spotter use big + medium places, Continent Check hides the six-continent hint, Missing Sign mixes one and two signs, Emoji Equations includes multiplication, Roman Rush goes to 200. Every game keeps easy / hard options in Settings.

## 3. Settings: all working
- Every game has the platform's tabbed settings window (Gameplay / Hints / Connection / Look & sound / Customize / Scores & feedback) with the same sections as WORD SHUFFLE.
- **Tested:** 6,300+ setting variants (every setting at its minimum, maximum and every option, plus random combinations) ran real rounds with bots - zero errors. Static check: every setting is read by the game or engine that owns it. The test found and fixed 4 edge-case bugs (Hangman bots with whole-word guessing off, Name 'Em All with extreme limits, Ladder Link with 3-letter words, Morse Decoder with a narrow length range).

## 4. Test mode: bots and human typing
- **Fake viewers are ON by default in Test mode** in all 67 arcade games (they answer by themselves, with adjustable speed and skill). "Make a fake viewer answer correctly" always types a valid answer.
- **Human typing works in every game:** tested through the real server mount - a typed answer in the guess box scored in all 67 games.
- The 33 earlier games keep their own existing test modes (not changed in this update).

## 5. TEAM ARENA (75 formats)
- **Four teams, fair test bots:** 24 test bots (6 per team with 4 teams, 8 with 3, 12 with 2); bots now join several at a time, play like solvers (word duels pick real words that fit their team's clues, so they actually solve), and every bot action picks the TEAM first, then one of its bots - so no team is favoured. Tested: all 4-team formats ran repeatedly with 4 teams, every team acted and scored, nothing hung; formats that looked skewed were re-run 40-60 times and came out even.
- **Boss Battle shows who attacks whom:** a banner "WHO IS ATTACKING WHOM" (e.g. RED ⚔ ➜ BLUE's boss), each boss card lists its attackers (🎯 = aiming now, ⚔ = has dealt damage, with the damage dealt), plus a log of the latest hits. A correct answer always hits exactly the boss the team is shown to be aiming at.
- **16 new Arena formats** from the new games (Solve for X Duel, Geometry Duel, Number Sense Duel, Money Math Duel, Fractions Duel, Chart Reader Duel, Morse Decoder Duel, Time Zone Duel, State Capitals Duel, Dial Code Duel, Food Origins Duel, Inventors Duel, Sports IQ Duel, Irregular Verbs Duel, Animal Families Duel, Calendar Quest Duel) - 41 "Arcade clashes" in total.

## Files
`server/arcade/` (engine, mount, data, content 1-3, games-a to games-e, public/arcade.js, boards.js, arcade.css, boards.css), `server/teamarena/` (arena-core.js, games-dle.js, games-quiz.js, games-arcade.js, public/arena.js, arena.css) and the registrations in `server.js`, `home-cards-store.js`, `engagement-hub.js`, `autopilot-config.js`, `public/index.html`, `home.js`, `home-views.js`, `platform-sync.js`, `records-ui.js`, `theme.js`, `game-chrome.css`, `game-customize.js`.
