# Commit Guidelines

Proper commit messages improve project history readability.

## Commit Message Format

Follow the [Conventional Commits](https://www.conventionalcommits.org/) standard:

```
<type>(<scope>): <short description>

[optional body]

[optional footer]
```
- **type** – Describes the purpose of the change (see types below).
- **scope** – *(optional)* Area of the codebase affected (e.g., `auth`, `ui`, `api`).
- **short summary** – Brief, imperative description (max ~72 characters).

### Types

- **feat** – New feature
- **fix** – Bug fix
- **docs** – Documentation only
- **style** – Formatting or styling (no logic changes)
- **refactor** – Code change that neither fixes a bug nor adds a feature
- **test** – Adding or updating tests
- **chore** – Maintenance tasks (e.g., build scripts, dependencies)
- **perf** – Performance improvements
- **ci** – Continuous integration/deployment changes

### Body

- Explain *why* and *what* changed, not just *how*.
- Wrap lines at ~72 characters.

### Footer

- Use to reference issues:  
  `Fixes #123`, `Closes #45`
- Indicate breaking changes:  
  `BREAKING CHANGE: database schema updated`

### Best Practices

1. **One logical change per commit** – Avoid mixing unrelated changes.
2. **Write in imperative mood** – e.g., "add", not "added" or "adds".
3. **Keep commits small and meaningful** – Large commits make reviews harder.


### Examples

```
feat(auth): add JWT-based authentication

fix(api): resolve crash when request payload is empty

refactor(ui): simplify modal component structure

chore: update dependencies to latest stable versions
```

## References
[Conventional Commits](https://www.conventionalcommits.org/)
