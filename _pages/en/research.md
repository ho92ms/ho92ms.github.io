---
title: "Research"
permalink: /en/research/
layout: single
lang: en
---

<div class="language-switcher" style="text-align: right; margin-bottom: 1em;">
  <a href="/hu/research/">🇭🇺 Magyar</a> | <strong>🇬🇧 English</strong>
</div>

## Research Interests

My research interests span **defensive security engineering**, **distributed systems theory**, and **applied machine learning**, with a focus on methods that are both **theoretically principled** and **operationally deployable**.

---

## Core Research Areas

### 1. Security Engineering & Threat Intelligence

#### Behavioral Threat Detection
- **Anomaly-based detection systems** — statistical models for identifying deviations from baseline behavior
- **Honeypot architectures** — deception techniques for early-stage attack identification
- **Event correlation** — temporal analysis of Windows Event Logs for advanced persistent threats (APT)

**Research Questions:**
- How can we minimize **false positive rates** while maintaining **high detection coverage**?
- What are the **optimal placement strategies** for honeypot resources in enterprise networks?
- Can **machine learning models** outperform rule-based SIEM systems for zero-day detection?

#### Automated Compliance & Hardening
- **Formal verification of security policies** — using model checking to prove GPO correctness
- **Configuration drift detection** — continuous monitoring for unauthorized changes
- **Hardening benchmarks** — comparative analysis of STIG, CIS, and vendor baselines

**Research Questions:**
- How can we **formally verify** that a GPO configuration satisfies STIG requirements?
- What is the **measurable impact** of hardening on attack surface reduction?
- Can we **automate** the mapping from compliance frameworks to GPO settings?

---

### 2. Distributed Systems & Network Protocols

#### Fault-Tolerant Architectures
- **Consensus protocols** — Paxos, Raft, and Byzantine fault tolerance
- **CAP theorem trade-offs** — consistency vs. availability in distributed databases
- **Failure injection testing** — chaos engineering for resilience validation

**Research Questions:**
- How can we design **low-latency consensus** for industrial control systems?
- What are the **minimal assumptions** required for Byzantine fault tolerance in IoT networks?
- Can we **quantify** the trade-off between consistency and partition tolerance?

#### WebSocket-based Tunneling
- **NAT traversal techniques** — reverse tunnels, STUN/TURN protocols
- **Protocol multiplexing** — bidirectional communication over a single connection
- **Connection management** — handling disconnects, retries, and state reconciliation

**Research Questions:**
- What is the **latency overhead** of WebSocket tunneling compared to direct TCP?
- How can we **optimize buffer sizes** for high-throughput industrial protocols (OPC UA)?
- Can we **prove correctness** of the relay server under concurrent requests?

#### Industrial IoT & OPC UA
- **Security extensions** — authentication, encryption, certificate management
- **Real-time constraints** — deterministic communication with bounded latency
- **Interoperability** — bridging legacy protocols with modern standards

**Research Questions:**
- How can we **secure OPC UA** against man-in-the-middle attacks in untrusted networks?
- What are the **performance characteristics** of OPC UA over WebSocket vs. TCP?
- Can we **formally model** the OPC UA protocol stack for verification?

---

### 3. Machine Learning for Security Applications

#### Adversarial Machine Learning
- **Robustness to adversarial examples** — perturbations that fool classifiers
- **Model poisoning attacks** — corrupting training data to degrade performance
- **Certified defenses** — provable guarantees against bounded perturbations

**Research Questions:**
- How can we **certify** that a malware classifier is robust to adversarial examples?
- What is the **trade-off** between adversarial robustness and benign accuracy?
- Can we **detect** poisoning attacks during training?

#### Anomaly Detection with Deep Learning
- **Autoencoders for outlier detection** — unsupervised learning of normal behavior
- **Recurrent networks for sequence anomalies** — temporal patterns in event logs
- **One-class SVMs** — classifiers trained only on benign samples

