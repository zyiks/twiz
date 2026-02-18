# World Selection

Most TWiz game-data commands need an active world.
If world context is wrong, command results can look valid but refer to the wrong game world.

## Resolution order

TWiz resolves world context in this order:

1. Channel world override (`/config channel_world`)
2. Global server world (`/config world`)

If neither is set, world-dependent commands return:

- `No world configured for this server/channel.`

Why this order is useful:

- You can run one server-wide default world for most channels.
- Strategy channels for other worlds can override only where needed.

## World format

Use short world names such as:

- `en112`
- `de203`
- `us91`

You can usually get this from the world domain prefix.
Example: `https://en112.tribalwars.net` -> `en112`.

## Commands

Global world:

- `/config world world:<short-name>`

Channel override:

- `/config channel_world world:<short-name>`

Reset channel override:

- `/config channel_world`

View current values:

- `/config show`

Typical admin pattern:

- Set one global world for the main community channel set.
- Override specific channels used by cross-world teams.

## Smart suggestions

If a world is not found exactly, TWiz can show clickable suggestions.
Clicking one applies it immediately.
