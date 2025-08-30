# Pull Request Guidelines

Pull requests (PRs) are the primary way to propose, review, and merge code changes. Following these guidelines ensures smooth collaboration and consistent quality.

## Creating a Pull Request

1. **Update your branch**  
   - Rebase or merge the latest `develop` (or target branch).
2. **Push your changes**  
   - Ensure all commits follow our [Commit Guidelines](02-commit-guidelines.md).
3. **Open a PR with:**  
   - A clear title using the same convention as commits (`type: short summary`).
   - A meaningful description explaining:
     - *What* changes were made
     - *Why* they were needed
     - Any relevant context or screenshots
   - Links to related issue(s) (`Closes #123`).

## When to Create a Draft PR

- If your work is **in progress** and you want early feedback.
- To share work with teammates before final polish.

## PR Checklist

- [ ] Code builds and passes CI/CD checks  
- [ ] Tests added or updated where applicable  
- [ ] Documentation updated if needed  
- [ ] No large, unrelated changes  
- [ ] Follows coding and commit conventions  

## Review and Merge Strategy

- At least **one approval** is required for merging into `develop`.
- At least **two approvals** are required for merging into `main`.
- Use **squash merge** for small, linear history unless multiple commits are meaningful.
- Avoid merging PRs with unresolved review comments or failing checks.

## Best Practices

- Keep PRs small and focused – large PRs delay reviews.
- Avoid mixing refactoring with new features unless necessary.
- Add clear test cases for your changes.

---

## Pull Request Template Example

```markdown
### Summary
<!-- Briefly describe the purpose of this PR -->

### Related Issues
<!-- Link to any related issues or tickets, e.g., Closes #123 -->

### Changes
<!-- List key changes made in this PR -->
- Added ...
- Updated ...
- Removed ...

### Testing Instructions
<!-- Describe how to test these changes -->

### Screenshots (if applicable)

### Checklist
- [ ] Code builds without errors
- [ ] Tests added/updated
- [ ] Documentation updated
- [ ] Follows [Commit Guidelines](02-commit-guidelines.md)
- [ ] No unrelated changes included
```