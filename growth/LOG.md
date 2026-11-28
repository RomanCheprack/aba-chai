# Experiment log

Newest at the bottom. Metrics from Meta Ads, attribution 7d click / 1d view.

## Baseline: 2026-11-17 to 2026-11-22 (index.html + shorturl link)
- Spend 255.51 ILS, 3,517 impressions, 144 link clicks, 128 LPV, 7 leads (cost per lead 36.5 ILS)
- Outbound CTR 4.1%, cost per click 1.77 ILS: the ad hook works.
- 5 of the 7 leads came on day 1 from 11 LPV (possibly owner tests). Days 2-6: 2 leads / 117 LPV = 1.7%.
- Ad "image-with-text" (to index.html): 109 LPV, 1 lead. 60 of its LPV came from Facebook Reels.
- Diagnosis: the funnel breaks on the page. Ad promised a free 3-recording challenge; page leads with a
  paid 30-day program, ~1,800 words before the form, phone required.

## PageSense baseline for index.html (2026-11-17 to 2026-11-22)
- Page is 11,650px tall, average screen 722px. Scroll retention: 75% of visits reach 900px, 50% reach 8,550px,
  25% reach 10,450px (the form zone). Biggest drop: 700-750px (end of first screen), 7.4% lost.
- Clicks: 116 visitors, 23 clicks total (0.2 per visit), 11% engaged. Form: #name 2 clicks, #phone 2, submit 1.
- 67 recordings, almost all mobile inside the Facebook in-app browser. Median session 27s; 46% under 20s.
- Reading: people who stay do read a lot, but only ~1 in 4 gets to the form and almost nobody starts it.
  The ask (phone for a paid-looking program) is where it breaks, not attention.

## Change 2026-11-22: targeting
- Ad set age set to hard 35-50, Advantage+ Audience off (owner request). Men, Israel. Budget 50 ILS/day.

## Experiment 1 (started 2026-11-22 ~12:20 Israel time, owner approved): v2 quiz funnel
- New ad "dad-35-50-v2-quiz" (ad 120251760058210305, creative 1356894669776587) -> v2.html.
  Copy matches the quiz: "what does tonight's joint really cost you? 60-second diagnosis, free, discreet".
- Old ads paused: 120251681110080305, 120251697925420305.
- Hypothesis: when the page matches the ad and asks for details at the end of a short quiz,
  LPV -> lead rate rises from ~1.7% to 5%+.
- Judge at: 100+ LPV on v2 (about 8-10 days at 50 ILS/day). Metric: leads / LPV and cost per lead.
- Note: this is a sequential test against the baseline, not a split test (budget too small to split).

- 2026-11-22: published and activated by the loop with owner approval. Ad set ACTIVE at 50 ILS/day,
  hard age 35-50 verified live, Advantage+ Audience off. New ad in Meta review at launch.
  The loop may keep this ad set running; it was activated with the owner's OK.

## Status 2026-11-23 (day 2 of experiment 1) - no change
- v2 ad since launch (11-22 to 11-23 partial): spend 59.96 ILS, 1,199 impressions, 55 link clicks, 48 LPV,
  4 leads (cost per lead 15.0 ILS, lead/LPV 8.3%). Outbound CTR ~4-6.6%. LPV/click 87%.
  Leads may include owner test submissions on launch day; the owner can check against the Sheet.
- Placements: FB feed 25 LPV / 2 leads, FB Reels 17 LPV / 1 lead, IG feed 1 / 1, IG Reels+Stories 5 / 0.
  Reels is not eating budget without leads this time; no placement change.
- Delivery ACTIVE, ad ACTIVE (approved), budget 50 ILS/day, age 35-50 + Advantage+ Audience off verified live.
  (Age breakdown shows small 25-34 / 55-64 spend on 11-22: that is the old ads before the targeting change.)
- PageSense v2 heatmap (11-22 to 11-23): 51 visitors, 200 clicks (3.5/visit vs 0.2 on index.html),
  47% engaged. Quiz options take most clicks; #go 10, #name 5, #phone 4, #consent 4, #r-call 8.
  Scroll: 81% reach 950px, 50% reach 1,550px, page max 2,150px. No broken step visible.
- Meta trend/benchmark tools returned no data (too new).
- Page check from the cloud not possible (github.io blocked by the sandbox proxy); LPVs and leads are
  coming in, so the page is up.
- Decision: 48 of 100 LPV needed, day 2 of 7 -> keep running, change nothing. Early read is positive
  (8.3% vs 1.7% baseline). Next judge ~2026-11-29.

## Change 2026-11-23: v2 copy accuracy fix (owner request), during experiment 1
- v2.html promised the call would "build you a plan for the evening, free". The owner does not give a plan for free.
  Reworded 4 places (hero sub, objection answer, 2 result-screen call messages) to: a free 15-minute call about
  your evening, no obligation, you leave with one first step for tonight.
- Only the hero sub line is seen before the lead; treat leads/LPV from 2026-11-23 midday on as slightly
  different copy when judging experiment 1. Not a reason to restart the test.

