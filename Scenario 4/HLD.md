# High-Level Design for Scenario 4: Insider Threat Involving AI Models

```mermaid
flowchart TD
    User[Authorized User] -->|Authenticate| AdminPanel[Admin Panel]
    AdminPanel -->|Manage Models| ModelStorage[AI Model Storage]
    ModelStorage -->|Store and Retrieve| Database[Model Database]
    AdminPanel -->|Monitor Logs| Monitoring[Audit Logs and Monitoring System]

