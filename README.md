# Premier League 2024/25 — Goal Rain

Every goal of the season, falling onto the pitch in the order it happened — an animated, playable visualization built from StatsBomb event data.

![Python](https://img.shields.io/badge/Python-3.10+-blue?style=flat-square&logo=python) ![SVG](https://img.shields.io/badge/Viz-SVG%20%2B%20JS-orange?style=flat-square) ![Data](https://img.shields.io/badge/Data-StatsBomb-red?style=flat-square)

---

## Live Demo

**[Open Goal Rain](https://leiderip.github.io/Premier-League-2024-25-Goal-Rain/Goal_Rain.html)**

---

## Features

- Every goal scored in the 2024/25 season falls from above onto its real shot location, in chronological order, leaving a permanent glowing mark
- Play / Pause, Restart, and Skip to End controls, with three playback speeds
- A live counter, progress bar, and a 'current leader' tag tracking the top scoring team as the season replays
- A info card shows the scorer, team, minute, and fixture for the most recent goal
- Optional **color-by-team** mode — toggle to see each club's goals in their own colour instead of a single rain colour
- **Dark / Light theme toggle**

---

## Method

Every `Shot` event with `outcome_name == "Goal"` across all 380 matches is collected with its real shot location, scorer, team, and minute. Own goals (StatsBomb's `Own Goal For` event) are also included, credited to the benefiting team, though they don't carry a meaningful shot location so they're placed just in front of the goal mouth.

**On chronological order:** StatsBomb's flattened event export has no match date or gameweek column — only an internal numeric `match_id`. Goals are sorted by `(match_id, minute)` ascending as the closest available proxy for real fixture order. This tracks the season closely in practice, but is not a verified calendar-date replay.

---

## Portfolio

| Project | Link |
|---|---|
| Title Race | [Live](https://leiderip.github.io/Premier-League-2024-25-Title-race/pl_position_race.html) |
| xG Race Explorer | [Live](https://leiderip.github.io/Premier-League-2024-25-xG-Title-race-/xG_Race_Explorer.html) |
| Season Shot Map | [Live](https://leiderip.github.io/Premier-League-2024-25-Shot-Map/Shot_Map.html) |
| Top Scorers vs xG | [Live](https://leiderip.github.io/Premier-League-2024-25-Top-Scorers-xG/Top_Scorers_xG.html) |
| Player Heatmap | [Live](https://leiderip.github.io/Premier-League-2024-25-Player-Heatmap/Player_Heatmap.html) |
| Scouting Radar | [Live](https://leiderip.github.io/Premier-League-2024-25-Scouting_Radar/Scouting_Radar.html) |
| Pass Network | [Live](https://leiderip.github.io/Premier-League-2024-25-Pass-Network/Pass_Network.html) |
| Match Momentum | [Live](https://leiderip.github.io/Premier-League-2024-25-Match-Momentum/Match_Momentum.html) |
| Goalkeeper Performance | [Live](https://leiderip.github.io/Premier-League-2024-25-Goalkeeper-Performance/Goalkeeper_Performance.html) |
| Attacking Bands | [Live](https://leiderip.github.io/Premier-League-2024-25-Attacking-Bands/Attacking_Bands.html) |
| Set Piece Threat | [Live](https://leiderip.github.io/Premier-League-2024-25-Set-Piece-Threat/Set_Piece_Threat.html) |
| Goal Rain | This project |

---

*Data © StatsBomb.*
