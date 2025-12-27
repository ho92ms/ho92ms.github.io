---
title: "Professional Experience"
permalink: /experience/
layout: single
---

## Overview

My professional background spans **enterprise security engineering**, **distributed systems architecture**, and **applied machine learning**. I have hands-on experience with **threat detection systems**, **infrastructure automation**, and **industrial protocol integration** in production environments.

---

## 1. Security Engineering & Infrastructure Hardening

### Windows Security Hardening
- **Applied security benchmarks:**
  - Implemented **STIG (Security Technical Implementation Guides)** for Windows Server 2016/2019
  - Deployed **CIS Benchmarks** via Group Policy Objects (GPO)
  - Applied **Microsoft Security Baselines** for Windows 10/11 (versions 21H2, 22H2, 25H2)
  
- **Automation tools:**
  - **HardeningKitty** — automated compliance checking and remediation
  - **PowerShell DSC** — declarative configuration for idempotent hardening
  - Custom scripts for **ADMX template deployment** and GPO synchronization

- **Attack Surface Reduction (ASR):**
  - Configured **Windows Defender ASR rules** for zero-day exploit mitigation
  - Blocked **Office macros**, **script execution**, and **credential theft** vectors
  - Enabled **controlled folder access** for ransomware prevention

**Key Achievement:** Reduced attack surface by **40%** across 100+ enterprise endpoints through automated GPO-based hardening.

---

### Threat Detection & Incident Response

#### Honeypot Systems
- **Decoy file monitoring:**
  - Deployed **honeypot files** (e.g., `passwords.txt`, `finances.xls`) in strategic locations
  - Implemented **real-time alerting** via Windows Event Log (Event ID 4663 — file access)
  - Built **PowerShell-based FileSystemWatcher** for behavioral detection

- **Ransomware detection:**
  - Monitored **C:\Users** directory for rapid file modifications (indicator of encryption)
  - Triggered **automated responses** (user lockout, network isolation, admin alerts)
  - Integrated with **Wazuh SIEM** for centralized log aggregation

**Key Achievement:** Detected and isolated **3 ransomware simulations** within **15 seconds** of initial file modification.

---

#### SIEM & Log Analysis
- **Wazuh integration:**
  - Deployed **Wazuh agents** on Windows endpoints and servers
  - Created **custom rules** for:
    - **RDP brute-force** detection (Event ID 4625 — failed logon)
    - **Event log tampering** (Event ID 1102 — log cleared)
    - **Privilege escalation** (Event ID 4672 — special privileges assigned)
  
- **Automated incident response:**
  - Built **IP blocking script** for repeated RDP failures (via Windows Firewall)
  - Configured **email alerts** for critical security events
  - Implemented **log retention policies** for compliance (GDPR, SOC 2)

**Key Achievement:** Reduced **mean time to detection (MTTD)** for RDP brute-force from **24 hours to 2 minutes**.

---

### Network Security Architecture

#### VPN & Secure Remote Access
- **Site-to-site VPN:**
  - Configured **IPSec VPN** for multi-location enterprise connectivity
  - Deployed **SSL VPN** for secure remote access without client software
  - Set up **PPTP** for legacy system compatibility (with security caveats documented)

- **SSH tunneling:**
  - Built **reverse SSH tunnels** for accessing internal services without exposing ports
  - Automated tunnel setup with **systemd** (Linux) and **Task Scheduler** (Windows)

- **DNS Security:**
  - Enabled **DNS-over-HTTPS (DoH)** for encrypted DNS resolution
  - Configured **DNS filtering** to block known malicious domains

**Key Achievement:** Secured **15+ remote sites** with zero VPN downtime over **12 months**.

---

#### Reverse Tunnel Architecture (C# / .NET 8.0)
- **Problem:** Industrial OPC UA servers behind NAT require external access without exposing internal networks
- **Solution:** Built **WebSocket-based relay server** for bidirectional tunneling

**Architecture:**
- **Tunnel Client:** Connects to relay server via WebSocket, forwards requests to local OPC UA server
- **Relay Server:** Routes HTTP requests to appropriate tunnel client based on site ID
- **Mock OPC Server:** Test harness for protocol validation

**Technical Details:**
- **Concurrency:** Used `ConcurrentDictionary` for thread-safe client management
- **Async I/O:** Applied `TaskCompletionSource` for request/response pairing
- **Error Handling:** Implemented connection retry logic with exponential backoff

**Key Achievement:** Enabled **secure remote monitoring** of industrial equipment without VPN overhead, reducing latency by **30%**.

---

## 2. Enterprise Infrastructure & Automation

### Active Directory & Group Policy

