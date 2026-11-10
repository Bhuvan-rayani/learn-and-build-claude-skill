# Templates for research-mentor

Create these under `docs/research/` in the user's project. Keep them short; they are working documents.

## RESEARCH_PLAN.md

```markdown
# <Working title>: Research Plan

**Goal / venue:** ...   **Deadline:** ...   **Resources:** ...
**Integrity rules in force:** no fabricated citations or results; user owns claims; AI use disclosed per venue.

| # | Stage | Output | Gate | Status |
|---|-------|--------|------|--------|
| 1 | Frame problem | PROBLEM_STATEMENT.md | user confirms statement | not started |
| 2 | Scan and overlap | LITERATURE_MATRIX.md + verdict | user decides proceed / narrow / pivot / reframe | not started |
| 3 | Read | READING_LOG.md | user says "read", answers checkpoints | not started |
| 4 | Design | EXPERIMENT_DESIGN.md | user approves | not started |
| 5 | Run | EXPERIMENT_LOG.md | results logged, no gaps | not started |
| 6 | Draft | paper sections + CLAIMS_EVIDENCE.md | user confirms each section | not started |
| 7 | Review | review report | user picks fixes | not started |
| 8 | Submission prep | checklist done | user submits | not started |

Status values: `not started` / `in progress` / `waiting on user` / `done`

## Parked ideas
- ...

## Open questions
- ...
```

## EXPERIMENT_LOG.md

```markdown
| Run id | Date | Hypothesis / purpose | Config (model, data, params, seed) | Command | Result | Notes (anything odd, failures) |
|---|---|---|---|---|---|---|
```

## CLAIMS_EVIDENCE.md

```markdown
| Claim in paper | Section | Evidence (run id / table / citation) | Strength | Hedge needed |
|---|---|---|---|---|
```

## DECISIONS.md entry

```markdown
## D<n>: <title> (Stage N, <date>)
- Context:
- Options:
- Decision (by user / Claude):
- Why:
- Revisit if:
```

## Session-resume opener

```
Where we are: Stage <N> (<name>) is <status>. Last confirmed: <problem statement vN / design / section>.
Waiting on you for: <reading / confirmation / results>.
```
