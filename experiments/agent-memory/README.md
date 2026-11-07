# Agent memory in Markdown

Status: planned. No test has been run.

## Source and claim

[Paweł Huryn's post](https://x.com/PawelHuryn/status/2118826877414490386) describes a small always-loaded index and task-specific Markdown files, with periodic review to remove stale or duplicate notes. It references [Anthropic's research on agent memory](https://www.anthropic.com/research/components-of-agent-memory).

Question: can a small, reviewed set of project notes improve answers to project-specific questions across fresh agent sessions?

## Proposed test

Create a fictional project with a small, documented history and a held-out set of questions whose answers can be checked against that history. Compare fresh sessions with no prepared memory against sessions given the same concise index and topic files. Use the same model, tools, task instructions, and question set; record which source files each condition can access. Randomize question order and repeat runs if feasible.

Score each answer against an answer key for correctness and unsupported assertions. Record elapsed time, token use or cost when available, and whether the agent cites the correct source. Include questions whose answers changed over time to check whether stale notes cause errors.

The result will apply to this dataset and setup. A small test cannot establish that the technique works across all projects or models.
