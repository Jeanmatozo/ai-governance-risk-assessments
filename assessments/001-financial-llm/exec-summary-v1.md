# Executive Summary — Customer-Facing Financial LLM (RAG-Based)

The organization has deployed a customer-facing AI assistant to support client inquiries related to financial products, policies, and general investment concepts. While the system improves accessibility and operational efficiency, it introduces a set of material risks that require immediate governance attention.

Our assessment identified three primary risk areas. First, the system is vulnerable to prompt injection and manipulation, where external users may influence model behavior and bypass intended safeguards. Second, the Retrieval-Augmented Generation (RAG) architecture creates a risk of unintended disclosure of internal policy content if data boundaries are not strictly enforced. Third, the model may generate misleading or incomplete financial information, which users may interpret as actionable guidance despite existing disclaimers.

Current controls are limited and rely heavily on system prompts and user-facing disclaimers, which are not sufficient to manage these risks in a regulated financial environment. Notably, there is no formal monitoring capability to detect harmful outputs or adversarial behavior in real time.

We recommend prioritizing three actions: (1) implement input and output validation controls to mitigate prompt injection and content leakage, (2) establish monitoring and logging mechanisms for model outputs, and (3) formalize governance policies defining acceptable system behavior and accountability. These actions are necessary to reduce regulatory exposure and maintain customer trust.
