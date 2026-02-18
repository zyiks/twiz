# CIRC Lists

Use `/circ` to build in-game mail recipient lists from one or more tribe tags.
This command is hybrid, so slash and prefix both work.

## `/circ`

Builds in-game mail recipient lists from one or more tribe tags.

Why you would use it:

- Prepare alliance-wide in-game messages quickly
- Avoid manual member copying from multiple tribe pages

Parameters:

- `tribes` (required): comma-separated tribe tags (example: `TAG1,TAG2`)

Requirements:

- Active world configured in the channel/server context

Example:


- Slash: `/circ tribes:TAG1,TAG2`
- Prefix: `!circ TAG1,TAG2`

Limits:

- Keep lists focused and readable; very large tribe sets may produce long output.