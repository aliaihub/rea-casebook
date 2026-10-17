# Warhammer III: save editing informed by native serializers

Category: Games

Evidence: **Public project** · Stage: **Working implementation**

Last source review: 2026-10-17

## Target and question

Recover save-format behavior to fix campaign conversion and support unit creation.

## REA workflow and result

The maintainer credits REA with Ghidra from version 1.2.4 onward for inspecting Warhammer3.exe save serializers. Specific findings include the IDLE_HUMAN player state, signed integer encoding, a unit-ID counter and the campaign AI's unit mirror. Those findings informed conversion fixes and later unit-creation support in an existing Python/PySide6 editor.

## Evidence and limits

Public source, release history and maintainer-reported in-game validation are available. Earlier versions predate the stated REA contribution; the entire editor should not be attributed to REA. The project uses a restrictive source-available license rather than an open-source license. In-game correctness and compatibility claims belong to the maintainer.

We reviewed published source and documentation without running the implementation or independently reproducing the reported tests.

## Sources and credit

- https://github.com/davehornik/WH3SaveEditor

Credit belongs to the maintainers and contributors identified in the linked project.

[Back to casebook](../README.md)
