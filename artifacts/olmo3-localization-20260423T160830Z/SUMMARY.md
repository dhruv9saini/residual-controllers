# olmo3-localization-20260423T160830Z

- Prompt count: `12`
- Patch layers: `[0, 4, 8, 12, 16, 20, 24, 28, 32]`
- Module patch layers: `[8, 12, 16, 20, 24, 28, 31]`

## Template Notes

- Think suffix: `'<|im_start|>assistant\n<think>'`
- Instruct suffix: `'<|im_start|>assistant\n'`

## Canonical Split

- Mean JS instruct->think `0.6929` [`0.6923`, `0.6934`], top-1 match `0.000` [`0.000`, `0.000`], think entropy `0.3969`, instruct entropy `0.5011`

## Tail And Control Patching

- `think_to_instruct` `tail_w1` best donor win `1.000` [`1.000`, `1.000`] at layer `16`
- `think_to_instruct` `tail_w2` best donor win `1.000` [`1.000`, `1.000`] at layer `0`
- `think_to_instruct` `tail_w4` best donor win `1.000` [`1.000`, `1.000`] at layer `0`
- `think_to_instruct` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `think_to_instruct` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `instruct_to_think` `tail_w1` best donor win `1.000` [`1.000`, `1.000`] at layer `8`
- `instruct_to_think` `tail_w2` best donor win `1.000` [`1.000`, `1.000`] at layer `4`
- `instruct_to_think` `tail_w4` best donor win `1.000` [`1.000`, `1.000`] at layer `0`
- `instruct_to_think` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `instruct_to_think` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`

## Module Split

- `think_to_instruct` `attention_only` width `1` best donor win `1.000` [`1.000`, `1.000`] at layer `12`
- `think_to_instruct` `attention_only` width `2` best donor win `1.000` [`1.000`, `1.000`] at layer `8`
- `think_to_instruct` `mlp_only` width `1` best donor win `0.000` [`0.000`, `0.000`] at layer `8`
- `think_to_instruct` `mlp_only` width `2` best donor win `0.000` [`0.000`, `0.000`] at layer `8`
- `think_to_instruct` `full_layer` width `1` best donor win `1.000` [`1.000`, `1.000`] at layer `12`
- `think_to_instruct` `full_layer` width `2` best donor win `1.000` [`1.000`, `1.000`] at layer `8`
- `instruct_to_think` `attention_only` width `1` best donor win `1.000` [`1.000`, `1.000`] at layer `8`
- `instruct_to_think` `attention_only` width `2` best donor win `1.000` [`1.000`, `1.000`] at layer `8`
- `instruct_to_think` `mlp_only` width `1` best donor win `0.000` [`0.000`, `0.000`] at layer `8`
- `instruct_to_think` `mlp_only` width `2` best donor win `0.000` [`0.000`, `0.000`] at layer `8`
- `instruct_to_think` `full_layer` width `1` best donor win `1.000` [`1.000`, `1.000`] at layer `8`
- `instruct_to_think` `full_layer` width `2` best donor win `1.000` [`1.000`, `1.000`] at layer `8`