# Heddle

**Testable AI workflows for the rest of us.**

Most AI tooling assumes you have a platform team and a Kubernetes
cluster. Heddle assumes you have a laptop — or a few of them — and a
problem to solve. Local-first, privacy-first, on-prem-friendly.

→ **[getheddle.dev](https://getheddle.dev)** for the full overview.

## The project family

| Repository | What it is | Status |
|---|---|---|
| **[heddle](https://github.com/getheddle/heddle)** | The runtime. Python actor-mesh over NATS. Six shipped workers, Workshop web UI, RAG, councils, MCP gateway. Wire-protocol source of truth. | v0.9.2 — active |
| **[heddle-sdk](https://github.com/getheddle/heddle-sdk)** | Foreign-language SDKs. .NET and Swift, with NATS adapters. Write Heddle processor workers in C# or Swift. | In development |
| **[warp-design](https://github.com/getheddle/warp-design)** | Vision and ADRs for *warp* — a macOS-first ad-hoc cluster orchestrator. Pre-implementation; production code lands in `warp` later. | Design phase |
| **[heddle-agent-toolkit](https://github.com/getheddle/heddle-agent-toolkit)** | Shared AI-agent guidance, skills, and subagents for the family. Anchors (philosophy, invariants, contract map) + install.sh. | Stable |

## 60 seconds to your first workflow

```bash
pip install heddle-ai[workshop]
heddle setup                            # auto-detects LM Studio + Ollama
heddle workshop                         # opens localhost:8080
```

Pick a worker in the browser, paste any text, click Run. When you're
ready to scale, Heddle adds a NATS message bus for production use.

## What makes Heddle different

- **Solo / SMB first.** No platform team required. No Kubernetes
  prerequisite. The headline user can install a CLI, edit YAML, and
  run a workflow in a browser.
- **Three model tiers.** Local (LM Studio / Ollama), standard (Claude
  Sonnet), frontier (Claude Opus). Pick cost and privacy per step.
- **Privacy by default.** Workloads tagged private never leave your
  machines. Knowledge silos and blind audit patterns prevent the same
  model from reviewing its own work.
- **Typed contracts everywhere.** Pydantic messages and per-worker
  JSON Schemas are the only safety net between actors. No untyped
  dicts on the wire.
- **Stateless workers, deterministic router.** Horizontal scaling
  without coordination; LLM-free dispatch in sub-millisecond.

## Built with Heddle

- **[Baft](https://github.com/IranTransitionProject/baft)** — Multi-agent
  analytical engine for the Iran Transition Project.
- **[Docman](https://github.com/IranTransitionProject/docman)** — Document
  processing pipeline (PDF/DOCX extraction, classification, vector search).

*Building something with Heddle? Open a discussion in
[`heddle`](https://github.com/getheddle/heddle/discussions) — we'd
like to hear about it.*

## License

[MPL 2.0](https://github.com/getheddle/heddle/blob/main/LICENSE).
Modified source files must remain open; unmodified files can be
combined with proprietary code.
