# Data Flow Diagram for Scenario 3: SQL Injection Attack

```mermaid
flowchart TD
    User[User Input] -->|Submit Data| Application[Application]
    Application -->|Query Execution| Database[Database]
    Database -->|Response| Application
    Application -->|Return Data| User
