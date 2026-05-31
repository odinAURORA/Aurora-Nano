Aurora Nano Quick Start

Aurora Nano is a lightweight runtime and evaluation framework for testing whether deterministic runtime systems can improve small language model reliability.

This guide gets you running in a few minutes.

---

Option 1 — Just Explore The Project

If you're new to Aurora:

1. Read "README.md"
2. Read "ARCHITECTURE.md"
3. Review the benchmark reports
4. Examine the benchmark suite

No installation required.

---

Option 2 — Run A Single Ticket

This is the fastest way to understand Aurora.

Step 1

Choose a benchmark ticket:

benchmark_suite/25_ticket_smoke/

Example:

b1-l001_ticket.json

---

Step 2

Generate a prompt:

python tools/make_prompt.py benchmark_suite/25_ticket_smoke/b1-l001_ticket.json

---

Step 3

Send the generated prompt to your model.

Examples:

- Qwen3 4B
- Llama 3.2 3B
- Gemma 3 4B
- Phi-4 Mini

---

Step 4

Save the model output.

Example:

raw_output.txt

---

Step 5

Repair and normalize JSON:

python tools/json_repair_wrapper.py \
  --raw raw_output.txt \
  --ticket benchmark_suite/25_ticket_smoke/b1-l001_ticket.json \
  --out oracle.json

---

Step 6

Run Aurora:

python tools/score_one.py \
  benchmark_suite/25_ticket_smoke/b1-l001_ticket.json \
  oracle.json

You now have your first Aurora result.

---

Option 3 — Run The 25-Ticket Smoke Test

The smoke benchmark is the recommended first benchmark.

Requirements:

- Local model
- Oracle JSON output
- Aurora runtime

Run:

bash scripts/score_25_oracle.sh

Outputs:

JSON validity score
Runtime score
Benchmark summary

---

Option 4 — Run The Full 250-Ticket Benchmark

Once the smoke test passes:

bash scripts/score_250_oracle.sh

Outputs:

Category scores
Comparison reports
Failure analysis
Runtime metrics

---

Recommended Models

Current Aurora testing targets:

1. Qwen3 4B
2. Llama 3.2 3B
3. Gemma 3 4B
4. Phi-4 Mini
5. SmolLM3 3B

---

Contributing Results

If you run Aurora Nano benchmarks:

Please submit:

- Model name
- Quantization
- Hardware
- JSON validity
- Runtime score
- Latency
- Benchmark reports

Use:

templates/real_benchmark_submission_template.json

---

Important

Aurora Nano v0.1 is a research preview.

The goal is to evaluate whether deterministic runtime systems can improve consistency, contradiction handling, and decision quality for small language models.
