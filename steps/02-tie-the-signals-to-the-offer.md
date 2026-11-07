# Step 2: Tie the Signals to the Offer

## Goal
Decide which of the five signals matter for what this user sells, what exactly counts as each one, how strong it is and how long it stays fresh. Fill in the signals section of [../signal-plan-template.md](../signal-plan-template.md) and get the user's sign-off.

## Why it matters
"A new managing director" is a strong signal for someone selling a new system, and almost nothing for someone selling cleaning services. A signal that isn't tied to the offer fills the `now` list with companies that have no reason to buy. And a signal that isn't defined exactly ("hiring") gets counted differently on every row.

## The five signals
| Signal | `signal_type` | What it usually means for a buyer |
|---|---|---|
| New leader | `new_leader` | New leaders review suppliers and systems in their first months, have a mandate to change things, and no loyalty to the old way |
| Staff growth | `staff_growth` | The way the company worked at the old size stops working; processes, tools and suppliers get replaced |
| Hiring | `hiring` | A stated need: the company is paying to add the capacity your offer touches, or the role it's hiring will use or buy what you sell |
| Funding | `funding` | Money to spend and a plan to spend it on, usually growth |
| Expansion | `expansion` | A new site, branch or subsidiary needs to be set up: people, systems, suppliers |

These five are the scope of this guide. You may find, from the offer, that another event matters more (a certification, a merger, a move to new premises). Nothing stops you or the user from tracking it: add it to the plan with the same fields and `signal_type` = `custom_<name>`. This guide doesn't cover where to find such signals or how to check them; say so in the summary.

## How
1. **Go through the five with the user.** For each one, answer: does this event make a company more likely to need what the user sells, and why? Write the reason in one sentence. Compare it with what the user said in step 1 about why customers bought.
2. **Drop what doesn't apply.** It's fine to track two or three signals. Record why each dropped signal was dropped.
3. **Define each kept signal exactly**, in terms you can check in a record or on a page:
   - **New leader:** which roles count (managing director only? any board member? a specific function?) and whether a change of title counts. Registers record directors and board members, not functional roles like a CTO or CFO. If the role that buys is a functional one, look for it in company news and the press, and consider a lower strength for a board change that only the register shows.
   - **Staff growth:** how much growth counts, as both a share and a number (for example, "up 20% and at least 5 people on the year before"). A share alone makes 2 → 3 people look like a surge.
   - **Hiring:** which roles or words in a job post count, and how many open posts. Write them as a short list.
   - **Funding:** what counts (an announced round, a new investor, a capital increase in the register) and any minimum size. Leave out capital raised only to the legal minimum for the legal form: that's a legal step, not investment. A new shareholder on its own is an ownership change, not investment; if it comes with a new board member around the same time, the company was probably sold. Agree with the user whether an ownership change counts, and label it as such in `signal_detail`.
   - **Expansion:** what counts (a new branch or site in the register, a new subsidiary, an announced new location) and whether expansion abroad counts.
4. **Set strength:** `strong`, `medium` or `weak`, from the reason in 1. A signal that almost always comes before a purchase of this kind is strong. One that sometimes does is medium. One that is only loosely related is weak. Strength is the user's call, informed by you; step 5 can change it.
5. **Set freshness:** how long after the event the signal still counts (the default is the look-back window from step 1). A new leader usually matters most in the first 3–6 months. Staff growth stays true until the next accounts are due; use that due date as the expiry.
6. **Write the "why now" pattern** for each signal: a short lowercase phrase that fits after "I noticed", built from the evidence only. Example: "you appointed a new managing director in september".
7. **Get the user's sign-off.** This is checkpoint 1.

## Illustrative example
*Made up, to show the shape. Not a recommendation.* A company sells production-planning software to food producers.

| Signal | Keep? | Reason | Counts when | Strength | Fresh for |
|---|---|---|---|---|---|
| New leader | yes | New managing or operations directors review how production is planned | New managing director or new board member | strong | 6 months |
| Staff growth | yes | Above about 50 staff, planning on spreadsheets breaks | Up 20% and 5+ people on the year before | medium | until next accounts |
| Hiring | yes | Hiring planners means planning is a stated bottleneck | Posts for production planner, scheduler or operations manager | strong | 3 months |
| Funding | yes | Growth money often goes into capacity | Announced round or capital increase | medium | 6 months |
| Expansion | yes | A second site doubles the planning problem | New site or branch in the register or the news | strong | 6 months |

## Pitfalls
- **Keeping every signal "just in case".** Each signal adds checks and noise. Keep only the ones with a clear reason.
- **Strength set by how easy a signal is to find.** Staff growth is easy to find in the accounts; that doesn't make it strong.
- **A "why now" line that guesses.** "You're clearly scaling fast" is an opinion. Write only what the evidence shows.

## Done when
Each of the five signals is kept or dropped with a reason, each kept signal has an exact definition, strength, freshness and a "why now" pattern, any custom signal is marked as outside the guide, and the user has signed off.
