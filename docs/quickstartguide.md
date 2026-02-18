# Quick Start Guide

This guide is written for server admins who are setting up TWiz for real day-to-day use.
Each step includes why it matters so you can decide what to configure immediately and what can wait.

## 1) Invite TWiz to your Discord server

Prerequisites:

- You have `Manage Server` or `Administrator` permission in the target server.

Invite link:

- https://discord.com/oauth2/authorize?client_id=591226665951297537&scope=bot%20applications.commands&permissions=519232

TWiz works best with these permissions:

- Required: `View Channel`, `Send Messages`, `Embed Links`
- Recommended: `Attach Files` (graphs/maps/report screenshots), `Manage Messages` (optional report source cleanup)

Why this matters:

- Without `Embed Links`, many TWiz responses lose useful formatting and context.
- Without `Attach Files`, maps, graphs, and report screenshots cannot be posted.
- Missing `Manage Messages` does not break core features, but report-cleanup options may not work.

## 2) Set your world

Most Tribal Wars commands need a configured world.

- Set a global world for the server:
  - `/config world world:en112`
- Optionally set a channel-specific world:
  - `/config channel_world world:en113`
- Check active settings:
  - `/config show`

Use world short names such as `en112`, `de203`, `us91`.

Why this matters:

- If no world is set, most game-data commands fail with "No world configured".
- If the wrong world is set, lookups will return correct data for the wrong world, which is usually worse than an explicit error.

## 3) Verify TWiz in a channel

Run these once:

- `/help` to open the interactive command guide
- `/doctor` to verify TWiz permissions in the current channel
- `/config` to confirm your server configuration is visible
- `/tribe tag:TAG` or `/player name:PlayerName` for a quick data check

Why this matters:

- `/doctor` catches channel permission problems before users start reporting missing alerts or failed screenshots.
- A quick `/tribe` or `/player` lookup confirms that world and data access are configured correctly.
- `/config` helps admins verify prefix/world settings before users start using commands heavily.

## 4) Optional quality-of-life settings

- `/config prefix prefix:?` (if you want a unique prefix)
- `/config channel_world world:en113` (if a specific channel should use another world)
- `/config delete_report_messages enabled:false` (recommended if you want to keep original report links visible)

Why this matters:

- A unique prefix prevents overlap when multiple bots respond to similar text commands.
- Channel world overrides let one Discord server support multiple Tribal Wars worlds.
- Keeping `delete_report_messages` disabled is safer when users want auditability and original links preserved.

## Legacy note

TWiz supports both slash commands and prefix commands for most user features.

If your server has many bots, set a unique TWiz prefix to avoid command overlap.
