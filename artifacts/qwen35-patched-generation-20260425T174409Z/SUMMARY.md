# qwen35-patched-generation-20260425T174409Z

- Model: `mlx-community/Qwen3.5-4B-4bit`
- Prompts: `12` (`6` GSM8K, `6` numeric MATH-500)
- Max generation tokens: `1024`
- Patched rows choose the first generated token from a residual intervention, then continue freely from the resulting visible token.

## Overall Behavior

- `canonical_no` `baseline`: accuracy `0.667`, reasoning-preface `0.000`, direct-answer `0.917`, self-correction `0.167`, mean tokens `502.8`, truncation `0.167`
- `canonical_think` `baseline`: accuracy `0.250`, reasoning-preface `0.833`, direct-answer `0.167`, self-correction `0.583`, mean tokens `977.7`, truncation `0.917`
- `forced_donor_top1_then_free` `no_think_to_think`: accuracy `0.417`, reasoning-preface `0.167`, direct-answer `0.000`, self-correction `0.417`, mean tokens `936.5`, truncation `0.750`
- `forced_donor_top1_then_free` `think_to_no_think`: accuracy `0.833`, reasoning-preface `0.083`, direct-answer `0.000`, self-correction `0.167`, mean tokens `524.6`, truncation `0.083`
- `forced_target_top1_then_free` `no_think_to_think`: accuracy `0.250`, reasoning-preface `0.833`, direct-answer `0.083`, self-correction `0.583`, mean tokens `940.4`, truncation `0.750`
- `forced_target_top1_then_free` `think_to_no_think`: accuracy `0.667`, reasoning-preface `0.000`, direct-answer `0.000`, self-correction `0.083`, mean tokens `494.8`, truncation `0.167`
- `full_residual_entry_then_free` `no_think_to_think`: accuracy `0.417`, reasoning-preface `0.167`, direct-answer `0.000`, self-correction `0.417`, mean tokens `936.5`, truncation `0.750`
- `full_residual_entry_then_free` `think_to_no_think`: accuracy `0.833`, reasoning-preface `0.083`, direct-answer `0.000`, self-correction `0.167`, mean tokens `524.6`, truncation `0.083`
- `rank2_residual_entry_then_free` `no_think_to_think`: accuracy `0.500`, reasoning-preface `0.000`, direct-answer `0.000`, self-correction `0.417`, mean tokens `935.5`, truncation `0.750`
- `rank2_residual_entry_then_free` `think_to_no_think`: accuracy `0.833`, reasoning-preface `0.167`, direct-answer `0.000`, self-correction `0.167`, mean tokens `567.8`, truncation `0.083`

## Entry Token Samples

- `gsm8k_0` `canonical_think` `baseline` entry `` style `reasoning_preface` correct `0`
- `gsm8k_0` `canonical_no` `baseline` entry `` style `direct_answer` correct `1`
- `gsm8k_0` `full_residual_entry_then_free` `think_to_no_think` entry `Here` style `other` correct `1`
- `gsm8k_0` `rank2_residual_entry_then_free` `think_to_no_think` entry `Here` style `other` correct `1`
- `gsm8k_0` `forced_donor_top1_then_free` `think_to_no_think` entry `Here` style `other` correct `1`
- `gsm8k_0` `forced_target_top1_then_free` `think_to_no_think` entry `Here` style `other` correct `1`
- `gsm8k_0` `full_residual_entry_then_free` `no_think_to_think` entry `Here` style `reasoning_preface` correct `1`
- `gsm8k_0` `rank2_residual_entry_then_free` `no_think_to_think` entry `To` style `other` correct `1`
- `gsm8k_0` `forced_donor_top1_then_free` `no_think_to_think` entry `Here` style `reasoning_preface` correct `1`
- `gsm8k_0` `forced_target_top1_then_free` `no_think_to_think` entry `Here` style `reasoning_preface` correct `1`
- `gsm8k_1` `canonical_think` `baseline` entry `` style `reasoning_preface` correct `1`
- `gsm8k_1` `canonical_no` `baseline` entry `` style `direct_answer` correct `1`
- `gsm8k_1` `full_residual_entry_then_free` `think_to_no_think` entry `Thinking` style `reasoning_preface` correct `1`
- `gsm8k_1` `rank2_residual_entry_then_free` `think_to_no_think` entry `Thinking` style `reasoning_preface` correct `1`
- `gsm8k_1` `forced_donor_top1_then_free` `think_to_no_think` entry `Thinking` style `reasoning_preface` correct `1`
- `gsm8k_1` `forced_target_top1_then_free` `think_to_no_think` entry `Here` style `other` correct `1`
- `gsm8k_1` `full_residual_entry_then_free` `no_think_to_think` entry `Here` style `reasoning_preface` correct `1`
- `gsm8k_1` `rank2_residual_entry_then_free` `no_think_to_think` entry `To` style `other` correct `1`
- `gsm8k_1` `forced_donor_top1_then_free` `no_think_to_think` entry `Here` style `reasoning_preface` correct `1`
- `gsm8k_1` `forced_target_top1_then_free` `no_think_to_think` entry `Thinking` style `reasoning_preface` correct `1`
- `gsm8k_2` `canonical_think` `baseline` entry `` style `reasoning_preface` correct `0`
- `gsm8k_2` `canonical_no` `baseline` entry `` style `direct_answer` correct `1`
- `gsm8k_2` `full_residual_entry_then_free` `think_to_no_think` entry `Here` style `other` correct `1`
- `gsm8k_2` `rank2_residual_entry_then_free` `think_to_no_think` entry `Here` style `other` correct `1`
