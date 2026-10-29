<img align="right" src="assets/LeLogo_white.svg" alt="Trainvent logo" width="64" height="64">

## Sports

<p><strong>Your training. Your progress. Your Obsidian vault.</strong></p>

<p>Plan in a spreadsheet. Track your workouts. Make every week count.</p>

<p>
  <a href="https://obsidian.md/">
    <img src="https://img.shields.io/badge/Obsidian-1.11.4%2B-7C3AED?style=flat-square&amp;logo=obsidian&amp;logoColor=white" alt="Obsidian 1.11.4 or later">
  </a>
  <a href="https://github.com/trainvent/obsidian-sports-plugin-releases/releases/latest">
    <img src="https://img.shields.io/github/v/release/trainvent/obsidian-sports-plugin-releases?style=flat-square&amp;color=16A085&amp;label=release" alt="Latest release">
  </a>
  <a href="#guides">
    <img src="https://img.shields.io/badge/notes-Markdown-374151?style=flat-square" alt="Markdown notes">
  </a>
</p>

<p>
  <a href="#install">Install</a> &nbsp;·&nbsp;
  <a href="#get-started">Get started</a> &nbsp;·&nbsp;
  <a href="#guides">Guides</a> &nbsp;·&nbsp;
  <a href="#optional-connections">Connections</a> &nbsp;·&nbsp;
  <a href="#help-and-support">Get help</a>
</p>

<p>Built by <a href="https://github.com/trainvent">Trainvent</a></p>

---

Sports connects your **training plans, workout results, calendars, and Garmin
recordings** in one Obsidian dashboard, with linked notes for goals, progress,
and weekly reflections. Bring an XLSX or ODS workbook and make it your own—from
calisthenics and street workout to running, swimming, and other sports.

## Install

Sports is available in Obsidian's community plugins directory.

1. Open **Settings → Community plugins → Browse**.
2. Search for **Sports**, select **Install**, then **Enable**.
3. Open **Settings → Sports** to set up your workbook, calendar, or Garmin connection.

Requires **Obsidian 1.11.4 or later** on desktop. Mobile is not supported.
Garmin integration is experimental and uses unofficial endpoints.

## What you can do

- **Plan:** connect goals, training parts, weekly targets, and dated sessions.
- **Record:** enter sets, time, rounds, added weight, and other measurements in your workbook.
- **Review:** compare plans and results, follow training trends, and write weekly reflections.
- **Combine sources:** see workbook sessions, recurring activities, calendar events, and Garmin recordings together.
- **Keep your notes:** browse ordinary Markdown files with space for your own commentary.

Sync flows **workbook → Obsidian**. Edit plans and results in your spreadsheet;
write reflections in Obsidian. Sports never uploads changes to your workbook.
Charts render locally without another community plugin or chart service.

## Get started

1. Open **Settings → Sports → Workbook guide → Open guide**. Read
   [Workbook.md](Workbook.md) before adapting a file; it is also saved under
   `Guide/Workbook.md` in your Sports notes folder.
2. Choose **Blank template** to build your own plan or **Example workbook** to
   learn from a filled plan. Both offer **Download XLSX** and **Download ODS**.
3. Use the guide to fill or adapt the file to your goals, availability, equipment,
   and preferred activities. You can do this yourself or give the file and guide
   to your chatbot. Keep future results blank.
4. Upload the completed file to Nextcloud or another service with an HTTPS
   download link. Paste it into **Cloud workbook link** and keep the sheet
   mappings **Strategy**, **Daily**, and **Recurring**.
5. Select **Sync now**, then **Open dashboard**.
6. Record training in the workbook, recalculate and save if it uses formulas,
   then sync again.
