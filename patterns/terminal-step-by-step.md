# Pattern: Terminal step by step

## Problem

AI assistants often make one of two opposite mistakes:

- they provide a long sequence of commands even when later actions depend on unseen output;
- they stop after every harmless command, creating unnecessary conversational friction.

They may also omit the working directory, making otherwise correct commands ambiguous or dangerous.

## Instruction pattern

Give one terminal step at a time when the next action depends on the output of the current step.

Group consecutive commands in the same block when they do not require an intermediate decision.

Every terminal command block must begin with:

1. `cl`, to clear the screen;
2. `cd "<working-directory>"`, to establish the explicit execution context;
3. only then, the commands to run.

Stop and wait only when the output is genuinely needed to choose the next step.

## Useful when

- debugging;
- Git workflows;
- migrations;
- installs;
- CI failures;
- file operations;
- repository maintenance;
- anything potentially destructive or context-dependent.

## Benefit

The user always knows where commands must run, receives fewer ambiguous command dumps, and is not forced through pointless checkpoints.
