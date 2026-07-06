---
name: fix-or-update-github-actions-workflow
description: Workflow command scaffold for fix-or-update-github-actions-workflow in qiandao.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /fix-or-update-github-actions-workflow

Use this workflow when working on **fix-or-update-github-actions-workflow** in `qiandao`.

## Goal

Fixes or updates GitHub Actions workflow files to improve CI/CD pipelines.

## Common Files

- `.github/workflows/*.yml`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Edit .github/workflows/*.yml files to fix or update workflow logic
- Commit changes with a message referencing the workflow

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.