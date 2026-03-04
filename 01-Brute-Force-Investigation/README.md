# 🔎 Incident Investigation: Brute Force Login Attack

## Summary
During log analysis, multiple failed login attempts were observed targeting the SSH authentication service.  
The activity originated from a single external IP address and occurred repeatedly within a short time frame, indicating a potential brute force attack attempt.

---

## Timeline of Activity
| Time | Event |
|-----|------|
| 10:14 | Multiple failed login attempts detected |
| 10:15 | Repeated authentication failures from same IP |
| 10:17 | Alert triggered due to excessive login attempts |

---

## Evidence Collected
Evidence was gathered from authentication logs showing repeated login failures.

Observed patterns included:

- repeated login failures
- multiple usernames attempted
- single IP address responsible for the activity

Screenshots of the logs are located in the **evidence folder**.

---

## Indicators of Compromise (IoCs)

| Indicator | Description |
|-----------|-------------|
| Suspicious IP Address | XXX.XXX.XXX.XXX |
| Targeted Service | SSH |
| Attack Pattern | Repeated password attempts |

---

## MITRE ATT&CK Mapping

| Tactic | Technique |
|------|-----------|
| Credential Access | Brute Force |

---

## Analysis
The activity appears consistent with a brute force login attempt.  
The attacker attempted to gain unauthorized access by repeatedly trying different password combinations against the SSH authentication service.

The pattern of rapid authentication failures from a single IP address is a strong indicator of automated credential guessing.

---

## Recommended Response Actions

- Block the malicious IP address at the firewall
- Enable multi-factor authentication (MFA)
- Implement account lockout policies
- Monitor authentication logs for additional suspicious activity

---

## Lessons Learned
Authentication logs provide valuable indicators of brute force attacks. Monitoring login patterns and detecting repeated authentication failures is essential for early detection of credential-based attacks.

---

## Tools Used

- TryHackMe Lab Environment
- Linux Authentication Logs
- Basic Log Analysis
