# Record your training

Use the supplied Daily layout first. Customize it only when the way you record
training needs to change. For initial setup and sheet definitions, use the
[workbook guide](Workbook.md).

## Record a session in the supplied workbook

1. Open the session's row in **Daily**. After training, replace prefilled set values
   with what you did and clear unused sets.
2. Enter actual minutes and any notes. If you used added weight, update the
   section's **Weight** to the kilograms actually used; blank means no weight
   entry and zero explicitly means bodyweight.
3. Select TRUE under **Session done**. FALSE or blank leaves the set inputs
   unrecorded. Positive Cal-Intervals rounds are recorded with Session done;
   zero or blank means that circuit was not done.
4. Optionally enter **Effort rating**, from 1 (easy) to 5 (very hard).
5. Recalculate if your workbook uses formulas, save to the cloud file, then select
   **Sync now** in Sports.

Session done marks the whole session completed in the supplied files. They have
no separate Status column. Weight applies to every set in its exercise section;
before completion it is planned weight, and after completion it is recorded weight.

Keep Recurring activities in Recurring. A calendar entry or Garmin recording does
not complete a manual Daily session. Future results and unknown measurements stay
blank; zero is a recorded value.

### Notes and time entries

Use **Notes topic** to route a reflection. General stays with the session;
Muscle-up, HSPU, and Pistol also appear on their selected goal page. Skills A,
Skills B, Technique, Swimming, Running, and Cal-Intervals route to the corresponding
routine. Notes are commentary, not measured goal results.

For timed set inputs, use a number in the prescription's unit or a clock-style
duration. Native spreadsheet times can display as `mm:ss`; enter `0:00:15` for
fifteen seconds so the spreadsheet does not interpret it as fifteen minutes.

## Review the result

