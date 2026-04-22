
# Scenario Brief — Customer-Facing Financial LLM (RAG-Based)

## Organization
A U.S.-based financial services firm offering investment products and advisory services to retail and high-net-worth clients.

## System Overview
The organization has deployed a customer-facing AI assistant designed to answer client questions related to financial products, account policies, and general investment concepts.

The system uses a Retrieval-Augmented Generation (RAG) architecture, where user queries are enriched with content retrieved from internal policy documents, product disclosures, and knowledge base materials before being processed by a large language model.

## Users
- External clients (retail investors and high-net-worth individuals)
- Prospective customers interacting via web interface

## Intended Functionality
- Answer questions about financial products and services
- Explain account policies and procedures
- Provide general educational content on investing
- Assist with navigation of firm offerings

The system is explicitly **not intended to provide personalized financial advice**, but operates in a space where responses may influence financial decisions.

## Data Sources
- Internal policy and compliance documents
- Product disclosures and offering documents
- FAQs and support knowledge base
- Public financial education materials

## Data Flow
User query → retrieval system (vector database) → relevant internal documents → LLM generates response → response returned to user interface

## Deployment Context
- Public-facing web application
- Cloud-hosted LLM service
- Retrieval system connected to curated internal document store
- No direct access to client account data (but responses may reference policies impacting accounts)

## Trust Boundaries
- External user input (untrusted)
- Internal document corpus (trusted but not immutable)
- LLM generation layer (non-deterministic behavior)

## Risk Context
The system operates at the intersection of:
- customer trust
- financial decision influence
- regulatory scrutiny

Failures in this system may result in:
- misleading or inappropriate financial guidance
- exposure of sensitive internal policies
- reputational damage and loss of client trust
- regulatory consequences under financial disclosure and consumer protection rules
