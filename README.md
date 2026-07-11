# AI Operating Profiles

Professional custom instruction profiles for practical human-AI workflows.

This repository collects reusable AI operating profiles: practical custom instructions, behavioral patterns, and workflow rules that help people use AI assistants in a more reliable, understandable, and task-oriented way.

## Why this exists

Most people customize AI assistants with vague instructions such as "be clear" or "be helpful".

This project focuses on operational instructions instead:

- how the assistant should guide the user;
- when it should ask questions;
- when it should wait;
- how it should handle uncertainty;
- how it should support learning;
- how it should avoid unnecessary friction;
- how it should preserve useful context and reusable knowledge.

## Core idea

Good AI customization is not about making the assistant nicer.

It is about making the assistant operationally compatible with the human.

## How to use these profiles

Start from a complete profile when you want a ready-to-adapt assistant behavior.

Use individual patterns when you only need one specific rule, such as terminal-first guidance, output formatting, uncertainty handling, restart-friendly recaps, or durable lesson capture.

A good workflow is:

1. pick the closest profile;
2. copy only the parts that match your real workflow;
3. add your personal constraints;
4. test the instructions on a small task;
5. simplify anything that feels vague, redundant, or theatrical.

These profiles are meant to be practical operating agreements, not magic prompts.

## Initial profiles

- [Scimmietta Operativa](profiles/scimmietta-operativa.md): terminal-first, learning-first guidance with explicit working-directory context, dependency-aware checkpoints, restart recaps, and durable lesson capture.

## Included patterns

- [Terminal step by step](patterns/terminal-step-by-step.md): group independent commands and stop only at real decision points.
- [Output formatting friction](patterns/output-formatting.md): request fenced output only when precision requires it.
- [Restart-friendly recap](patterns/restart-recap.md): generate a self-contained handoff prompt through an explicit trigger.
- [Durable lesson-learned capture](patterns/lesson-learned-capture.md): generalize, deduplicate, validate, and version reusable lessons safely.

## Repository structure

- `profiles/`: complete custom instruction profiles ready to adapt.
- `patterns/`: reusable instruction fragments.
- `examples/`: compact and extended examples.
- `docs/`: project notes and design rationale.

## Status

Active lab repository.
