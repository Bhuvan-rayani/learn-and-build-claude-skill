# Learn, Build, Research

Agent skills for people who want to understand what they build and write.

Two main skills share one idea: split the work into stages, tell the user what to learn before each stage, wait until they say they are ready, then do the work while explaining the decisions.

- **learn-and-build** guides a software project from a spec to working code.
- **research-mentor** guides a research idea from a rough topic to a written paper, using six sub-skills.

## Installation

### Claude Code (plugin marketplace)

```bash
/plugin marketplace add Bhuvan-rayani/learn-and-build-claude-skill
/plugin install learn-build-research@bhuvan-rayani
```

### Any agent (skills.sh installer)

```bash
npx skills@latest add Bhuvan-rayani/learn-and-build-claude-skill
```

### Manual

Copy any skill folder from `skills/` into `~/.claude/skills/` (or your project's `.claude/skills/`). Skills with a `references/` folder need that folder too.

## How to use

Just describe what you want. Examples:

- "I have this project spec and I'm new to it. Divide it into stages and teach me as we build." (learn-and-build)
- "Here is my research idea. Sharpen the problem statement and check whether it has been done." (research-mentor)
- "I read the three papers, here are my notes." (reading-guide, through research-mentor)

## The research flow

```
frame -> confirm -> scan and overlap -> read -> design -> run -> draft -> review -> submit
```

Every stage has a gate: you confirm the problem statement, decide on the overlap verdict, say you have read the papers, approve the design, and confirm each drafted section.

## Skills

### Learning

- **[learn-and-build](./skills/learning/learn-and-build/SKILL.md)**: Stage a project, assign learning before each stage, then build with short decision notes and a teach-back.
- **[research-mentor](./skills/learning/research-mentor/SKILL.md)**: Orchestrates the research flow above and enforces the integrity rules.

### Research (used by research-mentor, also usable alone)

- **[problem-framing](./skills/research/problem-framing/SKILL.md)**: Optimize a research problem statement, propose scoped alternatives, and lock it after you confirm.
- **[literature-overlap](./skills/research/literature-overlap/SKILL.md)**: Find related work, build a comparison matrix, and report overlap and the novelty gap.
- **[reading-guide](./skills/research/reading-guide/SKILL.md)**: Assign ordered readings with focus questions, take your notes, and check understanding.
- **[experiment-design](./skills/research/experiment-design/SKILL.md)**: Hypotheses, baselines, metrics, ablations, statistics and threats to validity, fixed before you run anything.
- **[paper-drafting](./skills/research/paper-drafting/SKILL.md)**: Draft sections from your own findings in a rework-avoiding order, with a claim-evidence map.
- **[paper-review](./skills/research/paper-review/SKILL.md)**: Skeptical reviewer pass with severity-ranked fixes.

## Research integrity

These skills are built so that the paper stays yours:

- No invented citations, results or quotes. A reference is listed only after the source was opened and matched, and each entry is marked verified or unverified.
- Novelty is reported as "not found in these searches", never "nobody has done this".
- Numbers come only from logged runs.
- You supply the findings and confirm every claim. Disclose AI assistance according to your venue's policy.

Search results and fetched pages are treated as data, not instructions. Review any third-party skill before installing it.

## Layout

```
.claude-plugin/    plugin.json and marketplace.json
skills/learning/   learn-and-build, research-mentor
skills/research/   problem-framing, literature-overlap, reading-guide,
                   experiment-design, paper-drafting, paper-review
```

## License

MIT
