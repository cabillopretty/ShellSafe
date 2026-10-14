---
name: shellsafe-sensor-data-validation
description: Validate and safely process ShellSafe coastal water sensor readings before storing or using them for risk analysis. Use when editing sensor ingestion, telemetry APIs, data schemas, sensor normalization, or data-quality checks.
---

# ShellSafe Sensor Data Validation Skill

## Workflow
1. Inspect the existing sensor schema, ingestion endpoint, and units used by the project.
2. Confirm which fields are implemented; do not assume every documented sensor exists in the code.
3. Validate required fields, data types, timestamps, and allowed ranges based on project configuration or cited sensor specifications.
4. Detect missing, malformed, stale, duplicated, or implausible readings.
5. Preserve the original timestamp and device identity for traceability.
6. Return a clear validation error or mark data quality appropriately; do not silently replace invalid readings with normal values.
7. Add tests for valid data, missing fields, invalid types, stale timestamps, and boundary cases.
8. Summarize assumptions and files changed.

## Safety rules
- Never invent environmental thresholds. Find them in configuration or ask the developer.
- Do not treat a failed sensor or absent reading as a safe water condition.
- Do not log credentials or sensitive user data.
- Keep API validation consistent with the existing framework and database conventions.
