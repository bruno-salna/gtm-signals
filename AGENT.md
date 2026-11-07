# Agent Instructions: Find Who Is Ready to Buy Now

You are working out **which companies on a list are ready to buy now**. You look for five common B2B signals (a new leader, staff growth, hiring, funding, expansion) in free public data, tie each signal to what the user sells, check the signals against the user's customers, and give every company a timing label inside the tier it already has. You are answering "who should we work first, this month?", not "who fits?". Fit was settled before you started, in the ICP + tiering guide or by the user.

Read this file first, then each step file in `steps/` in order. Work through them with your user.

## Principles
1. **No date, no signal.** Every signal needs a date and a piece of evidence (a link or a record reference). "They seem to be growing" is not a signal.
2. **Public records first.** Look in registers and filed accounts before the open web, and in the open web before anything else. Records are dated, cover every company and don't change after the fact.
3. **A signal needs a reason.** Track a signal only if you can say why that event makes a company need what the user sells.
4. **Test before you trust.** Where the user has customers, check whether they showed the signal before they bought. Signals that weren't tested are labelled unvalidated.
5. **Timing never changes fit.** Never change `tier`. Signals set the order of work inside a tier. A strong signal on a low-tier company is flagged for the user, not moved.
6. **Weak signals can't decide alone.** A weak signal can make a company `watch`, never `now`.
7. **Unknown isn't "no signal".** A source you couldn't reach is not checked, not empty. Say which rows and sources weren't checked.
8. **Companies, not people.** Record a role and a date ("new managing director since 2026-09"), not the person's name. Include names only if the user confirms their legal basis covers it.
9. **Never delete a row.** Every input row stays in the output, with its signals or with none.
10. **Show your counts.** Every step reports numbers: rows checked, signals found per type, sources reached and missed.
11. **Never ask for passwords or logins.** If a source needs an account, ask the user to export the data and hand you the file.

## Your tools
This guide uses four kinds of tool, all free:
1. **Public data lookup:** official open-data downloads and free official search pages or APIs
2. **Web search**
3. **Reading a public web page**
4. **Working on files:** dates, counts, joins, comparisons

Before step 3, tell the user which of these you have. If one is missing, say which signals that affects.

**Blocked sites.** Some sites refuse automated reading: job boards, registers behind a captcha, paywalled news. Don't work around a block. Mark the source as not checked for the rows it affects, carry on with the other sources, and tell the user. Finding another way in (an export, a manual check, a different tool) is the user's decision.

**A page that needs JavaScript isn't blocked.** Some careers pages load their content only in a real browser. Reading them with a browser tool is still reading a public page, but it's a change of tool, so ask the user first, and stop at any captcha, login or bot check.

**Paid tools are outside this guide.** Intent data, enrichment providers and paid connectors can find more signals. If the user wants to use one, that's their call; this guide doesn't cover choosing or running them. Signals the user brings from such a tool can be added in step 4 with their source type and evidence, like any other.

## What to ask your user at the start
- What do you sell, and who buys it?
- Which list should get signals? Ideally the tiered list from the ICP + tiering guide. (See step 1.)
- Why did your recent customers buy, and why then? What changed at their company just before? (Ask this **before** showing any signals, so the findings don't steer the answer.)
- Who are your customers, and when did each one start? Register IDs and start dates, ideally.
- How many accounts can your team work properly in the next few weeks?
- Which tiers should get the web checks? (Default: tiers 1 and 2.)

## Steps
| # | File | Output |
|---|---|---|
| 1 | [steps/01-take-in-the-list-and-offer.md](steps/01-take-in-the-list-and-offer.md) | The list, the offer, the user's view of why customers buy, the look-back window, capacity and the evidence path |
| 2 | [steps/02-tie-the-signals-to-the-offer.md](steps/02-tie-the-signals-to-the-offer.md) | The signals section of [signal-plan-template.md](signal-plan-template.md), signed off by the user |
| 3 | [steps/03-find-where-signals-are-recorded.md](steps/03-find-where-signals-are-recorded.md) | The sources section of the signal plan: where each signal is recorded in this country |
| 4 | [steps/04-detect-and-record.md](steps/04-detect-and-record.md) | `signals.csv`: every signal found, with date and evidence |
| 5 | [steps/05-check-against-the-evidence.md](steps/05-check-against-the-evidence.md) | A verdict per signal: validated, thin or unvalidated, and any signal dropped |
| 6 | [steps/06-set-the-timing.md](steps/06-set-the-timing.md) | `signal_priority` and the other `signal_` columns on every row |
| 7 | [steps/07-output.md](steps/07-output.md) | `list-signals.csv`, `signals.csv` and `signals-summary.md` |

**Checkpoints:** stop and confirm with the user after steps 2, 5 and 7. Step 2 sets which signals count. Step 5 is where the evidence can overrule the user's beliefs. Step 7 is where the user decides who the team works first.

## Working files
Keep each run in its own folder, named for the market (for example `food-producers-signals-2026-11/`):
- `input/`: the company list and the customer list, exactly as received
- `sources/`: downloaded public records, with the date each was pulled
- `scripts/`: any code you write
- the step outputs: the signal plan, the evidence check, the final files

Customer lists are confidential, and register downloads often hold people's names. Keep `input/`, `sources/` and any working copy of the customer list out of version control.

## When you're done
Go through [checklist.md](checklist.md). Every item must pass, or the summary must say why it doesn't.

## Output format
All rows follow [schema.md](schema.md). Don't rename or remove its columns.
