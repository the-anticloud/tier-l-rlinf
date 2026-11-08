# Developer Cookbook — L_RLINF
**Stack:** Python 3.11, PyTorch 2.10+, PAX 27B, RL policy (small model), AIOSS_FORMAT
**Domain:** RLInf: RL-guided inference: using RL policies to control PAX 27B decoding

## RL-guided inference
```python
from l_rlinf import RLInfEngine

engine = RLInfEngine(
    pax_model="./pax-27b-q4.gguf",
    rl_policy="./rlinf_policy.pt",
    aioss_chain="./rlinf.aioss"
)

result = engine.generate(
    prompt="Provide a differential diagnosis for irregular EEG with high theta",
    max_tokens=256,
    task_type="clinical_reasoning"
)
print(result.text)
print(f"Avg temperature used: {result.avg_temperature:.3f}")
print(f"Tokens accepted by policy: {result.acceptance_rate:.2%}")
```

## AIOSS Chain Append
```python
import hashlib, time

def aioss_append(chain_path, payload: bytes, module_id: str):
    entry_hash = hashlib.sha3_256(payload).digest()
    ts = int(time.time_ns()).to_bytes(8, 'big')
    with open(chain_path, 'rb') as f:
        f.seek(-32, 2); prev_hash = f.read(32)
    new_hash = hashlib.sha3_256(prev_hash + entry_hash + ts).digest()
    with open(chain_path, 'ab') as f:
        f.write(ts + entry_hash + new_hash)
    return new_hash.hex()
```
