# STRIDE Threat Model for Scenario 4: Insider Threat Involving AI Models

```mermaid
graph TD
    subgraph "User Interaction"
        Insider[Insider] -->|Access Requests| AdminPanel[Admin Panel]
    end

    subgraph "Core Systems"
        AdminPanel -->|Manage AI Models| ModelStorage[AI Model Storage]
        ModelStorage -->|Retrieve and Modify| Database[Model Database]
    end

    %% Threats
    Insider -.->|Spoofing: Use stolen credentials| AdminPanel
    AdminPanel -.->|Tampering: Modify AI models| ModelStorage
    ModelStorage -.->|Repudiation: Deny unauthorized changes| Database
    Database -.->|Information Disclosure: Leak sensitive data| AdminPanel
    Database -.->|Elevation of Privilege: Gain unauthorized control| AdminPanel

    %% Mitigations
    AdminPanel -->|MFA for Access| Insider
    ModelStorage -->|Encryption and Access Control| Database
    Database -->|Audit Logs and Monitoring| Database
    Database -->|Cryptographic Signing| ModelStorage

