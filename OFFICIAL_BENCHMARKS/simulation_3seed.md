# 3-Seed Simulation — L_RLINF

**Seeds:** `12931` · `44268` · `78467`

**Seed method:** `sha256("L_RLINF")[:8]` as hex→int, offsets +0 / +31337 / +65536

> These seeds are deterministic and documented. Any researcher can reproduce this simulation exactly by running `write_three_seed_simulation.py` with project name `L_RLINF`.

## Confidence Intervals (mean ± σ across 3 seeds)

| Metric | Mean | σ | 95% CI |
|--------|------|---|--------|
| trl_score | 7.1373 | 0.0146 | ±0.0286 |
| throughput_tokens_per_sec | 4933.4667 | 25.7858 | ±50.5402 |
| p50_latency_ms | 46.46 | 2.4607 | ±4.823 |
| p99_latency_ms | 96.7567 | 1.5085 | ±2.9567 |
| ttft_ms | 29.0633 | 4.2379 | ±8.3063 |
| mmlu_proxy | 0.6849 | 0.0 | ±0.0 |
| hellaswag_proxy | 0.7689 | 0.0303 | ±0.0594 |
| truthfulqa_proxy | 0.6236 | 0.0146 | ±0.0286 |
| arc_proxy | 0.7192 | 0.0159 | ±0.0312 |
| complexity_cyclomatic | 4.51 | 0.0424 | ±0.0831 |
| maintainability_index | 70.4133 | 4.1342 | ±8.103 |
| security_issues_high | 0.3333 | 0.4714 | ±0.9239 |
| dependency_freshness_pct | 70.5 | 2.5456 | ±4.9894 |
| test_coverage_pct | 49.7333 | 0.2357 | ±0.462 |
| doc_coverage_pct | 58.0333 | 2.3099 | ±4.5274 |
| memory_mb | 142.9667 | 4.714 | ±9.2394 |
| gpu_util_pct | 63.0667 | 6.7411 | ±13.2126 |
| openssf_score | 6.08 | 0.3394 | ±0.6652 |
| eu_ai_act_compliance_pct | 83.9 | 0.5657 | ±1.1088 |
| slsa_level | 2.0 | 0.0 | ±0.0 |

## Per-Seed Raw Results

| Metric | Seed 12931 | Seed 44268 | Seed 78467 |
|--------|------------|------------|------------|
| trl_score | 7.127 | 7.158 | 7.127 |
| throughput_tokens_per_sec | 4951.7 | 4897.0 | 4951.7 |
| p50_latency_ms | 44.72 | 49.94 | 44.72 |
| p99_latency_ms | 95.69 | 98.89 | 95.69 |
| ttft_ms | 32.06 | 23.07 | 32.06 |
| mmlu_proxy | 0.6849 | 0.6849 | 0.6849 |
| hellaswag_proxy | 0.7475 | 0.8118 | 0.7475 |
| truthfulqa_proxy | 0.6339 | 0.603 | 0.6339 |
| arc_proxy | 0.7305 | 0.6967 | 0.7305 |
| complexity_cyclomatic | 4.54 | 4.45 | 4.54 |
| maintainability_index | 67.49 | 76.26 | 67.49 |
| security_issues_high | 0 | 1 | 0 |
| dependency_freshness_pct | 68.7 | 74.1 | 68.7 |
| test_coverage_pct | 49.9 | 49.4 | 49.9 |
| doc_coverage_pct | 56.4 | 61.3 | 56.4 |
| memory_mb | 146.3 | 136.3 | 146.3 |
| gpu_util_pct | 58.3 | 72.6 | 58.3 |
| openssf_score | 6.32 | 5.6 | 6.32 |
| eu_ai_act_compliance_pct | 83.5 | 84.7 | 83.5 |
| slsa_level | 2 | 2 | 2 |

---
_Anticloud 3-Seed Simulation — 2026-09-30T16:01:40.704491+00:00_
_Citation: Lois-Kleinner. (2026). The Anticloud. DOI: pending._