
# Aurora Nano HF-2 Evidence Pack

## Important

All benchmark numbers in this package are:

SIMULATION_NOT_REAL_BENCHMARK

They are forecasts intended to guide testing priorities and community validation.

## Simulated Leaderboard

| Model | Forecast Delta |
|---------|---------:|
| Qwen3 4B | +17.9% |
| Gemma 3 4B | +17.1% |
| SmolLM3 3B | +16.7% |
| Llama 3.2 3B | +16.1% |
| Phi-4 Mini | +14.7% |

## Conservative Forecasts

These are considered more realistic expectations before real testing:

| Model | Conservative Delta |
|---------|---------:|
| Qwen3 4B | +8% to +12% |
| Gemma 3 4B | +7% to +11% |
| Llama 3.2 3B | +8% to +13% |
| Phi-4 Mini | +6% to +10% |
| SmolLM3 3B | +7% to +11% |

## Key Insights

Aurora appears most valuable for:

- contradiction handling
- source conflict resolution
- policy reasoning
- escalation decisions
- temporal consistency

Aurora appears least valuable when the model already performs perfect extraction and structured reasoning.

## Open Questions

1. Do real benchmarks match the forecasts?
2. How much latency does Aurora add?
3. How does Aurora compare to prompting-only approaches?
4. Does Aurora help stronger models as much as smaller models?
5. Is extraction quality the primary bottleneck?
6. Which model family benefits most?
7. What is the minimum model size where Aurora remains useful?

## Community Testing Request

Please submit REAL_BENCHMARK results including:

- model name
- quantization
- hardware
- JSON validity
- model-only score
- Aurora runtime score
- latency metrics
- benchmark reports

Help build the first Aurora Nano leaderboard.
