---
name: update-version-and-changelog
description: Workflow command scaffold for update-version-and-changelog in qiandao.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /update-version-and-changelog

Use this workflow when working on **update-version-and-changelog** in `qiandao`.

## Goal

Updates the version number and changelog to reflect new releases or changes.

## Common Files

- `version.json`
- `CHANGELOG.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update version.json with new version number
- Edit CHANGELOG.md to document changes

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.