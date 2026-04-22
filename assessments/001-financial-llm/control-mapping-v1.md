# Control Mapping v1 — Customer-Facing Financial LLM (RAG-Based)

This document maps each identified risk to:
- Relevant **NIST AI RMF subcategories** (Govern, Map, Measure, Manage)
- Applicable **OWASP LLM Top 10 risks**

The goal is to demonstrate how technical and operational risks translate into recognized governance and security control frameworks.

---

## Mapping Table

| Risk ID | Risk Name | NIST AI RMF Mapping | OWASP LLM Top 10 Mapping |
|--------|----------|--------------------|--------------------------|
| R-001 | Prompt Injection Leading to Policy Manipulation | **MAP 4.1** (System context and interactions understood) <br> **MANAGE 2.2** (Controls to manage AI risks are implemented and monitored) | **LLM01: Prompt Injection** |
| R-002 | RAG Data Leakage (Confidentiality Breach) | **MAP 2.1** (Data inputs and sources are identified) <br> **MANAGE 1.3** (Risk controls for data protection implemented) | **LLM02: Sensitive Information Disclosure** |
| R-003 | Hallucinated Financial Information | **MEASURE 2.1** (AI system performance and reliability are evaluated) <br> **MANAGE 2.1** (Risk treatment plans are defined and applied) | **LLM04: Model Hallucination** |
| R-004 | Misinterpretation as Financial Advice | **GOVERN 1.3** (Policies for responsible AI use are established) <br> **MAP 3.2** (Intended use and limitations are clearly defined) | **LLM05: Improper Output Handling** |
| R-005 | RAG Context Poisoning | **MAP 2.1** (Data sources and integrity understood) <br> **MEASURE 1.2** (Risks from data inputs are assessed) | **LLM06: Training Data Poisoning** |
| R-006 | Inconsistent or Biased Responses | **MEASURE 2.2** (Fairness and bias are evaluated) <br> **GOVERN 2.1** (Organizational risk tolerance defined) | **LLM07: Bias and Toxicity** |
| R-007 | System Availability / Service Disruption | **MANAGE 1.1** (Operational risks are managed) | *(Not directly mapped — general system risk outside OWASP LLM Top 10 scope)* |
| R-008 | Lack of Output Monitoring and Auditability | **MANAGE 2.3** (Monitoring and incident response mechanisms exist) <br> **GOVERN 3.2** (Accountability and oversight established) | **LLM09: Overreliance / Insufficient Oversight** |
| R-009 | Unauthorized Use or Abuse of System | **MAP 4.2** (User interactions and misuse scenarios considered) <br> **MANAGE 1.2** (Access and usage controls implemented) | **LLM08: Excessive Agency** |
| R-010 | Regulatory Non-Compliance (Disclosure / Consumer Protection) | **GOVERN 1.1** (Legal and regulatory requirements identified) <br> **MANAGE 2.1** (Risk response aligned to compliance obligations) | **LLM10: Model Misuse / Legal Risk** |

---

## Key Observations

### 1. Prompt Injection is a Cross-Functional Failure
R-001 highlights a breakdown across:
- system design (MAP)
- control enforcement (MANAGE)

This is not just a technical issue—it is a governance failure where expected safeguards are not effectively implemented or validated.

---

### 2. Data Risk is Central to RAG Architectures
R-002 and R-005 show that:
- data source control
- data integrity validation

are critical to managing AI risk in retrieval-based systems.

The system is only as secure as the documents it retrieves.

---

### 3. Integrity and Output Risk Drive Regulatory Exposure
R-003 and R-004 directly connect to:
- misleading outputs
- potential financial harm
- compliance violations

These risks are central to regulatory scrutiny in financial services environments.

---

### 4. Monitoring is a Critical Control Gap
R-008 demonstrates a key weakness:
- lack of real-time detection
- lack of auditability

Without monitoring, organizations cannot:
- detect harmful outputs
- respond to incidents
- demonstrate compliance

---

### 5. Not All Risks Map Cleanly to OWASP
R-007 (availability) is intentionally not mapped to OWASP LLM Top 10.

This reflects an important insight:
- OWASP focuses on **LLM-specific risks**
- governance must also account for **traditional system risks**

---

## Conclusion

This mapping demonstrates that:
- each identified risk aligns to recognized governance frameworks
- AI-specific risks (OWASP) and enterprise governance controls (NIST AI RMF) must be used together
- effective AI governance requires both **technical validation** and **framework-based risk management**

This mapping will be expanded and refined after adversarial testing in later phases.
