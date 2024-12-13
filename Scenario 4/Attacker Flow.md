```mermaid
sequenceDiagram
    participant Insider
    participant AdminPanel
    participant ModelStorage

    Insider->>AdminPanel: Access model controls with privileged credentials
    AdminPanel->>ModelStorage: Retrieve AI model and associated data
    ModelStorage->>Insider: Return proprietary AI model
    Insider->>ModelStorage: Modify or sabotage model functionality


