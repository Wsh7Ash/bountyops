# Usage

## Setup

```shell
git clone https://github.com/Wsh7Ash/bountyops.git
cd bountyops
python -m pip install -e ".[dev]"
```

## Day-to-day commands

```shell
python -m bountyops validate                # the 50/50 gate (exit 0 = all valid)
python -m bountyops validate --json         # machine-readable report for CI
python -m bountyops list                    # all 50 skills, one line each
python -m bountyops list --phase queue      # only queue-phase skills
python -m bountyops list --tag reporting    # filter by tag
python -m bountyops search duplicate payout # rank by keyword hits
python -m bountyops show weekly-queue-construction  # full SKILL.md
python -m bountyops build                   # regenerate skills/, pack.json, results/
```

## Turning a weekly queue into a runbook

Write a small JSON week file (or copy `examples/demo-week.json`):

```json
{
  "week": "2026-W44",
  "items": [
    {"program": "alpha", "state": "retesting", "tags": ["idor", "orders"]},
    {"program": "beta", "state": "report-writing", "tags": ["graphql"]}
  ]
}
```

Then:

```shell
python -m bountyops queue --week-file examples/demo-week.json
```

Output is a phase-ordered runbook: skills grouped under `## program`,
`## queue`, `## reproduce`, `## report`, `## followup`, `## portfolio`, each
with matching steps and the reason it matched. Phases that matched nothing
are listed under *Thin coverage* so you can see what the runbook does not yet
address. Add `--json` for a machine-readable payload and `--top N` to cap
plan length.

## Loading skills into agents

Each generated file `skills/<slug>/SKILL.md` has YAML front-matter
(`name`, `description`, `pack`, `version`, `category`, `tags`), which
agent skill loaders consume directly. Point your agent at the `skills/`
directory, or pick specific skills with `pack.json`'s per-skill paths and
SHA-256 digests.

## Regeneration discipline

Never edit `skills/`, `pack.json` or `results/` by hand. Edit the corpus
dicts in `src/bountyops/corpus/part*.py`, run `python -m bountyops build`,
then commit. The `test_committed_skills_match_corpus_render` test fails on
any drift, and CI rebuilds and diffs to prove it.

## Scope and ethics

bountyops plans, documents and reviews **authorized** testing. It contains
no exploitation technique and no instruction to test anything outside a
program's declared scope.