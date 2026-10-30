# Troubleshooting

## Choose the next action

| Problem | Start here |
| --- | --- |
| Workbook does not download | [Cloud links](#cloud-links) |
| Values or sessions are missing | [Check the import](#check-the-import) |
| Automatic refresh did not run | [Sync timing](#sync-timing) |
| Notes are missing or report conflicts | [Notes and recovery](#notes-and-recovery) |
| Garmin or calendar refresh fails | [Connection problems](#connection-problems) |

## Cloud links

Use an HTTPS link to the XLSX or ODS file itself. Nextcloud file-share links such
as `https://cloud.example/s/SHARE_TOKEN` work; Sports adds `/download` automatically.
The link must allow downloads without a login or password. Folder shares,
spreadsheet editor URLs, local paths, and encrypted workbooks are unsupported.
Downloads are limited to **5 MB** and **30 seconds**, with redirects restricted
to the same HTTPS server.

## Sync timing

Startup sync is enabled and the default interval is ten minutes. Choose five,
ten, or fifteen minutes, one hour, or **Manual only** under **Connections → Sync**. Startup sync
has its own toggle. Automatic sync runs while Obsidian is open; closed apps and
suspension stop or delay it. Garmin automatic refresh runs at most hourly.
Failed downloads or invalid imports retain the previous dataset.

## Check the import

- Under **Connections → Workbook → Sources**, check the exact tab names in **Strategy sheet**, **Tracking sheet**, and
  **Weekly schedule sheet**. A blank mapping disables that import and retains
  previously imported data and notes.
- Recalculate and save formulas in your spreadsheet editor. Sports reads saved
  results and does not calculate formulas.
- Check dates, supported headers, stable IDs, and table boundaries against the
  [workbook guide](Workbook.md#keep-the-workbook-contract).
- Check completion flags using [Tracking](Tracking.md). Prefilled targets are
  not results, and Garmin recordings do not mark Daily sessions complete.
- An invalid import retains the previous dataset. Resolve the reported error
  before relying on a new refresh.

## Notes and recovery

Sports uses hidden `sports:begin` / `sports:end` comments to identify generated
sections. Keep the markers and write reflections outside them. They appear in
source mode and stay hidden in Reading view. Edited generated content or damaged
markers cause a conflict; other notes can still update.

Choose the recovery action that matches the problem:

| Situation | Action |
| --- | --- |
| Refresh notes from the last import | **Generate notes from imported data** |
| A generated note was deleted | **Recreate missing notes** |
| A generated section was edited | Move personal changes outside it, restore the previous generated section, then refresh |
| Rebuild generated sections after persistent sync-state problems | **Clear cached data**, then **Sync now** |

A cache reset keeps settings and note files, but clears imported workbook, calendar, and Garmin
data and saved generated-section baselines. Existing target notes are backed up
in hidden plugin storage before their generated sections
are rebuilt. Reflections outside those sections and unrelated properties stay in
place. Changes inside a rebuilt section survive in its backup, not in the new output.

Recovery remembers pending notes across refreshes, including Garmin-backed day
and historical week notes that return after the workbook refresh. You do not need
to reset again just because one source returns later. Missing or damaged markers
still need repair; a reset does not bypass those checks. Results absent from both
the workbook and Garmin cannot be restored by syncing.

Backups are recovery copies, not active notes or sync inputs. Normal sync does
not create them. At most 10 recovery copies are retained; each new copy replaces
the oldest when storage is full.
Keep managed note filenames stable.
Each recovery copy records the original note path, timestamp, and full content
in the plugin's hidden `recovery-backups.json`. Finished-plan archives are separate
and do not expire automatically; see [Finish or restore a plan](Using-Sports.md#finish-or-restore-a-plan).

## Connection problems

**Garmin:** a failed refresh retains cached activities with a warning. If sign-in
or token refresh fails, reconnect under **Settings → Sports → Connect Garmin**.
The integration uses unofficial endpoints and can be affected by Garmin changes
or sign-in limits. **Disconnect** removes tokens and stops requests, while cached
activities remain until cleared. See [Garmin activity sync](Using-Sports.md#garmin-activity-sync).

**Calendar:** check that **ICS calendar** is the active source and that the link
returns an ICS feed. Private CalDAV URLs requiring login are unsupported. Failed
refreshes retain cached events. See [Connect an ICS calendar](Using-Sports.md#connect-an-ics-calendar)
for supported links and the imported date range.

## Guide updates

All four guides have a generated section that updates with Sports. Keep your own
notes below it, outside the hidden `sports:begin` / `sports:end` markers. An edit
inside the generated section causes a conflict rather than being overwritten.

When an older unmarked Workbook guide is first upgraded, Sports saves its exact
contents in a linked **Workbook previous** note before adding the current guide.
Your previous edits remain in that copy. Move any personal guidance you want to
keep nearby into the current guide's **My notes** section.

## Get help

[Report an issue](https://github.com/trainvent/obsidian-sports-plugin-releases/issues)
with your Obsidian and Sports versions, the error, and steps to reproduce it.
Remove private share links, credentials, and personal training data from attachments.
