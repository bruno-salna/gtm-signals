# Step 3: Find Where Each Signal Is Recorded

## Goal
For each signal kept in step 2, work out where it is recorded in this country, for free, and how you'll read it with your four tools. Fill in the sources section of [../signal-plan-template.md](../signal-plan-template.md).

## Why it matters
The same signal lives in different places in different countries. One register publishes every board appointment with a date as open data; another shows only current officers, one company at a time, behind a captcha. Working this out first tells you which signals can be checked on the whole list, which only on the top tiers, and which not at all.

## Where to look, in order
1. **The company register.** Most EU registers record officers (often with an appointment date), branches, registered address, share capital and shareholders. Many publish bulk open data; others offer a free search per company.
2. **Filed accounts.** Annual accounts often give average headcount and revenue for this year and the year before. Some countries also publish official employment figures (from tax or social security data) more often than once a year.
3. **Official notices.** Some countries publish register changes in an official gazette or bulletin, dated.
4. **The company's own site.** Careers pages, news pages, press releases.
5. **Job boards and the press.** Job posts and news about funding, new sites and appointments.

Use the record-based sources wherever they exist. They're dated, they cover every company, and you can check the whole list at once. The open web covers what the records miss (job posts, announced rounds) but costs time per company.

Examples, for direction only: a register's officer file may have fields like role, appointment date and end date; filed accounts may have average employees for both years; a register's branch file may have a registration date and an address.

## How
1. **Check your tools.** Tell the user which of the four you have: public data lookup, web search, reading a web page, working on files. Name any signal a missing tool affects.
2. **For each signal, find the source.** Search for the country's register, accounts filing, and official open-data portal. For each source, record:
   - what it is and who publishes it
   - the field that shows the signal, and the field that dates it
   - coverage: every company, or only some (for example, only companies above a size, or only those that filed on time)
   - access: bulk download, free search per company, or web pages only
   - licence or terms of use, if stated
   - whether it can be read back in time (step 5 needs the signal as it was before each customer started)
3. **Test each source on a few known companies** from the list. Can you read the field? Does the date make sense? If the source blocks automated reading, record it as `blocked` and tell the user.
4. **Decide the method per signal:**
   - `bulk`: from a downloaded or queried dataset, for every row with a register ID
   - `web`: one company at a time, only for the tiers agreed in step 1
   - `not_checked`: no free source, or the source is blocked; say what it would take
5. **Note personal data.** Officer records name people. Keep the role and the dates; leave the names out unless the user confirms their legal basis covers it.
6. **Tell the user the plan:** which signals run on every row, which on the top tiers, which can't be checked, and what that means for the result.

## Pitfalls
- **Current officers only.** Some registers show only who is in office now, so a director appointed and gone within a year disappears. That's usually fine for "new leader now", but it matters in step 5.
- **The registration date isn't the event date.** Some changes are filed weeks after they happen. Use the event date where the source gives one, and say which date you used.
- **Headcount ranges.** A range (10–49) can't show growth inside the range. Use exact figures; treat a range as unknown for growth.
- **Late or missing accounts.** Small companies may file late or file shortened accounts without headcount. Count how many rows have figures for both years before trusting the growth signal.
- **Trying to beat a block.** If a site refuses automated access, don't try to get round it. Record it and move on.

## Done when
Each kept signal has a source (or `not_checked` with the reason), a method (`bulk`, `web` or `not_checked`) and a test on a few known companies, blocked sources are recorded, and the user knows which signals can be checked on which rows.
