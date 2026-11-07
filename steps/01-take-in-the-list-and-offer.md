# Step 1: Take in the List and the Offer

## Goal
Get the list that needs signals, understand what the user sells and why their customers bought when they did, agree how far back to look and how many accounts the team can work soon, and decide which evidence path this run will take.

## Why it matters
A signal is only useful if it points to a reason to buy what this user sells. Before looking for anything, you need the user's own account of why customers bought, in their words. And you need capacity: a `now` list of 600 companies is as useless as no list.

## The inputs
**1. The company list.** It should follow the [shared schema](../schema.md). In order of preference:
- **A tiered list** (`list-tiered.csv` from the [ICP + tiering](https://github.com/bruno-salna/gtm-icp-tiering) guide). It already says who fits, so this guide only has to add timing.
- **A market map or a cleaned list** (from the [Market map](https://github.com/bruno-salna/gtm-market-map) or [List quality](https://github.com/bruno-salna/gtm-list-quality) guide). Fine, but with no tiers, every row is treated as one tier, and the web checks in step 4 need another way to pick the rows (agree it with the user).
- **Any other list.** Record-based signals need a register ID to match the records. Rows without one can only get web checks. Suggest List quality first; if the user declines, carry on and note it.

**2. The customers (optional, but they make the test possible).** Register IDs and the date each customer started (first contract, first invoice, or first meeting, as long as it's the same for all). Best customers are most useful. Without start dates there's nothing to test signals against (path C).

## How
1. **Save the files** in `input/` exactly as received. Count the rows, and the rows per tier.
2. **Ask the questions** in [../AGENT.md](../AGENT.md). Write down the user's view of why customers bought, and why then, in their own words, before you show any data.
3. **Agree the look-back window.** How recent must an event be to count? Default: 6 months for a new leader, hiring, funding and expansion; the latest filed year against the year before for staff growth. Some offers have long buying cycles; the user may want 12 months. Write it down; step 2 can set a different window per signal.
4. **Agree capacity for `now`.** How many accounts can the team work properly in the next few weeks? Example: "2 people, about 40 accounts a month each" = about 80 for the next month. This sizes `now` in step 6.
5. **Agree the web-check scope.** Record-based signals run on every row. Web checks (job posts, news, company sites) take time per company, so by default they run only on tiers 1 and 2. Agree the tiers and count the rows.
6. **Pick the evidence path**, from the customers with a start date:

| Path | Evidence | What the signals are |
|---|---|---|
| **A: Evidence** | About 20 or more customers with start dates | Each signal tested: did customers show it before they bought, more often than the market? |
| **B: Thin evidence** | 5–19 customers with start dates | Signals checked against the customers there are; the summary says the evidence is thin |
| **C: No evidence** | Fewer than 5, no start dates, or a new market | Signals tied to the offer but untested, labelled **"(unvalidated)"** |

   Count the customers after they're matched to records in step 4, not before.
   Path C is a proper result. A new market has no customers yet; the signals still give the team a sensible order of work.
7. Write it all down and get the user's sign-off.

## Worksheet
```
Run name:
What the user sells:
Company list: file, source (tiered list / market map / cleaned list / other), rows, rows per tier, date
Customers: file, rows, with start dates, how "start" is defined
Why customers bought, in the user's words (written before any data was shown):
Look-back window: default and any per-signal changes
Capacity for `now`: people × accounts × period =
Web-check scope: tiers, rows
Evidence path: A / B / C (provisional until step 4)
Signed off by user: yes / no, date
```

## Pitfalls
- **No tiers, so everything gets web checks.** On a list of thousands, that takes days and gets blocked. Agree a smaller set first.
- **Start dates that mean different things.** "Signed" for some customers and "first invoice" for others shifts the test by months. Use one definition.
- **Very old customers.** A customer who started eight years ago tells you little about signals today, and old records are harder to find. By default, test on customers from the last three years.
- **"They buy when they have budget."** True, but not observable. Ask what event in the company comes before the budget: a new leader, a funding round, a move.

## Done when
The files are saved, the user's view of why customers buy is written down, the look-back window, capacity and web-check scope are agreed, a provisional path is chosen, and the user has signed off.
