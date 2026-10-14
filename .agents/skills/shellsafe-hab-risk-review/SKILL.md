---
name: shellsafe-hab-risk-review
description: Review or implement ShellSafe's potential harmful algal bloom risk analysis, prediction explanations, and alert triggering. Use when changing model inputs, risk categories, threshold rules, prediction outputs, or alert logic.
---

# ShellSafe HAB Risk Review Skill

## Workflow
1. Locate the current risk-analysis implementation, model files, thresholds, and tests.
2. Identify the exact sensor fields used by the model/rules and verify their units.
3. Trace each risk result to the input readings and relevant model/rule output.
4. Preserve existing risk categories unless a requirements change is approved.
5. Check missing, stale, or invalid readings and ensure they cannot silently produce a normal-risk result.
6. Ensure alerts contain a timestamp, risk level, triggering reason, and source device/reading where supported by the current schema.
7. Test normal, borderline, high-risk, missing-data, and stale-data scenarios.
8. Clearly state that a risk result is an early warning and not proof of toxin presence or a confirmed toxic species.

## Safety rules
- Never claim toxin detection unless a validated toxin measurement feature exists.
- Do not change thresholds merely to make tests pass.
- Avoid sending alerts to users or groups not authorized by the current requirements.
- Document limitations and recommend laboratory verification for confirmation.
