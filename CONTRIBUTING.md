# Contributing to IntelliZen

We use [GitHub Flow](https://docs.github.com/en/get-started/quickstart/github-flow) for development. This means:

1.  **`main` Branch:** The `main` branch is always considered production-ready and deployable. Direct pushes to `main` are blocked.
2.  **Feature/Bugfix Branches:** All new work (features, bug fixes, chores) must be done on separate branches created from `main`.
    *   Use naming conventions like `feature/<short-description>`, `bugfix/<issue-number>-<short-description>`, `chore/<description>`.
    *   Example: `feature/user-login`, `bugfix/123-fix-profile-update`, `chore/setup-husky`
3.  **Commits:** Please use [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) for commit messages (e.g., `feat: add user login page`, `fix: correct calculation error`, `chore: update dependencies`). This helps automate release notes and versioning.
4.  **Pull Requests (PRs):**
    *   When your work is ready, push your branch to GitHub and open a Pull Request targeting the `main` branch.
    *   Ensure your PR has a clear title and description explaining the changes.
    *   Link any relevant issues.
    *   PRs must pass all automated checks (linting, testing, building) defined in the CI pipeline (GitHub Actions).
    *   PRs require at least one approving review from another team member before merging.
5.  **Merging:** Once approved and all checks pass, PRs should be merged into `main` using the **Squash and Merge** option on GitHub. This keeps the `main` branch history clean.
6.  **Keeping Branches Updated:** Before opening a PR or after significant changes to `main`, update your feature branch by rebasing onto the latest `main`:
    ```bash
    git checkout main
    git pull origin main
    git checkout your-feature-branch
    git rebase main
    # Resolve any conflicts and push your branch (potentially with --force-with-lease)
    ```

Thank you for contributing!
