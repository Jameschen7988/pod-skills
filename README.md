# pod-config

Dependency-free Claude Code config for a remote/containerized agent (OpenAB on K8s).
Auto-synced into the pod on boot via an init container.

- `AGENTS.md` — the pod's identity (CEO + multi-role org, working rules)
- `agents/` — native subagent definitions (CEO, COO, CTO, CFO, CMO, dev, qa, designer, PM, etc.)
- `skills/` — pure-instruction skills (ponytail, pyramid-principle, co-architect, yc-pipeline, ...)

All de-identified. No MCP, no credentials, no personal data.
