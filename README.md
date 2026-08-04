# E2B (e2b-dev)

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

E2B (e2b-dev) provides secure, isolated cloud sandboxes for AI agents and AI-generated code, built on a forked Firecracker microVM runtime. The platform ships a REST Sandbox API, JavaScript and Python SDKs, a Code Interpreter SDK, a Desktop Sandbox for computer-use agents, persistent volumes, a custom template build system, and an e2b CLI. The Apache-2.0 licensed core repos — E2B, infra, firecracker, code-interpreter, and desktop — also support self-hosted deployments on AWS, GCP, Azure, or bare Linux. E2B is LLM-agnostic and used by labs and enterprises building code interpreters, deep-research agents, data analysis features, reinforcement-learning environments, and computer-use agents.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/e2b-dev/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/e2b-dev/refs/heads/main/apis.yml)

## Scope

- **Position:** Consuming
- **Access:** 3rd-Party

## Tags

- AI
- Agents
- Code Execution
- Code Interpreter
- Sandboxes
- Firecracker
- microVMs
- Computer Use
- Desktop Sandbox
- Templates
- MCP
- Open Source

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-30

## APIs

### E2B Sandbox API

Create, control, and tear down isolated Firecracker microVMs on demand for AI agents. Sandboxes cold-start in under 200ms and run for up to 24 hours, supporting pause/resume/snapshot, metadata, env vars, metrics, log streaming, and connect upgrades. The same surface backs the JavaScript and Python SDKs as well as the e2b CLI.

