# Signals

**An agent-ready guide to finding which companies on your list are ready to buy now, from free public data, in any EU country.**

A tiered list tells your team who fits. It doesn't tell them who to call this week. Most signal playbooks answer that with paid intent data and US tools, and with long lists of "buying signals" nobody checks against real deals.

This guide makes an agent look for five common B2B signals in data that European countries already publish (company registers and filed accounts) and on the open web (job posts, news). It ties each signal to what you sell, dates every signal it finds, checks whether your customers showed the same signals before they bought, and puts each company on your list into `now`, `soon` or `watch`, inside the tier it already has.

## How to use it
This repo contains no code and no data. It's a set of instructions for an AI agent.

1. Fork or clone this repo.
2. Give it to your agent (Claude, ChatGPT, Cursor or any other) and point it to [AGENT.md](AGENT.md).
3. Hand the agent a company list, ideally tiered. The agent asks what you sell, why customers bought, and how many accounts your team can work in the next few weeks, then goes through the seven steps with you.

You supply the list, your offer, your customers if you have them, and your capacity. The agent finds the signals and checks with you at the points that matter.

**The best list to start from is a tiered market map.** The output of the [ICP + tiering](https://github.com/bruno-salna/gtm-icp-tiering) guide already says who fits; this guide adds who is ready. Any list in the [shared schema](schema.md) works, and record-based signals need register IDs, which the [Market map](https://github.com/bruno-salna/gtm-market-map) and [List quality](https://github.com/bruno-salna/gtm-list-quality) guides provide.

## The five signals
| Signal | What it is | Where it's usually recorded |
|---|---|---|
| **New leader** | A new managing director, board member or other officer | The company register |
| **Staff growth** | Headcount up clearly on the year before | Filed accounts or other official figures |
| **Hiring** | Open job posts for roles that use or buy what you sell | Job posts on the company site and job boards |
| **Funding** | A funding round, a new investor, or a capital increase | The register, the company's news, the press |
| **Expansion** | A new branch, site, location or subsidiary | The register, the company's news |

These five are the scope of this guide. An agent can work out more signals from your offer, and nothing here stops it. Finding and checking those is up to you and your agent, outside this guide.

## Four free tools
The guide works with four kinds of tool that any agent has or can get for free:
1. **Public data lookup:** official open-data downloads, and free official search pages or APIs (a register, an accounts filing service)
2. **Web search**
3. **Reading a public web page:** a company site, a job post, a news item
4. **Working on files:** comparing dates, counting, joining the list to the records

Some sites block automated reading (job boards, registers behind a captcha, paywalled news). When that happens, the agent marks that source as not checked and tells you. Finding another way in is up to you. Paid data tools (intent data, enrichment providers, connectors) can find more, but choosing and running them is your call and outside this guide.

## In, middle, out
- **In:** a company list in the [shared schema](schema.md), ideally tiered; what you sell and why customers bought; your customers with the date they started, if you have them; how many accounts the team can work in the next few weeks.
- **Middle:** the agent ties the five signals to your offer, finds where each one is recorded in your country, looks for them across the list, checks them against your customers, and sets a timing label for every company.
- **Out:** every company with a timing label, its strongest signal and a one-line "why now"; a file of every signal found with its date and evidence; and a one-page summary with the work order.

## The seven steps
| # | Step | What happens |
|---|---|---|
| 1 | [Take in the list and the offer](steps/01-take-in-the-list-and-offer.md) | Agree what you sell, why customers buy, the look-back window and capacity |
| 2 | [Tie the signals to the offer](steps/02-tie-the-signals-to-the-offer.md) | Decide which of the five signals matter for you, and what exactly counts |
| 3 | [Find where each signal is recorded](steps/03-find-where-signals-are-recorded.md) | Work out the free sources for each signal in your country |
| 4 | [Detect and record](steps/04-detect-and-record.md) | Look for the signals: records on every row, web checks on the top tiers |
| 5 | [Check against the evidence](steps/05-check-against-the-evidence.md) | Did your customers show these signals before they bought? |
| 6 | [Set the timing](steps/06-set-the-timing.md) | `now`, `soon` or `watch` inside each tier, sized to capacity |
| 7 | [Output](steps/07-output.md) | The list with signals, the signal file and the summary |

## Why find signals this way
- **The dates are already in the records.** A register shows when each director was appointed and when each branch was opened. Filed accounts show this year's headcount next to last year's. That's dated, checkable and free, for the whole market at once.
- **A signal needs a reason.** "They raised money" is only a signal if raising money makes a company need what you sell. Each signal is tied to the offer before anyone looks for it.
- **A signal needs a test.** If your customers didn't show a signal before they bought, it isn't telling you much. Checking against real customers separates signals from noise.
- **Timing never changes fit.** A poor-fit company with a fresh signal is still a poor fit. Signals set the order of work inside each tier, and never move a company between tiers.

## Part of a series
This is the fourth of five guides that chain together through a [shared row schema](schema.md):

[Market map](https://github.com/bruno-salna/gtm-market-map) → [List quality](https://github.com/bruno-salna/gtm-list-quality) → [ICP + tiering](https://github.com/bruno-salna/gtm-icp-tiering) → **Signals** → Orchestrator

Each guide works on its own. Used together, each one picks up the previous one's output. ICP + tiering answers *who fits*. This guide answers *who is ready now*.

## What's in the repo
```
AGENT.md                  start here (for the agent)
steps/                    one file per step
signal-plan-template.md   filled in by the agent in steps 2 and 3
schema.md                 output columns, shared across the series
checklist.md              definition of done
examples/                 made-up signal plan, rows and summary
LICENSE                   MIT
```

## Influences
The guide is written from scratch. It draws mainly on my own work finding timing signals for companies selling into European markets, and it also learned from public work:

- **Eric Nowoslawski, [coldoutboundskills](https://github.com/growthenginenowoslawski/coldoutboundskills)** (MIT). The signal playbooks (new in role, hiring surge, job-posting language, fundraising) reduce a timing play to one dated field on a row, with a short line that slots into an opening sentence. The "why now" line in step 7 follows that idea.
- **Amos Bar-Joseph and Maja Voje, [swan-gtm/gtm-skills](https://github.com/swan-gtm/gtm-skills)** (MIT). `account-tier-scoring` caps weak and anonymous signals and never lets one weak signal undo a stronger reading. Step 6 takes the same view.

Where this guide goes its own way: it finds signals in public registers and filed accounts rather than paid tools, ties each signal to the offer, and tests the signals against the user's own customers before trusting them.

## Licence
[MIT](LICENSE). Use it, fork it, adapt it, including commercially; keep the copyright notice.
