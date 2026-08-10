# The Knowledge

A browser game about learning a city with no map.

You drive a cab in a procedurally generated city. There is no minimap, no route
line and no arrow pointing the way — you learn the streets by driving them, and
you're paid on how efficiently you get there.

**Play:** https://atlas-asittley.github.io/the-knowledge/

## Why it's built this way

A 2024 analysis of ~9 million US death certificates across 443 occupations found
taxi and ambulance drivers had the lowest rate of death from Alzheimer's — about
1 in 100, against 1 in 60 overall. Bus drivers and pilots, who drive fixed routes,
showed no such benefit. The apparent difference is continuous real-time wayfinding,
which is work done by the hippocampus — among the first regions Alzheimer's damages.

Each mechanic traces to a specific finding:

| Mechanic | Why |
|---|---|
| No map, no route line | Habitual GPS use predicts declining spatial memory (Dahmani & Bohbot 2020) |
| New city often, no repeated routes | Repeated routes become memorised turn sequences — a different brain system (Konishi & Bohbot 2013) |
| Knowledge Test: point, place, compare | Measures the relational map directly; can't be faked by remembering turns |
| Peripheral hails with adaptive exposure | Speed-of-processing training is the only cognitive training shown to lower dementia incidence (ACTIVE trial) |
| Refreshers on old cities at widening intervals | In ACTIVE's 20-year follow-up, training without boosters had a hazard ratio of 1.01 — the whole effect was in the booster group |

**Honest limits**, also stated in-game: nobody has tested whether doing this on a
screen protects the brain the way navigating a real city does. The taxi study is
observational. Cognitive reserve delays symptoms rather than stopping the disease.
The largest known levers — hearing, blood pressure, exercise, sleep, social contact —
are not games. Nothing here is medical advice.

## Technical

Single self-contained `index.html`. No build step, no dependencies, no accounts,
no tracking. Progress is stored in `localStorage` on the device only.

Append `#debug` to the URL to expose `window.__knowledge` (city graph, game state,
pathfinding) for testing. It's off by default because it would spoil the game.
