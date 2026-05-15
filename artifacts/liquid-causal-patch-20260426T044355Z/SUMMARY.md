# liquid-causal-patch-20260426T044355Z

- Prompt sets: `full` `60`
- Patch layers: `[0, 4, 8, 12, 16]`

## Template Notes

- Think suffix: `'<|im_start|>assistant\n'`
- Instruct suffix: `'<|im_start|>assistant\n'`

## Canonical Split

- `full` JS instruct->think `0.6932` [`0.6930`, `0.6934`], top-1 match `0.000` [`0.000`, `0.000`]

## Reduced Causal Patching

- `full` `think_to_instruct` `tail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `full` `think_to_instruct` `tail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `full` `think_to_instruct` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `full` `think_to_instruct` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `full` `think_to_instruct` `prefix_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `full` `instruct_to_think` `tail_w2` best donor win `1.000` [`1.000`, `1.000`] at layer `12`
- `full` `instruct_to_think` `tail_w4` best donor win `1.000` [`1.000`, `1.000`] at layer `12`
- `full` `instruct_to_think` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `full` `instruct_to_think` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `full` `instruct_to_think` `prefix_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`