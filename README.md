# Release Flow Demo Repository

## Purpose

This repository demonstrates Release Flow using a small Python FastAPI task management application.

## Application Scope

Initial version `v1.0.0` contains:

- task creation through REST API
- task completion through REST API
- listing all tasks
- listing open tasks
- SQLite database persistence
- version output
- automated tests
- CI workflow

Feature branches, release maintenance, hotfix branches, and merge-back scenarios will be added later.

## Branching Strategy

Release Flow keeps active development on `main` and creates release branches for stable versions. Production fixes are handled on hotfix branches based on a release branch, then merged back into the maintained release line and into `main`.

## Branch Overview

Current initial setup:

- `main`
- `release/1.0`

Planned later:

- `release/1.1`
- `feature/add-task-priority`
- `feature/add-due-date`
- `feature/add-user-service`
- `feature/add-task-assignment`
- `feature/add-task-status`
- `bugfix/fix-task-completion`
- `hotfix/fix-production-task-bug`

## Release Flow

The planned release path is:

```text
feature branch -> main -> release branch -> version tag
```

The planned hotfix path is:

```text
release/1.0 -> hotfix branch -> release/1.0 -> tag patch release -> main
```

The initial version starts with `main` and `release/1.0` pointing to the same `v1.0.0` commit.

## CI Setup

The CI workflow runs on `push` and `pull_request`.

It installs Python dependencies and runs the test suite with `python -m pytest`.

## Tags / Releases

- `v1.0.0`: initial base application

