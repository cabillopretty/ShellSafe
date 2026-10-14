# ShellSafe Project Knowledge

## Project title
ShellSafe: An IoT-Based Real-Time Algal Bloom Detection and Predictive Analytics System for Coastal Water Monitoring.

## Purpose
ShellSafe is designed to support coastal water monitoring by collecting environmental readings, displaying current and historical conditions, estimating possible harmful algal bloom risk, and notifying authorized monitoring personnel when configured risk conditions are reached.

## Main workflow
1. IoT device collects water-quality readings.
2. Device sends readings to the system through the communication method implemented in the repository.
3. The system validates and stores incoming readings.
4. Monitoring and predictive/rule-based analysis evaluate the readings.
5. The dashboard displays current values, trends, device status, and risk information.
6. The alert component notifies authorized users when configured conditions trigger an alert.
7. Historical data supports reporting and later review.

## Environmental parameters
The project documentation describes temperature, pH, salinity, turbidity, and dissolved oxygen in earlier versions. The team's later implementation decisions may differ. Always inspect the current source code and confirm which sensors and fields are actually implemented before editing.

## Prediction limitations
- Risk scores are indicators based on measured parameters and model/rule outputs.
- A high-risk result is not laboratory confirmation of toxins.
- The system does not automatically identify a specific microscopic algal species unless such a validated feature is explicitly present.
- Sensor calibration, cellular connectivity, power availability, data quality, and location/time coverage can affect results.

## Expected user roles
Use the roles defined by the current implementation and requirements. Do not introduce new roles or widen alert recipients without confirmation.

## Developer guidance
- Keep data validation and risk analysis testable.
- Preserve timestamps and traceability from a risk result to its source readings.
- Make alert severity and triggering reasons understandable to users.
- Document assumptions and configuration changes.
- Verify the repository's actual framework, database, API routes, and deployment setup before making implementation claims.
