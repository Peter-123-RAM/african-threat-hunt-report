Threat Activity Report

Executive Summary

A threat hunt was conducted to identify possible mobile-money account takeover activity involving OTP interception and fraudulent wallet transfers.

The hunt identified suspicious behavior consistent with credential theft followed by unauthorized OTP usage.

Risk Level:
High

---

Hunt Hypothesis

If an attacker steals a user's credentials and intercepts OTP codes, then login activity will originate from one IP address while OTP validation and wallet transfers originate from another IP address shortly afterward.

---

Data Sources

- Web access logs
- Authentication events
- OTP validation events
- Wallet transfer events

---

Findings

Finding 1

08:16:01 UTC

Successful login observed from:

41.90.12.5

Classification:
Benign

Reason:
Normal authentication behavior.

---

Finding 2

08:16:20 UTC

OTP validation from:

41.90.12.5

Classification:
Benign

Reason:
Matches original login source.

---

Finding 3

08:16:50 UTC

OTP validation observed from:

102.67.44.90

Classification:
Suspicious

Reason:
Different IP address shortly after successful login.

Confidence:
Medium

---

Finding 4

08:17:10 UTC

Wallet transfer initiated from:

102.67.44.90

Classification:
Suspicious

Reason:
Transfer occurred immediately after anomalous OTP activity.

Confidence:
High

---

Finding 5

Multiple transfer attempts observed.

Classification:
Suspicious

Reason:
Behavior consistent with account takeover.

Confidence:
High

---

Recommendations

1. Alert on OTP validation from a different IP than the login session.

2. Require step-up authentication when OTP and transfer activity originate from different networks.

3. Implement transaction velocity monitoring.

4. Monitor repeated transfer attempts following OTP validation.

5. Review accounts associated with suspicious OTP activity.

---

Negative Findings

No evidence of malware execution or server compromise was identified during this hunt.

The activity appears limited to possible account takeover behavior.
