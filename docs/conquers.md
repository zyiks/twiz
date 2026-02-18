# Conquer Alerts

Conquer alerts are managed with the `/monitor` command group.

TWiz fetches conquer updates in the background (roughly once per minute) and sends digest messages to channels with active monitor subscriptions.

Why teams use this:

- Track gains/losses without manually refreshing external tools
- Keep Discord war rooms updated in near real time
- Separate strategic channels by target scope (tribe-focused vs player-focused)

## `/monitor list`

Shows monitor subscriptions for the current channel.

Parameters:

- `scope` (optional): `all`, `tribe`, or `player` (default: `all`)

Examples:

- `/monitor list`
- `/monitor list scope:tribe`
- `/monitor list scope:player`

Why you would use it:

- Audit what is actually being monitored in this channel
- Confirm whether toggles are active before reporting "missing alerts"

## `/monitor add`

Creates or edits a monitor for a tribe or player in the current channel.

Parameters:

- `scope` (required): `tribe` or `player`
- `target` (required): tribe tag or player name to monitor

Permissions and requirements:

- User must have `Manage Server`
- Channel must allow TWiz to `Send Messages` and `Embed Links`
- World must be configured for channel/server

Recommended pre-check:

- Run `/doctor` in the monitor channel before adding subscriptions.
- For another channel, run `/doctor channel:#your-channel`.

After command submission, TWiz opens an interactive toggle panel.

Toggle meanings:

- Gains: village gained by monitored target
- Losses: village lost by monitored target
- Barbarian: events involving barbarian ownership
- Self-Conquer: same owner before/after (self retake)
- Internal: conquer inside the same tribe

For new monitors, all toggles default to enabled.

Why this command matters:

- One command gives you granular event filtering for each monitored target.
- You can keep only relevant events (for example losses only) and reduce channel noise.
- `/doctor` helps you confirm channel permissions first, so monitor digests do not silently fail.

Examples:

- Tribe example: `/monitor add scope:tribe target:TAG`
- Player example: `/monitor add scope:player target:PlayerName`

## `/monitor remove`

Removes a monitor subscription from the current channel.

Parameters:

- `scope` (required): `tribe` or `player`
- `target` (required): tribe tag or player name to stop monitoring

Examples:

- Tribe example: `/monitor remove scope:tribe target:TAG`
- Player example: `/monitor remove scope:player target:PlayerName`

Why you would use it:

- Clean up old targets after diplomacy changes or world phase shifts
- Keep digest volume manageable in busy channels

## Channel-specific behavior

Monitor subscriptions are channel-local.
If you need separate monitor profiles, use separate channels.

Example setup pattern:

- `#conquer-gains`: gains-focused toggles
- `#conquer-losses`: losses-focused toggles
- `#conquer-special`: self/internal/barbarian investigations
