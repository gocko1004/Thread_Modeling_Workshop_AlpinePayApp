# Inherent Risk Assessment for Scenario 3: SQL Injection Attack

| Category          | Description                                         | Likelihood | Impact | Risk Rating | Mitigation                                               |
|-------------------|-----------------------------------------------------|------------|--------|-------------|----------------------------------------------------------|
| Data Integrity    | Injection of malicious SQL queries compromising data. | High       | High   | High        | Input validation, prepared statements, and database hardening. |
| Unauthorized Access | Gaining access to sensitive data via SQL injection. | High       | High   | High        | WAF, monitoring, and Zero Trust database access.         |
| Data Corruption   | Alteration or deletion of critical database records. | Medium     | High   | High        | Detection and monitoring tools to identify anomalies.    |
