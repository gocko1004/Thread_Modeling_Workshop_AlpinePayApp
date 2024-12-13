erDiagram
    USER }|..|{ TRANSACTION : "Initiates"
    USER ||--o{ ACCOUNT : "Has"
    TRANSACTION ||--o{ PAYMENT-GATEWAY : "Validated by"
    TRANSACTION ||--|{ DATABASE : "Stored in"
    PAYMENT-GATEWAY ||--o{ EXTERNAL-BANK : "Connects to"
    DATABASE ||--|{ AI-MODULE : "Analyzed by"
    AI-MODULE ||--o{ ALERTS : "Generates"
