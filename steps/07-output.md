# Step 7: Output

## Goal
Deliver the list with signals, the file of every signal found, and a one-page summary with the work order, and get the user's decision on who the team works first.

## Why it matters
The team needs one file to work from, with the order and the reason on every row. Anyone who doubts a signal needs to be able to check it. And the user needs to see, on one page, what the signals found, how far they were tested, and what wasn't checked.

## How
1. **Write `list-signals.csv`:** every input row, with the `signal_` summary columns from step 6, following [../schema.md](../schema.md). Sort by `tier`, then `signal_priority` (`now`, `soon`, `watch`, empty), then the score from the ICP guide if there is one.
2. **Write `signals.csv`:** one row per signal found, live or expired, for prospects and customers, following [../schema.md](../schema.md). Sort by `country`, `register_id`, `signal_date` (newest first).
3. **Write `signals-summary.md`** in the structure below.
4. **Go through [../checklist.md](../checklist.md).**
5. **Get the user's decision** on the work order. This is checkpoint 3. Record it in the summary.

### `signals-summary.md`
```
# Signals summary: <run name>

`now`: <n> companies (<n> in tier 1, <n> in tier 2) against capacity of <n> for <period>. <(unvalidated) on path C>
<one-sentence verdict: which signals mattered most, in plain words>
List: <file, source, rows>. Signals checked on <date>. Evidence: path <A/B/C>, <n> customers tested.

## Work order
<table: the top companies by tier and timing — name — tier — signal — date — why now>

## Signals used
<table: signal — definition — strength — freshness — source and method — verdict>

## What was found
<table: signal — rows checked — signals found — live — rows not checked and why>

## Evidence
<path A/B: the lift table with counts; the user's view vs the evidence. Path C: market rates, and "(unvalidated)".>

## Timing by tier
<table: tier — now — soon — watch — none — not checked — current customers>

## For the user to review
<strong signals on tier 3 or excluded companies; anything that looks wrong>

## Decisions made
- <signals dropped and why, strength changes, rule changes, user decisions against the evidence>

## Not covered
- Sources that were blocked or not free, and the rows affected
- Custom signals outside the five, if any
- Paid tools were not used; they may find more signals. Choosing them is the user's call.
```

## Pitfalls
- **A summary that hides the gaps.** If job posts were blocked for half of tier 1, that goes near the top, not at the bottom.
- **"Why now" lines that read as claims.** Each line must come from the evidence on that row. Spot-check five rows against `signals.csv` before you deliver.
- **Person names in the outputs.** Unless the user confirmed their legal basis in step 3, the files hold roles and dates only.

## Done when
The three files are written, the checklist passes or the summary says why not, and the user's decision on the work order is recorded.
