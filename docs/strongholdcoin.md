# Stronghold Coin Rewards

Use `/stronghold` to estimate coin rewards from stronghold attacks.
This is mainly a planning command for deciding whether a target is worth coordinated action.

## Command

- `/stronghold attacker:<tribe-tag> defender:<tribe-tag>`

Both `attacker` and `defender` are tribe tags.

Requirements:

- Active world configured for the channel/server

Output:

- Total estimated coin reward
- Per-player reward breakdown for attacker members

Why this is useful:

- Compare expected reward before committing attacks
- Share reward expectations clearly inside tribe planning channels
- Reduce manual calculations during fast decision windows

Autocomplete:

- Tribe autocomplete is available for both attacker and defender fields.

Examples:

- Slash: `/stronghold attacker:ATK defender:DEF`
- Prefix: `!stronghold ATK DEF`
