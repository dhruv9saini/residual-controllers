# prompt-boundary-robustness-nemotron-reduced-20260507T061500Z

- Scope: prompt-boundary robustness beyond AIME, including broad instruction/coding/multiturn/non-English prompts plus GPQA-Diamond science prompts.
- Controls in this reduced run: 16 norm-matched and 16 covariance-matched random directions per direction, alpha selected on the same public training prompts.  The wrapper script is configured for the full 512-control version.
- Localization: wrong-layer and wrong-position learned-vector controls.
- Sample efficiency: controllers trained from random subsets of 10/20/40/60 public prompts.

## Fixed Controllers

- `nemotron_nano_4b` `off_to_think`: effective `1.000`, donor win `1.000`, margin `0.6932`.
- `nemotron_nano_4b` `think_to_off`: effective `0.095`, donor win `1.000`, margin `0.0460`.

## Random Control Maxima

- `nemotron_nano_4b` `off_to_think` `random_covariance_matched`: p50/p95/p99/max effective `0.000`/`0.000`/`0.000`/`0.000`; margin max `-0.0065`.
- `nemotron_nano_4b` `off_to_think` `random_norm_matched`: p50/p95/p99/max effective `0.000`/`0.000`/`0.000`/`0.000`; margin max `-0.0070`.
- `nemotron_nano_4b` `think_to_off` `random_covariance_matched`: p50/p95/p99/max effective `0.000`/`0.000`/`0.000`/`0.000`; margin max `0.0074`.
- `nemotron_nano_4b` `think_to_off` `random_norm_matched`: p50/p95/p99/max effective `0.000`/`0.000`/`0.000`/`0.000`; margin max `0.0067`.

## Subset Curves

- `nemotron_nano_4b` `off_to_think` subset `10`: effective `1.000`, margin `0.6931`.
- `nemotron_nano_4b` `off_to_think` subset `20`: effective `1.000`, margin `0.6930`.
- `nemotron_nano_4b` `off_to_think` subset `40`: effective `1.000`, margin `0.6932`.
- `nemotron_nano_4b` `off_to_think` subset `60`: effective `1.000`, margin `0.6932`.
- `nemotron_nano_4b` `think_to_off` subset `10`: effective `0.081`, margin `0.0397`.
- `nemotron_nano_4b` `think_to_off` subset `20`: effective `0.100`, margin `0.0427`.
- `nemotron_nano_4b` `think_to_off` subset `40`: effective `0.105`, margin `0.0438`.
- `nemotron_nano_4b` `think_to_off` subset `60`: effective `0.095`, margin `0.0460`.

## Wrong Layer / Position

- wrong-layer `nemotron_nano_4b` `off_to_think` layer `8`: effective `1.000`, margin `0.6932`.
- wrong-layer `nemotron_nano_4b` `off_to_think` layer `16`: effective `1.000`, margin `0.6932`.
- wrong-layer `nemotron_nano_4b` `off_to_think` layer `24`: effective `1.000`, margin `0.6932`.
- wrong-layer `nemotron_nano_4b` `off_to_think` layer `26`: effective `1.000`, margin `0.6932`.
- wrong-layer `nemotron_nano_4b` `off_to_think` layer `30`: effective `1.000`, margin `0.6932`.
- wrong-layer `nemotron_nano_4b` `off_to_think` layer `32`: effective `1.000`, margin `0.6932`.
- wrong-layer `nemotron_nano_4b` `think_to_off` layer `8`: effective `0.000`, margin `0.0111`.
- wrong-layer `nemotron_nano_4b` `think_to_off` layer `16`: effective `0.024`, margin `0.0209`.
- wrong-layer `nemotron_nano_4b` `think_to_off` layer `24`: effective `0.048`, margin `0.0259`.
- wrong-layer `nemotron_nano_4b` `think_to_off` layer `26`: effective `0.119`, margin `0.0445`.
- wrong-layer `nemotron_nano_4b` `think_to_off` layer `30`: effective `0.071`, margin `0.0361`.
- wrong-layer `nemotron_nano_4b` `think_to_off` layer `32`: effective `0.095`, margin `0.0410`.
- wrong-position `nemotron_nano_4b` `off_to_think` offset `8`: effective `0.000`, margin `-0.6740`.
- wrong-position `nemotron_nano_4b` `off_to_think` offset `16`: effective `0.000`, margin `-0.6864`.
- wrong-position `nemotron_nano_4b` `think_to_off` offset `8`: effective `0.000`, margin `-0.6927`.
- wrong-position `nemotron_nano_4b` `think_to_off` offset `16`: effective `0.000`, margin `-0.6928`.
