# Reading results honestly

Read this before ranking posts, calling something a pattern, or recommending more of anything.

## Contents

- Why single posts mislead
- Comparing like with like
- How strong is the evidence
- Saying how sure you are
- What the numbers can't tell you

## Why single posts mislead

How far one post travels is mostly unpredictable: in a large study of Twitter cascades, the best models explained less than half of the variation in reach ([Martin et al., WWW 2016](https://arxiv.org/abs/1602.01013)). Even at large scale, ad experiments are noisy enough that a single result says little about the next one ([Lewis & Rao, QJE 2015](https://ideas.repec.org/a/oup/qjecon/v130y2015i4p1941-1973.html)). A post that did unusually well is likely to be followed by an ordinary one regardless of what you change (regression to the mean, [Quirk's](https://www.quirks.com/glossary/regression-to-the-mean)). So the best post is a poor guide to what to do next, and so is the worst.

## Comparing like with like

- **Same network.** X and TikTok count views differently; don't compare across them.
- **Same age.** Syndera reads results 1 hour, 1 day and 7 days after a post goes out (`variants[].results.readAt`). Compare 7-day numbers with 7-day numbers. A post read at 1 hour hasn't had its chance.
- **Boosted or not.** A boost buys reach; a boosted post's numbers aren't comparable with unboosted ones. Leave boosted posts out of organic comparisons, or show them separately.
- **The same measure.** Pick one before looking (for example likes per view) and use it for every post. Even X's own help pages define engagement rate in more than one way ([X glossary](https://help.x.com/en/business-and-advertising/x-ads-glossary)), so say which one you used.
- **Medians and ranges, not the top post.** Report the typical post and the spread.
- **Decide the comparison before you look,** and don't stop when the first good-looking result appears ([Evan Miller, "How not to run an A/B test"](https://www.evanmiller.org/how-not-to-run-an-ab-test.html)).
- **Watch for what else changed:** time of day, media type, topic, a news event, follower growth over the period.

## How strong is the evidence

There is no credible minimum number of posts that makes a social comparison reliable; the right number depends on how noisy the brand's results are. As a floor, below which ranking is mostly noise:

| Comparable posts with results | Say | Do |
|---|---|---|
| Fewer than about 10 | "Little evidence" | Describe; propose a test |
| About 10–30 | "Suggestive" | Point to repeated patterns; keep testing |
| 30+ over several weeks | "Consistent so far" | Recommend, and keep checking |

A test is a small, deliberate change tried on several posts, with the measure and the date to look again decided first.

## Saying how sure you are

Use the same words every time, so the person can calibrate you: **little evidence**, **suggestive**, **consistent so far**. Never "proven". With every claim give the metric, the window and the number of posts. When you don't know, say so; models tend to sound surer than their evidence ([Xiong et al.](https://arxiv.org/abs/2306.13063)), and fixed wording scales exist for exactly this ([UK Government, explaining uncertainty](https://www.gov.uk/government/publications/explaining-uncertainty-in-uk-intelligence-assessment)).

## What the numbers can't tell you

- **Hand-posted networks** have no results in Syndera. Don't treat them as zero.
- **Business outcomes.** Views and likes are outputs; visits, sign-ups and sales are outcomes. Organic social is hard to credit: link tracking undercounts it, and ad-measurement studies show observational methods often overstate effects ([Gordon et al., Marketing Science 2019](https://www.kellogg.northwestern.edu/faculty/gordon_b/files/fb_comparison.pdf)). If the person cares about outcomes, suggest tagged links or asking customers how they heard of them.
- **Cadence and timing.** Neither X nor TikTok publishes a best posting frequency or time; TikTok's own guidance is a target the creator can keep up ([TikTok Creator Academy](https://www.tiktok.com/creator-academy/en/article/posting-cadence-best-practices-publishers)). Studies disagree on frequency effects, so let the brand's own results and capacity decide.
