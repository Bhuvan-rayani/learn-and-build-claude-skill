---
name: paper-drafting
description: Draft a research paper section by section from the user's own findings and notes, in an order that avoids rework, with a claim-evidence map and verified citations. Use when the user says "help me write the paper", "write the introduction", "draft the methods/results/abstract", "structure my paper", or has results and needs them turned into a manuscript.
---

# Paper Drafting

Turns the user's confirmed problem, verified literature and logged results into a manuscript. The user supplies the ideas and findings; this skill supplies structure, clarity and consistency.

## Preconditions

Confirmed problem statement, literature matrix, and (for results sections) an experiment log with real results. Missing results means the Results section is not written yet. Say so instead of drafting placeholders that look like findings.

## Drafting order (and why)

| Order | Section | Why this order |
|---|---|---|
| 1 | Method | It is fixed once the design is fixed |
| 2 | Experimental setup | Copies directly from the design and the log |
| 3 | Results | Facts first: tables and figures, then text |
| 4 | Analysis and discussion | Needs the results |
| 5 | Related work | Uses the literature matrix and what the results revealed |
| 6 | Introduction | Easy to write once the contribution is known |
| 7 | Limitations and ethics | Honest reflection from the whole paper |
| 8 | Conclusion, then abstract, then title | They summarize what exists |

## Per-section loop

1. **Ask for input.** Request the user's own bullets, explanation or sketch for the section. If they have none, ask guiding questions and use their answers.
2. **Propose an outline** with one sentence per paragraph. Get a nod.
3. **Draft** from the user's material and the logs. Flag every sentence that makes a claim with `[evidence: <log id / table / citation>]` while drafting; remove the tags at the end.
4. **Check** each claim against the evidence, each number against the experiment log, and each citation against the literature matrix (`verified` only).
5. **Ask the user to read and confirm** it says what they mean. Revise with their edits.
6. Record claims in `docs/research/CLAIMS_EVIDENCE.md`.

## Claims and evidence file

```markdown
| Claim in paper | Section | Evidence (run id / table / citation) | Strength (strong / moderate / weak) | Hedge needed |
|---|---|---|---|---|
```

## Writing guidance

- Lead each paragraph with its point. One idea per paragraph.
- State contributions as specific, checkable bullets in the introduction, matching what the experiments show.
- Use the same name for each concept throughout. Define terms at first use.
- Prefer plain, direct sentences. Avoid inflated words and unsupported "significantly" without a test.
- Report numbers with their uncertainty and the setup that produced them. Report negative and null results.
- Match the venue's template, page limit and citation style; ask for them early.
- Write related work as a comparison to the user's problem, grouped by theme, not as a list of summaries.
- Figures and tables: each one supports a stated claim and is referenced in the text.

## Integrity rules

- Cite only `verified` entries from the literature matrix. If a needed citation is missing, ask to find and verify it.
- Do not generate results, p-values or quotes. Do not paraphrase a paper you have not read.
- Do not hide limitations to make claims sound stronger. Match each claim's strength to its evidence.
- Remind the user of the venue's policy on disclosing AI assistance. The user is the author and is responsible for every statement.
