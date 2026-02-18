# Map Generation

TWiz map generation is available as the slash command `/map generate`.
Maps are best when you need positional context, not only numbers.

## Command

- `/map generate player_or_tribe:<t|p> comparison_type:<score|odall|oda|odd|ods> [who_1] [who_2] [who_3] [who_4] [who_5]`

Parameters:

- `player_or_tribe`: choose tribe (`t`) or player (`p`) scope
- `comparison_type`: ranking metric (`score`, `odall`, `oda`, `odd`, `ods`)
- `who_1`..`who_5` (optional): up to five explicit targets (one per slot); when omitted, TWiz defaults to top 20 for the selected scope

Why the target list matters:

- No `who_*` values gives broad world overview (top 20 style).
- `who_*` values give focused maps for your current operation targets.

Notes:

- `ods` is not available for tribe maps.
- A per-user cooldown is applied (30 seconds for regular users).

## What the map includes

- World snapshot rendered from stored village ownership data
- Highlighted selected players/tribes with legend
- Ownership percentage of the world below the map
- Sidebar with map title and generation timestamp

Why you would use map output:

- Plan support routes and front-line pressure visually
- Identify pocket clusters and isolated targets faster

## Examples

- `/map generate player_or_tribe:p comparison_type:score`
- `/map generate player_or_tribe:p comparison_type:odall who_1:Alice who_2:Bob`
- `/map generate player_or_tribe:t comparison_type:oda`
- `/map generate player_or_tribe:t comparison_type:odd who_1:CICADA who_2:CRUNCH`
