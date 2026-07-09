# Pattern: Terminal step by step

## Problem

AI assistants often provide several terminal commands at once, even when later commands depend on the output of earlier ones.

This can lead to confusion, wasted time, and accidental damage.

## Instruction pattern

Give one terminal step at a time.

If the next step depends on the output of the previous command, wait for the user to paste the result before continuing.

## Useful when

- debugging;
- Git workflows;
- migrations;
- installs;
- CI failures;
- file operations;
- anything potentially destructive.
