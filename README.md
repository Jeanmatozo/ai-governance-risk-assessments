# ai-governance-risk-assessments

**AI system risk assessment packages aligned to NIST AI RMF, 
ISO/IEC 42001, OMB M-24-10, and OWASP LLM Top 10.**

This repository contains governance-focused AI risk assessments.  
All adversarial testing and attack simulations are maintained separately in:

https://github.com/Jeanmatozo/llm-adversarial-findings

---

## Assessment Index

| # | Scenario | Key Outputs | Status |
|---|---|---|---|
| 001 | Financial services LLM assistant | Scenario definition · Risk register · Control mapping · ISO 42001 SoA · Gap analysis | Completed |
| 002 | Federal contractor CUI deployment | CMMC domain mapping · AI gap analysis · SSP addendum | Planned |
| 003 | SEC AI disclosure — financial sector | Disclosure triggers · monitoring framework · risk cross-reference | Planned |
| 004 | Healthcare guardrail evaluation | Deployment scope · guardrail test plan · assurance statement | Planned |

---

## Repository Structure

```bash
assessments/
├── 001-financial-llm/
│   # Core Governance (Week 1–2)
│   ├── scenario-brief.md
│   ├── risk-categories.md
│   ├── risk-register-v1.md
│   ├── control-mapping-v1.md
│   ├── exec-summary-v1.md
│   ├── iso42001-applicability-notes.md
│   ├── soa-stub.md
│   ├── cross-framework-mapping.md
│   ├── gap-analysis-v1.md

```
---

## Framework Coverage

**NIST AI RMF 1.0** — Govern · Map · Measure · Manage  
**ISO/IEC 42001:2023** — AI management system controls  
**ISO/IEC 27001:2022** — Information security baseline  
**OMB M-24-10** — Federal AI impact assessment structure  
**OWASP LLM Top 10 (2025)** — Vulnerability classification  
**CMMC 2.0** — Federal contractor compliance  
**SEC Rule 33-11216** — AI disclosure risk mapping  

---


