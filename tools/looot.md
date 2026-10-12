---
slug: "looot"
name: "looot"
description: "One API key and prepaid balance for about 2,500 data endpoints, exposed to agents over a remote MCP server, CLI and REST API"
category: "api-access-orchestration-layers"
tags:
  - "mcp"
  - "data-api"
  - "enrichment"
  - "search"
  - "prepaid"
websiteUrl: "https://looot.ai"
githubUrl: "https://github.com/loootai/looot-mcp"
pricing: "paid"
classification: "agent-enabling"
entityType: "web-api"
developerName: "looot"
docsUrl: "https://docs.looot.ai"
pricingUrl: "https://docs.looot.ai/get-started/pricing-basics"
interfaces:
  - "REST API"
  - "MCP"
  - "CLI"
deploymentModes:
  - "hosted"
evidenceSources:
  - title: "looot documentation"
    url: "https://docs.looot.ai/"
    claim: "The documentation describes one catalog of external data APIs behind one token and one prepaid balance, reachable from the web, the CLI, a remote MCP server and a REST API, with search, price inspection and run steps for agents."
    accessedAt: "2026-10-12"
    sourceType: "official-documentation"
  - title: "looot MCP quickstart"
    url: "https://docs.looot.ai/get-started/quickstart-mcp"
    claim: "The quickstart documents adding the hosted looot MCP server to Claude Code, signing in with the browser, checking the balance, searching the catalog and running a job with fallback."
    accessedAt: "2026-10-12"
    sourceType: "official-documentation"
  - title: "looot pricing basics"
    url: "https://docs.looot.ai/get-started/pricing-basics"
    claim: "looot is prepaid, charged per call or per result, with $0 on failure and no subscription."
    accessedAt: "2026-10-12"
    sourceType: "official-pricing"
  - title: "looot-mcp repository"
    url: "https://github.com/loootai/looot-mcp"
    claim: "The public MIT-licensed repository holds the TypeScript MCP bridge, server.json and install steps for the hosted looot MCP server."
    accessedAt: "2026-10-12"
    sourceType: "official-repository"
verificationLevel: "documentation-reviewed"
classificationRationaleMd: "The service is a hosted data API that agents call through MCP, CLI or REST; it enables agent workflows rather than acting as an autonomous agent."
inclusionRationaleMd: "Agents can search a catalog of data endpoints, read the price before a call, and run a job with provider fallback under one credential."
bestForMd: "Agent builders who need work email, phone, company and people enrichment, Google SERP or web page data without managing a key per provider."
notBestForMd: "Teams that need a free tier, a subscription plan, or a single provider's full native API."
limitationsMd: "looot is prepaid with a $5 minimum top-up and no free tier. Provider coverage and per-call prices vary by endpoint; check the price on the catalog row before running."
unknownsMd: "No independent benchmark of data accuracy or provider fallback success rates was reviewed."
---

looot is a hosted data API with a remote MCP server at https://api.looot.ai/mcp. One API key and one prepaid balance cover about 2,500 endpoints from 90+ providers, including work email, phone, company and people enrichment, Google SERP, web search and web page reading.

## So agents can...

- search the catalog in plain words and read an endpoint's price before running it
- run a job and let looot pick a provider, with fallback to the next one on a miss
- pay only for calls that completed, with a receipt for each attempt
