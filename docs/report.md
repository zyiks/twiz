# Reports and Screenshots

TWiz can automatically screenshot Tribal Wars reports and store them for later browsing.
This is especially useful in war channels where many temporary links are shared.

## How reports are captured

TWiz listens for:

- Public report links containing `/public_report/...`
- `[report]...[/report]` tags in messages (uses the active world to build the URL)

When successful, TWiz posts the report screenshot and stores metadata for later lookup.

Why this is useful:

- Report links expire or get buried quickly during active wars.
- Screenshot storage gives your team a searchable local history by village coordinate.
- Users can review important reports without scrolling through long chat history.

## Manual screenshot option

TWiz also provides a message context menu action:

- `Screenshot Report` (right-click message -> Apps)

Use this when a report link was missed or you want to process one specific message manually.
The context action still respects channel screenshot settings.

## Browsing stored reports

Use:

- `/reports coords:<500|500>`

You get an interactive selector UI for stored reports at those coordinates.

Why you would use it:

- Check the last known troop composition of a village
- Re-check old attack/defense patterns for the same village
- Compare timings or unit compositions across repeated hits
- Share one stable command instead of reposting many old links

Notes:

- Up to 250 most recent stored reports are loaded.
- Selector is paged in chunks of 25 entries.

## Configuration controls

- `/config delete_report_messages enabled:<true|false>`

This command controls if the message containing the report link is deleted after screenshotting.

Suggested setup patterns:

- Fast war-room workflow: screenshot automation plus deletion enabled
- Audit-friendly workflow: screenshot automation plus deletion disabled

## Permission and safety behavior

- TWiz needs `Attach Files` to post report screenshots.
- TWiz needs access to read and post in that channel to process links.

## Legacy compatibility

Prefix command still supported:

- `reports` (`r`) for browsing stored screenshots by coordinate.

Slash and prefix examples:

- `/reports coords:500|500`
- `!reports 500|500` or `!r 500|500`
