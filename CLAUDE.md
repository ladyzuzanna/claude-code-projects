# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Git & GitHub Workflow

Every project in this repo uses Git for version control with changes pushed to GitHub after every meaningful unit of work.

### Setup (first time in a new project directory)
```bash
git init
gh repo create <repo-name> --public --source=. --remote=origin --push
```

### Commit conventions
- Commit after every meaningful, self-contained change (new feature, bug fix, config change, etc.)
- Message format: imperative mood, present tense, no period at end
  - `Add login form validation`
  - `Fix off-by-one error in pagination`
  - `Update API endpoint for user profile`
- Always push to GitHub after committing: `git push origin main`

### Typical workflow
```bash
git add <specific-files>          # stage only relevant files, never git add -A blindly
git commit -m "Descriptive message"
git push origin main
```

### Branching
- `main` is the stable branch — always kept in a working state
- Use feature branches for larger changes: `git checkout -b feature/name`
- Merge via PR on GitHub when the feature is complete
