# Codex exec: a reconstruction experiment with a public test kit

Category: Applications

Evidence: **Author report with public test artifacts** · Stage: **Partial reconstruction**

Last source review: 2026-10-17

## Target and question

Study a bounded non-interactive CLI reconstruction using published differential tests and research notes.

## REA workflow and result

The author reports reconstructing selected Codex CLI 0.162.1 exec behavior in Python from installed files. The first pass used black-box observation with zero REA calls. A second pass required REA: full-binary analysis timed out, so the agent carved the read-only data section into a smaller ELF, inspected selected bytes and strings with REA, and combined that evidence with Python extraction and differential runs against a fake model server.

## Evidence and limits

The repository publishes a test harness, scenarios, research notes and reported scores, not the reconstructed implementation. The author reports 416/422 checks across two suites; these are individual checks, not 422 independent tasks or a general accuracy estimate. Real-model behavior, working sandbox enforcement, interactive UI and resume/review behavior were not tested. The second pass also had more time and iteration, so its improvement does not isolate REA's causal effect. No full-target decompilation was obtained.

We reviewed published source and documentation without running the implementation or independently reproducing the reported tests.

## Sources and credit

- https://github.com/softsweb/codex-clone-hidden-test-kit
- https://github.com/softsweb/codex-clone-hidden-test-kit/blob/main/RESULTS.md
- https://github.com/softsweb/codex-clone-hidden-test-kit/blob/main/notes/NOTES-second-copy.md
- https://github.com/softsweb/codex-clone-hidden-test-kit/blob/main/exam/compare2.py

Credit belongs to the maintainers and contributors identified in the linked project.

[Back to casebook](../README.md)
