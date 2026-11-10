---
name: experiment-design
description: Design the method and experiments for a confirmed research problem, covering hypotheses, baselines, datasets, metrics, ablations, statistics, threats to validity, compute and budget, and an analysis plan fixed before running anything. Use when the user asks "how do I test this", "design the experiments", "what baselines and metrics", "plan the study", or after literature reading is done.
---

# Experiment Design

Decide what will count as evidence before collecting any. A design written first protects the user from cherry-picking, and reviewers look for exactly this.

## Preconditions

Confirmed problem statement and a literature matrix that names the closest baselines. If either is missing, go back to the earlier stage.

## Process

1. **Restate the hypotheses** from the problem statement and the result that would refute each.
2. **Choose the study type**: controlled experiment, benchmark comparison, ablation study, user study, simulation, theoretical analysis, qualitative study, or replication. Explain the choice.
3. **Fill the design table** below. Ask the user for decisions that depend on their resources (data access, compute, time); do not assume.
4. **Plan the analysis** before running: primary metric, how results are aggregated, how many seeds or repeats, what statistical test or interval, and what counts as a meaningful difference.
5. **Estimate cost and time** in compute hours, API spend and calendar days. Compare with the user's budget and cut scope before starting, not after.
6. **List threats to validity** and one mitigation each.
7. **Get approval.** The user confirms the design; save it as `docs/research/EXPERIMENT_DESIGN.md`.

## Design table

| Item | Content |
|---|---|
| Hypotheses | H1, H2 with refutation conditions |
| Method | What is new or varied; one paragraph and a diagram if helpful |
| Datasets | Name, size, license, splits, preprocessing; synthetic data if real data is sensitive |
| Baselines | At least a simple baseline, the strongest recent method, and an ablated version of our own method |
| Metrics | Primary (one), secondary, and why they measure the claim |
| Ablations | Each component removed or varied once |
| Controls | What is held fixed (model, data, prompts, seeds, hardware) |
| Repeats and statistics | Seeds, confidence intervals or tests, multiple-comparison handling |
| Compute and budget | Hardware, hours, API cost, caching |
| Reproducibility | Config files, seeds, versions, how to rerun |
| Ethics and data | Consent, privacy, licensing, sensitive data handling |

## Threats to validity checklist

Data leakage between train and test; test set tuned on; weak or untuned baselines; metrics that do not match the claim; small samples; one seed; prompt or hyperparameter sensitivity; benchmark contamination; confounds; evaluation by the same model that is being evaluated.

## Rules

- Fix the primary metric and the main comparisons before running. Anything added later is labeled exploratory in the paper.
- If a design needs resources the user lacks, offer a smaller design (fewer datasets, one strong baseline, smaller models) that still answers the main question.
- If the work needs code, hand implementation to `learn-and-build`, keeping the experiment log in `docs/research/EXPERIMENT_LOG.md`.
- Do not invent expected numbers. Say what pattern would support the hypothesis, without predicting magnitudes you cannot justify.
