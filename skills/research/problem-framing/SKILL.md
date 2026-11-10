---
name: problem-framing
description: Turn a rough research idea into a sharp, testable problem statement, then suggest improvements before the user confirms it. Use when the user gives a research topic or problem statement and wants it optimized, sharpened, scoped, made testable, or checked for vagueness, or says "help me define my research problem", "improve my problem statement", "is this a good research question".
---

# Problem Framing

A weak problem statement wastes every later stage. This skill makes it precise, scoped and testable, shows the user what changed and why, and only locks it after their explicit confirmation.

## Process

1. **Restate the idea in one sentence** and ask the user whether that is right. If you cannot restate it, the idea is not yet clear; ask what they want to find out.
2. **Diagnose** the draft against the checklist below. Name each weakness plainly.
3. **Propose 2-3 improved versions** at different scopes (narrow, medium, ambitious) with the trade-off for each: feasibility, data and compute needs, novelty risk, and time.
4. **Recommend one** and say why. Ask the user to choose or adjust.
5. **Confirm.** Show the final statement in the format below and ask: "Do you confirm this as the problem statement?" Do not proceed to later stages on silence.

## Diagnosis checklist

| Check | A good statement |
|---|---|
| Specific | Names the population, task, setting or system, not "improve X" |
| Testable | Could be answered by an experiment, proof, analysis or study |
| Scoped | Fits the user's time, data, compute and skill |
| Motivated | States who is hurt by the gap, with evidence the gap exists |
| Measurable | Has a metric or criterion for "better" or "answered" |
| Non-trivial | Not already settled by a textbook or one search |
| Falsifiable | Has an outcome that would show the hypothesis wrong |
| Single focus | One main question; extra questions are sub-questions |

## Output format (save as `docs/research/PROBLEM_STATEMENT.md`)

```markdown
# Problem Statement (v<N>, confirmed <date>)

**Working title:** ...
**Context and gap:** 2-3 sentences: what is known, what is missing, who cares.
**Problem statement:** one or two sentences.
**Research questions:** RQ1 (main), RQ2, RQ3 (sub-questions, at most 3).
**Hypotheses:** H1 ... (what result would support or refute it).
**Scope:** in scope / out of scope.
**Assumptions and constraints:** data, compute, time, ethics.
**Success criteria:** how we will know the question was answered.
**Contribution type:** new method / empirical study / benchmark / replication / survey / analysis.
**Risks:** top 3, with a fallback.
**Change log:** what was changed from the previous version and why.
```

## Improvement suggestions to consider

- Narrow a broad topic to one task, domain or dataset.
- Replace "better" with a named metric and a named baseline.
- Convert a "build X" goal into a question about why or when X works.
- Split compound questions; keep the one the user cares about most as RQ1.
- Add a falsifiable hypothesis.
- If the idea is mostly an engineering project, say so and offer `learn-and-build` instead of forcing a research framing.

## Notes

- Do not search the literature in depth here; that is `literature-overlap`. A quick check that the question is not trivially answered is fine.
- Keep the user's voice. Improve clarity and scope; do not replace their interests with yours.
- If a later stage shows the statement must change, update the file, bump the version, and record the reason in the change log.
