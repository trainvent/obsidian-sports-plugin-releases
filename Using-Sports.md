# Using Sports

Start in **Open dashboard**, or add a `sports-dashboard` block to your own homepage. Plan in weekly notes, record results
in the workbook, and write personal commentary outside generated sections.

The dashboard shows Monday through Sunday. Use the arrows to move by a week,
**Today** to return to today, and a day in the strip to jump to its sessions.
**This week**, **Stats**, **Log**, and **Plans**
open the weekly note, trends, training log, and plans. The gear opens Sports settings;
Finish, restore, and guide commands are available through the command palette.

## Settings

**Connections** contains **Workbook**, **Garmin**, and **Sync**. Under Workbook,
**Setup** holds the guide and templates; **Sources** sets sheet names and the schedule source.
**Display** controls charts and the dashboard. **Advanced** contains recovery tools.

## In this guide

- [Your notes](#your-notes)
- [Properties and tags](#properties-and-tags)
- [Training charts](#training-charts)
- [Schedules and calendars](#schedules-and-calendars)
- [Garmin activity sync](#garmin-activity-sync)
- [Finish or restore a plan](#finish-or-restore-a-plan)

## Your notes

Use your homepage embed or dashboard for recent progress and upcoming training, Log for past training days, and Stats for trends. Plans and Strategy stay under Structure. Stats links to Sheet and Garmin charts through its **related** property.

The default notes folder is `Sports/`. Files are created as their source data becomes available.

| Path | Contents |
| --- | --- |
| `Structure/Sports.base` (existing browser) | Sortable Weeks and Routines views over note properties |
| `Analytics/Stats.md` | Source totals and training trends |
| `Journal/Weeks/YYYY-MM-DD.md` | Primary weekly planning, results, and review |
| `Structure/Plans.md` | Goals, weekly progression, and upcoming sessions |
| `Structure/Strategy.md` | Program structure and recurring schedule |
| `Log.md` | Training entries: select the date for its day note, or the training name for its routine |
| `Journal/Days/YYYY-MM-DD.md` | Session details, sets, recordings, and personal reflections |
| `Analytics/Sheet.md` | Planned intensity, performance, and felt-effort trends |
| `Analytics/Garmin.md` | Garmin volume, running, and swimming graphs |
| `Goals/<goal_id>.md` | Goal targets, mapped results, matching activities, and reviews |
| `Routines/` | Routine explanations, exercises, and progressions; linked from Plans and Log |
| `Guide/` | Workbook, Tracking, Using Sports, and Troubleshooting |

Weekly notes cover the current week, imported sessions, and Week plans.
Day notes under Journal cover today and earlier dates with workbook or Garmin
entries, plus enabled calendar events. Opening a future day in the dashboard also creates its planned day note. Start in Journal/Weeks for planning; use Log to find recorded days.
Goal categories distinguish aspiration and maintenance; either can use workbook
results and Garmin activities. Configure their source mappings in Strategy.

Imported training is managed by Sports. Write personal observations in the reflection or review sections below it. Workbook completion, Garmin recordings, and goal achievement are independent.

You can rename or move managed notes within this vault. Delete an optional generated note to stop updating it; **Settings → Sports → Advanced → Recreate missing notes** restores deleted pages. Routines appear only when represented in your plan or imported training. Older notes are retained with your writing when their routine leaves the plan.

Overview, Calendar, the routines index, and the separate days index are no longer generated. An unchanged Overview with no personal writing is removed; customized copies are archived. Other existing managed copies are preserved in `Archive/Previous pages/`, including personal writing. Strategy and detailed chart pages remain available.

## Properties and tags

The dashboard and your homepage embed provide navigation. Stats and guides use **related** properties for connected notes; Plans links to routines and dated sessions. Keep links where they describe a relationship: goal links in routine
properties, a weekly-note link on each day, and dated links in logs and plans.

| Note | Managed properties | Source |
| --- | --- | --- |
| `Analytics/Stats.md` | `related` (Sheet and Garmin links) | Detailed chart pages |
| `Guide/` | `related` (other guide links) | Companion guides |
| `Goals/<goal_id>.md` | `goal_id`, `category`, `garmin_types` | Goals table and resolved source mappings |
| `Routines/<name>.md` | `targets` (list of goal links) | Part/goal relationships; running and swimming goal mappings |
| `Journal/Days/YYYY-MM-DD.md` | `date`, `week` (weekly-note link) | Entry date and its Monday-start week |
| `Journal/Weeks/YYYY-MM-DD.md` | `week_start`, `week_end`, `program_week`, `phase` | Calendar dates and matching Week plans row |

Goal categories appear as **Aspiration** or **Maintenance**. Baseline, target, and
test standard remain in the goal body. Empty optional properties are omitted;
for example, a week without a Week plans row has no program_week or phase.

A routine's properties can look like this:

```yaml
---
targets:
  - "[[Sports/Goals/muscle-up|Muscle-up]]"
  - "[[Sports/Goals/pistol|Pistol squat]]"
tags:
  - sports/planning
  - sports/goals
---
```

Sports uses your configured notes folder in the links. Sync updates the managed
properties from imported data. Change goal mappings and plan metadata in the
workbook; changes to those properties in Obsidian are not written back.
Unrelated custom properties are preserved.

| Shared tag | Pages |
| --- | --- |
| `sports/planning` | Plans, Strategy, routines, weeks |
| `sports/goals` | Plans, goals, routines |
| `sports/training` | Log, days, weeks |
| `sports/analytics` | Stats, Sheet, Garmin |
| `sports/guide` | All four guides |
| `sports/running`, `sports/swimming` | Matching routines and goals with those resolved Garmin types |

Use Obsidian's tag pane or search a tag such as `tag:#sports/planning` to find
related notes. Sports refreshes these tag groups on sync, removing stale managed
tags and keeping your custom tags. Use your own tag names for personal grouping.

### Browse weeks and routines

If you used the previous Sports browser, it now lives at `Structure/Sports.base`. Its
**Weeks** view shows dates, program week and phase; **Routines** shows linked goals.
Enable Obsidian's **Bases** core plugin to use these sortable tables. Only notes
in your current Sports folder are included; backups and the routine index are excluded.

The base reads existing properties and needs no separate sync. Customize its
columns, sorting and filters freely: Sports preserves existing Base views and updates their folder references during migration. Workbook-managed property edits made through
a base are still replaced on sync. Edit the workbook to change those values.

### Embed training in another note

Use the full widget for today, upcoming sessions, and **This week**, **Stats**, and **Log** links:

````markdown
```sports-dashboard
```
````

Enable **Settings → Sports → Display → Show recent training** to include recent results and the seven-day summary.

For just today’s training, without navigation, recent results, or upcoming sessions:

````markdown
```sports-today
```
````

Both render in Reading view and Live Preview. Select a date to open its day note, even when no training is planned or recorded.
Existing `sports-today` blocks now show only today; change them to `sports-dashboard` to keep the full widget.

## Training charts

Exercise comparisons show explicit targets and recorded results, with each unit
kept separate. Day notes include set tables and plan/result charts: accent outlines
show plans; green bars show results. Each plot supports two unit types with independent left and right axes.
Reps/rounds share a count axis; time uses min:ss. A third unit type gets a separate plot.
Exercise order stays unchanged within each plot; heights across different units are not comparable. Row-based tracking uses the configured aggregation
(total by default); individual set values remain available. Partial totals are labelled.

**Stats** keeps workbook and Garmin totals separate and compares felt effort with
available watch HR zones. The same workout can appear in both sources.
**Analytics/Garmin** shows recorded volume, running and swimming pace, heart
rate, and available zone data. Garmin recordings never complete manual sessions.

The example's Scoring sheet supplies planned intensity (0–10), performance (%),
and metric coverage. Optional Effort rating (1–5) records how hard training felt.
See [Scoring and Library](Workbook.md#scoring-and-library) for calculation inputs.

Sheet shows three time-series charts, all with dates on the horizontal axis:

1. Performance × intensity and planned intensity on one shared scale.
   Displayed performance = session intensity × actual performance / 100. At
   100% the lines coincide; at 80% the performance point is 20% lower. Values
   above 100% can extend above 10; the display expands without clipping.
2. Felt effort (left 0–5 axis, recorded ratings 1–5) and intensity (right 0–10).
3. Actual daily performance only, on a fixed 0–200% scale: 0% at the bottom,
   100% in the center, and 200% at the top. There is no expected-performance
   series. Values above 200% are marked at the top with actual values in point
   labels. With no results, the axes remain visible without data points.

Performance is scaled per session before taking the daily median. Other series
use the median of available session values per date. Intensity
can appear before performance or effort is recorded. Missing values are not
recorded zeros. Session coverage and felt-effort ratings remain in dated day notes, reached from Log.
The separate axes compare trends across different units, not equal values.
A score measures target attainment, not absolute training quality. Keep
commentary outside protected generated sections.

Charts render locally in Reading view or Live Preview with Sports enabled.
Source mode shows readable code blocks; no external chart service is used.

## Schedules and calendars

Enable **Show schedule** to include the selected schedule in the dashboard and
weekly notes. It is off by default; changing **Schedule source** enables it.
Choose **Workbook recurrence** or **ICS calendar**. The inactive source is
not synchronized or displayed. Recurring entries describe plans, not completions.

### Connect an ICS calendar

In **Settings → Sports → Connections → Workbook → Sources**, select **ICS calendar** as the schedule source and add an ICS subscription link from a dedicated training calendar, then select **Sync now**. For Google Calendar, use the calendar’s secret address in iCal format. For Nextcloud, paste the public calendar share link or an ICS subscription/export link. Public calendar share links are converted to ICS exports automatically; private CalDAV URLs requiring login are not supported. HTTPS and `webcal://` links are supported (`webcal` is downloaded over HTTPS).

Calendar events appear in the dashboard, embedded widgets and weekly notes. Refresh uses **Sync on startup** and **Sync interval**. Changes and deletions replace the cached calendar events after a successful download; failed downloads retain the previous cache. ICS is read-only: create, move and delete events in Google Calendar or Nextcloud. It does not mark workouts completed or change the workbook.

Each refresh imports event start dates from the past 30 days through the next 365 days, including recurring events and exceptions. Timed events use the device’s timezone; all-day events retain their calendar date. Multi-day events appear on their starting day. Dates beyond this window require a later refresh. Feeds are limited to 5 MB and recurrence expansion to 50,000 occurrences per refresh.

The subscription URL and imported event details are stored locally in the vault’s plugin data and may be copied by vault sync or backups. Treat a secret subscription link like a password. Requests go directly to the configured calendar provider; no vault data is uploaded. Clear the link and sync to disconnect and remove imported events from generated notes. Generated notes follow the usual edit-protection rules.

### Match calendar plans and Garmin recordings

Weekly notes, daily notes, the dashboard and embedded widgets group a Garmin activity inside its scheduled workout tile when the sport is compatible and the recording substantially overlaps the planned time. For example, an 08:00–09:00 swim can contain an 08:10–09:00 Garmin recording. The tile keeps planned minutes and recorded measurements separate. Unmatched activities get their own tiles; equally plausible matches remain separate. All-day events and entries without a duration are not matched automatically.

Matching supports both ICS calendar events and the workbook’s weekly schedule. Links are recalculated from the current source data after refresh; they do not edit the calendar, Garmin records, manual completion, or analytics totals. Several recordings can belong to one planned event, but a recording is shown only once. Existing note edits and reflections keep their usual protections.

### Calendar goal links

Add a line to an event’s description to associate it with a Strategy goal:

```text
goal-id: swimming
```

Use the exact `goal_id` from Strategy, rather than its display title. Multiple goals use `goal-ids: swimming, running`. The event appears on that goal’s page and in routines connected to it through Strategy’s part-to-goal links or Garmin type mapping. For example, a custom goal with Garmin types `swimming` feeds **Routines/Swimming**. These links also help match Garmin recordings when an event has a generic title such as “Morning practice.”

Exact Strategy goal IDs in descriptions also work without a label: `swimming` or `Tsve swimming`. IDs must stand alone, separated by whitespace, commas or semicolons; partial words are not matched. A labelled `goal-id:` takes priority. Only these IDs route calendar events to goals and routines. Event titles and goal display titles can use any language; descriptions without a known ID stay unassigned. Events remain visible in the main calendar regardless. The key line is hidden in workout tiles. On routine and goal pages, matching recordings share the event’s dated table row. Weekly and daily notes keep them inside the event tile.

### Compact sport pages

Routine and goal pages use compact tables. **Recurring schedule** lists each calendar series once with its weekdays, time and recurrence. **Dated sessions** contains one-off events, moved occurrences, and recorded sessions; a linked Garmin recording stays on its planned event’s row. Unrecorded recurring occurrences are not repeated as dated rows. Weekly and daily notes retain their workout tiles.


## Garmin activity sync

On desktop, select **Settings → Sports → Connections → Garmin → Connect Garmin**. Sign in with your
Garmin email and password, then enter the verification code if requested. No Python,
terminal commands or separate installation are required. This connection is experimental
until sign-in, MFA and token refresh have been checked with a live account.

Connecting explicitly enables network access to Garmin and starts an activity import.
Passwords and verification codes are held only in the sign-in dialog and are never
saved. Session tokens are saved through Obsidian's secret storage, separately from
plugin settings and generated notes. Obsidian 1.11.4 or later is required.

The bundled [garminconnect-js](https://github.com/DynamicsNinja/garminconnect-js)
client uses unofficial Garmin Connect endpoints. It also downloads public OAuth
application keys from `https://thegarth.s3.amazonaws.com/oauth_consumer.json`; no
credentials or activity data are sent to that host. This is JSON data, not remote
executable code. Garmin can change these endpoints or limit sign-ins. This feature
currently supports Garmin accounts on garmin.com, not garmin.cn.

Set **Garmin history start** to the first date to import. The initial default is 90
days ago. While Obsidian runs, automatic sync checks Garmin at most once an hour,
using the configured sync timer. **Sync now** requests an immediate refresh.
Garmin refreshes independently when workbook import fails. With all three workbook sheet
mappings blank, it can also run without a workbook.

Activity ID, local date/time, name, type, duration, distance, average heart
rate and heart-rate zone summaries are cached in the vault's plugin data and shown in **Log**, weekly notes and the
dashboard. No GPS routes or complete account responses are retained. Activities use
Garmin's local start time; GMT-only records use the plan's timezone, or your local
timezone without a plan. Garmin records never mark manual sessions complete.

Each successful refresh replaces the selected date range, so activity edits and
deletions do not create duplicates. On failure the previous snapshot remains visible
with a warning. **Disconnect** clears the saved tokens and stops Garmin requests;
cached activities remain available. **Clear cached data** removes the imported
activity cache while keeping connection settings. Generated notes and reflections
keep their existing edit protection.

### Optional Garmin Coach plans

Enable **Show Garmin Coach plans** to include published adaptive Coach workout
summaries for the next 28 days in Plans. This is off by default and
still needs live-account verification. Full workout steps, self-scheduled workouts,
and static training plans are excluded. Check Garmin Connect for the current prescription.
Failed refreshes retain cached summaries with a warning. Turning the setting off
stops Coach requests; disconnecting stops all Garmin requests.

## Finish or restore a plan

Run **Sports: Finish plan** from the command palette. The destination defaults
to `Archive/<plan name>` and can be changed. **Finish and move notes** moves the
current notes there (including managed notes moved elsewhere in the vault), disconnects the workbook, and clears the active plan.

Each finished folder includes `settings.md`, which keeps its original workbook
link, sheet names, imported plan, and generated-note baselines. These saved plans
are separate from the 10 rotating recovery copies and do not expire automatically.
The workbook itself, Garmin connection, and plugin preferences are retained.

Run **Sports: Restore from folder** from the command palette, enter the finished folder,
and select **Read saved plan**. You can copy its workbook link without restoring.
**Restore plan** moves the notes back and restores the saved plan and link.
Finish any active plan first; existing destination folders are never overwritten.
Workbook sync stays paused until you select **Sync now**, so you can inspect or
replace the recovered link first. To start a new plan instead, select a workbook.

For cloud downloads, sync timing, and recovery, see [Troubleshooting](Troubleshooting.md).
