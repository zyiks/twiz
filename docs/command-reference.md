# Command Reference

This page lists the currently available TWiz commands.

Important:

- Most TWiz commands are `hybrid` commands, which means they work as both slash commands and prefix commands.
- Example: `/tribe tag:TAG` and `!tribe TAG` (or `!t TAG`) are both valid if your prefix is `!`.

## General

- `/help`
- `/ping`
- `/scripts`
- `/privacy`
- `/doctor [channel]`

## Configuration (`/config` group)

- `/config` (same as `/config show`)
- `/config prefix prefix:<1-5 chars>`
- `/config world world:<short-name>`
- `/config channel_world [world:<short-name>]`
- `/config delete_report_messages enabled:<true|false>`

## Tribal Wars lookups

- `/tribe [tag]` (alias `t`)
- `/player [name]` (alias `p`)
- `/reports coords:<000|000>` (alias `r`)
- `/circ tribes:<tag1,tag2,...>`
- `/stronghold attacker:<tag> defender:<tag>`

## Graphs and maps

- `/graph od odtype:<all|a|d|s> tribe_or_player:<t|p> who_1:<target> [who_2..who_5]`
- `/graph score tribe_or_player:<t|p> who_1:<target> [who_2..who_5]`
- `/graph villages tribe_or_player:<t|p> who_1:<target> [who_2..who_5]`
- `/map generate player_or_tribe:<t|p> comparison_type:<score|odall|oda|odd|ods> [who_1..who_5]`

## Conquer monitor (`/monitor` group)

- `/monitor` (same as monitor list)
- `/monitor list [scope:<all|tribe|player>]`
- `/monitor add scope:<tribe|player> target:<tag-or-name>`
- `/monitor remove scope:<tribe|player> target:<tag-or-name>`

Current release note:

- Conquer monitor supports both tribe and player subscriptions.

## Context menu

- `Screenshot Report` (right-click message -> Apps)

## Automatic features (no command required)

- Village coordinate lookup from messages (`000|000` or `000-000`)
- Auto screenshot for Tribal Wars `public_report` links
- Auto screenshot for `[report]...[/report]` tags
- Screenshot posting for `tribal-reports.net/en/report/...` links

## Prefix usage

All hybrid commands above also work with your configured prefix.
Use `/config prefix` if you need to avoid overlap with other bots in your server.
