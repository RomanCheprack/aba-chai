# Experiment log

Newest at the bottom. Metrics from Meta Ads, attribution 7d click / 1d view.

## Baseline: 2026-11-17 to 2026-11-22 (index.html + shorturl link)
- Spend 255.51 ILS, 3,517 impressions, 144 link clicks, 128 LPV, 7 leads (cost per lead 36.5 ILS)
- Outbound CTR 4.1%, cost per click 1.77 ILS: the ad hook works.
- 5 of the 7 leads came on day 1 from 11 LPV (possibly owner tests). Days 2-6: 2 leads / 117 LPV = 1.7%.
- Ad "image-with-text" (to index.html): 109 LPV, 1 lead. 60 of its LPV came from Facebook Reels.
- Diagnosis: the funnel breaks on the page. Ad promised a free 3-recording challenge; page leads with a
  paid 30-day program, ~1,800 words before the form, phone required.

## Change 2026-11-22: targeting
- Ad set age set to hard 35-50, Advantage+ Audience off (owner request). Men, Israel. Budget 50 ILS/day.

## Experiment 1 (start: when the owner approves launch): v2 quiz funnel
- New ad "dad-35-50-v2-quiz" (ad 120251760058210305, creative 1356894669776587) -> v2.html.
  Copy matches the quiz: "what does tonight's joint really cost you? 60-second diagnosis, free, discreet".
- Old ads paused: 120251681110080305, 120251697925420305.
- Hypothesis: when the page matches the ad and asks for details at the end of a short quiz,
  LPV -> lead rate rises from ~1.7% to 5%+.
- Judge at: 100+ LPV on v2 (about 8-10 days at 50 ILS/day). Metric: leads / LPV and cost per lead.
- Note: this is a sequential test against the baseline, not a split test (budget too small to split).
