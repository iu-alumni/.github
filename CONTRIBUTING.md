# Contributing to IU Alumni

Thank you for your interest in contributing! Please read this guide before opening issues or pull requests.

---

## Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [Reporting Bugs](#reporting-bugs)
3. [Suggesting Features](#suggesting-features)
4. [Opening a Pull Request](#opening-a-pull-request)
5. [Branch Naming](#branch-naming)
6. [Commit Messages](#commit-messages)
7. [Code Style](#code-style)
8. [Testing](#testing)
9. [Review Process](#review-process)
10. [Contact](#contact)

---

## Code of Conduct

All participants must follow our [Code of Conduct](CODE_OF_CONDUCT.md). Be respectful, constructive, and inclusive.

---

## Reporting Bugs

1. Search existing issues to avoid duplicates.
2. Open an issue using the **Bug Report** template.
3. Include: steps to reproduce, expected vs actual behavior, screenshots or logs, OS and dependency versions.

---

## Suggesting Features

1. Open an issue using the **Feature Request** template.
2. Describe the problem you are solving, not just the solution.
3. Include use cases and any relevant context.

---

## Opening a Pull Request

```bash
# 1. Fork the repo and clone your fork
git clone https://github.com/<your-username>/<repo>.git

# 2. Create a branch
git checkout -b feat/your-feature-name

# 3. Make your changes, commit, and push
git push origin feat/your-feature-name

# 4. Open a PR against main
```

In your PR description:
- Summarize **what** changed and **why**
- Link related issues with `Closes #<number>`
- Describe how to verify the change

---

## Branch Naming

| Prefix | Use for |
|--------|---------|
| `feat/` | New features |
| `fix/` | Bug fixes |
| `docs/` | Documentation only |
| `chore/` | Maintenance, dependencies |
| `hotfix/` | Urgent production fixes |

---

## Commit Messages

Follow [Conventional Commits](https://www.conventionalcommits.org/):

```
feat: add alumni event RSVP endpoint
fix: correct token expiry calculation
docs: update setup instructions
chore: bump fastapi to 0.110
```

---

## Code Style

| Language | Tool |
|----------|------|
| Python | Black + isort + Ruff |
| TypeScript / Vue | ESLint + Prettier |
| Dart / Flutter | `dart format` + `flutter analyze` |

Run formatters and linters before pushing. CI will enforce them.

---

## Testing

- Write unit or integration tests for all non-trivial changes.
- Ensure existing tests pass before opening a PR.
- Refer to each repo's README for the specific test commands.

---

## Review Process

- CI (lint + tests) runs automatically on every PR.
- At least one approving review is required before merge.
- Address all review comments; mark resolved threads as resolved.
- Squash or rebase before merging to keep a clean history.

---

## Contact

- **Telegram:** [t.me/+8hrAOuObPXQzZGRi](https://t.me/+8hrAOuObPXQzZGRi)
- **Questions:** open an issue labeled `question`
