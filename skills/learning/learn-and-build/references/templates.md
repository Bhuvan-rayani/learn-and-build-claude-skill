# Templates for learn-and-build

Copy these layouts when creating the project files. Keep them short; they are working documents the user will reread.

## docs/LEARNING_PLAN.md

```markdown
# <Project name>: Learning and Build Plan

**Goal:** <portfolio / interview / personal tool>
**Learner level:** <summary from intake>
**Resources:** <courses, books, docs the user has>
**Project rules (from the spec):** <hard rules to honour in every stage>

## Roadmap

| # | Stage | We build | Learn first | Where to learn | Status |
|---|-------|----------|-------------|----------------|--------|
| 0 | Setup | ... | ... | ... | not started |
| 1 | ... | ... | ... | ... | not started |

Status values: `not started` / `brief sent` / `learning` / `building` / `verifying` / `done`

## Minimum viable cut
After stage <N> the project is demo-able: <one sentence on what it can do>.

## Reorders versus the original spec
- <what moved, and why>

## Parked for later
- <stretch ideas, not in scope yet>

## Open questions
- <unanswered intake questions>
```

## Stage brief (chat message or docs/stages/stage-N-brief.md)

```markdown
# Stage N: <name>

**Goal:** <what exists at the end, plain words>
**Why now:** <where it sits in the dependency chain>

## Learn first
- [ ] <topic> - <source or search term> - <depth: understand / can write>
- [ ] ...

## Self-check (answer these before saying "learnt")
1. <why-question>
2. <why-question>
3. <scenario-question>

## Acceptance check
<the test or demo that means this stage is done>

## Design questions you'll be asked while we build
- <preview of real decisions>
```

## Decision note (inline, before significant steps)

```
Next: <what I'm about to do>
Why: <what this step exists for / protects against>
Chose: <approach> over <alternative> because <trade-off>
Watch for: <one thing worth understanding or that could go wrong>
```

## Decision request (when the choice is the user's)

```
Decision needed: <question>
A) <option> - <cost/benefit>
B) <option> - <cost/benefit>
My lean: <A/B> because <reason>. Your call.
```

## docs/DECISIONS.md entry

```markdown
## D<number>: <title>  (Stage N, <date>)
- **Context:** <what forced a choice>
- **Options:** A) ... B) ...
- **Decision:** <chosen option>, decided by <user / Claude>
- **Why:** <reasons and trade-offs>
- **Revisit if:** <condition that would change this>
```

## docs/KNOWN_ISSUES.md entry

```markdown
- [ ] <issue> (found in Stage N) - <impact> - <proposed fix / stage to address it>
```

## Stage walkthrough (end of each stage)

```markdown
### Stage N walkthrough
**What was built:** <files/modules and how they connect, 3-6 bullets>
**Key decisions:** <2-3, with pointers to DECISIONS.md>
**Acceptance check result:** <what was run, what passed/failed>
**Deliberately left out:** <and where it will be handled>
**Teach-back question:** <one question for the user>
**Try it:** <optional: break X on purpose and see which test fails>
```

## Session-resume opener

When starting a new session on an existing project, read the three docs files, then say:

```
Where we are: Stage <N> (<name>) is <status>. Done so far: <stages>. Next: <next step>.
Open issues worth knowing: <0-2 items>.
```
