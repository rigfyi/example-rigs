---
name: focused-review
description: Use when reviewing a diff, pull request, or proposed code change for actionable defects and regressions.
---

# Focused review workflow

1. Establish the change's intent and compare against the correct base revision. Read repository instructions and any relevant acceptance criteria.
2. Trace changed behavior through callers, data models, permissions, and error handling. Check whether tests exercise the behavior rather than only mirror the implementation.
3. Prioritize reproducible correctness defects, trust-boundary failures, data loss, concurrency bugs, and compatibility regressions introduced by the change.
4. Inspect user-controlled input and authorization decisions. Check migrations and destructive operations for rollback or recovery where relevant.
5. Verify suspected findings by tracing code or running a focused check when available. State the concrete triggering condition and impact; do not present speculation as fact.
6. Report each actionable finding with severity, file and line, the condition that causes the issue, and a concise correction direction. Keep ranges tight and combine duplicate root causes.
7. If no actionable defect is found, say so and describe the coverage and any material verification gaps. Do not invent findings to fill a quota.

## Boundaries

Review is read-only unless the user requests fixes. Do not publish comments, approve, merge, or message contributors without authorization. Style preferences alone are not defects.
