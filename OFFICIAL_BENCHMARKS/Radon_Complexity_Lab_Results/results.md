# Radon_Complexity_Lab_Results
**Project:** `L_RLINF` | **Status:** `PASS` | **Run:** `2026-09-30T17:14:20.030944+00:00`

**Framework:** [Radon — Cyclomatic Complexity & Maintainability Index](https://radon.readthedocs.io/)

## Key Metrics

- **files_analyzed:** `10`
- **average_complexity:** `{'grade': 'B', 'score': 7.825581395348837}`
- **complexity_grade:** `B`
- **complexity_score:** `7.825581395348837`
- **mi_output:** `E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_RLINF\UPSTREAM\evaluations\eval_embodied_agent.py - A (74`

## Raw Output (first 50 lines)
```
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_RLINF\UPSTREAM\evaluations\eval_embodied_agent.py
    F 37:0 main - B (6)
E:\fenta\Downloads\The Anticloud\TIER_5_WORLD_NEURO_EMBODIED\L_RLINF\UPSTREAM\rlinf\config.py
    F 1075:0 validate_embodied_cfg - F (75)
    F 1701:0 validate_cfg - E (32)
    F 1371:0 validate_offline_cfg - D (23)
    F 649:0 validate_megatron_cfg - D (22)
    F 1837:0 build_transformer_config - D (22)
    F 371:0 validate_model_cfg_by_hf_config - D (21)
    F 492:0 validate_fsdp_cfg - C (18)
    F 1617:0 validate_coding_online_rl_cfg - C (13)
    F 986:0 validate_only_eval_rollout_model - B (10)
    F 1468:0 validate_sft_cfg - B (10)
    F 235:0 activation_to_func - B (8)
    F 1580:0 validate_searchr1_cfg - B (8)
    F 1032:0 validate_online_lerobot_env_cfg - B (7)
    F 1538:0 validate_reasoning_cfg - B (7)
    F 341:0 hf_rope_parameters - B (6)
    F 2033:0 _build_model_parallel_config - B (6)
    F 180:0 torch_dtype_from_precision - A (5)
    F 286:0 validate_rollout_cfg - A (5)
    F 476:0 validate_fp32_master_adamw_config - A (4)
    F 1513:0 _validate_steam_ensemble_cfg - A (4)
    F 1675:0 adv_requires_group_baseline - A (4)
    F 1825:0 build_config - A (4)
    M 51:4 SupportedModel.register - A (4)
    F 1017:0 validate_weight_sync_overlap_cfg - A (3)
    C 45:0 SupportedModel - A (3)
    F 1606:0 validate_reasoning_eval_cfg - A (2)
    M 65:4 SupportedModel.get - A (2)
    F 198:0 gelu_impl - A (1)
    F 207:0 openai_gelu - A (
```

---
_Anticloud Independent Benchmark — 2026-09-30T17:14:20.030944+00:00_