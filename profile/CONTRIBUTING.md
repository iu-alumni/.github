# Contributing Guide (CONTRIBUTING.md)

Thank you for your interest in contributing to the IU Alumni projects! We welcome ideas, fixes, and improvements. Please follow these guidelines to streamline the review process.

---

## Table of Contents

1. [Code of Conduct](#code-of-conduct)
2. [How to File an Issue](#how-to-file-an-issue)
3. [How to Create a Pull Request](#how-to-create-a-pull-request)
4. [Setting Up Your Environment](#setting-up-your-environment)
5. [Husky and Git Hooks](#husky-and-git-hooks)
6. [Code Style and Commits](#code-style-and-commits)
7. [Writing and Running Tests](#writing-and-running-tests)
8. [Review Process](#review-process)
9. [Contact and Support](#contact-and-support)

---

## Code of Conduct

Please review our [CODE\_OF\_CONDUCT.md](https://github.com/iu-alumni/.github/blob/main/CODE_OF_CONDUCT.md). All contributors are expected to abide by our standards of respectful and inclusive behavior.

---

## How to File an Issue

1. Ensure a similar issue does not already exist by searching the Issues tab (in respective repo)
2. Clearly describe the goal and expected behavior.
3. Provide reproduction steps, logs, or screenshots.
4. Specify the project version and your environment (OS, dependency versions).

Use the issue template to make sure all details are included.

---

## How to Create a Pull Request

1. Fork the target repository and create a new branch following the pattern:

   ```bash
   git checkout -b feature/your-branch-name
   ```
2. Make your changes, adhering to the [Code Style and Commits](#code-style-and-commits) guidelines.
3. Update or add tests if applicable.
4. Test locally:

   ```bash
   uvicorn app.main:app --reload
   ```
5. Sync with `main` and resolve conflicts:

   ```bash
   git fetch upstream
   git rebase upstream/main
   ```
6. Push your branch to your fork and open a PR against the organization repository.
7. In your PR description, include:

   * What you’ve done and why.
   * How to verify your changes.
   * Links to any related issues.

---

## Setting Up Your Environment

- [Instructions for the Backend repo](https://github.com/iu-alumni/iu-alumni-backend/blob/main/README.md)
- [Instructions for the Frontend repo](https://github.com/iu-alumni/iu-alumni-frontend/blob/main/README.md)
- [Instructions for the Mobile repo](https://github.com/iu-alumni/iu-alumni-mobile/blob/main/README.md)

---

## Husky and Git Hooks

We use [Husky](https://typicode.github.io/husky/) to manage Git hooks and automatically run tasks before commits and pushes:

1. Install dependencies:

   ```bash
   npm install husky lint-staged --save-dev
   ```
2. Add to your `package.json`:

   ```json
   {
     "scripts": {
       "prepare": "husky install"
     },
     "husky": {
       "hooks": {
         "pre-commit": "lint-staged",
         "pre-push": "npm test"
       }
     },
     "lint-staged": {
       "*.{js,ts,jsx,tsx}": [
         "eslint --fix",
         "git add"
       ],
       "*.py": [
         "black",
         "isort",
         "git add"
       ]
     }
   }
   ```
3. Enable Husky hooks:

   ```bash
   npm run prepare
   ```
4. To add new hooks:

   ```bash
   npx husky add .husky/pre-commit "npm run lint"
   npx husky add .husky/pre-push "npm test"
   ```

More details in the respective repositories and their README.md files.

---

## Code Style and Commits

* **Code:** Follow [PEP 8](https://www.python.org/dev/peps/pep-0008/) for Python and the official Vue/Dart style guides for frontend and mobile.
* **Branch Naming:** Use `feature/`, `bugfix/`, or `hotfix/` prefixes.
* **Commits:** Follow the [Conventional Commits specification](https://www.conventionalcommits.org/):

  ```
  feat: short description of the new feature
  fix: bug fix
  docs: documentation changes
  chore: maintenance tasks
  ```
* Write clear and descriptive commit messages.

---

## Writing and Running Tests

1. Cover your code with unit or integration tests.
2. Run tests:

   ```bash
   # example for backend
   pytest --cov=app
   ```
3. Ensure test coverage does not decrease.

---

## Review Process

* After opening a PR, CI checks (lint, tests) will run automatically.
* Assign reviewers using the GitHub UI.
* Address feedback and iterate as needed.
* Once approved, merge your PR into `dev`.

---

## Contact and Support

* For organization-wide questions, use [Discussions](https://github.com/iu-alumni/…/discussions).
* In urgent cases, reach out on Telegram: [t.me/+8hrAOuObPXQzZGRi](https://t.me/+8hrAOuObPXQzZGRi).
* For other queries, open an issue labeled `question`.
