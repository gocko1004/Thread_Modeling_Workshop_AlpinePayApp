```mermaid
  sequenceDiagram
    participant Attacker
    participant AlpinePayApp
    participant CnCServer
    participant BackendServer
    participant User

    activate Attacker
    Attacker->>AlpinePayApp: Reconnaissance to identify vulnerabilities
    AlpinePayApp->>Attacker: Application details exposed
    deactivate Attacker

    activate Attacker
    Attacker->>AlpinePayApp: AI-generated phishing campaign targeting users and admins
    note right of Attacker: Personalized emails, SMS, and social media messages leveraging deepfake techniques
    AlpinePayApp->>User: Phishing message delivered
    activate User
    User->>AlpinePayApp: Clicks malicious link or downloads attachment
    AlpinePayApp->>User: Malware deployed using steganography
    deactivate User
    deactivate Attacker

    activate Attacker
    Attacker->>AlpinePayApp: Execute payload to gain backend access
    AlpinePayApp->>BackendServer: Payload execution in progress
    BackendServer->>CnCServer: Establish communication channel via cloud platform
    CnCServer->>BackendServer: Send malicious commands
    BackendServer->>CnCServer: Perform actions (e.g., data exfiltration, manipulation)
    deactivate Attacker
```