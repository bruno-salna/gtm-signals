# Step 5: Check Against the Evidence

## Goal
For each signal, find out whether the user's customers showed it before they bought more often than the market shows it at any time. Give each signal a verdict, and agree with the user which signals stay and at what strength.

## Why it matters
Every signal sounds plausible. This step tells you which ones actually came before real deals. A signal that 40% of customers showed in the six months before they started, against 8% of the market in any six months, is worth working. A signal that customers showed no more often than the market is noise, however good the story.

## How
### Paths A and B: with customers
1. **Count the customers who showed each signal** in the window before they started (from step 4). Leave out customers where the signal couldn't be checked, and say how many.
2. **Count the market's rate for the same window length.** Across the in-market rows (or the whole list, if there's no market map), the share of companies that show the signal in a window of the same length. The simplest version: the share with the signal in the latest window, from step 4.
3. **Work out the lift:** the customers' share divided by the market's share. Show both shares and the counts beside each lift.

| Signal | Customers checked | Showed it before starting | Market rate (same window) | Lift |
|---|---|---|---|---|
| New leader | 24 | 9 (38%) | 9% | 4.2× |
| Staff growth | 20 | 7 (35%) | 14% | 2.5× |
| Funding | 24 | 1 (4%) | 2% | (too few) |

*Made-up numbers, to show the shape.*

4. **Give each signal a verdict**, as a rule of thumb:
   - `validated`: at least 5 customers showed it, and the lift is about 1.5× or more
   - `thin`: fewer than 5 customers showed it, or the lift is between about 1× and 1.5×, or path B
   - `not_supported`: enough customers were checked and the lift is about 1× or below
   - `unvalidated`: couldn't be checked back in time (for example, old job posts)
5. **Compare with the user's view from step 1.** For each reason they gave for why customers bought: supported, not supported or no evidence. Ask before overruling: if a signal the user believes in isn't supported, show the numbers and ask whether there's a business reason the data doesn't capture. If they keep it, record that as their decision, and keep its strength at `weak` or `medium`.
6. **Adjust strength.** A validated signal with a high lift can go up a level; a `not_supported` signal is dropped or set to `weak`, with the user's agreement. Record every change.
7. **Get the user's sign-off.** This is checkpoint 2.

### Path C: no customers
There's nothing to test against. Every signal stays as set in step 2, with `signal_validated` = `unvalidated`, and the summary says "(unvalidated)" in its first line. Still report each signal's market rate: if a signal shows up in half the market, it can't separate anyone, so say so and agree with the user whether to keep it.

## Pitfalls
- **Customers looked at after the fact.** Only events before the start date count.
- **A signal that's just size.** Bigger companies change leaders and open branches more often. If most customers are large and the market is mostly small, every signal looks strong. Where you can, compare customers with market companies in the same tier or size band, and say if the lift shrinks.
- **Small numbers.** Three customers out of eight is not a pattern. Report the counts, and use `thin` rather than `validated`.
- **Testing on the companies you'll call.** The test is on customers. Don't change signal definitions after looking at which prospects they'd pick.

## Done when
Each signal has a verdict with counts, the user's view has been compared with the evidence, every strength change is recorded with the reason, and the user has signed off.
