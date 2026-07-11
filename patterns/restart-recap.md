# Pattern: Restart-friendly recap

## Problem

Long AI conversations can become slow, noisy, or difficult to resume in a fresh chat.

A generic summary is not enough for operational work because it often loses repository state, completed actions, constraints, and warnings about what must not be repeated.

## Instruction pattern

Reserve a short explicit trigger such as `+recap`.

When the user invokes it, generate a complete prompt that can be pasted into a new conversation and includes:

- concise recap and current state;
- next objective;
- active constraints;
- repository, branch, pull request, and CI state when relevant;
- work already completed;
- actions that must not be repeated;
- concrete next steps in dependency order;
- useful commands;
- risks, blockers, and missing information.

The resulting prompt must be self-contained and immediately actionable.

## Benefit

The user can restart the conversation without reconstructing the project manually or accidentally repeating completed work.
