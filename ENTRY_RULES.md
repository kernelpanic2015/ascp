# Entry Rules — ASCP v0.1

These are the **minimum requirements** for a project to be considered for inclusion in the ASCP public registry.

This is version 0.1. Rules will evolve with community feedback and real usage.

## 1. License

- The repository **must** use a recognized open source license (OSI-approved preferred).
- The license must be clearly declared (LICENSE file or equivalent).
- Proprietary, source-available with strong restrictions, or unclear licenses are not accepted.

## 2. Public and Active Repository

- The repository must be public on GitHub (or equivalent public forge).
- There should be recent activity (commits, issues, or pull requests) that indicates the project is not abandoned.
- Empty or placeholder repositories are not accepted.

## 3. ASCP Manifest

- The project must contain a valid `ascp/manifest.json` (or the path declared by the protocol) that follows the current schema.
- The manifest must include at least the required fields defined in [SCHEMA.md](./SCHEMA.md).

## 4. Jobs Quality

- At least one well-formed job must be published.
- Jobs must follow the job schema (clear title, description, acceptance criteria, etc.).
- Extremely vague or “do everything” jobs will lower the project score and may block inclusion.

## 5. Intent and Honesty

- The project must genuinely want structured agent contributions.
- Misleading descriptions, spam-like behavior, or attempts to game the registry will result in exclusion.

## 6. Scoring (preview)

Projects receive a simple score based on:

- License clarity
- Manifest completeness
- Job quality and completeness
- Repository activity
- Basic security signals (no obvious secrets, reasonable structure)

In future versions:
- A pre-check skill/prompt will give maintainers an estimated score and recommendations before formal submission.
- Only projects reaching a defined threshold will be listed (or will enter a review queue).

## 7. Badge

Once accepted, projects are encouraged to display the ASCP Participant badge in their README.

## Appeals and Changes

Rules can be improved. Suggestions should be opened as jobs or issues in this repository following the ASCP process itself.
