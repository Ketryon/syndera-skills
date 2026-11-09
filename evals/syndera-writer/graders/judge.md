# Pairwise voice judge

Give the judge the brand's published posts and two captions (skill arm, no-skill arm) in random order; run every pair twice with the order swapped and keep only consistent verdicts. Use a different model family from the one that wrote the captions.

Prompt:

> Here are posts this brand has published: {published}
> Here are two new captions for the same request: A: {a} B: {b}
> Which caption reads more like it was written by the same people who wrote the published posts? Consider vocabulary, length, rhythm, punctuation, emoji and how they address readers. Don't judge which is better marketing. Answer "A", "B" or "same", then one sentence on why.

Report the win rate with a 95% interval. Tie on "same" counts as half.
