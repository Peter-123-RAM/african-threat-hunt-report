African Threat Hunt: Mobile-Money OTP Interception

Overview

This project demonstrates a hypothesis-driven threat hunt focused on mobile-money account takeover activity affecting African organizations.

The hunt hypothesis was based on a common regional threat where attackers obtain credentials, intercept OTP codes, and rapidly perform wallet transfers.

Data Sources

- Web access logs
- Authentication events
- OTP validation events
- Transaction events

Methodology

1. Define threat hypothesis.
2. Collect telemetry.
3. Develop hunt queries.
4. Analyze activity.
5. Classify findings as benign or suspicious.
6. Produce leadership-focused recommendations.

Deliverables

- Threat activity report
- Hunt queries
- Sample telemetry
- Findings and recommendations

Trade-Offs

The project uses representative telemetry instead of production data.

This allows repeatable analysis while demonstrating the threat-hunting process.

What This Does Not Cover

This hunt does not analyze endpoint malware, EDR telemetry, memory artifacts, or network packet captures.