#### Domain Controller Deployment
- **Automated AD DS installation:**
  - Created **PowerShell scripts** for unattended domain controller provisioning
  - Configured **forest/domain** setup, DNS integration, and FSMO roles
  - Implemented **backup domain controllers** for high availability

- **GPO Management:**
  - Developed **modular GPO framework** for centralized policy distribution
  - Automated **SYSVOL synchronization** for multi-DC environments
  - Built **GPO versioning system** with rollback capabilities

**Key Achievement:** Reduced domain controller deployment time from **4 hours to 20 minutes** via automation.

---

#### User Provisioning & RBAC
- **Automated user creation:**
  - Built **PowerShell scripts** for bulk user provisioning from CSV
  - Implemented **role-based access control (RBAC)** via security groups
  - Configured **user quotas**, **home directories**, and **roaming profiles**

- **Security policies:**
  - Enforced **password complexity** and **account lockout policies**
  - Configured **Kerberos** authentication settings
  - Implemented **least privilege** via **restricted groups**

---

### OS Deployment & PXE Boot

#### Windows Deployment Services (WDS) + MDT
- **PXE boot infrastructure:**
  - Configured **DHCP options 66/67** for network boot
  - Set up **TFTP server** for boot image distribution
  - Integrated **Microsoft Deployment Toolkit (MDT)** for customization

- **Automated installations:**
  - Created **unattended answer files** (autounattend.xml) for zero-touch deployments
  - Implemented **driver injection** for diverse hardware
  - Configured **post-deployment scripts** (Windows updates, software installation, domain join)

**Key Achievement:** Achieved **zero-touch deployment** for Windows 10/11, reducing imaging time from **3 hours to 45 minutes**.

---

### PowerShell Automation

#### Scripting Framework
- **Modular library:**
  - Developed **reusable modules** for common tasks (AD operations, GPO management, logging)
  - Implemented **error handling** and **logging** best practices
  - Created **parameter validation** for robust input handling

- **Event-driven monitoring:**
  - Built **real-time monitoring** scripts for:
    - **File system changes** (FileSystemWatcher)
    - **Event log anomalies** (Get-WinEvent)
    - **Service failures** (Get-Service)
  
- **Backup/Restore:**
  - Automated **incremental backups** with versioning
  - Implemented **integrity checks** (hash validation)
  - Built **disaster recovery** scripts for domain controller restoration

**Key Achievement:** Reduced **manual scripting errors** by **80%** through standardized module usage.

---

## 3. Distributed Systems & Protocols

### WebSocket-based Relay Server
- **Concurrent connection handling:**
  - Used `ConcurrentDictionary<string, WebSocket>` for thread-safe client registry
  - Implemented `TaskCompletionSource<TunnelResponse>` for async request/response pairing
  - Applied **connection pooling** for efficient resource usage

- **Protocol implementation:**
  - Designed **custom message format** (JSON-based) for tunnel communication
  - Implemented **heartbeat mechanism** for connection liveness detection
  - Built **reconnection logic** with exponential backoff

**Performance:** Handled **100+ concurrent tunnel connections** with **<50ms latency** for request forwarding.

---

### Industrial Protocols (OPC UA)
- **Mock OPC Server:**
  - Implemented **minimal OPC UA server** in C# for testing
  - Supported **basic read/write** operations
  - Validated **interoperability** with commercial SCADA systems

- **Security:**
  - Configured **certificate-based authentication**
  - Enabled **message encryption** (AES-256)
  - Implemented **access control** via user roles

---

## 4. Machine Learning & Data Science

### Deep Learning
- **Frameworks:** PyTorch, TensorFlow/Keras
- **Architectures:** CNNs, RNNs, Transformers
- **Tasks:** Image classification, sequence modeling, anomaly detection

### Large Language Models (LLMs)
- **Fine-tuning:** LoRA, prefix tuning for domain adaptation
- **Prompt engineering:** Few-shot learning, chain-of-thought prompting
- **Deployment:** REST API serving, containerized inference

### Data Analysis
- **Exploratory Data Analysis (EDA):** Pandas, Matplotlib, Seaborn
- **Feature Engineering:** Domain-specific transformations, dimensionality reduction
- **Statistical Testing:** A/B testing, hypothesis testing, confidence intervals

---

## Key Strengths

1. **Security Engineering** — threat detection, hardening automation, compliance frameworks
2. **Systems Architecture** — distributed design, fault tolerance, protocol implementation
3. **Automation & Scripting** — PowerShell, Python, infrastructure as code
4. **Operational Excellence** — monitoring, incident response, disaster recovery

---

## Contact

For professional inquiries or collaboration opportunities:

📧 **Email:** [neduabi@pm.me](mailto:neduabi@pm.me)  
🔗 **GitHub:** [github.com/ho92ms](https://github.com/ho92ms)



