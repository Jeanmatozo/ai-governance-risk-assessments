# ISO/IEC 42001:2023 — Applicability Notes  
## Scenario: Financial LLM Deployment (Internal Advisory Assistant)

---

## Overview
This document evaluates the applicability of ISO/IEC 42001:2023 controls to a financial services LLM deployment. The system provides internal advisory support for financial analysis and decision-making, introducing risks related to data handling, model behavior, and governance oversight.

The goal is not to list all controls exhaustively, but to identify which controls are **material to this deployment**, and explain why they are necessary from a governance and risk perspective.

---

## Scope Considerations
The system under assessment:
- Uses LLM-based responses for financial guidance
- May interact with sensitive or regulated financial data
- Is used by internal staff for decision support
- Introduces risks tied to accuracy, misuse, and lack of explainability

---

## Clause 6 — Planning (Risk-Based Approach)

### 6.1 Actions to Address Risks and Opportunities
**Applicability: HIGH**

This control is foundational. The LLM introduces:
- risk of incorrect financial guidance
- hallucinated outputs presented as facts
- over-reliance by users on AI-generated insights

A structured risk identification and treatment process must exist to ensure risks are documented, assessed, and mitigated.

---

### 6.2 AI Objectives and Planning to Achieve Them
**Applicability: HIGH**

The organization must define:
- acceptable use of the LLM
- accuracy expectations
- boundaries for financial recommendations

Without clear objectives, the system may operate outside acceptable risk tolerance.

---

## Clause 8 — Operation (Lifecycle Controls)

### 8.2 AI System Impact Assessment
**Applicability: HIGH**

The system influences financial decisions, making impact assessment critical.

Key considerations:
- potential financial loss from incorrect outputs
- regulatory exposure (misleading advice)
- internal decision-making reliance

---

### 8.3 Data Management
**Applicability: HIGH**

The LLM relies on:
- training data
- retrieval data (if RAG is used)
- user input

Risks include:
- exposure of sensitive financial data
- ingestion of low-quality or unverified data
- data leakage through model responses

Strong data governance controls are required.

---

### 8.4 AI System Development and Modification
**Applicability: MEDIUM to HIGH**

Changes to:
- prompts
- retrieval sources
- model versions

can significantly alter system behavior.

Change management must ensure:
- testing before deployment
- traceability of modifications
- rollback capability

---

### 8.5 AI System Operation and Monitoring
**Applicability: HIGH**

Continuous monitoring is required to detect:
- hallucinations
- unsafe outputs
- drift in system behavior

Logging and monitoring are essential to:
- identify incidents
- support audits
- improve system reliability

---

### 8.6 AI System Transparency and Explainability
**Applicability: HIGH**

Users must understand:
- that outputs are AI-generated
- limitations of the system
- when human validation is required

Lack of transparency increases risk of:
- over-trust
- misuse of outputs

---

### 8.7 Human Oversight
**Applicability: HIGH**

Given the financial context:
- outputs should not be fully autonomous
- human validation should be required for high-impact decisions

This control directly reduces:
- operational risk
- compliance risk

---

### 8.8 Incident Management
**Applicability: HIGH**

The organization must be able to:
- detect harmful outputs
- respond to incidents
- document and remediate failures

Examples:
- incorrect financial guidance
- data exposure through responses

---

## Annex A — Control Applicability Summary

| Control Area | Applicability | Notes |
|-------------|--------------|------|
| Risk Management | High | Core to identifying financial and operational exposure |
| Data Governance | High | Critical due to sensitive financial data |
| System Transparency | High | Prevents over-reliance and misuse |
| Human Oversight | High | Required for financial decision contexts |
| Monitoring & Logging | High | Needed for detection and auditability |
| Change Management | Medium-High | Important due to model and prompt variability |
| Third-Party Management | Medium | Depends on external model/vendor usage |
| Security Controls | High | Protects against data leakage and misuse |

---

## Key Observations

1. Most ISO 42001 controls are **directly applicable** due to the high-risk nature of financial decision support systems.

2. The highest priority areas for this deployment are:
   - data governance  
   - human oversight  
   - monitoring and incident response  

3. The primary risk is not system failure alone, but **misplaced trust in system outputs**, which ISO 42001 addresses through transparency and oversight requirements.

---

## Conclusion

ISO/IEC 42001 provides a structured approach to governing AI systems, but its effectiveness depends on how controls are applied to real system risks.

In this scenario, the LLM introduces:
- decision risk  
- data risk  
- trust risk  

The applicable controls focus on ensuring that:
- risks are identified and managed
- system behavior is monitored and controlled
- human judgment remains central in high-impact decisions
