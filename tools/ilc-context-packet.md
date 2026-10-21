---
slug: "ilc-context-packet"
name: "ILC Context Packet"
description: "A stateless context API for passing user-selected, caller-controlled context to an assistant."
agentSummary: "An app loads the context a person chose from the app or device store or its own PostgreSQL database, then POSTs selected items to ILC for a structured packet. The API does not receive database credentials, access that storage, persist the packet, or run the model; the caller decides what to share and how the assistant interprets it."
seoTitle: "ILC Context Packet: User-Controlled Context for AI Agents"
seoDescription: "A free REST endpoint packages selected personal context for downstream AI assistants while the integrating app retains storage access and control."
category: "long-term-memory-state-management"
tags:
  - "user-context"
  - "agent-memory"
  - "privacy-controls"
websiteUrl: "https://ilc-x402-api-1.onrender.com/agents"
githubUrl: "https://github.com/ILC-API-code/ilc-x402-api"
pricing: "free"
classification: "agent-enabling"
entityType: "web-api"
developerName: "ILC"
docsUrl: "https://ilc-x402-api-1.onrender.com/openapi.json"
interfaces:
  - "REST API"
deploymentModes:
  - "hosted"
verificationLevel: "documentation-reviewed"
classificationRationaleMd: "The endpoint is specifically designed to structure user-selected context with its source and confirmation metadata for an assistant workflow. It gives agent builders a reusable contract for using context from a store controlled by the caller, rather than generic access to an unrelated API."
bestForMd: "Builders of AI assistants or notes apps that already retain user context on a device or in their own database and want to pass only selected context into a model request."
limitationsMd: "This listing covers the stateless packet route. The calling application must load and retain context, select what to send, and verify its own storage. The endpoint does not read device or user PostgreSQL storage, verify context claims, run model inference, or persist the request. Other ILC API routes have their own availability and pricing."
unknownsMd: "Third-party integrations, adoption, and comparative user demand have not been established. The API does not verify caller-owned storage."
evidenceSources:
  - title: "Published ILC capability map"
    url: "https://ilc-x402-api-1.onrender.com/capabilities"
    claim: "The live capability map lists POST /api/v1/context/packet as a free stateless operation that does not require an ILC tenant key or persistent-memory database."
    accessedAt: "2026-10-21"
    sourceType: "official-documentation"
  - title: "ILC context packet API schema"
    url: "https://ilc-x402-api-1.onrender.com/openapi.json"
    claim: "The published OpenAPI schema documents the context packet request and response contract."
    accessedAt: "2026-10-21"
    sourceType: "official-documentation"
  - title: "ILC user-controlled context documentation"
    url: "https://github.com/ILC-API-code/ilc-x402-api/blob/main/README.md"
    claim: "Project documentation describes client/device-managed and user-owned PostgreSQL context; the caller selects and sends context while retaining storage credentials and responsibility."
    accessedAt: "2026-10-21"
    sourceType: "official-repository"
---

ILC Context Packet structures context selected by the user in the calling app. The app retains access to its device or PostgreSQL store and sends only the context selected for the current request.

## So agents can...

- Receive a context packet assembled from notes held in a client-controlled store.
- Use user-confirmed context with caller-supplied source information.
- Leave storage, model selection, and interpretation with the integrating app.
