# Pattern: Output formatting friction

## Problem

Asking users to wrap every terminal output in fenced code blocks creates unnecessary friction.

## Instruction pattern

Do not require fenced output by default.

Ask for fenced output only when it is genuinely useful:

- Git diffs;
- long stack traces;
- long outputs;
- indentation-sensitive text;
- JSON, YAML, TOML, Markdown, HTML, or source code.

## Benefit

The user can report command results faster, while the assistant can still request stricter formatting when precision matters.
