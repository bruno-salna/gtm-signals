# Signals summary: Examplia food producers, November 2026

`now`: 132 companies (58 in tier 1, 74 in tier 2) against capacity of 80 for the next month.
A new managing director or a new production site are the signals that came before most deals; staff growth helps, funding doesn't.
List: tiered Examplia market map (ICP + tiering, food-producers-v1), 1,412 rows (1,376 prospects, 36 customers). Signals checked on 2026-11-05. Evidence: path A, 26 customers tested.

*Made-up example. See [README.md](README.md).*

**Gaps first:** hiring couldn't be tested against customers (old job posts are gone), and 37 tier 1–2 careers pages blocked automated reading, so those rows weren't checked for hiring. Tier 3 and excluded rows got the register and accounts signals only.

## Work order
Capacity runs out inside tier 2 `now`: work all 58 tier 1 `now`, then the first 22 tier 2 `now` by strength and date.

| Company | Tier | Signal | Date | Why now |
|---|---|---|---|---|
| Kestmoor Bakehouse | 1 | hiring (+ staff growth) | 2026-10-14 | you are hiring a production planner |
| Orvale Dairy | 1 | new leader | 2026-09-03 | you appointed a new managing director in september |
| Tamsel Foods | 2 | expansion (+ funding) | 2026-08-11 | you opened a new production site in august |
| … | | | | |

Next after `now`: tier 1 `soon` (41), for example Pellbrook Meats (your team grew from 44 to 55 people last year).

## Signals used
| Signal | Definition | Strength | Fresh for | Source and method | Verdict |
|---|---|---|---|---|---|
| New leader | New managing director or operations board member | strong | 6 months | register officers, bulk | validated (4.3×) |
| Staff growth | +20% and 5+ people, 2025 vs 2024 | medium | until 2026 accounts due | filed accounts, bulk | validated (2.6×) |
| Hiring | Planner, scheduler or operations manager post | strong | 3 months | careers pages and web search, tiers 1–2 | unvalidated |
| Funding | Round, new investor or capital increase | weak | 6 months | register bulk; news, tiers 1–2 | thin |
| Expansion | New site or branch | strong | 6 months | register bulk; news, tiers 1–2 | validated (4.6×) |

## What was found
| Signal | Prospect rows checked | Signals found | Live | Not checked, and why |
|---|---|---|---|---|
| New leader | 1,376 | 118 | 104 | 0 |
| Staff growth | 1,211 | 167 | 167 | 165 (no headcount for both years) |
| Hiring | 673 | 61 | 58 | 37 (careers page blocked); 666 (outside tiers 1–2) |
| Funding | 1,376 register; 710 web | 41 | 33 | 666 web (outside tiers 1–2) |
| Expansion | 1,376 register; 710 web | 72 | 69 | 666 web (outside tiers 1–2) |

## Evidence
| Signal | Customers checked | Showed it before starting | Market rate | Lift |
|---|---|---|---|---|
| New leader | 26 | 9 (35%) | 8% | 4.3× |
| Staff growth | 24 | 8 (33%) | 13% | 2.6× |
| Hiring | 0 | — | 6% | — |
| Funding | 26 | 2 (8%) | 3% | too few |
| Expansion | 26 | 6 (23%) | 5% | 4.6× |

The user's view: growth and a second site are supported; investment has no evidence (kept as weak, by the user's decision). A new leader wasn't in the user's view, but it is one of the two strongest signals.

## Timing by tier
| Tier | now | soon | watch | none | Current customers with a live signal |
|---|---|---|---|---|---|
| 1 | 58 | 41 | 7 | 140 | 6 |
| 2 | 74 | 63 | 15 | 312 | 2 |
| 3 | 39 | 52 | 4 | 391 | 1 |
| excluded | — | — | — | — | 0 |

Tier 3 and excluded rows had the register and accounts signals only.

## For the user to review
- 21 tier 3 companies and 4 excluded companies have a strong live signal (`signal_review_flag` = `strong_signal_low_tier`). 3 of them are lost deals with a new managing director since the deal was lost, for example Wrenfold Mills. Their tier is unchanged; whether to look again at their fit is the user's call.
- 6 current customers in tier 1 have a new site or a new leader: expansion cues for the account owners.

## Decisions made
- Funding kept as `weak`, against the user's first view (thin evidence: 2 of 26 customers).
- Hiring kept as `strong` although it couldn't be tested: the user's decision.
- `now` exceeds capacity: the team works tier 1 `now`, then tier 2 `now` by strength and date until capacity is used.
- Person names kept out of all files.
- The user's decision: the team works the first 80 of the work order in November (recorded 2026-11-05).

## Not covered
- 37 careers pages blocked automated reading; one job board refused it. Hiring for those rows is unknown.
- No custom signals.
- Paid tools were not used; they may find more signals. Choosing them is the user's call.
