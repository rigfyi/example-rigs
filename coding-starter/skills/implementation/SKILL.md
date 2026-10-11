---
name: implementation
description: Use when implementing a feature or fixing a reproducible bug in an existing codebase.
---

# Implementation workflow

1. Restate the desired behavior and identify the smallest observable success condition.
2. Read repository instructions and the relevant caller, implementation, and tests. Trace inputs, state changes, outputs, and failure paths before editing.
3. Reuse existing behavior or extend the helper that owns the invariant. Prefer the standard library or installed dependencies over new infrastructure.
4. For a bug, reproduce it and isolate the cause. For a feature, preserve compatibility and validate input at trust boundaries.
5. Make one coherent change. Preserve authorization, error handling, accessibility, and concurrency safeguards.
6. Run the smallest meaningful check that distinguishes the intended behavior from the old behavior. Use the repository's test, lint, and build commands where appropriate.
7. Review the diff for unrelated edits and accidental secrets. Report the outcome, verification, and any remaining limitation.

## Completion criteria

The requested behavior works, relevant checks pass, and the surrounding behavior remains intact. Never claim a command passed if it was not run.
