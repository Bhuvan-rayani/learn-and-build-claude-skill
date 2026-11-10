---
name: paper-review
description: Review a research draft the way a skeptical peer reviewer would, by auditing claims against evidence, find overclaiming, missing baselines, unclear writing, and venue-fit problems, then rank the fixes. Use when the user says "review my paper", "act as reviewer 2", "is this ready to submit", "find weaknesses in my draft", or before submission.
---

# Paper Review

Finds the problems a reviewer would find, while there is still time to fix them. Be specific and fair: the goal is a stronger paper, not a long list.

## Process

1. **Read the whole draft** plus `PROBLEM_STATEMENT.md`, `EXPERIMENT_DESIGN.md`, `EXPERIMENT_LOG.md` and `CLAIMS_EVIDENCE.md` if they exist. Ask the user for the target venue's review criteria, or use the generic ones below.
2. **Summarize the paper in 3 sentences** as a reviewer would. If your summary differs from the user's intent, the paper is unclear; report that first.
3. **Score** each criterion below from 1 (serious problem) to 5 (strong), with a one-line justification and a location.
4. **Run the claim-evidence audit.** For each claim in the abstract and contributions, find its evidence. Mark: supported, partly supported, unsupported, or contradicted.
5. **List weaknesses by severity**: Critical (would cause rejection), Major, Minor. Each item includes where, why it matters, and a concrete fix.
6. **List strengths** honestly, so the user knows what to keep.
7. **Give a readiness verdict**: submit / revise then submit / major revision needed, and the three fixes with the highest payoff.

## Criteria

| Criterion | Questions |
|---|---|
| Significance | Does the problem matter? Is the contribution clear? |
| Novelty | Is it distinguished from the closest work, with fair comparison? |
| Soundness | Is the method correct? Are conclusions justified? |
| Evaluation | Strong baselines, ablations, enough runs, correct statistics, no leakage? |
| Clarity | Can an informed reader follow and reproduce it? |
| Honesty | Limitations stated? Claims match evidence? Negative results shown? |
| References | All verified, relevant work covered, accurate attribution? |
| Reproducibility | Code, data, seeds, hyperparameters, compute disclosed? |
| Ethics | Data use, privacy, harm, AI-use disclosure? |

## Common problems to check for

Contribution statements that experiments do not support; the main claim hidden in the discussion; baseline missing or untuned; improvement within noise reported as a win; tuning on the test set; inconsistent numbers between text, tables and abstract; undefined notation; related work that lists papers without comparing; a conclusion stronger than the results.

## Rules

- Quote locations (section, table, line) instead of vague remarks.
- Separate "I could not verify this" from "this is wrong".
- Do not rewrite the paper unasked. Offer fixes and let the user choose.
- Do not guess what a venue's reviewers will do. Say "a reviewer may" and why.
- Remind the user that this is a self-check and not a substitute for supervisor or peer feedback.
