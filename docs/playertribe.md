# Player and Tribe Lookup

These commands use the active world and are useful for diplomacy, scouting, target prioritization, and activity tracking.

## `/tribe` (alias: `t`)

Finds tribes by tag and returns rank/points/member/village overview.

Why you would use it:

- Quick diplomatic context before contact or conflict
- Compare tribe size and growth pace without leaving Discord
- Verify tag spelling before monitor/map/graph commands

Parameters:

- `tag` (optional): tribe tag text

Example:

- Slash: `/tribe tag:TAG`
- Prefix: `!tribe TAG` or `!t TAG`

If no tag is provided, TWiz returns top matching tribes from the world.

## `/player` (alias: `p`)

Finds players by name and returns player/tribe/village summary.

Why you would use it:

- Fast checks during ops calls ("who is this player and where are they?")
- Identify whether a player has a tribe and how large their footprint is
- Confirm exact player names before adding to lists or comparison commands

Parameters:

- `name` (optional): player name text

Example:

- Slash: `/player name:SomePlayer`
- Prefix: `!player SomePlayer` or `!p SomePlayer`

If no name is provided, TWiz returns top matching players from the world.