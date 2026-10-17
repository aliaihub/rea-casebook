# Wispr Flow: a documented local dictation reconstruction

Category: Applications

Evidence: **Public project** · Stage: **Partial reconstruction**

Last source review: 2026-10-17

## Target and question

Investigate Wispr Flow for Windows 1.6.1102 and implement a small local version of its hold-to-dictate-and-paste workflow.

## REA workflow and result

The project records initial REA MCP timeouts, manual extraction and JavaScript inspection, later successful REA CLI analysis, and a Ghidra pass through REA on a native helper. Its reports distinguish supported findings, inferences, and unavailable server internals.

The public Python implementation, FlowLite, records while F9 is held, transcribes locally with faster-whisper, pastes the result, and restores clipboard text. Later changes incorporate app-specific paste keys and delays identified in the helper analysis.

This is az9713's follow-up project, which credits Eric Tech's video; it is not presented as Eric Tech's original implementation.

## Evidence and limits

- Public artifacts include implementation code, a teardown report, development notes, a Ghidra report, and test receipts.
- The successful saved workflow test injects prerecorded WAV audio in place of the microphone input while retaining the hotkey, transcription, paste, and clipboard-restoration paths. Earlier speaker-to-microphone tests returned empty transcripts. The receipt therefore does not establish successful live microphone dictation.
- The original Wispr application was not run for a runtime or network comparison. Cloud transcription, formatting, streaming, and context behavior are not reconstructed.
- Clipboard restoration covers text, not every clipboard format.
- REA contributed alongside manual inspection and implementation work. This is a limited independent reconstruction, not full Wispr Flow parity.
- We reviewed the published artifacts without running the implementation or independently reproducing its tests.

## Sources and credit

- [Project and source code](https://github.com/az9713/wispr-flow-rea-teardown)
- [Teardown report](https://az9713.github.io/wispr-flow-rea-teardown/wispr-flow-teardown.html)
- [Ghidra pass](https://az9713.github.io/wispr-flow-rea-teardown/ghidra-pass.html)
- [Development journey and test receipts](https://az9713.github.io/wispr-flow-rea-teardown/DEVELOPMENT-JOURNEY.html)
- [Implementation](https://github.com/az9713/wispr-flow-rea-teardown/blob/main/flowlite/flowlite.py)
- [Eric Tech's reference video](https://www.youtube.com/watch?v=FnB9tHKBJXQ)

Credit belongs to az9713 and the contributors identified in the linked project. Eric Tech's demonstration inspired the follow-up.

[Back to casebook](../README.md)
