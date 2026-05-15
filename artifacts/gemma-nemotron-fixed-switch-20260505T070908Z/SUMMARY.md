# gemma-nemotron-fixed-switch-20260505T070908Z

- Controller: train-learned fixed width-2 prompt-boundary residual vectors.
- Training prompts: public GSM8K/MATH-500 only; evaluation prompts: AIME 2025+2026.
- Evaluation is next-token branch control with no AIME donor activations in the deployed fixed-vector controller.

## AIME Branch Control

- `gemma4_e2b` `off_to_think` `fixed_mean`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6914`, JS donor `0.0002`
- `gemma4_e2b` `off_to_think` `full_tail_patch`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6931`, JS donor `0.0000`
- `gemma4_e2b` `off_to_think` `opposite_mean`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.3980`, JS donor `0.6931`
- `gemma4_e2b` `off_to_think` `random_norm_matched`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.4610`, JS donor `0.6931`
- `gemma4_e2b` `think_to_off` `fixed_mean`: donor win `0.183` [`0.083`, `0.283`], effective `0.167` [`0.083`, `0.267`], margin `-0.4080`, JS donor `0.5641`
- `gemma4_e2b` `think_to_off` `full_tail_patch`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6930`, JS donor `0.0002`
- `gemma4_e2b` `think_to_off` `opposite_mean`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.6931`, JS donor `0.6931`
- `gemma4_e2b` `think_to_off` `random_norm_matched`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.6931`, JS donor `0.6931`
- `nemotron_nano_4b` `off_to_think` `fixed_mean`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6937`, JS donor `0.0000`
- `nemotron_nano_4b` `off_to_think` `full_tail_patch`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6937`, JS donor `0.0000`
- `nemotron_nano_4b` `off_to_think` `opposite_mean`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.0257`, JS donor `0.6931`
- `nemotron_nano_4b` `off_to_think` `random_norm_matched`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.0227`, JS donor `0.6931`
- `nemotron_nano_4b` `think_to_off` `fixed_mean`: donor win `1.000` [`1.000`, `1.000`], effective `0.950` [`0.883`, `1.000`], margin `0.5337`, JS donor `0.1595`
- `nemotron_nano_4b` `think_to_off` `full_tail_patch`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6851`, JS donor `0.0080`
- `nemotron_nano_4b` `think_to_off` `opposite_mean`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.6937`, JS donor `0.6937`
- `nemotron_nano_4b` `think_to_off` `random_norm_matched`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.6878`, JS donor `0.6924`

## Selected Controllers

- `gemma4_e2b` `off_to_think` layer `35` alpha `0.25`: train donor win `0.000`, effective `0.000`, margin `-0.6211`
- `gemma4_e2b` `off_to_think` layer `35` alpha `0.5`: train donor win `0.183`, effective `0.167`, margin `-0.3453`
- `gemma4_e2b` `off_to_think` layer `35` alpha `1.0`: train donor win `0.983`, effective `0.983`, margin `0.6042`
- `gemma4_e2b` `off_to_think` layer `35` alpha `2.0`: train donor win `1.000`, effective `1.000`, margin `0.6739`
- `gemma4_e2b` `off_to_think` layer `35` alpha `4.0`: train donor win `1.000`, effective `1.000`, margin `0.5454`
- `gemma4_e2b` `off_to_think` layer `35` alpha `8.0`: train donor win `1.000`, effective `0.000`, margin `0.0193`
- `gemma4_e2b` `think_to_off` layer `35` alpha `0.25`: train donor win `0.250`, effective `0.217`, margin `-0.4124`
- `gemma4_e2b` `think_to_off` layer `35` alpha `0.5`: train donor win `0.483`, effective `0.450`, margin `-0.0588`
- `gemma4_e2b` `think_to_off` layer `35` alpha `1.0`: train donor win `0.950`, effective `0.817`, margin `0.4273`
- `gemma4_e2b` `think_to_off` layer `35` alpha `2.0`: train donor win `0.950`, effective `0.783`, margin `0.4320`
- `gemma4_e2b` `think_to_off` layer `35` alpha `4.0`: train donor win `0.950`, effective `0.767`, margin `0.4372`
- `gemma4_e2b` `think_to_off` layer `35` alpha `8.0`: train donor win `0.950`, effective `0.717`, margin `0.3243`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `0.25`: train donor win `0.000`, effective `0.000`, margin `-0.6394`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `0.5`: train donor win `0.467`, effective `0.467`, margin `-0.0143`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `1.0`: train donor win `1.000`, effective `1.000`, margin `0.6936`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `2.0`: train donor win `1.000`, effective `1.000`, margin `0.6936`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `4.0`: train donor win `1.000`, effective `1.000`, margin `0.6936`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `8.0`: train donor win `1.000`, effective `1.000`, margin `0.6936`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `0.25`: train donor win `0.000`, effective `0.000`, margin `-0.6875`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `0.5`: train donor win `0.150`, effective `0.150`, margin `-0.4094`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `1.0`: train donor win `0.983`, effective `0.783`, margin `0.4745`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `2.0`: train donor win `1.000`, effective `0.833`, margin `0.4629`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `4.0`: train donor win `1.000`, effective `0.033`, margin `0.0175`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `8.0`: train donor win `1.000`, effective `0.033`, margin `0.0113`