Select **History** in the dashboard or open the dated day note for sets, notes, and session
coverage. Use the weekly note for your review and **Stats** for trends.
See [Using Sports](Using-Sports.md#your-notes) for the full note map and
[training charts](Using-Sports.md#training-charts) for chart scales.

If you use the example's Scoring sheet, performance measures target attainment;
partial results can still produce a score, so check **Scored metrics / Planned
metrics**. Felt effort does not change performance. Formula inputs and calculations
are documented in [Scoring and Library](Workbook.md#scoring-and-library).

## Alternative Daily layouts

The filled example uses A–E exercise groups; the blank template starts with A/B/C.
Group names, Cal-Intervals, and five set columns are examples, not required exercise
names or limits. The plugin reads the tab selected under **Tracking sheet**.
Preserve the supplied layout while filling it. When redesigning, keep session IDs
and recorded history, and adapt any dependent formulas, tables, and validation.

### Customize one row per session

Rename, add, or remove exercise groups, or extend set columns. A grouped
heading can be `Squat`, `D`, `Intervals`, or any other name, above **Done** and
**1, 2, 3, …** (or **Rounds**). Structural columns retain their existing names.
Do not merge two exercise groups under the same name.

Flat equivalents are `Squat done`, `Squat 1 result`, `Squat 2 result`, etc.
`Circuit done` with `Circuit rounds result` also works. Numbered inputs and rounds
remain gated by the corresponding Done flag.

For a flat session layout, required headers are `Date`, `Block`, and `Plan`.
Optional fields include `Title`, `Planned minutes`, `Actual minutes`, `Status`,
`Notes`, `Session ID`, `Part version`, and `Sport`. Custom measurement columns end
with ` result`; completion columns end with ` done` and contain TRUE, FALSE, or
blank. Use `Reps result` rather than an arbitrary `Reps` header. Grouped headings
are the exception: their subcolumns are imported as `<group> 1 result`, etc.

For numeric comparisons, match the group name in Plan, one prescription per line:

```text
Squat) Back squat: 6 x 5
Carry) Farmer carry: 4 x 30 m
Hold) Wall hold: 3 x 20 sec
Circuit: 4 rounds
```

Group names, exercise names, units, and set counts are configurable. Compound
instructions stay readable as text. Prefer the row-based format for changing
per-set targets or recording multiple metrics instead of encoding these in prose.
Example metadata `max_sets` and `max_reps` are descriptive; they do not impose
import limits or automatically resize a workbook.

### One row per set or measurement

Choose this format for variable per-set targets or several metrics per set.

Use these exact headers. Additional sets and exercises add rows, not columns.

| Date | Session ID | Exercise | Set | Unit | Target | Result | Done |
| --- | --- | --- | --- | --- | --- | --- | --- |
| YYYY-MM-DD | strength-1 | Squat | 1 | reps | 8 | 8 | TRUE |
| YYYY-MM-DD | strength-1 | Squat | 1 | kg | 60 | 55 | TRUE |
| YYYY-MM-DD | strength-1 | Squat | 2 | reps | 6 | | FALSE |
| YYYY-MM-DD | strength-1 | Squat | 2 | kg | 65 | | FALSE |
| YYYY-MM-DD | strength-1 | Farmer carry | 1 | m | 30 | 25 | TRUE |
| YYYY-MM-DD | strength-1 | Wall hold | 1 | seconds | 00:30 | 00:25 | TRUE |
| YYYY-MM-DD | intervals-1 | Run work | 1 | seconds | 60 | | FALSE |
| YYYY-MM-DD | intervals-1 | Run recovery | 1 | seconds | 90 | | FALSE |

These rows are illustrative, not imported training achievements.

- Required headers: **Date, Exercise, Set, Unit, Target, Result**. An optional
  **Session ID** distinguishes sessions on the same date; keep IDs stable.
  Without it, identity is Date + Block, so repeat Block on every row of that
  session (or leave it blank on every row).
- **Exercise** is any name. **Set** is any positive whole number, not a fixed
  1–5 range. Rows sort by set number; gaps retain their original labels.
- **Unit** is explicit and customizable: reps, reps/leg, seconds, minutes, m, km,
  kg, rounds, RPE, %, or another metric. Separate rows with the same exercise and
  set can record several metrics, such as reps and load. Exercise + unit + set
  must be unique within a session. Each unit stays separate in tables and graphs.
- Optional **Aggregate** controls each exercise/unit graph: `total` (default),
  `average`, `min`, `max`, or `last`. Set it consistently on all rows of that
  exercise/unit. For example, use `average` for kg or RPE, `max` for peak load,
  and `total` for volume or time. Individual set values always remain visible.
- **Target** and **Result** are independent nonnegative numbers or blanks. Targets
  can vary every set. Blank target means no numeric target; blank result means
  unrecorded. Zero is a real value. Text instructions belong in **Plan** or **Notes**.
- Time units accept numbers, native Excel times, `mm:ss`, or `hh:mm:ss`. Numeric
  minutes convert to seconds; colon times always mean a duration, independent of
  the chosen time unit. Other units remain exactly as named (no km/m conversion).
- With a **Done** column, only TRUE records a result. FALSE and blank are distinct
  unrecorded states. Without that column, a nonblank Result is an explicit result.
  Targets alone never become achievements.
- Optional session fields: **Block, Part version, Title, Sport, Plan, Status,
  Planned minutes, Actual minutes, Notes**, and custom columns ending in ` result`.
  Set Block and Part version on the first row of a linked session. Other shared
  metadata may appear once or repeat consistently. Conflicting values are rejected;
  notes from different rows are retained. Date is required on every row.
- **Plan** is free text. Structured targets and results drive the graphs without
  parsing instructions. Use it for supersets, tempo, rest, AMRAP/EMOM instructions,
  technique cues, or descriptions of a training regime.
- A session's Status is independent of set completion. Use `completed` explicitly
  when appropriate. Without Status, recorded results mean `in-progress`.
- Keep goal measurements in custom ` result` columns with the same exact names
  used by Strategy's goal mappings. They are independent of set metrics.

There is no fixed exercise count, no mandatory Cal-Intervals, and no five-set limit in
this format. It supports numeric measurements for varied regimes; the plugin
does not infer exercise relationships or automatically score a regime.

## Duration and load conventions

Use human-sized units: a run lasting 20 minutes is Unit `minutes`, Amount per set
`20`, not `seconds` and `1200`. Short holds can stay in seconds. Keep target and
result in the same unit. For example, `Handstand walk: 3 x 3 m` uses three set
fields with metres, including decimal distances. Sports displays them as metres.
The filled example weights planned intensity by sets,
without converting time into reps. A running
activity kept only in Recurring uses its Minutes field and needs no Scoring row.

For manual grouped tracking, `A) Easy run: 1 x 20 minutes` supplies a minute target;
a plain numeric result `22` means 22 minutes. Clock-style `22:00` also means 22
minutes. For second-based prescriptions, numeric results are seconds. Obsidian
normalizes times internally and presents minute-based measurements in minutes;
short seconds-based holds retain their seconds unit.

For optional section weights and the example formulas, see
[Exercise weights](Workbook.md#exercise-weights).
