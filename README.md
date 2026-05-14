# 📄 AegisQ Consensus Protocol: Official Whitepaper

[![Role](https://img.shields.io/badge/Role-Security%20Research-blue.svg)]()
[![Topic](https://img.shields.io/badge/Topic-Distributed%20Systems-orange.svg)]()
[![Cryptography](https://img.shields.io/badge/Cryptography-Post--Quantum%20(PQC)-purple.svg)]()
[![License](https://img.shields.io/badge/License-MIT-red.svg)]()

> **Deterministic Consensus • Adversarial Analysis • System-Level Design**
> This repository hosts the official documentation, research, and whitepaper for the **AegisQ Protocol**. It focuses heavily on the theoretical and practical behavior of deterministic BFT-style consensus protocols under controlled execution and adversarial environments.

---

## 📖 Read the Whitepaper

The complete research, system models, architectural design, and failure analysis are available at the official portal:

### **🔗 [AegisQ Whitepaper Portal](https://sai-shashank-2005.github.io/aegisq-consensus-whitepaper/)**
*(Includes access to the full PDF version)*

---

## 🧠 Core Research Areas

This document bridges the gap between system design and adversarial analysis, exploring what is truly required to ensure safety and liveness in real-world distributed networks.

<table width="100%">
  <tr>
    <th width="30%">Area of Study</th>
    <th width="70%">Description</th>
  </tr>
  <tr>
    <td><strong>Consensus Execution</strong></td>
    <td>Deep-dive into the deterministic <code>Prepare → Commit → Finalize</code> execution model and <code>2f + 1</code> quorum guarantees.</td>
  </tr>
  <tr>
    <td><strong>Adversarial Analysis</strong></td>
    <td>Demonstrates how distributed systems can fail despite quorum guarantees (e.g., ordering divergence, replay attacks).</td>
  </tr>
  <tr>
    <td><strong>Post-Quantum Integration</strong></td>
    <td>Analysis of incorporating Dilithium (ML-DSA-44) and SHA3-256 into high-throughput consensus pipelines.</td>
  </tr>
  <tr>
    <td><strong>System Observability</strong></td>
    <td>The necessity of real-time introspection and telemetry in distributed networks to detect state divergence.</td>
  </tr>
</table>

---

## ⚠️ Key Findings & Failure Modes

The whitepaper highlights several critical failure modes discovered during adversarial testing, emphasizing that code-level correctness is not enough to secure a network.

<table width="100%">
  <tr>
    <th width="30%">Vulnerability / Failure</th>
    <th width="70%">Impact & Observation</th>
  </tr>
  <tr>
    <td><strong>Replay Attacks</strong></td>
    <td>Data-layer vulnerabilities exposed by the absence of strict nonce enforcement.</td>
  </tr>
  <tr>
    <td><strong>Liveness Failures</strong></td>
    <td>Complete network stalls caused by the lack of a dynamic view-change mechanism.</td>
  </tr>
  <tr>
    <td><strong>Ordering Divergence</strong></td>
    <td>Consensus fractures occurring without explicit attacker intervention due to transaction ordering mechanics.</td>
  </tr>
  <tr>
    <td><strong>Cross-View Voting</strong></td>
    <td>Safety breaks in distributed settings when validators vote across views without proper state locking.</td>
  </tr>
</table>

> *Core Philosophy:* "Correctness in deterministic environments does not imply security in distributed adversarial systems."

---

## 🔗 Related Implementations

This repository is strictly for **design, research, and analysis**. The protocol concepts have been fully implemented in code in the following repositories:

* **[AegisQ Protocol (Core Engine)](https://github.com/Sai-shashank-2005/aegisq-protocol):** The Go-based consensus engine and cryptographic layer.
* **[AegisQ Explorer](https://github.com/Sai-shashank-2005/aegisq-protocol/tree/main/aegisq-explorer):** The Next.js real-time observability platform and UI.

---

## ⚖️ License & Author

**Sai Shashank P**
*Cybersecurity Engineer | Protocol Researcher*

*Released under the [MIT License](LICENSE). This document is intended for educational and research purposes.*
