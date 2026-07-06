```markdown
# qiandao Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches you the core development patterns and workflows used in the `qiandao` Python codebase. You'll learn the project's coding conventions, how to manage releases, update dependencies, maintain documentation, handle frontend and backend updates, and fix bugs efficiently. The guide also covers the structure of tests and provides quick commands for common tasks.

## Coding Conventions

- **File Naming:**  
  Use camelCase for file names.
  ```
  # Example
  userHandler.py
  versionManager.py
  ```

- **Import Style:**  
  Use relative imports within modules.
  ```python
  from .utils import parseConfig
  from .models import User
  ```

- **Export Style:**  
  Use default exports (i.e., no explicit `__all__` unless needed).
  ```python
  # At the end of a module
  # No need for explicit export lists
  ```

- **Commit Messages:**  
  - Freeform style, sometimes with a `chore` prefix.
  - Keep messages concise (~27 characters on average).
  ```
  chore: update dependencies
  fix: correct login handler bug
  ```

## Workflows

### Update Version and Changelog
**Trigger:** When preparing a new release or documenting recent changes  
**Command:** `/update-version`

1. Update `version.json` with the new version number.
2. Edit `CHANGELOG.md` to document the changes.
3. Commit your changes.
   ```
   chore: bump version to 1.2.3
   ```

### Fix or Update GitHub Actions Workflow
**Trigger:** When CI/CD workflow needs fixing or updating  
**Command:** `/fix-ci`

1. Edit `.github/workflows/*.yml` files to fix or update workflow logic.
2. Commit changes with a message referencing the workflow.
   ```
   chore: fix CI workflow for Python 3.11
   ```

### Update Requirements or Pipfile
**Trigger:** When dependencies need to be added, removed, or updated  
**Command:** `/update-deps`

1. Edit `requirements.txt` and/or `Pipfile` and `Pipfile.lock`.
2. Commit changes with a message referencing the dependency update.
   ```
   chore: update requests to 2.28.0
   ```

### Update or Fix Documentation
**Trigger:** When documentation needs to be added, updated, or fixed  
**Command:** `/update-docs`

1. Edit Markdown files under `web/docs/guide/` and `web/docs/zh_CN/guide/`.
2. Edit `.vitepress` config or locale files if navigation or localization is affected.
3. Commit changes with a message referencing the documentation update.
   ```
   chore: update zh_CN user guide
   ```

### Frontend JS Component Update
**Trigger:** When frontend dependencies or JS components need updating  
**Command:** `/update-frontend`

1. Edit `web/package.json` and/or `web/pnpm-lock.yaml`.
2. Update files under `web/static/components/` or `web/static/har/`.
3. Commit changes with a message referencing the frontend update.
   ```
   chore: update har parser component
   ```

### Fix Bug in Backend or Template
**Trigger:** When a bug is reported or discovered in backend or template logic  
**Command:** `/fix-bug`

1. Edit `web/handlers/*.py` or `web/tpl/*.html` files to fix the bug.
2. Commit changes with a message referencing the bug or issue number.
   ```
   fix: handle NoneType in login handler
   ```

## Testing Patterns

- **Framework:** Unknown (not explicitly detected).
- **File Pattern:** Test files are named with the pattern `*.test.*`.
  ```
  # Example test file
  userHandler.test.py
  ```
- **Location:** Test files are typically placed alongside the code they test or in a dedicated test directory.

## Commands

| Command           | Purpose                                               |
|-------------------|-------------------------------------------------------|
| /update-version   | Update version number and changelog for a new release |
| /fix-ci           | Fix or update GitHub Actions workflows                |
| /update-deps      | Update Python dependencies                            |
| /update-docs      | Update or fix documentation files                     |
| /update-frontend  | Update frontend JS components and dependencies        |
| /fix-bug          | Fix bugs in backend Python or HTML template files     |
```