# Hotfix and Bugfix Workflow

This workflow ensures that critical issues and urgent defects in production are resolved quickly, without disrupting ongoing development activities. It provides a structured approach to managing both urgent hotfixes (critical production issues) and non-critical bugfixes (regular defects identified during development or testing).

---

## Workflow Overview

```mermaid
graph TD
    A[Identify Critical Bug] --> B[Create hotfix/<issue-number> branch from main]
    B --> C[Implement fix]
    C --> D[Write tests and verify fix]
    D --> E[Create Pull Request to main and develop]
    E --> F[Code Review and Approval]
    F --> G[Merge to main (hotfix release)]
    G --> H[Tag Release e.g., v1.2.1]
    H --> I[Merge back to develop]
```

---

## Steps

1. **Identify Issue**
   - Confirm severity and urgency with the team.

2. **Branching**
   - Branch from the latest `main`:
     ```bash
     git checkout main
     git pull origin main
     git checkout -b hotfix/<issue-number>
     ```

3. **Implement and Test Fix**
   - Commit using the following format:
     ```
     fix: resolve <short description of issue>
     ```

4. **Pull Request**
   - Open a PR targeting both `main` and `develop`.

5. **Code Review**
   - Must pass review and testing before merge.

6. **Release and Tag**
   - After merging into `main`, create a patch release:
     ```bash
     git tag -a v1.2.1 -m "Hotfix: <issue description>"
     git push origin v1.2.1
     ```

7. **Merge Back**
   - Merge the hotfix changes into `develop` to keep branches in sync.

---

## Best Practices

- Keep hotfix branches focused on the urgent issue.
- Avoid introducing new features in a hotfix.
- Always test in a staging environment before tagging.
- Communicate with the team about hotfix impact.
