```mermaid
sequenceDiagram
    participant Attacker
    participant Application
    participant Database

    Attacker->>Application: Inject malicious SQL query
    Application->>Database: Execute compromised query
    Database->>Attacker: Return unauthorized data
    Database->>Application: Potential data corruption

