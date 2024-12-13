# STRIDE Threat Model for Scenario 3: SQL Injection Attack

```mermaid
graph TD
    subgraph "User Interaction"
        User[User Input] -->|Submit Data| Application[Frontend Application]
    end

    subgraph "Core Application"
        Application -->|Process Input| API[Backend API]
        API -->|Execute Queries| Database[Relational Database]
    end

    %% Threats
    User -.->|Spoofing: Fake User Input| Application
    Application -.->|Tampering: Inject Malicious SQL| API
    API -.->|Repudiation: Deny Unauthorized Query Execution| Database
    Database -.->|Information Disclosure: Leak Sensitive Data| Application
    Database -.->|Denial of Service: Overload Database with Queries| API

    %% Mitigations
    User -->|Authentication and Validation| Application
    Application -->|Input Sanitization| API
    API -->|Rate Limiting and Monitoring| Database
    Database -->|Encryption and Access Control| Database
