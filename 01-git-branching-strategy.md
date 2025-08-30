# Git Branching Strategy

We follow a modified Git Flow approach to ensure efficient collaboration.

## Branch Types

- **main** – Production-ready code.
- **develop** – Active development branch.
- **feature/*** – For new features or enhancements.
- **hotfix/*** – For urgent production fixes.
- **bugfix/*** – For non-urgent bug fixes.
- **release/*** – For preparing a new production release.

## Workflow

1. Create a feature branch from `develop`:
   ```bash
   git checkout develop
   git checkout -b feature/feature-name
   ```
2. Work on the feature and commit changes.
3. Create a pull request (PR) to merge into `develop`.
4. After approval, merge into `develop`.
5. When ready for production, create a release branch and merge it into both `main` and `develop`.

