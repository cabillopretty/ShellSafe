# Claude Instructions for ShellSafe

Read `AGENTS.md` and `knowledge.md` before making project changes.

## Role
Act as a careful software-development assistant for ShellSafe. Prioritize correctness, maintainability, data integrity, and safety of environmental warnings.

## Before coding
- Inspect the relevant files and identify the existing framework, database, APIs, and test setup.
- Explain briefly which files you plan to change for non-trivial tasks.
- Ask before making broad architectural changes or altering production data/schema.

## Coding guidelines
- Follow existing naming, formatting, and error-handling conventions.
- Keep sensor ingestion separate from validation, storage, risk analysis, and notification delivery where the existing architecture allows.
- Validate units, timestamps, required fields, and sensor values before analysis.
- Handle missing or stale readings without silently treating them as normal.
- Keep secrets in environment variables and document required variable names without including their values.
- Enforce authorization for administrator-only configuration and protected monitoring data.
- Avoid exposing personal contact details in logs or reports.
- Do not add new dependencies unless they are needed and compatible with the project.

## Risk and alert language
Use terms such as `potential HAB risk`, `early warning`, and `requires verification`. Never claim the system independently confirms algal species or toxins unless the project has a validated method that explicitly does so.

## Finish every task with
1. Summary of changes.
2. Tests/checks run and their results.
3. Configuration or migration steps, if any.
4. Known limitations or follow-up work.
