# qwen35-fixed-controller-20260427T152833Z

- Model: `mlx-community/Qwen3.5-4B-4bit`
- Main intervention: fixed train-learned residual vector at the target tail; held-out interventions do not use held-out donor activations or held-out donor-target differences.

## Prompt-Boundary Fixed Controller

- `no_think_to_think` `fixed_mean` test: donor win `0.967` CI [`0.939`, `0.989`], JS donor `0.0816`, JS target `0.6098`, margin `0.5282` CI [`0.4954`, `0.5593`]
- `no_think_to_think` `opposite_mean` test: donor win `0.128` CI [`0.083`, `0.178`], JS donor `0.6781`, JS target `0.6216`, margin `-0.0565` CI [`-0.0665`, `-0.0469`]
- `no_think_to_think` `random_norm_matched` test: donor win `0.085` CI [`0.065`, `0.107`], JS donor `0.5792`, JS target `0.3416`, margin `-0.2376` CI [`-0.2576`, `-0.2174`]
- `think_to_no_think` `fixed_mean` test: donor win `0.922` CI [`0.883`, `0.961`], JS donor `0.2866`, JS target `0.6046`, margin `0.3180` CI [`0.2864`, `0.3490`]
- `think_to_no_think` `opposite_mean` test: donor win `0.000` CI [`0.000`, `0.000`], JS donor `0.5384`, JS target `0.1211`, margin `-0.4173` CI [`-0.4406`, `-0.3929`]
- `think_to_no_think` `random_norm_matched` test: donor win `0.070` CI [`0.039`, `0.107`], JS donor `0.5579`, JS target `0.3220`, margin `-0.2359` CI [`-0.2561`, `-0.2160`]

## Selected Prompt Controllers

- fold `0` `think_to_no_think` layer `15` alpha `0.5` train donor win `0.500` margin `-0.2666`
- fold `0` `think_to_no_think` layer `15` alpha `1.0` train donor win `1.000` margin `0.6094`
- fold `0` `think_to_no_think` layer `15` alpha `2.0` train donor win `1.000` margin `0.6314`
- fold `0` `think_to_no_think` layer `15` alpha `4.0` train donor win `1.000` margin `0.0027`
- fold `0` `no_think_to_think` layer `19` alpha `0.5` train donor win `0.875` margin `0.2974`
- fold `0` `no_think_to_think` layer `19` alpha `1.0` train donor win `1.000` margin `0.5142`
- fold `0` `no_think_to_think` layer `19` alpha `2.0` train donor win `1.000` margin `0.4990`
- fold `0` `no_think_to_think` layer `19` alpha `4.0` train donor win `1.000` margin `0.4658`
- fold `1` `think_to_no_think` layer `15` alpha `0.5` train donor win `0.375` margin `-0.2949`
- fold `1` `think_to_no_think` layer `15` alpha `1.0` train donor win `1.000` margin `0.6213`
- fold `1` `think_to_no_think` layer `15` alpha `2.0` train donor win `1.000` margin `0.6301`
- fold `1` `think_to_no_think` layer `15` alpha `4.0` train donor win `1.000` margin `0.0021`
- fold `1` `no_think_to_think` layer `19` alpha `0.5` train donor win `1.000` margin `0.3151`
- fold `1` `no_think_to_think` layer `19` alpha `1.0` train donor win `1.000` margin `0.5217`
- fold `1` `no_think_to_think` layer `19` alpha `2.0` train donor win `1.000` margin `0.5025`
- fold `1` `no_think_to_think` layer `19` alpha `4.0` train donor win `1.000` margin `0.4662`
- fold `2` `think_to_no_think` layer `15` alpha `0.5` train donor win `0.250` margin `-0.2896`
- fold `2` `think_to_no_think` layer `15` alpha `1.0` train donor win `1.000` margin `0.6168`
- fold `2` `think_to_no_think` layer `15` alpha `2.0` train donor win `1.000` margin `0.6353`
- fold `2` `think_to_no_think` layer `15` alpha `4.0` train donor win `1.000` margin `0.0026`
- fold `2` `no_think_to_think` layer `19` alpha `0.5` train donor win `0.875` margin `0.2969`
- fold `2` `no_think_to_think` layer `19` alpha `1.0` train donor win `1.000` margin `0.5136`
- fold `2` `no_think_to_think` layer `19` alpha `2.0` train donor win `1.000` margin `0.4947`
- fold `2` `no_think_to_think` layer `19` alpha `4.0` train donor win `1.000` margin `0.4627`

## Generated-Prefix Controllers

- `think_to_no_think` layer `15` alpha `0.5` train prefixes `640` donor win `0.000` margin `-0.1332`
- `think_to_no_think` layer `15` alpha `1.0` train prefixes `640` donor win `0.022` margin `-0.1304`
- `think_to_no_think` layer `15` alpha `2.0` train prefixes `640` donor win `0.048` margin `-0.1168`
- `think_to_no_think` layer `15` alpha `4.0` train prefixes `640` donor win `0.170` margin `-0.0359`
- `no_think_to_think` layer `19` alpha `0.5` train prefixes `640` donor win `0.037` margin `-0.0741`
- `no_think_to_think` layer `19` alpha `1.0` train prefixes `640` donor win `0.183` margin `-0.0640`
- `no_think_to_think` layer `19` alpha `2.0` train prefixes `640` donor win `0.467` margin `0.0240`
- `no_think_to_think` layer `19` alpha `4.0` train prefixes `640` donor win `0.700` margin `0.0567`

## Public Generation

- `canonical_no` `baseline`: accuracy `0.500`, reasoning-preface `0.000`, direct-answer `0.917`, self-correction `0.083`, tokens `400.2`, truncation `0.417`
- `canonical_think` `baseline`: accuracy `0.167`, reasoning-preface `0.833`, direct-answer `0.167`, self-correction `0.250`, tokens `508.3`, truncation `0.917`
- `fixed_generated_prefix_controller_then_free` `no_think_to_think`: accuracy `0.167`, reasoning-preface `0.000`, direct-answer `0.750`, self-correction `0.167`, tokens `511.8`, truncation `1.000`
- `fixed_generated_prefix_controller_then_free` `think_to_no_think`: accuracy `0.333`, reasoning-preface `0.000`, direct-answer `0.917`, self-correction `0.000`, tokens `377.3`, truncation `0.500`
- `fixed_prompt_boundary_entry_then_free` `no_think_to_think`: accuracy `0.250`, reasoning-preface `0.000`, direct-answer `0.000`, self-correction `0.167`, tokens `505.4`, truncation `0.917`
- `fixed_prompt_boundary_entry_then_free` `think_to_no_think`: accuracy `0.417`, reasoning-preface `0.167`, direct-answer `0.000`, self-correction `0.083`, tokens `464.6`, truncation `0.583`