**Research Questions:**
- How can we **tune** the reconstruction threshold for autoencoders to minimize false positives?
- Can **LSTMs** outperform statistical baselines for detecting ransomware behavior?
- What is the **label efficiency** of semi-supervised anomaly detection?

#### Explainable AI for Security
- **Model interpretability** — understanding why a model flagged an event as malicious
- **Feature attribution** — SHAP, LIME, and gradient-based explanations
- **Human-in-the-loop systems** — integrating analyst feedback into models

**Research Questions:**
- Can we **trust** model explanations for high-stakes security decisions?
- How can we **quantify** the interpretability of different model architectures?
- What is the **impact** of human feedback on model accuracy over time?

---

### 4. Large Language Models (LLMs) & Applied NLP

#### Fine-Tuning for Domain-Specific Tasks
- **Parameter-efficient methods** — LoRA, prefix tuning, adapter layers
- **Domain adaptation** — transfer learning from general to specialized corpora
- **Evaluation metrics** — perplexity, BLEU, human evaluation

**Research Questions:**
- How many **domain-specific examples** are required for effective fine-tuning?
- What is the **trade-off** between parameter efficiency and task performance?
- Can we **quantify** the impact of pre-training data quality on downstream tasks?

#### Prompt Engineering & Optimization
- **Few-shot learning** — designing effective prompts with minimal examples
- **Chain-of-thought prompting** — eliciting reasoning steps from LLMs
- **Automated prompt search** — gradient-based optimization of discrete prompts

**Research Questions:**
- What are the **theoretical limits** of few-shot learning with LLMs?
- Can we **automate** the discovery of optimal prompts?
- How can we **ensure** that LLMs produce factually correct outputs?

#### LLM-Powered Security Tools
- **Automated threat intelligence** — extracting indicators of compromise (IOCs) from reports
- **Log analysis** — natural language queries over structured event data
- **Malware code generation detection** — identifying AI-generated exploits

**Research Questions:**
- Can LLMs **accurately** extract IOCs from unstructured threat reports?
- What is the **false positive rate** of LLM-based log analysis?
- How can we **detect** when LLMs are used to generate malicious code?

---

## Methodological Principles

I emphasize approaches that prioritize:

### 1. Theoretical Rigor
- **Formal modeling** — using mathematical frameworks (automata, Petri nets, temporal logic)
- **Provable properties** — correctness, liveness, safety guarantees
- **Complexity analysis** — time/space bounds, scalability limits

### 2. Empirical Validation
- **Reproducible experiments** — version-controlled code, documented procedures, public datasets
- **Statistical testing** — hypothesis testing, confidence intervals, power analysis
- **Ablation studies** — isolating the impact of individual components

### 3. Operational Feasibility
- **Real-world constraints** — deployment costs, backward compatibility, human factors
- **Incremental deployment** — A/B testing, canary releases, rollback strategies
- **Cost-benefit analysis** — quantifying the trade-off between security and usability

---

## Current Focus

My current work explores:

### 1. Automated Security Policy Verification
- **Goal:** Prove that a GPO configuration satisfies STIG requirements
- **Approach:** Model GPO as a finite state machine, use model checking (SPIN, TLA+)
- **Impact:** Eliminate manual audit burden, ensure compliance by construction

### 2. Distributed Honeypot Networks
- **Goal:** Deploy coordinated honeypots across enterprise environments
- **Approach:** Centralized log aggregation, correlation analysis, automated response
- **Impact:** Early detection of lateral movement, reduced attacker dwell time

### 3. LLM-Assisted Threat Hunting
- **Goal:** Use LLMs to query event logs with natural language
- **Approach:** Fine-tune on annotated security datasets, integrate with SIEM
- **Impact:** Lower barrier to entry for threat hunters, faster hypothesis testing

---

## Publications & Open Source

Selected work and experiments are available on [GitHub](https://github.com/ho92ms).

For collaboration or discussions, feel free to reach out at [neduabi@pm.me](mailto:neduabi@pm.me).

---

> *"Security through formal methods. Resilience through distributed design. Intelligence through empirical science."*



