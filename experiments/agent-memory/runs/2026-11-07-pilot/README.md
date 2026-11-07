# Pilot run: November 7, 2026

The baseline and the memory-note condition each answered **8 of 8** questions correctly. The note did not improve the score on this fixture. Because the baseline already reached the maximum, this test could not measure an improvement beyond it.

| Condition | Correct | Input tokens reported | Output tokens reported |
| --- | ---: | ---: | ---: |
| Baseline | 8/8 | 20,991 | 58 |
| Memory note | 8/8 | 21,060 | 61 |

The input-token totals include the Codex session's overhead and cannot be interpreted as the size of the fixture alone. The memory run reported 7,168 cached input tokens. Cost was not available and duration was not captured.

## Method and evidence

Two separate ephemeral sessions used Codex CLI 0.167.0, `--ignore-user-config`, `--sandbox read-only`, and the same default model selection. The CLI did not report the actual model identifier, so it cannot be independently verified from this record. The working directory was an isolated temporary directory containing the two prompt files and output logs. Prompts instructed the model not to use tools or access files; the recorded event streams contained no tool calls. The full history was present in both prompts and the note was present in only one.

- [Baseline prompt](baseline.txt) and [response](baseline-response.txt)
- [Memory prompt](memory.txt) and [response](memory-response.txt)
- [Baseline usage](baseline-usage.json) and [memory usage](memory-usage.json)
- [Fixture](../../fixture.md) and [answer key](../../answer-key.md)

Each answer was checked against the key by the assistant that conducted the run. The protocol called for a human scorer; no independent human review has been performed. The baseline was run first without randomizing order, another deviation from the protocol. Exact elapsed time was not measured. These deviations limit reproducibility and confidence.

The published baseline prompt has one trailing blank line removed from the submitted prompt; its substantive text is unchanged.

The run was invoked once per condition with `codex exec --ephemeral --ignore-user-config --skip-git-repo-check --sandbox read-only --json`, using the corresponding prompt on standard input. Both sessions completed successfully. No tool calls were reported. This fixture is short and the note directly restates the answers, so a larger test with distractors, varied tasks, and repeated runs is needed before making claims about real project memory.
