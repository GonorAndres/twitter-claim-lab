# Agent memory in Markdown

Status: [pilot completed](runs/2026-11-07-pilot/README.md). Both conditions answered all eight questions correctly. The pilot is too small and easy to establish whether memory helps.

## Source and question

[Paweł Huryn's post](https://x.com/PawelHuryn/status/2118826877414490386) describes a small always-loaded index and task-specific Markdown files, with periodic review to remove stale or duplicate notes. It references [Anthropic's research on agent memory](https://www.anthropic.com/research/components-of-agent-memory).

Can a concise, accurate note improve answers about a project's current decisions when the complete project history is also available?

## Pilot protocol

The fictional project history, questions, and note are in [fixture.md](fixture.md). The answer key is in [answer-key.md](answer-key.md). These are public, synthetic data; the answers are not real-world facts.

Run two fresh sessions with the same model and settings. In both, provide the project history and questions, without the answer key. In the memory condition, also provide the memory note. Do not allow either session to browse or read other files. Ask for a numbered answer to each question and an explicit unknown where the history does not establish an answer. Randomize condition order before running; record the order.

Score each of the eight answers as correct, incorrect, or ambiguous against the key. An unknown answer is correct for the unanswerable item; a confident invented answer is incorrect. Report individual answers and the number correct in each condition. Record model and version, run date, exact prompts, outputs, settings, duration, and usage or cost when available. A human scorer should assess both outputs against the same key before comparing totals. Preserve raw answers and identify any post-run changes to the protocol.

The pilot has one small fictional history and one run per condition. It is a smoke test, not evidence of a general accuracy improvement. Providing a correct note also gives one condition more information and tokens, so the comparison measures the effect of this particular added summary. It does not isolate retrieval, validate the author's workflow, measure stale-note maintenance, or establish statistical significance.
