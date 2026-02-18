# Village Lookup

Village lookup is automatic and does not require a command.
It is one of the most-used quality-of-life features in active Discord planning channels.

When village coordinate resolution is enabled, TWiz scans messages for coordinates in these formats:

- `000|000`
- `000-000`

Coordinates can appear inside regular text and you can include multiple coordinates in one message.

TWiz replies with village ownership/link details using the active world context.

Why this is useful:

- Saves time when players paste many coords during ops
- Reduces copy/paste to external websites for quick ownership checks

## World and settings behavior

- World selection follows channel override first, then global world.
- Auto lookup is active when a valid world is configured.

Related commands:

- `/config world world:<short-name>`
- `/config channel_world world:<short-name>`
- `/config`

## Operational note

If no world is configured, TWiz cannot resolve village coordinates and will stay silent for those messages.
