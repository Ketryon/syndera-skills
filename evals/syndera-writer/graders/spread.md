# Spread (are the outputs different where they should be?)

The skill must not make brands converge. Compute on the saved captions, skill arm vs no-skill arm:

- **Across brands, same task shape:** mean pairwise embedding similarity between Fjord Tea and Pixelpunch captions for `blank-x-quiet` vs `blank-x-loud` and the TikTok pair. Lower is better; the skill arm must not be higher.
- **Within a task with an open angle** (`blank-open-angle`): pairwise similarity between the drafts offered. Lower is better; drafts that differ only in wording count as one.
- **Against the brand's own posts:** distinct-2 and mean length vs the brand's published posts on that network. Closer to the brand's own numbers is better.
- **Repetition across runs:** run each blank task 5 times; flag phrases that recur in more than half the runs across different brands. Those are house-style leaks.
