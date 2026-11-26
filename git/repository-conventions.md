# Repository Conventions

Consistent repository names make the organisation easier to navigate, search and link to. Anyone should be able to guess roughly what a repo contains from its name alone.

These conventions apply to all new repositories in `SSI-SunbYte`. Existing repositories are being renamed to match (see [Renaming an existing repository](#renaming-an-existing-repository)).

## Format

```
<scope>-<short-description>
```

- **Lowercase only.** Write SunbYte as `sunbyte` in repo names; the stylised capital Y belongs in the README title and repo description.
- **Hyphens between words.** No spaces, underscores, camelCase or PascalCase.
- **Keep it short.** Aim for two to four words after the scope.
- **Describe what it is, not its status.** Avoid words like `initial`, `new`, `old`, `final` or `test`. Status goes in the README, and finished or abandoned repos get archived.
- **Spell out unclear abbreviations.** Well-known ones like `ros`, `sbc` and `opencv` are fine.

## Scopes

| Scope | Use for | Example |
| ------- | --------- | --------- |
| `sol-` | SOL education programme material (workshops, activity guides) | `sol-electrical-thermal` |
| `sunbyte<n>-` | Codebases tied to one SunbYte iteration, using the iteration number in digits | `sunbyte5-core` |
| `<subsystem>-` | Code for a specific subsystem | `tracking-ros-prototype` |
| `pcb-` | Hardware files from KiCAD | `pcb-motor-board` |
| *(none)* | Org-wide tooling and documentation | `software-handbook` |

If a repo doesn't fit any scope, ask the software team lead (Liam Pallett) before creating it rather than inventing a new one.

### Prototypes

Exploratory or throwaway work can use a `-prototype` suffix, e.g. `tracking-opencv-prototype`. Once a prototype is superseded, archive it.

## Repository setup

When creating a repository:

1. Name it following the format above.
2. Add a one-line description in the repo settings.
3. Add a README based on the [README template](../documentation/README-template.md).

## Exceptions

Some names are fixed by GitHub and must not be changed:

- `.github` (organisation profile and default community files)
- `ssi-sunbyte.github.io` (GitHub Pages site)

## Renaming an existing repository

GitHub redirects the old URL to the new one after a rename, so existing clones and links keep working. To tidy up afterwards:

```bash
git remote set-url origin https://github.com/SSI-SunbYte/<new-name>.git
```

Never create a new repository with a renamed repo's old name, as this breaks the redirect.
