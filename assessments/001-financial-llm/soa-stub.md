# Statement of Applicability (SoA) — ISO/IEC 42001:2023  
## Scenario: Financial LLM Deployment (Internal Advisory Assistant)

---

## Overview
This Statement of Applicability (SoA) identifies which ISO/IEC 42001 Annex A controls are applicable to the financial LLM deployment under assessment. Each control is evaluated based on system context, risk exposure, and operational use.

Status definitions:
- **Applicable** → Control is required for this system
- **Partially Applicable** → Control is relevant but not fully implemented or conditional
- **Not Applicable** → Control does not apply based on system scope

---

## Annex A — Control Applicability

| Control ID | Control Area | Applicability | Justification |
|-----------|-------------|--------------|--------------|
| A.5.1 | AI Risk Management Framework | Applicable | The system introduces financial and compliance risks requiring formal risk management processes aligned with AI governance standards. |
| A.5.2 | AI Policy | Applicable | A defined policy is required to establish acceptable use, risk tolerance, and governance expectations for AI-assisted financial decisions. |
| A.5.3 | Roles and Responsibilities | Applicable | Clear ownership is required to manage model behavior, outputs, and risk accountability across business and technical teams. |
| A.5.4 | AI System Inventory | Applicable | The organization must maintain an inventory of AI systems for oversight, regulatory alignment, and audit traceability. |
| A.5.5 | Risk Assessment Process | Applicable | Continuous risk assessment is required due to evolving model behavior and changing financial data inputs. |
| A.5.6 | Risk Treatment | Applicable | Identified risks (e.g., hallucinations, incorrect guidance) must be mitigated through controls and governance processes. |
| A.5.7 | Impact Assessment | Applicable | The system influences financial decisions, requiring evaluation of potential operational and regulatory impact. |
| A.5.8 | Data Governance | Applicable | The system processes potentially sensitive financial data, requiring controls over data quality, access, and protection. |
| A.5.9 | Data Quality Management | Applicable | Model outputs depend on input data quality, making data validation essential to reduce inaccurate responses. |
| A.5.10 | Model Development & Acquisition | Partially Applicable | If using third-party models, development control is limited but evaluation and selection criteria still apply. |
| A.5.11 | System Integration | Applicable | Integration with internal systems and data sources introduces risk that must be managed and validated. |
| A.5.12 | Change Management | Applicable | Updates to prompts, models, or data sources can impact outputs and must be controlled and tracked. |
| A.5.13 | Monitoring and Logging | Applicable | Continuous monitoring is required to detect incorrect outputs, misuse, and system drift. |
| A.5.14 | Incident Management | Applicable | The organization must detect, respond to, and document harmful or incorrect AI outputs. |
| A.5.15 | Human Oversight | Applicable | Financial decision support requires human validation to prevent over-reliance on AI outputs. |
| A.5.16 | Transparency | Applicable | Users must be informed that outputs are AI-generated and understand system limitations. |
| A.5.17 | Explainability | Partially Applicable | Full explainability may be limited, but sufficient context must be provided to support decision-making. |
| A.5.18 | Security Controls | Applicable | Controls are required to prevent data leakage, unauthorized access, and manipulation of inputs/outputs. |
| A.5.19 | Third-Party Management | Partially Applicable | Applicable if external LLM providers or APIs are used; requires vendor risk assessment and oversight. |
| A.5.20 | Compliance & Legal | Applicable | The system must align with financial regulations and avoid misleading or non-compliant outputs. |

---

## Key Observations

- The majority of controls are **fully applicable** due to the system’s role in financial decision support.
- **Partially applicable controls** are primarily related to:
  - third-party model usage
  - explainability limitations inherent to LLMs
- The most critical control areas are:
  - risk management  
  - data governance  
  - human oversight  
  - monitoring and incident response  

---

## Conclusion

This SoA demonstrates that ISO/IEC 42001 controls are broadly applicable to LLM-based financial systems due to their impact on decision-making, data handling, and organizational risk exposure.

The effectiveness of governance depends not only on control selection but on how these controls are operationalized within the AI lifecycle.
