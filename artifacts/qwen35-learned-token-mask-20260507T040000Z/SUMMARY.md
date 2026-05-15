# Qwen learned branch-token masking

- Model: `mlx-community/Qwen3.5-4B-4bit`.
- Fixed thinking-induction controller: layer `15`, width `2`, alpha `1.0` selected on train prompts.

## Learned Branch-Token Masking
- mask top `0` tokens: donor win `1.000`, margin `0.5849`, JS donor `0.0274`.
- mask top `10` tokens: donor win `0.900`, margin `0.5421`, JS donor `0.0382`.
- mask top `25` tokens: donor win `0.800`, margin `0.3170`, JS donor `0.0379`.
- mask top `50` tokens: donor win `0.800`, margin `0.3160`, JS donor `0.0379`.
- mask top `100` tokens: donor win `0.800`, margin `0.2931`, JS donor `0.0379`.
- mask top `250` tokens: donor win `0.900`, margin `0.4114`, JS donor `0.0604`.

Random norm-matched controls never exceed donor win `0.300` across the learned-mask grid and have negative mean margins.