## Change 2026-11-23: v2 result-screen stats redesign (owner request)
- Money and nights shown as cards (money card dark, amber number, plus a yearly figure). After the Lead fires, so no effect on experiment 1.

## Change 2026-11-23: v2 result-screen video replaced (owner request)
- "How I record myself" video now https://youtu.be/WlKdvKthdZU (was _6IBpACopZ0). After the Lead, no effect on experiment 1.

## Change 2026-11-23: accessibility fixes (owner approved)
- Small amber text darkened to #985b0a (contrast 4.8-5.2:1, was 3.0-3.2) on v2 and course.html; this includes the v2 hero callout seen before the lead (color only).
- Small text sizes 13.5px -> 14.5-15px. course.html: sticky mobile buy bar, shown only when PAY_URL is set and neither buy box is on screen.

## Status 2026-11-24 (day 3 of experiment 1) - ad PAUSED by owner, no change
- The v2 ad (120251760058210305) was paused manually by the owner in Ads Manager on 2026-11-23 ~22:40 (account time).
  Not paused by the loop -> per rule 7 the loop does not reactivate it. Ad set ACTIVE, but delivery "all ads off".
  No spend on 11-24. Waiting for the owner's OK (or reason) before anything resumes.
- v2 totals 11-22 to 11-23: spend 98.97 ILS, 2,044 impressions, 78 link clicks, 71 LPV, 6 leads
  (cost per lead 16.50 ILS, lead/LPV 8.5% vs 1.7% baseline). Outbound CTR 3.7-4.0%. LPV/click 91%.
- Placements: FB feed 61.11 ILS / 34 LPV / 2 leads, FB Reels 18.19 / 27 / 3, IG feed 7.89 / 2 / 1,
  IG Reels 5.45 / 5 / 0, IG Stories 5.10 / 3 / 0, FB Stories 0.94, Threads 0.29. No placement problem.
- PageSense v2 (11-22 to 11-24): 73 visitors, 258 clicks (3.0/visit), 45% engaged. #go 16, #name 7, #phone 6,
  #consent 7, #r-call 8. Scroll: 78% reach 950px, 51% reach 1,400px, 25% reach 1,950px; biggest drop 2,000-2,050px (8.5%).
  No broken step visible. Meta trend/benchmark tools: no data.
- Decision: no change. 71 of 100 LPV, day 2 of 7 of delivery. The test clock is stopped while the ad is paused.
  If the owner resumes it, keep judging experiment 1 at 100+ LPV and 7 days of delivery.

## Status 2026-11-25 (experiment 1, day 2 of 7 of delivery) - ad still PAUSED by owner, no change
- Ad 120251760058210305 still PAUSED (owner, 2026-11-23 22:40). Activity log: no changes since. No spend 11-24 or 11-25.
- Totals unchanged: v2 since 11-22: 99.04 ILS (44.72 + 54.32 as reported today), 71 LPV, 6 leads, ~16.5 ILS/lead.
- PageSense not re-read: no paid traffic since the pause. Meta trend/benchmark: no data.
- Decision: rule 7, do not reactivate. Waiting for the owner's OK. Test clock stays at 71 of 100 LPV.

## Status 2026-11-26 (experiment 1, day 2 of 7 of delivery) - ad still PAUSED by owner, no change
- Ad 120251760058210305 still PAUSED (owner, 2026-11-23 22:40). Activity log: no changes since. No spend 11-24 to 11-26.
- Totals unchanged: v2 since 11-22: 99.04 ILS, 78 link clicks, 71 LPV, 6 leads, ~16.5 ILS/lead.
- PageSense not re-read: no paid traffic since the pause.
- Decision: rule 7, do not reactivate. Waiting for the owner's OK. Test clock stays at 71 of 100 LPV.

## Status 2026-11-27 (experiment 1, day 2 of 7 of delivery) - ad still PAUSED by owner, no change
- Ad 120251760058210305 still PAUSED (owner, 2026-11-23 22:40). Activity log: no changes since 11-25. No spend 11-24 to 11-27.
- Totals unchanged: v2 since 11-22: 99.04 ILS, 78 link clicks, 71 LPV, 6 leads, ~16.5 ILS/lead (lead/LPV 8.5%).
- PageSense not re-read: no paid traffic since the pause.
- Decision: rule 7, do not reactivate. Waiting for the owner's OK. Test clock stays at 71 of 100 LPV.

## Status 2026-11-28 (experiment 1, day 2 of 7 of delivery) - ad still PAUSED by owner, no change
- Ad 120251760058210305 still PAUSED (owner, 2026-11-23 22:40). Activity log: no changes since 11-25. No spend 11-24 to 11-28.
- Totals unchanged: v2 since 11-22: 99.04 ILS, 78 link clicks, 71 LPV, 6 leads, ~16.5 ILS/lead (lead/LPV 8.5%).
- Meta trend/benchmark: no data. PageSense not re-read: no paid traffic since the pause.
- Decision: rule 7, do not reactivate. Waiting for the owner's OK. Test clock stays at 71 of 100 LPV.
