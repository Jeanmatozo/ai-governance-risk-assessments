# ai-governance-risk-assessments

**AI system risk assessment packages aligned to NIST AI RMF, 
ISO/IEC 42001, OMB M-24-10, and OWASP LLM Top 10.**

Each assessment is a complete work product: executive summary, system 
description, risk register, control gap analysis, and remediation roadmap. 
Written for two audiences simultaneously — leadership and technical reviewers.

---

## Assessment Index

| # | Scenario | Frameworks | Status |
|---|---|---|---|
| 001 | Financial services LLM assistant | NIST AI RMF · ISO 42001 · OWASP LLM Top 10 | In progress |
| 002 | Federal contractor CUI deployment | CMMC 2.0 · NIST AI RMF | Planned — Week 7 |
| 003 | SEC AI disclosure — financial sector | SEC Rule 33-11216 · NIST AI RMF | Planned — Week 8 |
| 004 | Healthcare guardrail evaluation | HIPAA · OWASP LLM Top 10 | Planned — Week 9 |

---

## Repository Structure

```bash
assessments/
├── 001-financial-llm/
│   ├── exec-summary.md
│   ├── risk-register.md
│   ├── control-mapping.md
│   └── remediation-roadmap.md
├── 002-cmmc-federal/
├── 003-sec-disclosure/
└── 004-healthcare-guardrail/

methodology/
└── assessment-approach.md      ← Published Week 10

templates/
├── risk-register-template.md
└── exec-summary-template.md
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

*Adversarial findings that inform these assessments are documented in 
[llm-adversarial-findings](https://github.com/Jeanmatozo/llm-adversarial-findings)
