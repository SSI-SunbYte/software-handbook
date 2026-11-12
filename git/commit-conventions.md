# Commit Guidelines

This document defines the commit message conventions used by the SunbYte Software Team.

Our goal is to maintain a readable, consistent Git history that makes it easy to understand what changed and why.

## 1. Commit Message Format

We follow the [Conventional Commits](https://www.conventionalcommits.org/en/v1.0.0/) specification.

Each commit message should follow this structure:

`<type>(<optional scope>): <description>`

**Examples:**

- `chore(repo): initialise repository`
- `feat(tracking): implement solar centroid detection`
- `fix(camera): handle missing video frames`
- `docs: add ROS2 installation instructions`
- `test(tracking): add unit tests for centroid calculation`

## 2. Commit Types

| Type | Purpose |
| --- | --- |
| `feat` | Introduces new functionality |
| `fix` | Corrects a bug |
| `docs` | Changes documentation |
| `refactor` | Restructures code without changing its behaviour |
| `test` | Adds or modifies tests |
| `chore` | General maintenance |
| `build` | Changes dependencies or build configuration |
| `ci` | Changes continuous integration configuration |
| `perf` | Improves performance |

## 3. Writing Good Commit Messages

- Use the imperative mood: `add`, not `added` or `adds`.
- Keep the subject concise, ideally within 50 characters.
- Use lowercase for the type and description.
- Do not end the subject with a full stop.
- Describe what changed, not merely that work was completed.
- Include a commit body when the reasoning behind a change needs explaining.

**Avoid:**

- `update`
- `fixed stuff`
- `work done`
- `final version`

**Prefer:**

- `fix(tracking): correct camera offset calculation`
- `feat(vision): add threshold-based sun detection`

## 4. Commit Scope

A scope identifies the subsystem affected by a change.

Examples include `tracking`, `camera`, `vision`, and `ros`.

Scopes are optional and should reflect the actual structure of the project.

## 5. Commit Frequency

Commit regularly, but ensure each commit represents a meaningful, logically related change.

- Prefer small, focused commits over large unrelated changes.
- Avoid combining unrelated fixes and features.
- Ensure code is in a reasonable working state before committing.
- Never commit secrets, credentials, or generated files that should be ignored.

## 6. Breaking Changes

Changes that break existing interfaces or expected behaviour must be clearly identified.

Use `!` after the type or scope:

`feat(api)!: change tracking coordinate format`

Explain the breaking change and any required migration steps in the commit body.

---

These guidelines apply to all SunbYte software repositories. They may evolve as the team's development practices mature.
