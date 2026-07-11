# Pattern: Durable lesson-learned capture

## Problem

Useful lessons discovered during technical work are easily lost inside long conversations. Naively saving every observation creates duplicates, leaks project-specific details, and can corrupt derived indexes.

## Instruction pattern

Reserve an explicit trigger such as `+lele:"TOPIC"`.

When the user invokes it:

1. extract one or more lessons that are generalizable beyond the current project;
2. remove private data and details that are too project-specific;
3. inspect the canonical vault referenced by an environment variable such as `$LELE_VAULT_DIR`;
4. determine whether to create a new lesson, update an equivalent existing lesson, or make no change;
5. use the vault's canonical Markdown schema and save under `$LELE_VAULT_DIR/<topic>/`;
6. validate frontmatter, identifiers, and duplicates;
7. create a separate Git commit for the lesson change;
8. never edit derived artifacts such as JSONL indexes directly.

If filesystem or terminal access is unavailable, do not claim that the lesson was saved. Instead, provide:

- the complete Markdown content;
- the intended path;
- the exact commands required to save, validate, and commit it.

## Benefit

Conversation knowledge becomes durable and searchable without duplicating lessons, exposing private context, or confusing authoritative sources with generated indexes.
