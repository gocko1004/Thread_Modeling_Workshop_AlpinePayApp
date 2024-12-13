```mermaid
graph TD
    subgraph User Interaction
        A[User] -->|HTTP Requests| B[Web Server]
        A -->|API Calls| K[Public APIs]
    end

    subgraph Web Server
        B -->|Access| C[Database]
        B -->|Receive Input| D[Input Validation]
        B -->|Execute| E[Application Logic]
        K -->|Validate| D
    end

    subgraph Database
        C -->|Store/Fetch Data| F[Data Storage]
    end

    A((User)) -.->|Authentication| G[Authentication Mechanism]
    B -.->|Logging| H[Logging Service]
    A -.->|Access| I[Admin Panel]
    I -.->|Controls| J[Admin Functionality]

    %% Threats
    T1([Spoofing: Spoof User Identity]) -.-> A
    T2([Tampering: Alter API Request]) -.-> K
    T3([Repudiation: Deny Financial Transactions]) -.-> H,
    T4([Information Disclosure: Data Leak]) -.-> F
    T5([Denial of Service: Overload APIs]) -.-> B
    T6([Elevation of Privilege: Unauthorized Admin Access]) -.-> I
    T7([API Abuse: Exploit API Rate Limits]) -.-> K
    T8([AI Model Exploitation: Tamper Insights]) -.-> E
    
    %% Mitigations
    M1([Mitigation: Strong Authentication - FIDO2]) --> T1
    M2([Mitigation: HTTPS + Rate Limiting]) --> T2
    M3([Mitigation: Non-repudiation Mechanisms]) --> T3
    M4([Mitigation: Data Encryption]) --> T4
    M5([Mitigation: API Gateway + WAF]) --> T5
    M6([Mitigation: RBAC and Admin Audit Logs]) --> T6
    M7([Mitigation: API Validation + Monitoring]) --> T7
    M8([Mitigation: AI Model Encryption + Anomaly Detection]) --> T8
