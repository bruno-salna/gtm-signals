# Signal Plan: Examplia food producers, November 2026

*Made-up example. See [README.md](README.md).*

## The offer
- What the user sells: production-planning software for food producers
- Why customers bought, in the user's words (from step 1): "They buy when they grow past what spreadsheets can handle, usually when they open a second site. And after they get investment."
- Look-back window (default): 6 months; staff growth = 2025 accounts against 2024
- Capacity for `now`: 2 people × about 40 accounts = about 80 for the next month

## Signals (step 2)
| Signal | Keep? | Reason it creates a need | Counts when (exact definition) | Strength | Fresh for | "Why now" pattern |
|---|---|---|---|---|---|---|
| New leader (`new_leader`) | yes | A new managing director reviews how production is planned | New managing director, or a new board member with an operations role | strong | 6 months | you appointed a new managing director in <month> |
| Staff growth (`staff_growth`) | yes | Above about 50 staff, planning on spreadsheets breaks | Average staff up 20% and at least 5 people, 2025 against 2024 | medium | until the 2026 accounts are due | your team grew from <a> to <b> people last year |
| Hiring (`hiring`) | yes | Hiring planners means planning is a stated bottleneck | Open post for production planner, scheduler or operations manager | strong | 3 months | you are hiring a <role> |
| Funding (`funding`) | yes | Growth money often goes into capacity | Announced round, new investor, or capital increase in the register | medium | 6 months | you raised new capital in <month> |
| Expansion (`expansion`) | yes | A second site doubles the planning problem | New site or branch in the register, or an announced new production site | strong | 6 months | you opened a new production site in <month> |

Dropped signals: none.
Custom signals: none.

Signed off by user (step 2): yes, 2026-11-05

## Sources (step 3)
Tools available: public data lookup, web search, reading web pages, working on files

| Signal | Source | Field that shows it | Field that dates it | Coverage | Access | Read back in time? | Method | Tested on |
|---|---|---|---|---|---|---|---|---|
| New leader | Company register, officers file | role | appointment date | all companies | bulk download | yes (current and former officers) | `bulk` | 5 known companies |
| Staff growth | Accounts filing service | average employees, both years | financial year end | 88% of rows filed both years | bulk download | yes | `bulk` | 5 |
| Hiring | Company careers pages, then web search for job posts | role in post | posting date | tiers 1–2 | web | no (old posts gone) | `web` | 5 |
| Funding | Register capital changes; company news; press | capital change, round announced | change date, article date | all (register), tiers 1–2 (web) | bulk + web | yes | `bulk` + `web` | 5 |
| Expansion | Register branches file; company news | new branch or site | registration date, article date | all (register), tiers 1–2 (web) | bulk + web | yes | `bulk` + `web` | 5 |

Blocked sources: one large job board refused automated reading. Hiring was checked on company careers pages and through web search instead; 37 tier 1–2 careers pages also blocked automated reading and are marked not checked for hiring.

Personal data: names kept out.

## Verdicts (step 5)
Customers from the last three years with start dates: 26.

| Signal | Customers checked | Showed it before starting | Market rate | Lift | Verdict | Strength after |
|---|---|---|---|---|---|---|
| New leader | 26 | 9 (35%) | 8% | 4.3× | `validated` | strong |
| Staff growth | 24 | 8 (33%) | 13% | 2.6× | `validated` | medium |
| Hiring | 0 | (old posts gone) | 6% | — | `unvalidated` | strong (user's decision) |
| Funding | 26 | 2 (8%) | 3% | (too few) | `thin` | weak (agreed with user) |
| Expansion | 26 | 6 (23%) | 5% | 4.6× | `validated` | strong |

User's view vs evidence:
- "Grow past what spreadsheets can handle": supported (staff growth 2.6×).
- "When they open a second site": supported (expansion 4.6×).
- "After they get investment": no evidence (2 customers). The user agreed to keep funding as `weak`.
- Not mentioned by the user, but the strongest pattern together with expansion: a new leader before buying (4.3×).

Signed off by user (step 5): yes, 2026-11-05
