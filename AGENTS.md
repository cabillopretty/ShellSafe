# ShellSafe Project Instructions

## Project context
ShellSafe is an IoT-based coastal water monitoring system intended to identify environmental conditions associated with possible harmful algal blooms (HABs). It combines sensor data collection, monitoring, risk analysis, historical trends, and authorized alerts.

## Core domain
- Monitor water temperature, pH, salinity, turbidity, and any additional parameters that are explicitly implemented in the current codebase.
- Support device health monitoring where implemented, such as battery level and connectivity.
- Treat predictions as early-warning indicators, not proof of toxins or a confirmed toxic species.
- Laboratory testing and authorized environmental agencies remain necessary for confirmation.

## Working rules
1. Inspect the repository and existing patterns before editing.
2. Do not invent routes, tables, environment variables, sensors, or dependencies. Verify them in code first.
3. Keep changes focused and compatible with the current stack.
4. Do not commit secrets, API keys, credentials, private phone numbers, or production data.
5. Validate inputs and handle missing, stale, or out-of-range sensor readings explicitly.
6. Keep alert generation explainable: report the readings/rules that contributed to the risk level.
7. Do not change thresholds or prediction logic without documenting the reason and impact.
8. Do not describe an HAB risk prediction as a confirmed toxic bloom.
9. Add or update tests when changing data processing, risk classification, alerts, or database operations.
10. Before finishing, summarize changed files, checks performed, and any remaining risks.

## Git workflow
- Work on a feature branch, not directly on `main`.
- Review `git status` and `git diff` before committing.
- Never discard user changes or run destructive Git commands without explicit confirmation.
- Use clear, scoped commit messages.

## Suggested verification
Use the repository's existing scripts and test commands. If none are documented, inspect `package.json`, requirements files, or project configuration first rather than guessing.
