---
name: reading-guide
description: Build an ordered reading plan for a research topic, tell the user which papers and background topics to read and why, ask checkpoint questions, and take the user's notes as input to update the literature record. Use when the user needs to learn a research area, asks "what should I read first", "which papers do I read", "teach me this topic before we write", or reports back "I read it" with notes.
---

# Reading Guide

Research understanding comes from the user reading, not from a summary. This skill assigns the right reading in the right order, then checks understanding and records what the user learned.

## Build the reading plan

1. Start from `docs/research/LITERATURE_MATRIX.md` and the problem statement. If missing, run `literature-overlap` first.
2. Split reading into three tiers, each item with a reason:
   - **Foundations** (1-3 items): background concepts the user needs to follow the closest papers. Name them as topics to study and point to textbooks, survey papers or course material the user already has.
   - **Core** (3-6 papers): the closest prior work, ordered so each paper makes the next easier. Start with a survey or the clearest paper, not the densest.
   - **Edge** (2-4 papers): adjacent methods, baselines, datasets, and critiques.
3. For each paper give: title, link, what to read (abstract, intro, method, results, limitations), what to skip on first pass, estimated time, and **2-3 focus questions** to answer while reading.
4. Teach a reading method on request: three passes (skim, structure, details), and a notes template.

## Notes template to give the user

```
Paper: ...
One-sentence claim:
Problem they solve:
Method in my words:
Data and evaluation:
Main results (numbers):
What they admit they cannot do:
How it differs from my problem:
Questions I still have:
```

## The "read" gate

When the user says they have read a paper or tier:

1. Ask them to paste or describe their notes. Take them as input.
2. Ask 2-3 checkpoint questions that need understanding, such as "Why does their method need X?" or "What would break their result?".
3. Correct misunderstandings gently, with the relevant passage location when you can see the paper. If you have not read it, say so and avoid guessing.
4. Update the matrix and `docs/research/READING_LOG.md` with the user's own takeaways and any change to the overlap judgment.
5. Ask whether the reading changes the problem statement. If yes, hand back to `problem-framing`.

## Reading log entry

```markdown
## <Paper short name> (read <date>, depth: full / partial)
- Claim:
- Method in my words:
- Useful for our work:
- Limitations to exploit or avoid:
- Open questions:
```

## Rules

- Do not substitute your summary for the user's reading. Give focus questions and structure, and provide a short orientation only if the user is stuck.
- Only describe papers you have actually read in this session. Otherwise say "abstract only".
- Keep the list short. Ten well-read papers beat forty skimmed ones. Add more only when the user asks or a gap appears.
- Leave a "read later" list so the main list stays small.
