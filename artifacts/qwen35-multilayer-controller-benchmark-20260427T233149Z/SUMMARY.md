# qwen35-multilayer-controller-benchmark-20260427T233149Z

- Model: `mlx-community/Qwen3.5-4B-4bit`
- Training prompts: `24` public benchmark prompts, disjoint from eval.
- Eval prompts: `40` (`20` GSM8K, `20` numeric MATH-500).
- Learned controller: mean donor-minus-target generated-prefix residual at tail width `2` across layers `[15, 19, 24, 28]`.
- Deployment: no eval donor activations; controller-specific fixed vectors are added for up to `64` generated decisions, then the model continues freely.

## Selected Controllers

- `reasoning_controller` active steps `1`, entry layer `15` alpha `1.0`, prefix alpha `4.0`: push a no-think prompt toward public reasoning behavior.
- `direct_answer_controller` active steps `8`, entry layer `19` alpha `2.0`, prefix alpha `4.0`: push a think prompt toward direct-answer behavior.

## Public Eval Behavior

- `canonical_no` `baseline`: accuracy `0.725`, reasoning-preface `0.000`, direct-answer `0.925`, self-correction `0.075`, mean tokens `530.5`, truncation `0.150`
- `canonical_think` `baseline`: accuracy `0.200`, reasoning-preface `0.775`, direct-answer `0.125`, self-correction `0.850`, mean tokens `1012.8`, truncation `0.950`
- `multilayer_generated_prefix_controller_then_free` `direct_answer_controller`: accuracy `0.075`, reasoning-preface `0.000`, direct-answer `1.000`, self-correction `0.225`, mean tokens `1013.0`, truncation `0.950`
- `multilayer_generated_prefix_controller_then_free` `reasoning_controller`: accuracy `0.800`, reasoning-preface `0.000`, direct-answer `0.000`, self-correction `0.000`, mean tokens `516.1`, truncation `0.100`

## By Benchmark

- `gsm8k` `canonical_no` `baseline`: accuracy `0.850`, tokens `378.6`, truncation `0.050`
- `gsm8k` `canonical_think` `baseline`: accuracy `0.250`, tokens `1005.9`, truncation `0.950`
- `gsm8k` `multilayer_generated_prefix_controller_then_free` `direct_answer_controller`: accuracy `0.100`, tokens `1002.6`, truncation `0.900`
- `gsm8k` `multilayer_generated_prefix_controller_then_free` `reasoning_controller`: accuracy `0.900`, tokens `350.4`, truncation `0.000`
- `math500_numeric` `canonical_no` `baseline`: accuracy `0.600`, tokens `682.5`, truncation `0.250`
- `math500_numeric` `canonical_think` `baseline`: accuracy `0.150`, tokens `1019.8`, truncation `0.950`
- `math500_numeric` `multilayer_generated_prefix_controller_then_free` `direct_answer_controller`: accuracy `0.050`, tokens `1023.5`, truncation `1.000`
- `math500_numeric` `multilayer_generated_prefix_controller_then_free` `reasoning_controller`: accuracy `0.700`, tokens `681.8`, truncation `0.200`

## Selection Grid

- `reasoning_controller` `entry` alpha `0.5`: donor-win `0.667`, margin `0.0814`, JS donor `0.2294`
- `reasoning_controller` `entry` alpha `1.0`: donor-win `1.000`, margin `0.4583`, JS donor `0.0294`
- `reasoning_controller` `entry` alpha `2.0`: donor-win `1.000`, margin `0.3850`, JS donor `0.1719`
- `reasoning_controller` `entry` alpha `4.0`: donor-win `0.375`, margin `0.0000`, JS donor `0.6909`
- `reasoning_controller` `entry` alpha `8.0`: donor-win `0.458`, margin `0.0002`, JS donor `0.6928`
- `reasoning_controller` `generated_prefix` alpha `0.5`: donor-win `0.135`, margin `-0.0990`, JS donor `0.1130`
- `reasoning_controller` `generated_prefix` alpha `1.0`: donor-win `0.448`, margin `-0.0442`, JS donor `0.0907`
- `reasoning_controller` `generated_prefix` alpha `2.0`: donor-win `0.885`, margin `0.0717`, JS donor `0.0929`
- `reasoning_controller` `generated_prefix` alpha `4.0`: donor-win `0.927`, margin `0.0565`, JS donor `0.4216`
- `reasoning_controller` `generated_prefix` alpha `8.0`: donor-win `0.896`, margin `0.0079`, JS donor `0.6758`
- `direct_answer_controller` `entry` alpha `0.5`: donor-win `0.375`, margin `-0.0019`, JS donor `0.2277`
- `direct_answer_controller` `entry` alpha `1.0`: donor-win `0.958`, margin `0.4802`, JS donor `0.0845`
- `direct_answer_controller` `entry` alpha `2.0`: donor-win `1.000`, margin `0.5196`, JS donor `0.1182`
- `direct_answer_controller` `entry` alpha `4.0`: donor-win `1.000`, margin `0.5008`, JS donor `0.1746`
- `direct_answer_controller` `entry` alpha `8.0`: donor-win `1.000`, margin `0.0898`, JS donor `0.5930`
- `direct_answer_controller` `generated_prefix` alpha `0.5`: donor-win `0.156`, margin `-0.1341`, JS donor `0.1376`
- `direct_answer_controller` `generated_prefix` alpha `1.0`: donor-win `0.625`, margin `0.0715`, JS donor `0.0603`
- `direct_answer_controller` `generated_prefix` alpha `2.0`: donor-win `0.854`, margin `0.1184`, JS donor `0.2020`
- `direct_answer_controller` `generated_prefix` alpha `4.0`: donor-win `0.958`, margin `0.0724`, JS donor `0.4416`
- `direct_answer_controller` `generated_prefix` alpha `8.0`: donor-win `0.885`, margin `0.0258`, JS donor `0.6273`
