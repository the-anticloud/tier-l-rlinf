# Deploy Guide — L_RLINF
**Tier:** TIER_5_WORLD_NEURO_EMBODIED | **Stack:** Python 3.11, PyTorch 2.10+, PAX 27B, RL policy (small model), AIOSS_FORMAT
**Air-gap capable after initial setup.**

## Prerequisites
Python 3.11+, PyTorch 2.10+, T4 GPU. Small RL policy model (~100M params) runs alongside PAX 27B.

## Environment
T4 GPU. Small RL policy adds ~300MB VRAM on top of PAX 27B Q4.

## AIOSS Integration
```bash
aioss init --module L_RLINF --output ./l_rlinf.aioss
aioss append --chain ./l_rlinf.aioss --payload ./output.bin --module L_RLINF
aioss verify --chain ./l_rlinf.aioss
```

## Air-Gap Setup
```bash
pip download -r requirements.txt -d ./wheels/
pip install --no-index --find-links ./wheels/ -r requirements.txt
```

## PAX 27B Harness Wiring
```python
from anticloud_pax import PAXHarness
harness = PAXHarness(
    model_path="./pax-27b-q4.gguf",
    module="L_RLINF",
    aioss_chain="./L_RLINF.aioss",
    classification="L5_NARROW_L2_GENERAL"
)
result = harness.process(input_data)
```

## Verification
```bash
aioss verify --chain ./L_RLINF.aioss --verbose
python -m L_RLINF.tests.smoke
```
