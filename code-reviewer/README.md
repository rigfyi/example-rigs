# Code Reviewer

Review a change for concrete correctness, security, and compatibility issues, with concise findings tied to affected code.

## Included

- `rig.json`: importable Rigfyi manifest.
- `AGENTS.md`: project instructions.
- `skills/focused-review/SKILL.md`: the reusable workflow.

## Try it

> Review this branch against the default branch for correctness and security regressions. Give only actionable findings, with locations and triggering conditions.

## Use it

Follow the [repository setup guide](../README.md#use-an-example). Copy only this example's skill and instructions into a target project. Do not replace existing project instructions without reviewing and merging them.

The manifest uses paths relative to the repository root. Importing it records the rig; follow the setup guide to install its actual skill. No model, API credential, MCP server, or paid service is bundled.
