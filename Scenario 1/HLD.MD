```mermaid
flowchart TD
    subgraph "User Interface"
        UI[User Interface]
    end
    subgraph "Frontend (EC2)"
        FE[Frontend Server]
    end
    subgraph "Backend"
        BE[Backend Server]
        subgraph "Security Layers"
            WAF[Web Application Firewall]
            IAM[Identity and Access Management]
        end
    end
    subgraph "Database"
        DB[Database Server]
    end
    subgraph "External Services"
        PaymentGateway[Payment Gateway]
        BankAPI[External Banking Systems]
        AI[AI/ML Module]
    end

    UI --> FE
    FE --> WAF
    WAF --> BE
    BE --> IAM
    BE --> DB
    BE --> PaymentGateway
    PaymentGateway --> BankAPI
    DB --> AI
    AI --> BE
