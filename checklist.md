# Definition of Done

Every item passes, or the summary explains why it doesn't.

## Intake
- [ ] The company list (and customer list, if any) are saved in `input/`, unedited
- [ ] The user's view of why customers buy was written down before any data was shown
- [ ] The look-back window, capacity for `now` and the web-check scope are written down
- [ ] The evidence path (A, B or C) is confirmed after matching

## Signals and sources
- [ ] Each of the five signals is kept or dropped, with a reason tied to the offer
- [ ] Each kept signal has an exact definition, strength, freshness and a "why now" pattern, signed off by the user
- [ ] Any custom signal is marked `custom_<name>` and noted as outside this guide
- [ ] Each kept signal has a source and method (`bulk`, `web` or `not_checked`), tested on a few known companies
- [ ] Blocked sources are recorded with the rows they affect; no block was worked around

## Signals found
- [ ] Every signal in `signals.csv` has a `signal_date` and `signal_evidence`
- [ ] No signal was recorded without a date or a fact
- [ ] News was matched on more than the company name
- [ ] For customers, only events before the start date were used
- [ ] Every row in scope was checked for every kept signal, or `signal_not_checked` says why not

## Evidence
- [ ] Paths A and B: each signal's verdict is shown with customer counts, market rate and lift
- [ ] The user's view from step 1 has a verdict for each reason given
- [ ] Every strength change and every signal kept against the evidence is recorded as the user's decision
- [ ] Path C: every signal is `unvalidated`, and the summary says "(unvalidated)" in its first line

## Rows
- [ ] `list-signals.csv` holds every input row, and no more, following [schema.md](schema.md)
- [ ] `tier` is unchanged on every row
- [ ] No `now` comes from weak signals alone
- [ ] Strong signals on tier 3 or excluded companies are flagged, not moved
- [ ] Current customers are marked and counted separately
- [ ] `now` was checked against capacity
- [ ] Five "why now" lines were spot-checked against `signals.csv`
- [ ] No person names in the outputs, unless the user confirmed their legal basis

## Summary
- [ ] `now` count, capacity and a plain-words verdict are in the first lines
- [ ] Gaps (blocked sources, rows not checked) are stated near the top
- [ ] The user's decision on the work order is recorded
