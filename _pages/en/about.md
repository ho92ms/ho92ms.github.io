---
title: "About"
permalink: /en/about/
layout: single
lang: en
---

<div class="language-switcher" style="text-align: right; margin-bottom: 1em;">
  <a href="/hu/about/">HU Magyar</a> | <strong>EN English</strong>
</div>

## Professional Profile

I am a **security engineer** and **systems architect** with deep expertise in **enterprise infrastructure hardening**, **distributed systems**, and **applied machine learning**. My work bridges the gap between **formal security theory** and **practical system implementation**, with emphasis on:

1. **Defensive Security Engineering** — threat detection, hardening frameworks, and automated compliance
2. **Distributed Systems Architecture** — fault-tolerant designs, network protocols, and industrial integration
3. **Empirical Rigor** — data-driven validation, reproducible methodologies, and measurable outcomes

---

## Philosophy

I approach system design through three complementary lenses:

### 1. Security as a First-Class Property
Security is not an afterthought—it is an **architectural invariant**. I apply:
- **Defense in depth** — layered controls with fail-safe defaults
- **Principle of least privilege** — minimal access rights enforced via GPO and RBAC
- **Behavioral detection** — anomaly-based monitoring beyond signature-based defenses

### 2. Automation through Formal Specification
Manual processes introduce human error. I emphasize:
- **Declarative configuration** — infrastructure as code (PowerShell DSC, Ansible-like patterns)
- **Idempotent operations** — safe to re-run, predictable state transitions
- **Event-driven architectures** — real-time response to system changes

### 3. Empirical Validation
Theoretical models must withstand real-world constraints. I prioritize:
- **Measurable metrics** — mean time to detection (MTTD), false positive rates, compliance scores
- **Reproducible experiments** — version-controlled configurations, documented procedures
- **Post-mortem analysis** — learning from incidents, iterative improvement

---

## Technical Domains

### Security Engineering

#### Windows Hardening & Compliance
- Applied **STIG (Security Technical Implementation Guides)** and **CIS Benchmarks** via Group Policy
- Deployed **Microsoft Security Baselines** for Windows 10/11 and Server 2016/2019
- Automated hardening with **HardeningKitty** and custom PowerShell DSC scripts
- Configured **Windows Defender ASR rules** for zero-day exploit mitigation

#### Threat Detection & Response
- Built **honeypot systems** for ransomware early warning (file monitoring, decoy files)
- Developed **behavioral detection scripts** (PowerShell-based EDR) for suspicious activity
- Integrated **Wazuh SIEM** with custom rules for Windows Event Log analysis
- Implemented **automated incident response** for RDP brute-force attacks (IP blocking, alerting)

#### Network Security
- Designed **reverse tunnel architecture** over WebSockets for secure industrial protocol access
- Configured **site-to-site VPN** (IPSec, SSL VPN) for multi-location enterprises
- Deployed **DNS-over-HTTPS (DoH)** for encrypted DNS resolution
- Built **SSH tunneling** solutions for secure remote access

---

### Distributed Systems & Protocols

#### WebSocket-based Relay Architecture (C# / .NET 8.0)
- Designed **bidirectional tunneling** for NAT traversal without VPN overhead
- Implemented **concurrent connection management** with `ConcurrentDictionary` and `TaskCompletionSource`
- Built **OPC UA mock server** for industrial automation testing
- Applied **asynchronous I/O patterns** for high-throughput data forwarding

#### Industrial Protocols
- Integrated **OPC UA** (industrial standard for machine-to-machine communication)
- Developed **protocol adapters** for legacy systems
- Tested interoperability with **SCADA** environments

---

### Enterprise Infrastructure & Automation

#### Active Directory & Group Policy
- Automated **domain controller deployment** with PowerShell (AD DS installation, forest configuration)
- Created **GPO management framework** for centralized policy distribution
- Built **SYSVOL synchronization tools** for multi-DC environments
- Developed **user provisioning scripts** with role-based access control (RBAC)

#### OS Deployment & PXE Boot
- Deployed **Windows Deployment Services (WDS)** with **Microsoft Deployment Toolkit (MDT)**
- Configured **PXE boot** (DHCP options 66/67, TFTP) for network-based installations
- Automated **unattended installs** with custom answer files
- Integrated **driver injection** and post-deployment configuration

#### Scripting & Automation
- Developed **modular PowerShell library** for common operations (backup, restore, monitoring)
- Created **event-driven monitoring systems** with real-time Event Log analysis
- Built **firewall rule automation** for dynamic service exposure
- Implemented **compliance reporting** for audit readiness

---

### Machine Learning & Data Science

#### Neural Network Design
- Designed **convolutional** and **recurrent** architectures for domain-specific tasks
- Applied **transfer learning** with pre-trained models (ResNet, BERT)
- Conducted **hyperparameter optimization** with Bayesian methods

#### Large Language Models (LLMs)
- Fine-tuned **domain-specific models** using LoRA and prefix tuning
- Developed **prompt engineering strategies** for task-specific performance
- Built **LLM-powered agents** with error handling and fallback mechanisms

#### Data Analysis
- Performed **exploratory data analysis (EDA)** with statistical summaries and visualizations
- Applied **feature engineering** for domain-specific representations
- Conducted **A/B testing** for statistical validation

---

## Approach to Problem-Solving

I am particularly interested in problems where **theoretical structure meets operational constraints**, such as:

### Security
- Designing **detection systems** that balance **false positive rates** with **coverage**
- Implementing **zero-trust architectures** in legacy enterprise environments
- Applying **formal verification** to security policy enforcement

### Distributed Systems
- Building **fault-tolerant architectures** with **Byzantine failure** resilience
- Optimizing **latency vs. consistency** trade-offs in distributed databases
- Designing **protocol stacks** for industrial IoT with real-time constraints

### Machine Learning
- Creating **interpretable models** for high-stakes decisions (security, healthcare)
- Balancing **model complexity** with **generalization** performance
- Ensuring **adversarial robustness** in deployed ML systems

---

## Collaboration

I am open to collaboration on projects involving:

- **Security engineering** — threat detection, hardening automation, SIEM integration
- **Distributed systems** — protocol design, fault tolerance, industrial integration
- **Applied machine learning** — security applications, anomaly detection, interpretability
- **Open-source tools** — infrastructure automation, security frameworks, research prototypes

Feel free to reach out via [email](mailto:neduabi@pm.me) or [GitHub](https://github.com/ho92ms).

---

## Core Values

> *"Security through engineering rigor. Automation through systematic design. Intelligence through empirical validation."*

These principles guide my approach to both **defensive engineering** and **research**:
1. **Rigor** — formal methods, provable properties, documented assumptions
2. **Pragmatism** — operational feasibility, cost-benefit analysis, incremental deployment
3. **Transparency** — open-source contributions, reproducible results, knowledge sharing



