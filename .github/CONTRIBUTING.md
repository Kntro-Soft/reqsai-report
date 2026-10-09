# Contributing Guide — Kntro-Soft / Report

Thank you for contributing to the **Reqs-AI** project report. This guide describes the workflow agreed upon by the team to keep the repository organized and the commit history clean.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Branch Structure](#branch-structure)
- [Commit Convention](#commit-convention)
- [Workflow](#workflow)
- [Pull Requests](#pull-requests)
- [Updating the CHANGELOG](#updating-the-changelog)

---

## Prerequisites

- Git installed and configured with your UPC name and email
- Access to the `Kntro-Soft/ReqsAI-Report` repository on GitHub
- A Markdown-compatible editor (VS Code, IntelliJ, etc.)

---

## Branch Structure

| Branch                   | Purpose                                                                   |
|--------------------------|---------------------------------------------------------------------------|
| `main`                   | Final deliverable version. Only merged from `develop` with team approval. |
| `develop`                | Integration branch. All features are merged here first.                   |
| `feature/<issue>-<slug>` | New section, diagram, or new content.                                     |
| `bugfix/<issue>-<slug>`  | Fix for typos, broken links, or incorrect data.                           |

Every branch starts from an issue on the [ReqsAI project board](https://github.com/orgs/Kntro-Soft/projects/3)
(status Backlog → Ready → In Progress → In Review → Testing → Done).

**Branch name examples:**
```
feature/76-context-mapping-acl-patterns
feature/77-c4-container-diagram
bugfix/78-broken-image-backlog
```

`main` and `develop` are protected by rulesets: pull request with 1 approval (stale approvals are dismissed),
the **Lint Markdown files** check must pass, no force-push or deletion, merge commits only. The link check
(*Verify image and markdown links*) still runs on every pull request but is not required, because external sites
can fail independently of the change.

---

## Commit Convention

We follow [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/):

```
<type>(<scope>): <short description in lowercase>
```

| Type       | When to use                                                     |
|------------|-----------------------------------------------------------------|
| `feat`     | New section or new content added                                |
| `fix`      | Correction of errors in the report                              |
| `docs`     | Changes to README, CHANGELOG, or other repo documentation files |
| `refactor` | Reorganization of sections without content change               |
| `chore`    | Changes to assets, images, `.gitignore`                         |
| `style`    | Markdown formatting changes (spacing, tables, headings)         |

**Examples:**
```
feat(ch4): add context mapping ACL pattern toward Jira with detailed contract
fix(ch2): correct competitor names in comparison table
docs(changelog): record changes for version 2.1
chore(assets): replace C4 container diagram with updated version
```

---

## Workflow

```
1. Create a branch from develop
   git checkout develop
   git pull origin develop
   git checkout -b feature/76-my-section

2. Make changes to the report (README.md or assets/)

3. Commit following the convention
   git add .
   git commit -m "feat(ch4): description of the change"

4. Update CHANGELOG.md with the change made

5. Push and open a Pull Request targeting develop with "Closes #<issue>"
   git push origin feature/76-my-section
```

---

## Pull Requests

- Every PR must target `develop`, never directly `main`
- At least **1 approval** is required before merging
- The PR author fills out the `PULL_REQUEST_TEMPLATE.md` honestly
- Reviews must be completed within a maximum of **48 hours**
- Do not self-merge without another member's approval
- The PR description says `Closes #<issue>`, so merging closes the issue and links both on the board

Traceability: Issue → `feature/<issue>-<slug>` → commits → PR (`Closes #<issue>`) → `develop` → `main`.
This repository has no deployment channel: `generate-pdf.yml` only builds the PDF, Word and ZIP files as
workflow artifacts of each push to `main`, so it has no environment, approval or deploy switch.

Merges from `develop` to `main` are performed at the end of each deliverable (TB1, TP1, TB2, TF) and require approval from all active team members.

---

## Updating the CHANGELOG

Every time report content is modified, update `CHANGELOG.md` at the root of the repository following the [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) format:

```markdown
## [X.Y] - YYYY-MM-DD
### Added
- New section added

### Changed
- Description of what was modified

### Fixed
- Correction made
```