- **Human URL:** [https://e2b.dev/docs](https://e2b.dev/docs)
- **Base URL:** `https://api.e2b.app`

#### Tags

- AI
- Agents
- Sandboxes
- Code Execution
- Firecracker
- microVMs

#### Properties

- [Documentation](https://e2b.dev/docs)
- [Documentation](https://e2b.dev/docs/sandbox)
- [Documentation](https://e2b.dev/docs/sandbox/api/lifecycle)
- [Documentation](https://e2b.dev/docs/sandbox/persistence)
- [Documentation](https://e2b.dev/docs/sandbox/lifecycle-events-webhooks)
- [Documentation](https://e2b.dev/docs/sandbox/lifecycle-events-api)
- [OpenAPI](openapi/e2b-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/e2b-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [OpenAPI](openapi/e2b-events-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/e2b-events.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-events.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/e2b-sandbox-schema.json) — [JSON Schema](https://json-schema.org/specification)
- [JSON-LD](json-ld/e2b-dev-context.jsonld) — [JSON-LD](https://www.w3.org/TR/json-ld11/)

### E2B Template API

Define, build, version, and publish reusable sandbox base images. Templates are built from an e2b.toml or programmatic SDK definition, cache layers across builds, support custom CPU and RAM, expose namespace/alias aliasing, and can be marked public or team-private. Builds expose status and streaming logs via the API and the e2b CLI.

- **Human URL:** [https://e2b.dev/docs/sandbox-template](https://e2b.dev/docs/sandbox-template)
- **Base URL:** `https://api.e2b.app`

#### Tags

- AI
- Agents
- Templates
- Sandboxes
- Build

#### Properties

- [Documentation](https://e2b.dev/docs/sandbox-template)
- [Documentation](https://e2b.dev/docs/cli)
- [OpenAPI](openapi/e2b-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/e2b-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [JSON Schema](json-schema/e2b-template-schema.json) — [JSON Schema](https://json-schema.org/specification)

### E2B Volume API

Provision and manage persistent volumes that can be attached to sandboxes so agent state, datasets, and workspaces survive across sandbox runs. The Volume Content API uses a short-lived JWT to read and write files and directories inside a mounted volume from any sandbox or external client.

- **Human URL:** [https://e2b.dev/docs/sandbox/persistence](https://e2b.dev/docs/sandbox/persistence)
- **Base URL:** `https://api.e2b.app`

#### Tags

- AI
- Agents
- Storage
- Volumes
- Persistence

#### Properties

- [Documentation](https://e2b.dev/docs/sandbox/persistence)
- [OpenAPI](openapi/e2b-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/e2b-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [OpenAPI](openapi/e2b-volumes-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/e2b-volumes.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-volumes.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### E2B Sandbox Events and Webhooks API

REST surface for sandbox lifecycle events. Exposes polling endpoints at /events/sandboxes and /events/sandboxes/{sandboxID} for created, updated, killed, paused, resumed, and checkpointed events, and a webhook subscription surface at /events/webhooks for push delivery. Webhook deliveries are signed with a SHA-256 HMAC-style hash of the shared secret concatenated with the raw body, sent in the e2b-signature header alongside e2b-webhook-id, e2b-delivery-id, and e2b-signature-version.

- **Human URL:** [https://e2b.dev/docs/sandbox/lifecycle-events-webhooks](https://e2b.dev/docs/sandbox/lifecycle-events-webhooks)
- **Base URL:** `https://api.e2b.app`

#### Tags

- AI
- Agents
- Events
- Webhooks
- Lifecycle

#### Properties

- [Documentation](https://e2b.dev/docs/sandbox/lifecycle-events-webhooks)
- [Documentation](https://e2b.dev/docs/sandbox/lifecycle-events-api)
- [OpenAPI](openapi/e2b-events-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/e2b-events.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-events.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### E2B Team and Identity API

Manage E2B team identity, API keys, and CLI access tokens. API keys authenticate SDK and REST traffic via the X-API-Key header. Access tokens authenticate the e2b CLI and CI workflows. Team metrics expose aggregated sandbox usage counts for the workspace.

- **Human URL:** [https://e2b.dev/docs/api-key](https://e2b.dev/docs/api-key)
- **Base URL:** `https://api.e2b.app`

#### Tags

- AI
- Agents
- Teams
- Administration
- API Keys

#### Properties

- [Documentation](https://e2b.dev/docs/api-key)
- [OpenAPI](openapi/e2b-api-openapi.yml) — [OpenAPI Specification](https://spec.openapis.org/oas/latest.html)
- [Postman Collection](collections/e2b-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### E2B Code Interpreter SDK

Higher-level SDK on top of the Sandbox API that exposes a Jupyter-style code interpreter for LLM-driven Python and JavaScript execution. Returns structured execution results including stdout, stderr, text, png, jpeg, svg, html, markdown, latex, json, javascript, pdf and chart outputs that map cleanly onto tool-use schemas for Anthropic, OpenAI, Mistral, Llama and other model providers.

- **Human URL:** [https://github.com/e2b-dev/code-interpreter](https://github.com/e2b-dev/code-interpreter)

#### Tags

- AI
- Agents
- Code Interpreter
- Jupyter
- Data Analysis

#### Properties

- [Documentation](https://github.com/e2b-dev/code-interpreter)
- [Documentation](https://e2b.dev/docs/code-interpreting/analyze-data-with-ai)
- [SDK](https://github.com/e2b-dev/code-interpreter)
- [Postman Collection](collections/e2b-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/e2b-events.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-events.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/e2b-volumes.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-volumes.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

### E2B Desktop Sandbox SDK

Sandbox flavor that boots a Linux desktop environment with a noVNC stream and exposes mouse, keyboard, screenshot, and window-management primitives. Built for computer-use agents pairing vision-capable models like Claude and GPT with a real graphical desktop they can drive end to end.

- **Human URL:** [https://github.com/e2b-dev/desktop](https://github.com/e2b-dev/desktop)

#### Tags

- AI
- Agents
- Desktop
- Computer Use
- GUI

#### Properties

- [Documentation](https://github.com/e2b-dev/desktop)
- [SDK](https://github.com/e2b-dev/desktop)
- [Postman Collection](collections/e2b-api.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-api.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/e2b-events.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-events.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)
- [Postman Collection](collections/e2b-volumes.postman_collection.json) — [Postman Collection 2.1](https://schema.getpostman.com/json/collection/v2.1.0/collection.json)
- [Open Collection](collections/e2b-volumes.opencollection.json) — [Open Collection 1.0](https://schema.opencollection.com/opencollection/v1.0.0.json)

## Common Properties

- [Portal](https://e2b.dev)
- [Documentation](https://e2b.dev/docs)
- [Getting Started](https://e2b.dev/docs/quickstart)
- [API Reference](https://e2b.dev/docs/sdk-reference)
- [Authentication](https://e2b.dev/docs/api-key)
- [Documentation](https://e2b.dev/docs/cli)
- [Portal](https://e2b.dev/dashboard)
- [Authentication](https://e2b.dev/dashboard?tab=keys)
- [Sign Up](https://e2b.dev/auth/sign-up)
- [Blog](https://e2b.dev/blog)
- [Changelog](https://e2b.dev/changelog)
- [Support](https://e2b.dev/contact)
- [Terms of Service](https://e2b.dev/terms)
- [Privacy Policy](https://e2b.dev/privacy)
- [Trust Center](https://e2b.dev/security)
- [Twitter](https://x.com/e2b_dev)
- [LinkedIn](https://www.linkedin.com/company/e2b-dev)
- [Forum](https://discord.gg/U7KEcGErtQ)
- [GitHub Organization](https://github.com/e2b-dev)
- [GitHub Repository](https://github.com/e2b-dev/E2B)
- [GitHub Repository](https://github.com/e2b-dev/infra)
- [GitHub Repository](https://github.com/e2b-dev/firecracker)
- [GitHub Repository](https://github.com/e2b-dev/code-interpreter)
- [GitHub Repository](https://github.com/e2b-dev/desktop)
- [GitHub Repository](https://github.com/e2b-dev/surf)
- [GitHub Repository](https://github.com/e2b-dev/fragments)
- [GitHub Repository](https://github.com/e2b-dev/ai-analyst)
- [GitHub Repository](https://github.com/e2b-dev/open-computer-use)
- [Code Examples](https://github.com/e2b-dev/e2b-cookbook)
- [GitHub Repository](https://github.com/e2b-dev/dashboard)
- [GitHub Repository](https://github.com/e2b-dev/docs)
- [GitHub Repository](https://github.com/e2b-dev/awesome-ai-agents)
- [GitHub Repository](https://github.com/e2b-dev/awesome-ai-sdks)
- [GitHub Repository](https://github.com/e2b-dev/awesome-mcp-gateways)
- [SDK](https://www.npmjs.com/package/e2b)
- [SDK](https://www.npmjs.com/package/@e2b/code-interpreter)
- [SDK](https://pypi.org/project/e2b/)
- [SDK](https://pypi.org/project/e2b-code-interpreter/)
- [SDK](https://pypi.org/project/e2b-desktop/)
- [SDK](https://www.npmjs.com/package/@e2b/desktop)
- [C L I](https://www.npmjs.com/package/@e2b/cli)
- [Plans](plans/e2b-dev-plans-pricing.yml)
- [Rate Limits](rate-limits/e2b-dev-rate-limits.yml)
- [Fin Ops](finops/e2b-dev-finops.yml)
- [Features](undefined)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
**URL:** https://apievangelist.com
