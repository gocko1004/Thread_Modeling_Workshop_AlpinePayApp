# MITRE ATT&CK Sequence Summary for Scenario 3: SQL Injection Attack

## **Stages of the Attack**

### **1. Reconnaissance**
- The attacker scans for vulnerabilities in public-facing input fields and endpoints.
- Techniques:
  - T1595.002 - Vulnerability Scanning

### **2. Weaponization**
- The attacker crafts malicious SQL payloads to exploit input validation weaknesses.
- Techniques:
  - T1210 - Exploitation of Remote Services

### **3. Delivery**
- Malicious SQL queries are delivered through input fields in the application.
- Techniques:
  - T1566.002 - Spear Phishing via Input Forms

### **4. Exploitation**
- The SQL injection payload manipulates database queries to gain unauthorized access.
- Techniques:
  - T1190 - Exploit Public-Facing Application

### **5. Installation**
- The attacker establishes persistence by injecting malicious triggers or stored procedures.
- Techniques:
  - T1547 - Boot or Logon Autostart Execution

### **6. Command and Control (C2)**
- A communication channel is established with the database to extract or manipulate data.
- Techniques:
  - T1071.001 - Application Layer Protocol: Web Traffic

### **7. Actions on Objectives**
- **Data Exfiltration:** Retrieve sensitive database records.
- **Data Manipulation:** Alter or delete critical data.
- Techniques:
  - T1565.001 - Data Manipulation
  - T1020 - Automated Exfiltration

```mermaid
flowchart TD
    A[Reconnaissance] --> B[Weaponization]
    B[Weaponization] --> C[Delivery]
    C[Delivery] --> D[Exploitation]
    D[Exploitation] --> E[Installation]
    E[Installation] --> F[Command and Control]
    F[Command and Control] --> G[Actions on Objectives]
    G[Actions on Objectives] -->|Data Exfiltration| G
    G[Actions on Objectives] -->|Data Manipulation| G

