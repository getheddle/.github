# Heddle

**Open-source AI workflow orchestration.**

Heddle is an actor-based Python framework for orchestrating multi-LLM workflows via NATS messaging. Turn what you know into testable AI steps. Chain them into workflows. Measure whether they work. Scale when ready.

## Get Started

```bash
pip install heddle-ai[workshop]
heddle setup
heddle workshop   # opens web UI at localhost:8080
```

## What Heddle Does

Most AI tools give you one big prompt and one model. Heddle splits AI work into focused, independently testable steps — each with typed contracts, deterministic routing, and the ability to use different models per step.

**Key capabilities:** stateless workers with strict I/O contracts, YAML-driven configuration, knowledge silos for audit independence, multi-agent councils, RAG pipelines, MCP gateway, Workshop web UI for testing without deployment.

## Built with Heddle

- **[Baft](https://github.com/IranTransitionProject/baft)** — Multi-agent analytical engine for the Iran Transition Project
- **[Docman](https://github.com/IranTransitionProject/docman)** — Document processing pipeline (PDF/DOCX extraction, classification, search)

## Links

- **[Heddle Repository](https://github.com/getheddle/heddle)** — Source code, docs, and examples
- **[PyPI: heddle-ai](https://pypi.org/project/heddle-ai/)** — Install via pip
- **License:** [MPL 2.0](https://github.com/getheddle/heddle/blob/main/LICENSE)