7. **Optional: use [Calcrow](https://calcrow.com/) for everyday Daily-sheet edits.**
   Calcrow is made by Trainvent. Save changes to the cloud workbook before syncing Sports.

## Guides

| Guide | Use it for |
| --- | --- |
| [Workbook](Workbook.md) | Fill the template, define goals and sheets, configure scoring, validate a plan |
| [Tracking](Tracking.md) | Record workouts, handle completion and weights, customize Daily layouts |
| [Using Sports](Using-Sports.md) | Navigate notes, read charts, connect calendars and Garmin, finish or restore plans |
| [Troubleshooting](Troubleshooting.md) | Cloud links, sync timing, missing data, note conflicts, and recovery |

Guides are also available under `Guide/` in your Sports notes folder. Open the
workbook guide in settings or any guide from the command palette. Each guide updates its generated section while keeping
personal notes outside it.

| Starting point | XLSX | ODS |
| --- | --- | --- |
| Blank template | [Training-Template.xlsx](templates/Training-Template.xlsx) | [Training-Template.ods](templates/Training-Template.ods) |
| Filled example | [Training-Example.xlsx](templates/Training-Example.xlsx) | [Training-Example.ods](templates/Training-Example.ods) |

Both blank formats retain all five sheets, tables, and formatting, with training
data and cell formulas cleared. The filled example includes a 12-week calisthenics
and movement plan, five exercise groups, Cal-Intervals, and set-based intensity
calculations. Daily A/B plan text links to the weekly Strategy blocks. Both
formats contain the same data. Adapt the example to your needs before training.

## Optional connections

- **Garmin:** connect in settings to import recorded activities. This can run
  without a workbook. See [Garmin activity sync](Using-Sports.md#garmin-activity-sync)
  for setup, stored data, and the experimental Coach option.
- **Calendar:** select **ICS calendar** under **Schedule** for a Google Calendar,
  Nextcloud, or other ICS training feed. See [Schedules and calendars](Using-Sports.md#schedules-and-calendars).

## Current limits

- Desktop only, with one active workbook plan. Finish the current plan before starting or restoring another.
- No workbook write-back, watch workout uploads, calendar write-back, or automatic coaching.
- Sheet names are configurable; arbitrary column mapping and import previews are not available.
- Recurring activities use a weekly schedule; per-occurrence edits and schedule-timezone conversion are not implemented.
- Completed sessions and linked part versions are protected. Removed completed sessions remain cached; removed unfinished rows leave the active plan.
- Generated-note conflicts require manual recovery; there is no conflict-resolution interface.

Development is maintained in a separate private repository.

## Privacy

External requests start after you configure a cloud workbook link, select an ICS
calendar with a subscription link, or connect Garmin. Workbook sync downloads only the configured HTTPS source and never uploads
or edits it. The share URL is saved in plugin settings and may grant access to
anyone with the link. The generated template is offered as a browser download;
the plugin does not read or write files outside the vault.

Imported training data, sync preferences, and generated-block baselines are stored
in vault-local plugin settings. These may travel with your vault sync provider.
Generated notes and guides are written through Obsidian's vault API.
Finished-plan `settings.md` files retain the workbook link, imported plan, and
generated-section baselines in the archive folder. Recovery copies retain full
note contents in hidden plugin storage. These files may travel with vault sync
or backups; remove private links and training data before sharing them.
Garmin tokens use Obsidian secret storage; credentials are never saved. No
telemetry is collected. Plugin settings and compiled output are excluded from
version control.

## License and attribution

Based on the [Obsidian sample plugin](https://github.com/obsidianmd/obsidian-sample-plugin).
The original copyright notice and 0-BSD license are retained in [LICENSE](LICENSE).
Bundled dependency licenses and attribution are in [THIRD_PARTY_NOTICES.md](THIRD_PARTY_NOTICES.md)
and included in the distributed `main.js`, including fflate, read-excel-file, its
saxen-derived parser, worker-f, garminconnect-js, and ical.js.

## Help and support

[Report an issue](https://github.com/trainvent/obsidian-sports-plugin-releases/issues) with
your Obsidian and Sports versions, the error, and steps to reproduce it. Remove
private share links, credentials, and personal training data from attachments.
You can also use [Trainvent support](https://next.trainvent.com/de/software-support/)
or [sponsor development](https://github.com/sponsors/trainvent).
