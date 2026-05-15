# liquid-causal-layer-scan-20260430T051648Z

- Prompt sets: `main` `4`, `alt` `4`
- Patch layers: `[0, 4, 8, 12, 16]`

## Template Notes

- Think suffix: `'<|im_start|>assistant\n'`
- Instruct suffix: `'<|im_start|>assistant\n'`

## Canonical Split

- `alt` JS instruct->think `0.6932` [`0.6927`, `0.6937`], top-1 match `0.000` [`0.000`, `0.000`]
- `main` JS instruct->think `0.6932` [`0.6924`, `0.6939`], top-1 match `0.000` [`0.000`, `0.000`]

## Reduced Causal Patching

- `main` `think_to_instruct` `tail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `think_to_instruct` `tail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `think_to_instruct` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `think_to_instruct` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `think_to_instruct` `prefix_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `instruct_to_think` `tail_w2` best donor win `1.000` [`1.000`, `1.000`] at layer `12`
- `main` `instruct_to_think` `tail_w4` best donor win `1.000` [`1.000`, `1.000`] at layer `12`
- `main` `instruct_to_think` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `instruct_to_think` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `instruct_to_think` `prefix_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `think_to_instruct` `tail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `think_to_instruct` `tail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `think_to_instruct` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `think_to_instruct` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `think_to_instruct` `prefix_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `instruct_to_think` `tail_w2` best donor win `1.000` [`1.000`, `1.000`] at layer `12`
- `alt` `instruct_to_think` `tail_w4` best donor win `1.000` [`1.000`, `1.000`] at layer `12`
- `alt` `instruct_to_think` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `instruct_to_think` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `instruct_to_think` `prefix_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`