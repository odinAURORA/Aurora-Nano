Aurora Nano v0.1 — Research Preview

Aurora Nano is a lightweight runtime and evaluation framework designed to improve consistency, contradiction handling, escalation decisions, and structured reasoning for small language models.

The project explores a simple idea:

Can a small model paired with a deterministic runtime perform more reliably than the model alone?

Aurora Nano separates language generation from decision structure. Models are used for extraction and interpretation, while the Aurora runtime provides deterministic processing for contradiction detection, routing, confidence assessment, policy-aware handling, and auditability.

Key Features

- Lightweight runtime for small language models (3B–7B class)
- Contradiction and conflict detection
- Structured claim extraction workflows
- JSON validation and repair utilities
- Benchmark and evaluation framework
- Model-only vs runtime+model comparison tooling
- Android and local-device testing support
- Compute and latency audit tools
- Reproducible synthetic benchmark suites

Repository Contents

- Aurora Runtime v0.1
- 25-ticket smoke benchmark
- 250-ticket synthetic benchmark suite
- Evaluation and scoring pipelines
- Android/Termux testing kit
- Documentation and research reports

Current Status

Aurora Nano v0.1 is a research preview.

The repository currently focuses on methodology, benchmarking, and evaluation infrastructure. Synthetic benchmark validation has been completed. Real-world benchmarking of open-weight models is ongoing.

Design Philosophy

Aurora Nano is not intended to replace language models.

Instead, it investigates whether deterministic runtime systems can improve reliability, consistency, and decision quality while preserving the efficiency of smaller models.

Input
  ↓
Claim Extraction
  ↓
Aurora Runtime
  ↓
Routing & Analysis
  ↓
Decision & Audit Trail

Roadmap

Near-term validation targets include:

- Qwen3 4B
- Llama 3.2 3B
- Gemma 3 4B
- Phi-4 Mini

Future development will focus on real-world benchmarking, extraction quality, contradiction handling, and runtime-assisted small-model performance.

License

Released under the Apache License 2.0.
