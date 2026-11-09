# Evals for syndera-lead

Not installed with the skill. Same method as the writer's: run every task with and without the skill, on at least two models, against a test account seeded with `../syndera-writer/brands/` plus `history.json` (published posts with results at several ages, one boosted). Graded by:

1. **Behaviour** (`graders/behaviour.md`): binary checks on tool calls and claims. These decide whether it ships.
2. **Calibration** (`graders/calibration.md`): does it say how sure it is, and does that match the evidence it had?
3. **Triggers** (`triggers.json`): loads for planning, results and boost questions; stays out of writing a single post (the writer's job) and of unrelated requests.

`tasks.json` is stratified by job (plan, results, boost) and evidence (little, some, more). Add a task whenever a real failure shows up.
