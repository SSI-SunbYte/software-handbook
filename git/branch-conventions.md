# Branching Guidelines

This document outlines the branching conventions used by the SunbYte Software Team.

## 1. Branching Strategy

We use a lightweight feature-branch workflow.

The `main` branch contains the latest approved changes. All contributions should be developed on a separate branch and merged into `main` through a pull request.

**Do not commit directly to `main`.**

## 2. Branch Naming

Branches should follow this format:

`<type>/<short-description>`

Use lowercase letters and hyphens to separate words.

| Prefix | Purpose |
| --- | --- |
| `feat/` | New functionality |
| `fix/` | Bug fixes |
| `docs/` | Documentation changes |
| `refactor/` | Code restructuring |
| `test/` | Adding or modifying tests |
| `chore/` | General maintenance |

**Examples:**

- `feat/solar-tracking`
- `fix/camera-offset`
- `docs/branching-guidelines`
- `refactor/image-processing`

## 3. Creating a Branch

Before starting work, ensure your local `main` branch is up to date.

```bash
git switch main
git pull --ff-only
git switch -c docs/update-guidelines
```

Make your changes and commit them following our [Commit Guidelines](commit-conventions.md).

Push your branch to GitHub:

```bash
git push -u origin docs/update-guidelines
```

## 4. Pull Requests

Once your changes are ready:

1. Open a pull request targeting `main`.
2. Provide a clear title and description of your changes.
3. Request a review from the software team lead.
4. Address any feedback before merging.

Only authorised maintainers may merge pull requests into `main`.

## 5. Cleaning Up

After your pull request has been merged, delete the feature branch on GitHub.

You can also remove the local branch:

```bash
git switch main
git pull --ff-only
git branch -d docs/update-guidelines
```

---

These conventions apply to all SunbYte software repositories unless otherwise specified.
