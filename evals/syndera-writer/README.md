# Evals for syndera-writer

Not installed with the skill. Run every task twice, with and without the skill, on at least two models (a small and a large one), against a test Syndera account seeded with `brands/`. Each run is graded four ways:

1. **Behaviour** (`graders/behaviour.md`): binary checks on the tool calls and the saved post. These decide whether the skill ships.
2. **Spread** (`graders/spread.md`): across the drafts for one task and across brands, do outputs differ? A skill that makes every brand sound the same fails here even if each post looks fine.
3. **Voice** (`graders/judge.md`): a pairwise judge, order swapped, asks which draft is closer to the brand's own published posts. Never "which is better".
4. **Triggers** (`triggers.json`): does the skill load for writing requests and stay out of the others?

Seed the test account with `brands/` (profile, channels, published posts with results) and `drafts.json` (the drafts tasks refer to by `fixture`). `tasks.json` is stratified by latitude (blank request, voice present, point edit), network (X, TikTok, both) and brand. Add a task whenever a real failure shows up.
