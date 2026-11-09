# Evals for syndera-strategist

Not installed with the skill. Same method as the writer's and the lead's: run every task with and without the skill, on at least two models, against a test account seeded with `../syndera-writer/brands/`, `drafts.json` here (drafts with planted problems, and clean ones) and `intel.json` (a recorded Intel brief per brand, so runs don't spend research). Graded by:

1. **Behaviour** (`graders/behaviour.md`): binary checks on tool calls and claims. These decide whether it ships.
2. **Planted problems** (`drafts.json` → `planted`): did the audit find each one, with its source? A clean draft reported as clean counts as a pass; a finding on it that isn't real counts against.
3. **Strategy** (`graders/strategy.md`): is the recommended position backed by the brief's sources, specific to the brand, and labelled with how sure it is?
4. **Triggers** (`triggers.json`): loads for competitors, market, positioning and audits; stays out of writing, calendar planning and results questions.

Add a task whenever a real failure shows up.
