---
name: update-provider-documentation
description: Workflow command scaffold for update-provider-documentation in kilocode.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-provider-documentation

Use this workflow when working on **update-provider-documentation** in `kilocode`.

## Goal

Updates or adds documentation for a specific AI provider in the documentation site.

## Common Files

- `packages/kilo-docs/pages/ai-providers/*.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit or create the relevant markdown file for the provider under packages/kilo-docs/pages/ai-providers/
- Commit the changes with a docs(kilo-docs): message prefix

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.