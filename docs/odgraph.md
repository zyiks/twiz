# Graph Commands

TWiz graph commands are under the `/graph` slash-command group and require an active world.
Use graphs when snapshots and rankings are not enough and you need trend direction over time.

## Available commands

- `/graph od`
- `/graph score`
- `/graph villages`

All three commands use target slots (`who_1` to `who_5`).
`who_1` is required and `who_2`..`who_5` are optional.

## `/graph od`

Parameters:

- `odtype`: `all`, `a`, `d`, `s`
- `tribe_or_player`: `t` or `p`
- `who_1`: first target (required)
- `who_2`..`who_5`: additional targets (optional)

Notes:

- `s` (support ODS) is available only for players.
- If you graph players, TWiz may include a dashed tribe-average line for context.

Why you would use it:

- Spot offensive spikes before major pushes
- Identify defenders carrying most of the tribe load
- Compare individuals against tribe-average performance

## `/graph score`

Parameters:

- `tribe_or_player`: `t` or `p`
- `who_1`: first target (required)
- `who_2`..`who_5`: additional targets (optional)

Why you would use it:

- Track growth momentum, not only current rank
- See whether gains are steady or one-time jumps

## `/graph villages`

Parameters:

- `tribe_or_player`: `t` or `p`
- `who_1`: first target (required)
- `who_2`..`who_5`: additional targets (optional)

Why you would use it:

- Visualize expansion or collapse speed
- Confirm whether recent wars changed footprint materially

## Cooldown

- A per-user cooldown is applied (30 seconds for regular users).

## Prefix note

- Graph commands are documented under `/graph ...`.

## Examples

- `/graph od odtype:all tribe_or_player:p who_1:Player1 who_2:Player2`
- `/graph score tribe_or_player:t who_1:TAG1 who_2:TAG2`
- `/graph villages tribe_or_player:p who_1:Player1`
