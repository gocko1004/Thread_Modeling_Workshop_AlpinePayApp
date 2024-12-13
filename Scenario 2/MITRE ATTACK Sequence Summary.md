# MITRE ATT&CK Sequence Summary: Scenario 2

## **Attack Stages**

### **1. Reconnaissance**
- The attacker identifies public-facing APIs and gathers details about the trading algorithm’s operations.
- Techniques: 
  - T1595.001 - Active Scanning
  - T1592 - Gather Information on System Configurations

### **2. Weaponization**
- The attacker crafts malicious payloads targeting input validation vulnerabilities or API misconfigurations.
- Techniques:
  - T1210 - Exploitation of Remote Services

### **3. Delivery**
- Malicious requests are sent to trading APIs or market data feeds to inject biased input.
- Techniques:
  - T1566.001 - Spear Phishing via Service
  - T1190 - Exploit Public-Facing Applications

### **4. Exploitation**
- The attacker exploits the API to manipulate algorithm parameters or inject corrupted data streams.
- Techniques:
  - T1190 - Exploit Public-Facing Applications
  - T1059.006 - Command and Scripting Interpreter: Python

### **5. Installation**
- The attacker installs persistent scripts or backdoors within the backend trading infrastructure.
- Techniques:
  - T1547 - Boot or Logon Autostart Execution

### **6. Command and Control (C2)**
- A secure channel is established to maintain control over the tampered algorithm.
- Techniques:
  - T1105 - Ingress Tool Transfer
  - T1571 - Non-Standard Port Communication

### **7. Actions on Objectives**
- **Data Exfiltration:** Proprietary algorithm data and sensitive trade records are exfiltrated.
- **Trade Manipulation:** Unauthorized trades are executed to cause financial disruption or personal profit.
- Techniques:
  - T1020 - Automated Exfiltration
  - T1565.001 - Data Manipulation
  - T1078 - Valid Accounts

```mermaid
graph LR
    A[Reconnaissance] -->|Identify vulnerabilities| B[Weaponization]
    B[Weaponization] -->|Create malicious payloads| C[Delivery]
    C[Delivery] -->|Send requests to APIs| D[Exploitation]
    D[Exploitation] -->|Manipulate algorithm| E[Installation]
    E[Installation] -->|Install backdoors| F[Command and Control]
    F[Command and Control] -->|Maintain Access| G[Actions on Objectives]
    G[Actions on Objectives] -->|Data Exfiltration| G
    G[Actions on Objectives] -->|Trade Manipulation| G
