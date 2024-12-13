# High-Level Design for Scenario 3: SQL Injection Attack

```mermaid
flowchart TD
    User[User] -->|Submits Data| Application[Frontend Application]
    Application -->|Processes Request| Backend[Backend Services]
    Backend -->|Executes Queries| Database[Relational Database]
