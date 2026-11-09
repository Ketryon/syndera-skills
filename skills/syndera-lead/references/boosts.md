# Boosts on X and TikTok

What the networks document about boosting one post, and how a boost works in Syndera. Use the network's own numbers; don't invent benchmarks for cost per view or per follower.

Last checked: 2026-11-09.

## In Syndera

- A boost runs on the person's own ads account and card; Syndera never pays for it.
- With **Approve before anything goes out** on (the default), starting a boost only creates a proposal on the post; the person chooses **Approve and start** or **Decline** in Syndera. Say "proposed", not "running".
- One boost per brand at a time: starting one pauses the brand's other running boost first.
- Running boosts can be paused or stopped from anywhere. Resuming spends again; with approval on, it's done in the app.
- Check access first: `x_boost_state` / `tiktok_boost_state` say whether ads are allowed for the account, on which ads accounts, and (TikTok) each currency's minimum daily budget. If ads aren't allowed yet, give the person the link to open.

## X

- **Goals in Syndera:** reach, engagement, video views. Each is billed on its own measure: reach per thousand impressions, engagement per engagement, video views per view ([X Ads glossary](https://help.x.com/en/business-and-advertising/x-ads-glossary)).
- **Budget:** the daily budget is a ceiling X won't exceed; X sets no minimum. In Syndera, a boost runs 1 to 30 days.
- **Judging it:** use the measure the goal is billed on. X's numbers can still change for up to 3 days, so don't call it before then. `x_estimate` gives X's own reach estimate before starting.

## TikTok

- **Goals in Syndera:** reach, video views, followers.
- **Minimum daily budget:** 20 USD a day per ad group (TikTok Ads Manager), or the equivalent the account's currency requires; `tiktok_boost_state` gives it. Source: [TikTok budget](https://ads.tiktok.com/resources/help/article/budget).
- **Learning:** TikTok says delivery steadies after about 25 results or 7 days ([TikTok learning phase FAQ](https://ads.tiktok.com/help/article/learning-phase-faq)), and recommends waiting at least 2 days between changes ([budget best practices](https://ads.tiktok.com/help/article/budget-best-practices)).
- **Spark Ads** boost the creator's own video. The creator makes an ad authorization code in the TikTok app, in the post's ad settings; the person pastes it. Once authorized, the caption can't be changed, and a private video becomes public ([Spark Ads guide](https://ads.tiktok.com/help/article/spark-ads-creation-guide?lang=en)).

## Proposing one

Propose a boost complete, so the person can approve it in one look:

```
Boost: <post> on <network>
Why: <its results so far, against the brand's typical post, with n and window>
Goal: <reach / engagement / video views / followers>, judged by <the billed measure>
Budget: <daily> × <days> = <total>, on <ads account>
Audience: <places, languages, interests>
Look again: <date, not before 2–3 days in>
```
