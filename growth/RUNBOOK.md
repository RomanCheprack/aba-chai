# Aba Chai growth loop: runbook

This folder is the memory of the self-correcting ad + landing-page system.
Every scheduled run starts with no memory: read this file, then `LOG.md`, before doing anything.

## Goal
Get registrations (Lead events) from fathers aged 35-50 in Israel who smoke cannabis in the evenings,
at the lowest sustainable cost per lead. Later goal: paid program sign-ups (decided by the owner).

## Assets
- Meta ad account: 1295015102701768 (rideal ad account), currency ILS
- Campaign: dads_35_50 (120251681110060305), objective OUTCOME_LEADS
- Ad set: New Leads Ad Set (120251681110070305), optimizes for pixel Lead event
- Pixel: 1286446833546477 (Lead fires on successful form submit in index.html and v2.html)
- Page: 1303434932852676, Instagram: 17841432997472614, ad image hash 25cafb93251934920697aa619d76035e
- Landing pages (GitHub Pages, repo romancheprack/aba-chai, branch main, deploys on push):
  - index.html: long page, 30-day program + free challenge (baseline)
  - v2.html: 6-question quiz "evening diagnosis", form at the end of the quiz
- Zoho PageSense (US data center): portal domain_name "abahai", project link_name "my-project".
  Heatmap/scrollmap for index.html: experiment link_name "--2". Heatmap for v2.html: "-v2-".
  Session recordings (whole site): experiment link_name "-". Owner's own visits come from Kefar Hamaccabi
  (Chrome, multi-page sessions): exclude them when judging behaviour.
- Leads land in a Google Sheet (Apps Script) and web3forms email. The owner can see them; the loop cannot.

## Hard rules (never break)
1. Daily budget never above 50 ILS. Never raise budget; the owner decides budget.
2. Never change prices, the offer, the guarantee or the product. Recommend only.
3. No medical claims or guaranteed outcomes ("quit in one session", "100%", "cure"). Meta health policy + honesty.
4. Never put personal data (names, phones, answers) in this repo. The repo is PUBLIC.
5. One change at a time. Every change gets a LOG entry with a hypothesis and the metric that will judge it.
6. Do not judge a test before ~100 landing page views per variant OR 7 days, whichever is later,
   unless something is clearly broken (0 leads after 150 LPVs, pixel not firing, ad rejected, page down).
7. Activating a paused campaign/ad set/ad that was not paused by this loop needs the owner's OK.
8. Ad age targeting is hard 35-50 (Advantage+ Audience off) by owner request. Keep it.

## Each run
1. Read RUNBOOK.md and LOG.md. Find the active experiment.
2. Pull data (Meta Ads tools, ad + day level, since the experiment start): spend, impressions, link clicks,
   landing page views, leads, CTR, cost per lead; breakdown by placement and by age.
3. Sanity checks: delivery running? ads approved? pages return 200? Lead still firing (leads > 0 recently)?
4. Diagnose where the funnel breaks:
   - CTR (outbound) < 1%  -> the ad hook is the problem -> test a new ad text/angle.
   - CTR ok but LPV/click < 70% -> page speed / redirect problem.
   - LPV ok but lead rate < 3% -> the page / form is the problem -> one page change.
   - One placement eats budget with zero leads (e.g. Facebook Reels) -> consider excluding it.
5. If the active experiment has enough data: decide winner, log it, start the next single change.
   Otherwise: log a one-line status and change nothing.
6. Page edits: edit the HTML, keep the pixel and form endpoints intact, commit with a clear message, push to main.
7. Ad edits: creatives can't be edited; create a new creative + ad in the same ad set, pause the old ad.
   Draft mode is on for this account: publish staged objects with ads_activate_entity (object_ids) and
   verify with a live read-back.
8. Append to LOG.md and push. Send the owner a short Hebrew summary: numbers, what changed, what's next.

## Idea backlog (in rough priority order)
- index.html: move the form to the top, short version for ad traffic, fix visible meta-viewport text
- Ad angles: cost of the evening (money/time), morning-after with the kids, "the reward", privacy
- Quiz: shorten to 4 questions; show part of the result before asking for phone
- Ask phone OR WhatsApp-click as alternative opt-in
- Add one real testimonial when the owner provides one
