# Configuration

TWiz configuration is handled through `/config ...` commands.
These settings are primarily for server admins and let you tune TWiz per server and per channel.

Permission requirement:

- Most configuration commands require `Manage Server`.

## View active settings

- `/config` (same as `/config show`)

This displays server-level settings, channel overrides, and effective values.

Why this matters:

- It is the fastest way to debug "why is TWiz behaving differently in this channel?"
- You can immediately see whether a channel override is active or inheriting global defaults.

## Prefix setting (legacy commands)

- `/config prefix prefix:<value>`

Rules:

- Prefix length must be 1 to 5 characters.
- This affects only legacy prefix commands (`tribe/player/reports`).

Why you might change prefix:

- In many servers, multiple bots share common prefixes like `!`.
- That can cause command overlap (for example, two bots reacting to `!help` or similarly named commands).
- Setting a unique TWiz prefix reduces accidental triggers and confusion for users who still use legacy commands.

Practical recommendation:

- If your server is slash-command focused, keep legacy prefix usage minimal.
- If your users rely on prefix shortcuts, choose a unique prefix that no other bot in your server uses.

## World settings

- `/config world world:<short-name>` sets the global server world.
- `/config channel_world world:<short-name>` sets channel override world.
- `/config channel_world` (no `world` value) resets channel override to global.

TWiz provides world suggestions if the value does not match exactly.

See [World Selection](worlds.md) for details.

Why this matters:

- World context controls almost every Tribal Wars lookup.
- Channel overrides are useful when one Discord server coordinates multiple worlds.

## Report screenshot settings

- `/config delete_report_messages enabled:<true|false>` controls whether source report-link messages are deleted after successful screenshot posting.

Default:

- Delete report messages: disabled

Why this matters:

- Enabling deletion keeps channels cleaner after screenshots are posted.
- Keeping deletion disabled preserves original links and context for later.