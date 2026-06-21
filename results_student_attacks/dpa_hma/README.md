# DPA-HMA Student Contribution

This folder contains the verified Assignment 4 result artifacts for the `DPA_HMA` attack on `docs/subset_input_pairs.csv`.

## Attack

- Implementation name: `DPA_HMA`
- Type: Diverse-parameters augmentation with hard-model-view gradient aggregation
- Default iterations: `5`
- Seed: `1`
- Epsilon: `0.062`

## Reference

- Paper basis: Diverse Parameters Augmentation (DPA), CVPR 2025
- Code reference: https://github.com/Trustworthy-AI-Group/TransferAttack

## Adaptation

The implementation stays inside `core/transfer_attack_core.py` and uses the repository's existing DeepFace attacker models. It does not train new models or modify thresholds, subset files, baseline files, scripts, notebooks, preprocessing, or evaluation rules.

## Verified Latest Result

- Overall breach rate: `39.58%`
- Mean impact: `0.214`
- Evaluation rows: `480`
- Successful breaches: `190`

## Goal Split

- Dodging: `51.25%`, impact `0.276`
- Impersonation: `27.92%`, impact `0.151`

## Files

- `dpa_hma_attack_eval_long.csv`: combined 480-row evaluation, including IR152.
- `dpa_hma_attack_summary.csv`: overall summary.
- `dpa_hma_attack_summary_by_goal.csv`: dodging vs impersonation summary.
- `dpa_hma_attacker_victim_summary.csv`: old-format 30-row-per-attacker-victim comparison table.
- `dpa_hma_vs_current_baseline_summary.csv`: comparison against current baseline/student attacks in the repository.
