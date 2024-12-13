# MITRE ATT&CK Sequence Summary for Scenario 4: Insider Threat Involving AI Models

## **Stages of the Attack**

### **1. Reconnaissance**
- The insider reviews accessible systems and gathers information about AI model storage and configurations.
- Techniques:
  - T1592 - Gather Information on System Configurations

### **2. Initial Access**
- The insider uses legitimate credentials to access administrative tools and AI model storage.
- Techniques:
  - T1078 - Valid Accounts

### **3. Privilege Escalation**
- The insider escalates privileges to gain administrative control over AI models.
- Techniques:
  - T1068 - Exploitation of Privilege Escalation

### **4. Execution**
- The insider downloads AI models or injects malicious changes into the models.
- Techniques:
  - T1059.006 - Command and Scripting Interpreter: Python

### **5. Exfiltration**
- The insider exfiltrates proprietary AI models or training data to external storage.
- Techniques:
  - T1041 - Exfiltration Over C2 Channel

### **6. Impact**
- The insider manipulates AI models, sabotaging functionality or using them for personal gain.
- Techniques:
  - T1565.001 - Data Manipulation

```mermaid
flowchart TD
    A[Reconnaissance] --> B[Initial Access]
    B[Initial Access] --> C[Privilege Escalation]
    C[Privilege Escalation] --> D[Execution]
    D[Execution] --> E[Exfiltration]
    E[Exfiltration] --> F[Impact]


