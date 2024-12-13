# Data Flow Diagram for Scenario 4: Insider Threat Involving AI Models

```mermaid
flowchart TD
    Insider[Insider] -->|Access Requests| AdminPanel[Admin Panel]
    AdminPanel -->|Query AI Models| ModelStorage[AI Model Storage]
    ModelStorage -->|Return Model Data| AdminPanel
    AdminPanel -->|Respond| Insider
    Insider -->|Modify| ModelStorage

