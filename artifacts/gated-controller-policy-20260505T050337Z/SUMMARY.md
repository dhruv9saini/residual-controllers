# gated-controller-policy-20260505T050337Z

Derived cross-model deployment policy from the existing 100-prompt public-task generation rows.

Policies: `benchmark_gated_policy` uses the controller on GSM8K word problems and canonical target/direct mode on numeric MATH-500 prompts. `model_task_gated_policy` additionally uses Qwen's controller on both public subsets, because Qwen is the one family where the held-out controller improves both GSM8K and numeric MATH-500.

## Aggregate

- `canonical_target`: correct `205/300`, accuracy `0.683`, tokens `420.6`, truncation `0.127`
- `universal_controller`: correct `197/300`, accuracy `0.657`, tokens `498.9`, truncation `0.220`
- `crossvalidated_gated_policy`: correct `210/300`, accuracy `0.700`, tokens `446.0`, truncation `0.147`
- `benchmark_gated_policy`: correct `211/300`, accuracy `0.703`, tokens `444.9`, truncation `0.153`
- `model_task_gated_policy`: correct `213/300`, accuracy `0.710`, tokens `447.8`, truncation `0.150`

## Paired Accuracy Deltas vs Canonical Target

- `benchmark_gated_policy`: delta `0.020` CI [`-0.010`, `0.053`], wins/losses/ties `15/9/276`
- `crossvalidated_gated_policy`: delta `0.017` CI [`-0.017`, `0.050`], wins/losses/ties `17/12/271`
- `model_task_gated_policy`: delta `0.027` CI [`-0.010`, `0.063`], wins/losses/ties `20/12/268`
- `universal_controller`: delta `-0.027` CI [`-0.080`, `0.027`], wins/losses/ties `27/35/238`

## By Model

- `olmo3_7b` `benchmark_gated_policy`: correct `75/100`, accuracy `0.750`, tokens `484.5`, truncation `0.150`
- `olmo3_7b` `model_task_gated_policy`: correct `75/100`, accuracy `0.750`, tokens `484.5`, truncation `0.150`
- `phi4_mini` `benchmark_gated_policy`: correct `56/100`, accuracy `0.560`, tokens `355.0`, truncation `0.190`
- `phi4_mini` `model_task_gated_policy`: correct `56/100`, accuracy `0.560`, tokens `355.0`, truncation `0.190`
- `qwen35_4b` `benchmark_gated_policy`: correct `80/100`, accuracy `0.800`, tokens `495.3`, truncation `0.120`
- `qwen35_4b` `model_task_gated_policy`: correct `82/100`, accuracy `0.820`, tokens `503.9`, truncation `0.110`

## By Benchmark

- `gsm8k` `benchmark_gated_policy`: correct `121/150`, accuracy `0.807`, tokens `335.6`, truncation `0.067`
- `gsm8k` `model_task_gated_policy`: correct `121/150`, accuracy `0.807`, tokens `335.6`, truncation `0.067`
- `math500_numeric` `benchmark_gated_policy`: correct `90/150`, accuracy `0.600`, tokens `554.3`, truncation `0.240`
- `math500_numeric` `model_task_gated_policy`: correct `92/150`, accuracy `0.613`, tokens `560.1`, truncation `0.233`
