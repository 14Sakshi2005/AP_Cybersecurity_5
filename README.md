# Capstone Project: Samba Exploitation & Incident Response Simulation

![Status](https://img.shields.io/badge/Status-Completed-green)
![Platform](https://img.shields.io/badge/Platform-Kali%20Linux-blue)
![Tool](https://img.shields.io/badge/Tool-Metasploit-red)
![VM](https://img.shields.io/badge/Target-Metasploitable-orange)
![Focus](https://img.shields.io/badge/Security-Pentesting-critical)

##  Overview
This project demonstrates a controlled security assessment of a vulnerable system using Metasploit Framework. The objective was to identify, exploit, and analyze a known Samba vulnerability in a test environment and simulate a real-world incident response scenario.

Target system used: Metasploitable (intentionally vulnerable VM)


##  Tools Used
- Metasploit Framework
- Nmap
- Netcat payloads
- Metasploitable VM
- Kali Linux


##  Objective
- Perform vulnerability exploitation in a controlled environment
- Gain remote shell access
- Analyze system compromise
- Simulate incident response lifecycle

##  Network Architecture

Attacker Machine (Kali Linux)
        ↓
Metasploit Framework Attack
        ↓
Target Machine (Metasploitable)

##  Exploitation Summary

### 1. Exploit Used
exploit/multi/samba/usermap_script

### 2. Payload
cmd/unix/reverse

### 3. Target
Metasploitable VM


##  Attack Process

1. Identified target IP using network scanning
2. Confirmed Samba service running on ports 139 and 445
3. Launched Metasploit Framework
4. Selected Samba exploit module
5. Configured:
   - RHOSTS = Target IP
   - LHOST = Attacker IP (Kali)
   - Payload = reverse shell
6. Executed exploit successfully
7. Gained remote shell access


## 🖧 Attack Flow Diagram

```mermaid
flowchart TD
A[Attacker Machine - Kali Linux] --> B[Metasploit Framework]
B --> C[Exploit: Samba usermap_script]
C --> D[Target: Metasploitable VM]
D --> E[Remote Shell Access Gained]
E --> F[Post Exploitation Commands]
F --> G[Incident Response Simulation]
G --> H[Mitigation & Cleanup]
```


##  Post Exploitation Activities

Executed system reconnaissance commands:
- whoami
- id
- hostname
- ps aux

Verified successful compromise of target system.



##  Incident Response Simulation

### Detection
- Unauthorized remote shell access detected

### Analysis
- Exploitation via vulnerable Samba service

### Containment
- Terminated malicious shell session
- Identified attacker connection

### Eradication
- Stopped vulnerable service (smbd)
- Recommended patching Samba


##  Mitigation Strategies
- Disable unused services
- Patch Samba vulnerabilities
- Restrict SMB ports via firewall
- Implement intrusion detection systems
- Regular vulnerability scanning



## 📸 Evidence

|       Step           |         Screenshot                |
|----------------------|-----------------------------------|
| Exploit Execution    | <img width="1470" height="956" alt="1_ifconfig" src="https://github.com/user-attachments/assets/85af5a2e-cf97-479f-bf9a-e30d456523d1" />
        |
| Session Opened       | <img width="1470" height="956" alt="3_Sus_Log_Entries" src="https://github.com/user-attachments/assets/e455bb39-82f8-4d6b-967b-b9088f8b0227" />
 |
| Post Exploitation    | <img width="1470" height="956" alt="2_ShellAccess" src="https://github.com/user-attachments/assets/214c6716-6a3e-45e8-bd88-8ed5dc919be0" />
     |


##  Key Learning Outcomes
- Understanding SMB vulnerabilities
- Real-world exploitation workflow
- Metasploit usage
- Incident response lifecycle
- System compromise analysis

