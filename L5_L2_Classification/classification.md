# L5 Narrow / L2 General Classification — L_RLINF
**Platform:** Anticloud | **Tier:** TIER_5_WORLD_NEURO_EMBODIED | **PAX:** 27B
**IP:** USPTO pending 2026, Anticloud FZ LLE, 0-1.gg | **License:** Apache-2.0

## L5 Narrow
L_RLINF uses a learned RL policy to control PAX 27B's token sampling: instead of fixed temperature/top-p, an RL policy dynamically selects decoding parameters based on the current generation context. Narrow scope: PAX 27B inference optimization for Anticloud tasks.

## L2 General
L2 General: L_RLINF's adaptive decoding improves output quality for any tier without retraining PAX 27B. TIER_7 clinical precision queries and TIER_6 security code generation both benefit from context-aware decoding.

## PAX 27B Integration
PAX 27B generates tokens; L_RLINF's RL policy observes the current sequence and dynamically sets temperature, top-p, and repetition penalties for the next token. The policy is trained to maximize downstream task success.

## AIOSS Audit Chain
Every inference step (context hash + RL policy decision hash + token hash + task reward) is chained: H_n = SHA3-256(H_{n-1} || entry_hash_n || timestamp_n).
Offline-verifiable, tamper-evident, zero cloud dependency.

## Regulatory / Compliance
NIST AI RMF 1.0 (reliable AI). ISO/IEC 42001.
