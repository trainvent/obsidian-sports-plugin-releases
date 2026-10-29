# Adapting the Sports workbook

[Workbook](Workbook.md) · [Tracking](Tracking.md) · [Using Sports](Using-Sports.md) · [Troubleshooting](Troubleshooting.md)

Use this guide to fill the supplied template or adapt a workbook. For daily
recording, see [Tracking](Tracking.md); for note navigation and integrations, see
[Using Sports](Using-Sports.md).

In **Settings → Sports**, open **Workbook guide → Open guide**, then choose a
starting point in XLSX or ODS:

| Option | Contents | Choose it when |
| --- | --- | --- |
| **Blank XLSX template** (`Training-Template.xlsx`) | Five sheets with a generic three-group Daily layout; training data and formulas cleared | You want to fill the workbook yourself or with a chatbot |
| **Blank ODS template** (`Training-Template.ods`) | All five sheets, tables and formatting; training data and formulas cleared | You prefer LibreOffice Calc or ODS |
| **Example workbook** (`Training-Example`) | A filled 12-week plan, library, exercise weights, and scoring | You want to learn the format or adapt a working example |

Use this guide with either file. Adapt goals, exercises, schedule, equipment and
training volume before uploading and syncing. The example is not a personalized
recommendation. Sports reads the workbook and never writes results back to it.

## In this guide

