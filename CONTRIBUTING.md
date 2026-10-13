# Contributing to Proyecto_DAMN

This repository follows a strict review flow: **nothing reaches `develop` or `main` without the Scrum Master's approval** (Dani, @DaniRZ10).

## Branches

| Branch | Purpose | Who writes to it |
| --- | --- | --- |
| `main` | Stable, deliverable version | Nobody directly. Only via PR from `develop`, opened and merged by Dani |
| `develop` | Sprint integration | Nobody directly. Only via approved PR |
| `feature/<issue>-<short-name>` | One task from the board (e.g. `feature/12-login-form`) | The assignee |
| `release/<version>` | Preparing a delivery from `develop` | Dani |
| `hotfix/<short-name>` | Urgent fix on `main` | Whoever fixes it, same review flow |

`main` and `develop` are protected: pull request required, Code Owner approval required, force pushes and deletion blocked. An approval is dismissed if new commits are pushed afterwards.

## Workflow

1. Pick a card assigned to you on the GitHub Projects board.
2. Create your branch from an up-to-date `develop`.
3. Commit locally, in English, following [Conventional Commits](https://www.conventionalcommits.org/) (`feat:`, `fix:`, `docs:`, `refactor:`, `test:`, `chore:`).
4. Generate the diff against `develop` and send it to Dani privately.
5. Wait for Dani's OK. If he asks for changes, fix them on the same branch and send the diff again.
6. With the OK, push the branch and open a PR against `develop` using the template.
7. Dani approves and merges. Do not merge PRs yourself.

```bash
# 1. Start from an up-to-date develop
git switch develop
git pull
git switch -c feature/12-login-form

# 2. Work and commit
git add .
git commit -m "feat: add login form"

# 3. Generate the diff and send it to Dani privately
git fetch origin
git diff origin/develop...HEAD > feature-12-login-form.diff

# 4. Only after Dani's OK: push the branch, then open the PR on GitHub
git push -u origin feature/12-login-form
```

## Rules

- Never push to `main` or `develop`.
- Never open a PR against `main`.
- Keep PRs small: one card, one branch, one PR.
- Never commit secrets, `.env` files or credentials.
- Code, comments, commits, branches, issues and docs are in English. Only the team contract is in Spanish.
- Move your card to **Review** when the PR is open; it goes to **Done** only after the merge (see the Definition of Done in [docs/team/README.md](docs/team/README.md)).
