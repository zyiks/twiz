# Legacy Prefix Commands

TWiz supports both slash commands and prefix commands.
This page helps server admins keep prefix usage reliable in multi-bot servers.

Common prefix commands include:

- `help`, `ping`, `scripts`, `privacy`
- `tribe` (`t`), `player` (`p`), `reports` (`r`), `circ`, `stronghold`
- `od`, `score`, `villages`, `map`
- `monitor ...`, `config ...`

Notable exception:

- Context-menu actions (for example `Screenshot Report`) are Discord UI actions, not prefix commands.

## Set the prefix

Use `/config prefix` to set the server prefix:

- `/config prefix prefix:!`
- `/config prefix prefix:?`

Limits:

- Prefix length must be 1 to 5 characters.

## Why prefix overlap happens

Prefix commands are plain text, so TWiz cannot know whether a user "meant" another bot.

Common overlap situations:

- Multiple bots in one server all using `!`
- Similar short commands across bots (for example `!p`, `!help`, `!r`)
- Users mixing old habits from different servers

When overlap happens, users can get unexpected replies or think TWiz is broken.

How to reduce overlap:

- Set a unique TWiz prefix with `/config prefix`
- Move frequent usage to slash commands, which are unambiguous
- Keep legacy commands for quick compatibility only

## Example usage

If your prefix is `!`:

- `!t TAG`
- `!p PlayerName`
- `!r 500|500`
- `!map player score`
- `!monitor add TAG`

If your prefix is `?`:

- `?t TAG`
- `?p PlayerName`
- `?r 500|500`
- `?map tribe oda`
- `?monitor remove TAG`

## Important

If a command is available as both slash and prefix, slash is generally safer in busy servers because it avoids prefix ambiguity.
