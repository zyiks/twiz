# General Commands

These are TWiz utility commands that are not tied to one Tribal Wars feature.
All commands on this page work as slash and prefix commands.

## `/help`

Opens an interactive help menu with command categories and per-command usage.

- Visibility: reply is ephemeral (only you can see it)
- Best use: discover parameters quickly without leaving Discord
- Why it matters: helps new users self-serve instead of asking admins for syntax each time

Prefix equivalent:

- `!help` (or your custom prefix)

Example:

- `/help`

## `/ping`

Returns bot latency in milliseconds.

Why it matters:

- Quick health check before blaming command failures on settings
- Useful when users report slow responses

Example:

- `/ping`

Prefix equivalent:

- `!ping`

## `/scripts`

Posts the Tribal Wars Script Library Discord invite.

Why it matters:

- Gives teams a standard place to discover and discuss Tribal Wars scripts

Example:

- `/scripts`

Prefix equivalent:

- `!scripts`

## `/privacy`

Links to the TWiz privacy policy page.

Why it matters:

- Useful for server admins who need policy links for moderation/compliance questions

Example:

- `/privacy`

Prefix equivalent:

- `!privacy`

## `/doctor`

Checks TWiz permissions in the current channel or a selected channel.

Why it matters:

- Quickly explains why commands may fail in one channel but work in another
- Validates required and recommended permissions before setting up monitor/report channels

Parameters:

- `channel` (optional): channel to inspect; if omitted, checks current channel

Examples:

- `/doctor`
- `/doctor channel:#war-room`

Notes:

- This command is server-only.
- There is no prefix variant for `doctor`.