- [Fill the blank template](#fill-the-blank-template)
- [Check the workbook](#check-before-returning-the-workbook)
- [Workbook contract](#keep-the-workbook-contract)
- [Strategy](#strategy), [Recurring](#recurring), and [Daily](#daily)
- [Protect recorded history](#protect-recorded-history)
- [Scoring and Library](#scoring-and-library)
- [ODS imports](#ods-imports)

## Fill the blank template

Keep all sheets, section labels, header rows, native Excel tables, formatting and
input controls by default. Unused **data cells** may remain blank. Do not clear
whole sections or remove their headers to disable a feature. Remove or redesign
structure only when the user explicitly requests it.

1. In **Strategy → Plan**, set a stable plan_id, your plan_name, timezone and
   Monday start_date. Keep schema_version at 1. Fill Goals, Parts and Week plans
   for the agreed plan, retaining their IDs and links. Put data directly below
   each header; blank rows end Strategy tables. Preserve Plan summary's labels
   and Plan recap's prompts, even before any training has been recorded.
2. In **Daily**, enter dated sessions with readable Plan, Title and planned
   minutes. Block links to a Parts ID. Write explicit exercise targets such as
   `A) Band squat: 3 x 10` in Plan. Put each exercise on its own actual line,
   with group names matching its input columns. Put time, warm-up, rest and
   other instructions on separate lines, never before/after a dose on the same
   line. Visual cell wrapping is not a line break. For blank future results, leave
   the numbered rep/time cells empty until training; targets still come from Plan.
   Alternatively prefill targets there and replace them with actuals before
   selecting Session done. Never treat planned targets as completed results.
   Add stable Session IDs if a date and block contain multiple sessions.
3. In **Recurring**, enter activities managed as a repeating timetable, such as
   a weekly run recorded by Garmin. Do **not** expand those activities into dated
   Daily rows. Daily is for the separate manual workouts you plan and record
   there. If a workout needs manual set results, choose Daily instead of Recurring;
   repeating on the calendar alone does not make a manual workout a Recurring row.
   Activity enables an entry; use positive Minutes or start/end times. Recorded by
   identifies the actual recording source (for example Garmin), not a request to
   copy events into Daily. Enable **Show schedule** to display the
   timetable alongside the separate manual workouts. Recurring supplies no manual
   results, Daily scoring rows or recorded-performance statistics.
4. In **Library**, add exercises, units and equipment. Use minutes for runs
   (20 minutes, not 1200 seconds) and seconds for short holds. Intensity ratings and
   Growth per kg are optional for tracking, but required inputs where the agreed
   scoring method uses them. Do not invent measured resistance for bands. Describe
   the band in Equipment Notes and the prescription; Weight accepts added kg only.
5. Agree on scoring before filling the workbook. If requested, populate Scoring's
   exercise targets, formulas and per-session summaries, and Daily's planned
   intensity. Scoring Date/Session must match Daily Date/exact Title, not Block.
   Use the calculation reference below only when the user chooses
   that method; label provisional ratings as planning estimates. If scoring is
   declined or still undecided, keep its structure and say it remains unconfigured.
6. Save calculated formula results, verify the workbook as described below, then
   upload it, configure the sheet mappings and select **Sync now**.

The blank template retains five sheets, including A/B/C set columns,
Cal-Intervals, Library, Scoring, Plan summary and Plan recap. These labels
and calculation slots are structure, not prescribed exercises. Training data and
all cell formulas/cached results are empty; layout defaults remain editable.
Enter dates and prescriptions directly. Build only the calculations agreed with
the user. The later formula examples describe the filled example, not formulas
already present in this template. The ODS template has the same full five-sheet
layout. See [Tracking.md](Tracking.md) for alternative tracking layouts when a
user requests a redesign.

## Optional sections and sheets

Optional means their **use** can be declined, not that an agent should delete
provided structure. Keep every supplied section and sheet unless removal is
explicitly requested. Report which features are configured, unused or awaiting
input. Do not silently choose a reduced workbook.

| Area | When unused | When enabled |
| --- | --- | --- |
| Goals and Parts | Keep labels/headers; leave unused data empty | Fill goals, prescriptions and their ID links |
| Week plans | Keep labels/headers | Fill weekly dates, focus, targets and minutes |
| Plan summary | Keep Metric/Value headers and metric labels | Add summary formulas suited to the plan; unrecorded performance stays blank |
| Plan recap | Keep Prompt/Response headers and prompts | Leave future reflections blank; record useful setup decisions without inventing outcomes |
| Recurring | Keep weekdays and headers; leave Activity empty only when no schedule is agreed | Fill the repeating activities and identify where results are recorded |
| Scoring | Keep title, headers, native table and any supplied settings area | Add agreed calculations and cached results; no fabricated actual performance |
| Library | Keep exercise/equipment/interval headers | Add references actually used, with ratings only when scoring needs them |
| Daily Weight | Leave blank for unweighted sections | Enter kg for the section and update it to the weight used before completing the session |

Unused Cal-Intervals or set inputs can remain blank without erasing their headers.
If removal or a new tracking layout is requested, check formulas, table ranges,
validations and import mappings before changing structure.

### Fill it with a chatbot

Attach the workbook and this guide. For example:

```text
Use Workbook.md to fill the attached Training-Template workbook for my needs.
Ask for missing goals, availability, experience, equipment and starting levels.
Agree on recurring activities and whether/how to calculate intensity and scoring.
Keep all supplied sheets, tables, section labels, header rows, formatting and
controls. Leave unused data blank; do not delete structure unless I request it.
Do not invent completed workouts, measured baselines, equipment kg or results.
Leave future actuals blank. Recalculate and save any formulas you add.
Check the entire workbook against the original template, including unused areas.
Return the workbook and a short list of configured features, unused features,
assumptions and any missing input. Do not call the plan complete if requested
features are still missing.
```

### Check before returning the workbook

Compare every supplied sheet with the original, including all Strategy sections,
Scoring's headers and tables, Library sections and Daily Weight fields. Preserve native Excel
tables and their header ranges, not just visible text. Write beneath headers;
for example Equipment's first entry is Library!A62, not A61.

Verify dates and stable session/part references, the agreed recurring schedule,
equipment and planned intensity/scoring coverage. Check that Recurring activities
have not also been generated as Daily sessions. Scoring summaries belong only to
Daily sessions; do not invent Daily rows just to score a recurring activity. There is no need to make up
load rows for bands or write future recap answers merely to fill empty cells.
With scoring enabled, verify every dated session has its intended summary. A
future session can have planned intensity and Planned metrics; its Result and
Performance must stay blank, with Scored metrics 0. Test a completed session in a
disposable copy: results, performance and coverage must update and save correctly.
Check that clearing results returns them to blank, rather than a fabricated zero.

For an existing plan, also preserve recorded history. Report a missing input or
unsupported metric rather than deleting the affected table. Successful import
alone does not establish that the requested workbook is complete.

## Reading the filled example

The filled example has three weekly strength/movement sessions and optional
easy technique practice. Friday includes Cal-Intervals. Weeks 4 and 8 reduce
volume; week 12 records tests. Added Weight fields start blank.

Daily's A/B plan text references that week's blocks in **Strategy!H:I**.
Edit those blocks to change the shared exercise text. Warm-up and rest instructions
remain in Daily. These text links do not change set inputs or Scoring targets.

## Example workbook color key

| Color | Meaning | How to use it |
| --- | --- | --- |
| Pale green, alternating tones | Editable entry cells | Enter or adjust your training values. |
| White / light gray, alternating tones | Reference information and formulas | Read the plan and preserve formulas. |
| Neutral blue-gray | Headings | Keep structural column names; exercise group names are customizable. |

Both editable and reference areas alternate row tones to help you follow a session
across the sheet. Colors are cues, not access restrictions.

In **Daily**, actual minutes, Session done, exercise-group entries, Cal-Intervals, Notes,
Notes topic, and effort inputs are editable. Dates, plans, titles and planned minutes stay
neutral. In **Recurring**, start/end times, activity, recorded-by and notes are
green; the calculated Minutes column stays neutral. Strategy's `max_sets` and
`max_reps` cells and all headings stay neutral.

## Keep the workbook contract

- Save as `.xlsx` or `.ods`, under 5 MB. Do not add macros or external workbook links.
- Keep the tabs **Strategy**, **Recurring**, **Daily**. In Sports settings select
  **Strategy** as the strategy sheet and **Daily** as the tracking sheet.
  Select **Recurring** as the weekly schedule sheet. Each mapping accepts an exact
  tab name; leave a mapping blank to disable that import. Older workbooks with **Training log** remain supported.
- Keep section names alone in column A. Put their exact headers on the next row.
  A section name alone in column A begins the next table. Do not insert blank
  rows inside a Strategy table; they end that table.
- Do not put decorative titles, legends or commentary inside the data tables.
  Extra Daily columns must follow the supported names below.
- Keep identifiers unique and nonempty. Use simple IDs such as `pull-strength`.
  Preserve references when changing IDs in a new, unrecorded plan.
- Use real dates formatted `yyyy-mm-dd`, or explicit `YYYY-MM-DD` text. Use
  nonnegative numbers for minutes. Blank means unrecorded, not zero.
- The blank template has no cell formulas. If you add formulas or adapt the
  filled example, calculate and save their cached results before returning the
  file. The plugin reads saved values, not formula expressions.

## Strategy

The XLSX and ODS templates and filled examples retain these sections and headers.
Leave unused section data empty; remove structure only at the user’s request:

| Section | Headers |
| --- | --- |
| Plan | `schema_version`, `plan_id`, `plan_name`, `timezone`, `start_date`, `max_sets`, `max_reps` |
| Goals | `goal_id`, `title`, `benchmark`, `baseline`, `test`, `category`, `garmin_types` |
| Parts | `part_id`, `version`, `title`, `prescription`, `goal_ids` |
| Week plans | `Week`, `Start`, `Phase`, `Focus`, `Targets`, `Advance when`, `Minutes`, `A`, `B` |
| Plan summary | `Metric`, `Value` |
| Plan recap | `Prompt`, `Response` |

**Plan:** exactly one row. Keep `schema_version` equal to `1`. Use a valid IANA
timezone, such as `Europe/Berlin`. Choose a stable `plan_id`; switching an imported
plan ID requires clearing the cached plan. `start_date` stays at **E3**. Set a
Monday before recording history. Plugin-created workbooks start next Monday in
the user's local calendar and use the user's local timezone.

The example's `max_sets` and `max_reps` cells describe its example layout only.
They do not impose an exercise count, require A/B/C/Cal-Intervals, or limit set counts.
Changing these cells does not automatically resize the workbook.

**Goals:** use `milestone` for skills to achieve or `maintenance` for abilities to
maintain. Baselines and results must reflect actual information; do not invent
measurements or achievements.

Each goal creates a note at `Goals/<goal_id>.md` under the configured Sports notes
folder. Keep the ID stable so reviews stay attached when renaming a goal. The
review area is outside the generated section and is preserved on every sync.
Goal category and Garmin types appear in note properties;
baseline, target and test standard stay in the body. These properties follow the
workbook on sync. Edit their values in Strategy; unrelated custom properties are preserved.

Tracking results and Garmin activities are independent sources available to every goal.
Results match the goal ID/title and the muscle-up, HSPU and pistol aliases when
there is one unambiguous match. Nonempty results are copied with date, session
status and shared session notes.

- `garmin_types`: comma-separated stable Garmin activity type keys. `running`
  matches running, track/trail/indoor/treadmill running and supported run variants.
  `swimming` matches pool and open-water swimming. Other keys match exactly.
  Activity names such as German `Laufen` do not determine the match. Without an
  explicit mapping, goals named/identified as running or swimming are detected.
  Custom goals should use explicit type keys to avoid guessing from goal prose.
- A running aspiration can have `Running result` and `running`; a swimming
  maintenance goal can have `Swimming result` and `swimming`. The corresponding result column must exist in Daily.
- The example includes swimming as a maintenance goal. Its starting routine is
  reported background, not a recorded performance or a change to Recurring.

**Parts:** `part_id` and `version` together identify a training block. Daily `Block`
values refer to these IDs. In `goal_ids`, separate goal IDs with commas, for example
`muscle-up, pistol`. Each must exist in Goals. A legacy `PartGoals` table with
`part_id`, `version`, `goal_id` is also supported.

**Week plans:** use unique positive week numbers and unique Monday Start dates.
In the filled example, Start formulas link to `$E$3`; preserve or adapt those
when using that example. Enter explicit Start dates in the formula-free template.
`Minutes` is the manual training
budget; recurring tracker activities are separate. `A` and `B` contain the weekly
block prescriptions and feed Daily Plan formulas. Changing block names or adding
other block columns requires adapting the Daily formulas as well. The plugin
currently imports A and B as weekly prescriptions. Keep a full description in
Parts and Daily Plan for any other blocks.

## Recurring

Keep `Weekly schedule` in A1 and these headers in row 2:

`Day`, `Time Start`, `Time End`, `Minutes`, `Activity`, `Recorded by`, `Notes`.

Use English weekday names. Additional rows can repeat the day or leave it blank
to inherit the preceding day. A blank Activity creates no event; blank spare rows
are allowed. Use native spreadsheet times formatted `hh:mm`, or `HH:mm` text.
With text times, replace the duration formula with a positive numeric duration.
The example's formula uses native times, leaves incomplete times blank, and
supports overnight activities. Equal start/end times produce zero and must be
corrected for an activity. Keep duration positive or blank; missing cached duration
can be derived from valid start/end times during import.

Recurring activities are planned events, not completed sessions. They appear in
the strategy note; enable **Show schedule** for the dashboard and weekly
notes. Keep the weekly schedule in Recurring only. For legacy workbooks with a `Weekly schedule` section in Strategy, select
**Strategy** as the weekly schedule sheet as well. Only the selected schedule is imported.

## Daily

The supplied workbooks use one row per manual session and two header rows.
The filled example has groups A–E; the blank template starts with A/B/C.
These group names, Cal-Intervals, and five numbered set fields are examples, not required
exercise names or limits. Keep this layout when filling the template; see
[Tracking](Tracking.md#alternative-daily-layouts) when redesigning it.

| Field | Filled example columns | Blank template columns |
| --- | --- | --- |
| Date, Block, Plan, Title, Planned minutes, Actual minutes | A–F | A–F |
| Session done | G | G |
| A/B/C set inputs 1–5 | H–L, N–R, T–X | H–L, N–R, T–X |
| D/E set inputs 1–5 | Z–AD, AF–AJ | Add groups if needed |
| Weight per group | M, S, Y, AE, AK | M, S, Y |
| Cal-Intervals rounds | AL | Z |
| Notes, Notes topic | AM–AN | AA–AB |
| Planned intensity, Effort rating | AO–AP | AC–AD |

The same column positions apply to XLSX and ODS. Preserve group headings and
subcolumn alignment when adding or moving fields.

**Session identity:** Date plus Block identifies a session unless you add an
explicit Session ID. Use distinct stable IDs for sessions sharing a date and
block. Block refers to a Strategy Parts `part_id`; use Part version when that ID
has several versions. Blank or `empty` Block means no linked strategy part.

**Plan:** put each exercise on its own actual line, with its group name matching
the input columns. Session Block A/B and exercise groups A–E are separate labels.
Keep warm-up, tempo, rest, and other instructions on separate lines:

```text
18:00; warm up 5 minutes.
A) Band squat: 3 x 10
B) Band bent-over row: 3 x 10
C) Band chest press: 3 x 10
Rest 60 seconds between sets.
```

Visual wrapping is not a line break. Check that each prescription produces the
intended group, set count, unit, and target in the comparison. The blank template
has no automatic dates or prescriptions; enter these directly or build formulas
for your own plan.

**Completion:** the supplied files use Session done and have no Status column.
Other layouts can use Status: `planned`, `in-progress`, `completed`, `skipped`,
or `cancelled`. Exercise-specific Done flags record exercise results without
completing a session. Without explicit completion, recorded results imply
`in-progress`. Recording rules and Notes topic destinations are in
[Tracking](Tracking.md#record-a-session-in-the-supplied-workbook).

## Protect recorded history

Never shift the start date, change session identity, or rewrite completed training
when adapting future weeks. Preserve completed rows, dates, IDs, results and part
versions. If a part has completed history, preserve that part definition and add a
new version for future sessions. Keep the old version and select versions in Daily.
The plugin rejects changes to linked part definitions and dates it can recognize
as completed history, and retains missing completed sessions. Stable explicit
Session IDs make those checks more reliable.

Write reflections outside generated sections in Obsidian. Sync protects those
sections against accidental edits; change plans in the workbook instead.

## Scoring and Library

[Training charts](Using-Sports.md#training-charts) explains how these values are displayed.

The example includes a **Scoring** formula sheet. Keep the plugin's three import
mappings on Strategy, Daily, and Recurring. The filled example uses one Scoring
table for exercise targets, results, intensity and performance. Scoring is read
automatically alongside Daily; keep its tab name.

**Scoring session key:** Date and Session must match a dated Daily row’s Date
and exact **Title**. Session is not the Block/Parts ID or Session ID. Repeat that
date/title for its exercise rows; place the P:S summary on only the first row of
each session. Different sessions on the same date need distinct titles for this
summary lookup. Daily Planned intensity must link to its Scoring summary value.

Result links to explicit Done and result fields in Daily. Exercise performance
is result / target × 100. The first row of each session contains its planned
intensity, median Performance, Scored metrics and Planned metrics. Coverage
makes partial results visible. Cal-Intervals occupies one row per session, scoring
completed rounds and using its shared Library definition for intensity.

The example calculates **Planned intensity** from exercise assumptions and planned
volume, rounded to one decimal on a **0–10** scale (0 means no planned demand,
10 means highest planned demand). Optionally enter **Effort rating** (1–5)
afterward to record how hard it felt, or leave it blank. Neither rating affects
the performance calculation. No duration × RPE score is required or inferred.
When extending the workout layout, update Scoring's actual-cell references,
explicit targets, and the Daily median/count ranges for that session.
Recalculate and save the workbook before syncing.

### Exercise library and added load

**Library** holds the reference data. Keep this tab name: it is imported
automatically alongside Strategy or Daily.

Preserve section labels and header rows; write entries underneath them. In the
unchanged XLSX layout, Equipment is the section label at **A60**, headers are
**A61:D61**, and the first equipment entry belongs in **A62:D62**.
For resistance bands, leave Min kg and Max kg blank unless you have a meaningful
measured range. Describe the band/resistance in Notes and name it in the workout
prescription. Weight is for added kilograms; bands do not require a weight value.
Base intensity and Growth per kg may stay blank when you are not using scoring.

| Table | Headers |
| --- | --- |
| Exercise arsenal | `Group`, `Exercise`, `Unit`, `Base intensity (0–10)`, `Growth per kg` |
| Equipment | `Equipment`, `Min kg`, `Max kg`, `Notes` |

The XLSX arsenal occupies **Library!A2:E58**. Units are in **C**, base intensity in
**D**, and growth per kg in **E**. Growth is an editable relative multiplier:
4% means each added kg increases the exercise rating by 4% of its base rating.
The seeded rates are planning estimates, not measured physiological effects.
Pulling and muscle-up exercises start at 4%/kg; upright band transition drills
and pistol variations at 3%/kg; push-ups, squats and dips at 2%/kg.
Pike push-ups, handstands/HSPU, low-bar drills, inverted work and mobility
leave this field blank. A blank rate leaves the base intensity unchanged.
Rates do not prescribe vest use: only Daily Weight entries add planned weight.
Weighted and unweighted work share the same exercise entry; there are no separate
vest variants. The Cal-Intervals definition supplies its own work seconds.

**Exercise arsenal:** one exercise per row, unique across the arsenal. Repeat the
group on each row, or leave Group blank to inherit the preceding group. Start
with a nonempty group. **Never put a comma or colon in an exercise name.** These
characters separate items and prescriptions in the example's block text.
Use `High pull (chest-to-bar intent)`, not `High pull, chest-to-bar`.
Keep dosage outside the arsenal name: write `Pike push-up` here and
`Pike push-up: 3 x 5` in the weekly block. Commas are allowed between exercises
in block prescriptions, and are required as separators in `goal_ids`.
The arsenal is imported as reference information; it does not automatically
rewrite or validate the free-text prescriptions. Update matching text yourself.
The legacy `Exercises` table is not supported.

### Exercise weights

Each Daily section (**A**, **B**, **C**, or a custom exercise group) can have a
**Weight** subcolumn after its set fields. Enter kilograms, or leave it blank.
The value applies to every set in that section; zero explicitly means bodyweight.
There is no separate Loads sheet. Keep **Weight** beneath its group heading so
Sports can associate it with the matching exercise in Plan.

The example has no preset added loads. Cal-Intervals remains unweighted.
Enter the weight you actually use before
selecting **Session done**. Until completion, kg appears only as planned weight;
a completed section records the entered weight alongside its set results.

Scoring reads Weight directly from Daily: **M, S, Y, AE, AK** for groups A–E
in the filled example. Library supplies exercise ratings and growth per kg.

### Duration units

Use the same visible unit for each target and result. Handstand walking uses metres;
timed practice uses seconds or minutes. See [Duration and load conventions](Tracking.md#duration-and-load-conventions)
for numeric and clock-style inputs.

### Load-adjusted intensity formula

```text
loaded_intensity_i = MIN(10, base_intensity_i × (1 + planned_kg_i × growth_per_kg_i))
set_weight_i = prescribed_sets_i
circuit_set_weight = rounds × station_count
circuit_intensity = SUM(station_intensity × work_seconds) / SUM(work_seconds)
session_intensity = ROUND(SUM(loaded_intensity_i × set_weight_i)
                          / SUM(set_weight_i), 1)
```

For example, a base rating of 5 at 2%/kg becomes **5.6 at 6 kg**. With Weight left blank,
planned kg is 0 and the base rating is unchanged. Ratings are capped at 10 before
averaging. The filled example weights ratings by prescribed sets. Reps, metres,
and seconds remain separate targets; none is converted into another unit.

In the Scoring table, **C:F** holds exercise, unit, sets and amount per set;
**G:I** holds target, result and exercise performance; **J:M** holds base intensity,
planned kg, growth and loaded intensity. **N:O** holds set weight and contribution.
**P:S** contains the session summary on its first row. For example:

```excel
=MIN(10,J5*(1+K5*L5))
```

**Scoring!P3** combines its session rows; **Daily!AO3** links to that result:

```excel
=IF(COUNT(O3:O7)<>COUNT(N3:N7),"",ROUND(SUM(O3:O7)/SUM(N3:N7),1))
```

Changing plan prose does not rewrite Scoring’s sets or amounts. Update them and
the performance targets together. **Library!A65:F70** defines Cal-Intervals once:
four exercises, each with editable work and rest seconds. The initial timing is
30 seconds work + 20 seconds rest. Station intensity is weighted by its share of
work time; planned rounds multiply the number of station sets. Rest is excluded.
Missing or duplicate exercise matches and invalid inputs
leave intensity unavailable. Rep/time performance and felt effort remain
separate; added kg is shown as its own comparison metric, not added to reps.

### End-of-plan recap

At the bottom of Strategy, **Plan summary** shows planned/completed sessions,
recorded manual minutes, and median recorded performance. **Plan recap** has six
short response fields for goal progress, what worked, changes, recovery, load
observations, and the next plan. Completion uses **Session done** in the provided files, or explicit **Status** in other
layouts. Tracker imports and exercise-specific Done flags do not complete a session.

## ODS imports

ODS uses the same sheet mappings and training layouts as XLSX. In LibreOffice
Calc, save a copy as `.ods`, recalculate and save, then update the plugin’s cloud
workbook link. Sports imports saved cell values, including formula results; it
does not evaluate formulas. Verify calculated intensity and Done values after
conversion. Choose **Download XLSX** or **Download ODS** in settings. Both start next Monday.
Both starting points use a manual TRUE/FALSE **Session done** dropdown. In the
filled example, Notes topics, Weight fields, Library, Scoring and Cal-Intervals use the
same structure in both formats. Both blank templates keep all five sheets and
their tables, formatting and controls, with training data and cell formulas cleared.
