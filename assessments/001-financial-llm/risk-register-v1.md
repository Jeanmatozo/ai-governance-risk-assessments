# Risk Register v1 — Customer-Facing Financial LLM (RAG-Based)

This risk register identifies and evaluates key risks associated with the deployment of a customer-facing LLM assistant connected to internal policy documents via a RAG architecture.

Scoring:
- Likelihood (L): 1 (Rare) → 5 (Almost Certain)  
- Impact (I): 1 (Low) → 5 (Severe)  
- Inherent Risk Score = L × I  

---

## Risk Register

| ID | Risk Name | Description | L | I | Score | Risk Owner | Current Controls |
|----|----------|------------|---|---|-------|------------|------------------|
| R-001 | Prompt Injection Leading to Policy Manipulation | External users may craft inputs that override system instructions, causing the model to ignore constraints and produce unintended or misleading responses. | 4 | 5 | 20 | AI Product / Security | Basic system prompt constraints |
| R-002 | RAG Data Leakage (Confidentiality Breach) | The retrieval layer may surface internal policy documents or content not intended for external users, leading to unintended disclosure. | 3 | 5 | 15 | Security / Compliance | Curated document corpus (manual review) |
| R-003 | Hallucinated Financial Information | The model may generate incorrect or fabricated financial explanations not grounded in retrieved documents, misleading users. | 4 | 4 | 16 | Product / Compliance | General disclaimers in UI |
| R-004 | Misinterpretation as Financial Advice | Users may interpret responses as personalized investment advice despite system disclaimers, creating regulatory exposure. | 4 | 5 | 20 | Compliance / Legal | Disclaimer: “Not financial advice” |
| R-005 | RAG Context Poisoning | Malicious or compromised documents in the knowledge base may influence model outputs, leading to manipulated or harmful responses. | 3 | 5 | 15 | Security / Data Governance | Controlled ingestion process (limited validation) |
| R-006 | Inconsistent or Biased Responses | The model may provide inconsistent or biased explanations depending on phrasing, leading to fairness concerns and reputational risk. | 3 | 3 | 9 | Product / Risk | None formally defined |
| R-007 | System Availability / Service Disruption | Failures in LLM API, retrieval system, or infrastructure may lead to downtime or degraded performance for users. | 3 | 3 | 9 | Engineering | Cloud redundancy (basic) |
| R-008 | Lack of Output Monitoring and Auditability | The organization may lack sufficient logging and monitoring to detect harmful or non-compliant outputs in real time. | 4 | 4 | 16 | Security / Compliance | Limited logging of user queries |
| R-009 | Unauthorized Use or Abuse of System | Users may intentionally misuse the system (e.g., probing for sensitive data, generating misleading content). | 4 | 3 | 12 | Security | Basic rate limiting |
| R-010 | Regulatory Non-Compliance (Consumer Protection / Disclosure) | The system may produce responses that violate financial regulations related to disclosures, accuracy, or customer communication standards. | 3 | 5 | 15 | Compliance / Legal | Manual policy review during development |

---

## Observations

- The highest-risk areas are concentrated in:
  - Prompt injection and manipulation (R-001)
  - Misinterpretation as financial advice (R-004)
  - Integrity failures (R-003)
  
- Several risks currently rely on **weak controls**:
  - Disclaimers (not sufficient control)
  - Manual document curation
  - Basic system prompts

- There is a **notable gap in monitoring and detection capabilities**, particularly for:
  - harmful outputs
  - policy violations
  - adversarial behavior

---

## Next Steps

This initial register will be:
- mapped to NIST AI RMF and OWASP LLM Top 10 (control-mapping-v1.md)
- expanded and refined based on adversarial testing findings (Weeks 3–5)
- consolidated into a final version (risk-register-v2.md)
