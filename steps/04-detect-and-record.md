# Step 4: Detect and Record

## Goal
Look for every kept signal on the rows the plan covers, and record each one found in `signals.csv`, with its date and evidence. Do the same for the user's customers, as they were before they started, for the test in step 5.

## Why it matters
This is where the list gets its signals. Every signal has to carry its own proof: a date and a reference someone can check. If the team calls a company because of a "new director" and there isn't one, trust in the whole list is gone.

## How
1. **Run the bulk signals on every row with a register ID.** Download or query the sources from step 3, save them in `sources/` with the date pulled, and join them to the list by `country` + `register_id`. For each row, check each bulk signal against its definition and the look-back window.
2. **Run the web checks on the agreed tiers.** For each company: its own site (careers, news), then a web search for the signals the records don't cover (job posts, funding, new sites). Record what you checked, even when you found nothing.
3. **Record every signal found** as one row in `signals.csv` (columns in [../schema.md](../schema.md)):
   - `signal_type`, `signal_date` (the event date, `YYYY-MM-DD`; if only the month is known, use the first of the month and say so in `signal_detail`)
   - `signal_strength` and `signal_expires` (the date plus the freshness from step 2; for staff growth, the date the next accounts are due)
   - for staff growth, `signal_date` is the end of the financial year the growth was filed for
   - `signal_source_type` and `signal_evidence` (a link, or a record reference such as the dataset and row)
   - `signal_detail`: the facts, in a few words ("managing director appointed 2026-09-03"; "average staff 41 → 52")
4. **No date, no signal.** If a page says a company is "expanding" without a date or a fact, don't record it. If you can't find a date, it's not a signal.
5. **Record what wasn't checked.** For each row, note which signals were checked and which weren't (blocked source, no register ID, outside the web-check tiers). This goes into `signal_not_checked` in step 6.
6. **Detect the signals for customers too** (paths A and B). For each customer with a start date, look for each signal in the look-back window **before the start date**. Use sources you can read back in time: appointment dates, accounts for the earlier years, dated news. Some signals can't be read back (old job posts are usually gone). Mark those as not checkable for the test.
7. **Report the counts:** rows checked per signal and method, signals found per type, rows with at least one signal, sources blocked and rows affected.

## Pitfalls
- **Matching news to the wrong company.** Two companies share a name; the news is about the other one. Match on more than the name: the city, the domain, the register ID in the article.
- **Group news.** A parent company's funding round is not the local subsidiary's. Record it only if the subsidiary is named, and say so.
- **Old posts still online.** A job post from last year can still be on a careers page. Use the posting date, not the date you saw it.
- **The same event twice.** A new site in the register and the same new site in the news is one signal. Record one row, with the better evidence. A new shareholder and a new board member registered within weeks of each other are usually one event (a sale): record both, and say in `signal_notes` that they are one reason to call, not two.
- **Job posts under another name.** Companies often post jobs under a brand or trading name, not the registered name. Matching on the registered name alone misses them; say so in the summary if that's all you could do.
- **Looking after the start date.** For customers, anything after they started is a result of the deal, not a signal before it.

## Done when
Every row in scope is checked for every kept signal or marked as not checked with a reason, every signal in `signals.csv` has a date and evidence, customers' signals before they started are recorded where they can be, and the counts are reported.
