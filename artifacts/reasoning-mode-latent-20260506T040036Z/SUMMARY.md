# Mode-Entry Branch-State Adapter Evidence

This is a derived evidence artifact over stored paired-mode training vectors and held-out AIME prompt-boundary row-level evaluations. It does not rerun model inference.

## Claim

Thinking-mode entry is represented by a shared-sign mode-entry coordinate whose positive direction is realized by model-specific branch-state adapters.

## Trained Branch-State Adapters

- Coordinate: `z_mode_entry`, dimension 1.
- Shared direction: `+z` means enter the thinking-mode branch.
- Model realization: `h_tail <- h_tail + alpha * A_model z`, where `A_model` is a learned width-2 branch-state adapter.
- Instantiation data: 60 paired public prompts per model.
- Held-out test: all 60 AIME 2025+2026 prompt-boundary audits per model, with no held-out donor activations or answers used by the adapter intervention.

## Held-Out Control

- Positive shared-sign direction: 240/240 prompt-boundary branch-control cases across Qwen, OLMo, Gemma, and Nemotron.
- Opposite-sign direction: 0/240 effective controls.
- Norm-matched random directions: 19/720 effective controls.
- Exact width-2 tail patch ceiling: 239/240 effective controls and 240/240 donor wins.

## Low-Dimensionality

- Adapter coordinate dimension is 1 for every model; the model-specific realization is a rank-1 map into a width-2 residual-tail state.
- Cross-validated Qwen/OLMo low-rank subspace tests give 240/240 donor wins, with matched random subspaces at 0/960.

## Per-Model Adapters

- `qwen35_4b`: layer `15`, alpha `1.0`, hidden size `2560`, train pairs `60`, held-out effective `60/60`.
- `olmo3_7b`: layer `8`, alpha `1.0`, hidden size `4096`, train pairs `60`, held-out effective `60/60`.
- `gemma4_e2b`: layer `35`, alpha `2.0`, hidden size `1536`, train pairs `60`, held-out effective `60/60`.
- `nemotron_nano_4b`: layer `28`, alpha `4.0`, hidden size `3072`, train pairs `60`, held-out effective `60/60`.
