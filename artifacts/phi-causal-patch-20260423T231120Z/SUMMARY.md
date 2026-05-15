# phi-causal-patch-20260423T231120Z

- Main prompts: `8`
- Alt prompts: `8`
- Patch layers: `[0, 4, 8, 12, 16, 20, 24, 28, 32]`

## Template Notes

- Think suffix: `''`
- Instruct suffix: `''`

## Canonical Split

- `alt` JS instruct->think `0.6934` [`0.6932`, `0.6935`], top-1 match `0.000` [`0.000`, `0.000`]
- `main` JS instruct->think `0.6933` [`0.6931`, `0.6934`], top-1 match `0.000` [`0.000`, `0.000`]

## Reduced Causal Patching

- `main` `think_to_instruct` `tail_w2` best donor win `1.000` [`1.000`, `1.000`] at layer `28`
- `main` `think_to_instruct` `tail_w4` best donor win `1.000` [`1.000`, `1.000`] at layer `28`
- `main` `think_to_instruct` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `think_to_instruct` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `think_to_instruct` `prefix_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `instruct_to_think` `tail_w2` best donor win `1.000` [`1.000`, `1.000`] at layer `16`
- `main` `instruct_to_think` `tail_w4` best donor win `1.000` [`1.000`, `1.000`] at layer `16`
- `main` `instruct_to_think` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `instruct_to_think` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `main` `instruct_to_think` `prefix_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `think_to_instruct` `tail_w2` best donor win `1.000` [`1.000`, `1.000`] at layer `28`
- `alt` `think_to_instruct` `tail_w4` best donor win `1.000` [`1.000`, `1.000`] at layer `28`
- `alt` `think_to_instruct` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `think_to_instruct` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `think_to_instruct` `prefix_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `instruct_to_think` `tail_w2` best donor win `1.000` [`1.000`, `1.000`] at layer `16`
- `alt` `instruct_to_think` `tail_w4` best donor win `1.000` [`1.000`, `1.000`] at layer `16`
- `alt` `instruct_to_think` `nontail_w2` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `instruct_to_think` `nontail_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`
- `alt` `instruct_to_think` `prefix_w4` best donor win `0.000` [`0.000`, `0.000`] at layer `0`