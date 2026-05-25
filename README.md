# E2B (e2b-dev)

E2B (e2b-dev) provides secure, isolated cloud sandboxes for AI agents and AI-generated code, built on a forked Firecracker microVM runtime. The platform ships a REST Sandbox API, JavaScript and Python SDKs, a Code Interpreter SDK, a Desktop Sandbox for computer-use agents, persistent volumes, a custom template build system, and an e2b CLI. The Apache-2.0 licensed core repos — E2B, infra, firecracker, code-interpreter, and desktop — also support self-hosted deployments on AWS, GCP, Azure, or bare Linux. E2B is LLM-agnostic and used by labs and enterprises building code interpreters, deep-research agents, data analysis features, reinforcement-learning environments, and computer-use agents.

**URL:** [Visit APIs.json](https://raw.githubusercontent.com/api-evangelist/e2b-dev/refs/heads/main/apis.yml)

**Run:** [Capabilities Using Naftiko](https://github.com/naftiko/fleet?utm_source=api-evangelist&utm_medium=readme&utm_campaign=company-api-evangelist&utm_content=repo)

## Tags

 - AI, Agents, Code Execution, Code Interpreter, Sandboxes, Firecracker, microVMs, Computer Use, Desktop Sandbox, Templates, MCP, Open Source

## Timestamps

- **Created:** 2026-05-25
- **Modified:** 2026-05-25

## APIs

### E2B Sandbox API
Create, control, and tear down isolated Firecracker microVMs on demand for AI agents. Sandboxes cold-start in under 200ms and run for up to 24 hours, supporting pause/resume/snapshot, metadata, env vars, metrics, log streaming, and connect upgrades. The same surface backs the JavaScript and Python SDKs as well as the e2b CLI.

**Human URL:** [https://e2b.dev/docs](https://e2b.dev/docs)
**Base URL:** `https://api.e2b.app`

- [Documentation](https://e2b.dev/docs)
- [Documentation — Sandbox](https://e2b.dev/docs/sandbox)
- [Documentation — Lifecycle](https://e2b.dev/docs/sandbox/api/lifecycle)
- [Documentation — Persistence](https://e2b.dev/docs/sandbox/persistence)
- [OpenAPI](openapi/e2b-api-openapi.yml)
- [JSON Schema — Sandbox](json-schema/e2b-sandbox-schema.json)
- [JSON-LD](json-ld/e2b-dev-context.jsonld)
- [Naftiko Capability — Sandboxes](capabilities/sandboxes-sandboxes.yaml)
- [Naftiko Capability — Lifecycle](capabilities/sandboxes-lifecycle.yaml)
- [Naftiko Capability — Metrics](capabilities/sandboxes-metrics.yaml)

### E2B Template API
Define, build, version, and publish reusable sandbox base images. Templates are built from an `e2b.toml` or programmatic SDK definition, cache layers across builds, support custom CPU and RAM, expose namespace/alias aliasing, and can be marked public or team-private. Builds expose status and streaming logs via the API and the e2b CLI.

**Human URL:** [https://e2b.dev/docs/sandbox-template](https://e2b.dev/docs/sandbox-template)

- [Documentation](https://e2b.dev/docs/sandbox-template)
- [Documentation — CLI](https://e2b.dev/docs/cli)
- [OpenAPI](openapi/e2b-api-openapi.yml)
- [JSON Schema — Template](json-schema/e2b-template-schema.json)
- [Naftiko Capability — Templates](capabilities/templates-templates.yaml)
- [Naftiko Capability — Builds](capabilities/templates-builds.yaml)
- [Naftiko Capability — Tags and Aliases](capabilities/templates-tags.yaml)

### E2B Volume API
Provision and manage persistent volumes that can be attached to sandboxes so agent state, datasets, and workspaces survive across sandbox runs. The Volume Content API uses a short-lived JWT to read and write files and directories inside a mounted volume from any sandbox or external client.

**Human URL:** [https://e2b.dev/docs/sandbox/persistence](https://e2b.dev/docs/sandbox/persistence)

- [Documentation](https://e2b.dev/docs/sandbox/persistence)
- [OpenAPI — Platform](openapi/e2b-api-openapi.yml)
- [OpenAPI — Volume Content](openapi/e2b-volumes-openapi.yml)
- [Naftiko Capability — Volumes](capabilities/volumes-volumes.yaml)
- [Naftiko Capability — Volume Content](capabilities/volumes-content.yaml)

### E2B Team and Identity API
Manage E2B team identity, API keys, and CLI access tokens. API keys authenticate SDK and REST traffic via the `X-API-Key` header. Access tokens authenticate the e2b CLI and CI workflows. Team metrics expose aggregated sandbox usage counts for the workspace.

**Human URL:** [https://e2b.dev/docs/api-key](https://e2b.dev/docs/api-key)

- [Documentation](https://e2b.dev/docs/api-key)
- [OpenAPI](openapi/e2b-api-openapi.yml)
- [Naftiko Capability — Teams](capabilities/teams-teams.yaml)
- [Naftiko Capability — API Keys](capabilities/teams-api-keys.yaml)
- [Naftiko Capability — Access Tokens](capabilities/teams-access-tokens.yaml)

### E2B Code Interpreter SDK
Higher-level SDK on top of the Sandbox API that exposes a Jupyter-style code interpreter for LLM-driven Python and JavaScript execution. Returns structured execution results including stdout, stderr, text, png, jpeg, svg, html, markdown, latex, json, javascript, pdf and chart outputs that map cleanly onto tool-use schemas for Anthropic, OpenAI, Mistral, Llama and other model providers.

**Human URL:** [https://github.com/e2b-dev/code-interpreter](https://github.com/e2b-dev/code-interpreter)

- [Documentation](https://github.com/e2b-dev/code-interpreter)
- [Documentation — Analyze Data With AI](https://e2b.dev/docs/code-interpreting/analyze-data-with-ai)
- [SDK](https://github.com/e2b-dev/code-interpreter)
- [Naftiko Capability — Execute](capabilities/code-interpreter-execute.yaml)

### E2B Desktop Sandbox SDK
Sandbox flavor that boots a Linux desktop environment with a noVNC stream and exposes mouse, keyboard, screenshot, and window-management primitives. Built for computer-use agents pairing vision-capable models like Claude and GPT with a real graphical desktop they can drive end to end.

**Human URL:** [https://github.com/e2b-dev/desktop](https://github.com/e2b-dev/desktop)

- [Documentation](https://github.com/e2b-dev/desktop)
- [SDK](https://github.com/e2b-dev/desktop)
- [Naftiko Capability — Desktop](capabilities/desktop-desktop.yaml)

## Plans, Rate Limits, and FinOps

- [Plans and Pricing](plans/e2b-dev-plans-pricing.yml) — Hobby (free + $100 credit), Pro ($150/mo + per-second usage), Enterprise (custom)
- [Rate Limits](rate-limits/e2b-dev-rate-limits.yml) — Concurrency, session-length, storage, and minimum CPU/RAM per tier
- [FinOps](finops/e2b-dev-finops.yml) — vCPU-second, GiB-second, and storage meters mapped to FOCUS

## SDKs, CLI, and Open Source

- [E2B Core (Python + JS/TS)](https://github.com/e2b-dev/E2B)
- [Infra (Go)](https://github.com/e2b-dev/infra)
- [Firecracker (Rust, forked)](https://github.com/e2b-dev/firecracker)
- [Code Interpreter (Python + JS/TS)](https://github.com/e2b-dev/code-interpreter)
- [Desktop (Python + JS/TS)](https://github.com/e2b-dev/desktop)
- [Surf — computer use agent](https://github.com/e2b-dev/surf)
- [Fragments — AI-generated app template](https://github.com/e2b-dev/fragments)
- [AI Analyst](https://github.com/e2b-dev/ai-analyst)
- [Open Computer Use](https://github.com/e2b-dev/open-computer-use)
- [E2B Cookbook](https://github.com/e2b-dev/e2b-cookbook)
- [Awesome AI Agents](https://github.com/e2b-dev/awesome-ai-agents)
- [Awesome AI SDKs](https://github.com/e2b-dev/awesome-ai-sdks)
- [Awesome MCP Gateways](https://github.com/e2b-dev/awesome-mcp-gateways)

## Common Links

- [Website](https://e2b.dev)
- [Documentation](https://e2b.dev/docs)
- [Quickstart](https://e2b.dev/docs/quickstart)
- [SDK Reference](https://e2b.dev/docs/sdk-reference)
- [Dashboard](https://e2b.dev/dashboard)
- [Sign Up](https://e2b.dev/auth/sign-up)
- [Pricing](https://e2b.dev/pricing)
- [Blog](https://e2b.dev/blog)
- [Changelog](https://e2b.dev/changelog)
- [Discord](https://discord.gg/U7KEcGErtQ)
- [Twitter / X](https://x.com/e2b_dev)
- [LinkedIn](https://www.linkedin.com/company/e2b-dev)
- [GitHub](https://github.com/e2b-dev)
- [Terms](https://e2b.dev/terms)
- [Privacy](https://e2b.dev/privacy)
- [Security](https://e2b.dev/security)
