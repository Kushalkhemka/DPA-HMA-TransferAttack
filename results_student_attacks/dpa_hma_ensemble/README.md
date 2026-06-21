# DPA-HMA Ensemble Result

This folder contains the verified 3-surrogate ensemble evaluation for the `DPA_HMA_ENSEMBLE` callable implemented in `core/transfer_attack_core.py`.

## Attack

- Implementation name: `DPA_HMA_ENSEMBLE`
- Default iterations: `5`
- Seed: `1`
- Evaluation rows: `150`
- Victim models: `Facenet512`, `ArcFace`, `GhostFaceNet`, `VGG-Face`, `IR152`

## Important Usage Note

The repository's default `run_attack(...)` path receives only one attacker model, so the ensemble must be evaluated by calling `dpa_hma_ensemble(...)` with the selected three surrogate models and their matching target embeddings. This avoids changing the assignment runner, scripts, notebooks, or evaluation flow.

## Verified T=5 Result

- Overall breach rate: `60.67%`
- Mean impact: `0.294`

## Victim Split

- ArcFace: `70.00%`
- Facenet512: `60.00%`
- GhostFaceNet: `53.33%`
- IR152: `56.67%`
- VGG-Face: `63.33%`

## Files

- `dpa_hma_ensemble_attack_eval_long.csv`: 150-row ensemble evaluation.
- `dpa_hma_ensemble_attack_summary.csv`: overall T=5 summary.
- `dpa_hma_ensemble_attack_summary_by_goal.csv`: dodging vs impersonation split.
- `dpa_hma_ensemble_victim_summary.csv`: per-victim split.
- `dpa_hma_ensemble_vs_dpa_hma_variants_summary.csv`: T=5/T=10/T=20 ensemble sweep summary.
