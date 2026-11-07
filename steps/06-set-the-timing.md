# Step 6: Set the Timing

## Goal
Give every company a timing label (`now`, `soon`, `watch` or empty) inside the tier it already has, size `now` to capacity, and fill in the summary `signal_` columns for every row.

## Why it matters
This turns a pile of signals into a work order. The team works tier 1 `now` first, then tier 1 `soon` and tier 2 `now`, and so on. Fit decides who is worth working; timing decides who goes first.

## The labels
| `signal_priority` | Default rule |
|---|---|
| `now` | At least one live `strong` signal, or two live `medium` signals |
| `soon` | One live `medium` signal, or a `strong` signal in the last quarter of its freshness |
| `watch` | Only `weak` signals |
| empty | No live signal found (see `signal_not_checked` for what wasn't checked) |

"Live" means today is on or before `signal_expires`. Signals marked `not_supported` in step 5 and kept by the user count at the strength the user agreed.

## How
1. **Set the label for every row** from its live signals, using the rules above. Agree any change to the rules with the user and record it.
2. **Weak signals can't make `now`.** Not even several of them.
3. **Never change `tier`.** If a tier 3 or excluded company has a strong live signal, set `signal_review_flag` = `strong_signal_low_tier` and leave the tier as it is. List these for the user in the summary; whether to look again at their fit is the user's decision.
4. **Current customers.** Signals on current customers are expansion cues, not new business. Keep their labels, mark them, and count them separately.
5. **Fill in the summary columns:** `signal_count` (live signals), `signal_top_type`, `signal_top_date`, `signal_top_strength` (the strongest live signal; on a tie, the newest), `signal_why_now` (the "why now" line for the top signal, from the pattern in step 2 and the facts in `signal_detail`), `signal_validated` (the verdict for the top signal), `signal_checked_date`, `signal_not_checked`.
6. **Check `now` against capacity.** Count `now` rows in the tiers the team works first (usually tier 1, then tier 2), excluding current customers, and compare with capacity from step 1.
   - **Much larger than capacity:** order `now` by tier, then by strength, then by date (newest first), and show the user where capacity runs out. If `now` is a large share of the list, a signal is too loose; go back to step 2 with the user.
   - **Much smaller than capacity:** fine. The rest of the team's time goes to tier 1 by fit, as the ICP + tiering guide set it. Say so. If the list has no tiers, there's no fit order to fall back on: say so, and suggest the [ICP + tiering](https://github.com/bruno-salna/gtm-icp-tiering) guide.
7. **Show the user the top of the work order** with the "why now" lines, before step 7.

## Pitfalls
- **Stacking the same event.** A new site in the register and the hiring for that site are two signals but one story. Count both, but say so in `signal_notes` if they're the same event.
- **A label from an unchecked row.** Empty means "no signal found in what was checked". If most signals weren't checked for a row, `signal_not_checked` must say so, and the summary counts these rows.
- **"Now" for months.** A signal from the start of the window is close to expiring. That's what `soon` is for.

## Done when
Every row has `signal_priority` (or empty) and the summary columns, no tier was changed, strong signals on low tiers are flagged, current customers are counted separately, and `now` has been checked against capacity with the user.
