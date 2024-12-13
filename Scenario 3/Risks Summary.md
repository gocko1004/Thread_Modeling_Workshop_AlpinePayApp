# Risks Summary for Scenario 3: SQL Injection Attack

| Risk ID | Description                                         | Severity | Likelihood | Impact | Mitigation Plan                                      |
|---------|-----------------------------------------------------|----------|------------|--------|------------------------------------------------------|
| R1      | Exploitation of input validation vulnerabilities leading to unauthorized database access. | High     | High       | High   | Input validation, prepared statements, and database hardening. |
| R2      | Injection of malicious SQL altering or deleting critical data. | High     | Medium     | High   | WAF to block malicious patterns, and activity monitoring. |
| R3      | Extraction of sensitive data via SQL injection.    | High     | High       | High   | Zero Trust database access and end-to-end encryption. |
| R4      | Persistent database compromise using malicious stored procedures. | Medium   | Medium     | Medium | Regular audits and penetration testing to detect anomalies. |

