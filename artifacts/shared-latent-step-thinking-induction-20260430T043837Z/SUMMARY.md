# shared-latent-step-thinking-induction-20260430T043837Z

- Controller: shared latent branch codes (`direct_erasure`, `thinking_induction`) with model-specific residual adapters.
- Adapter training: generated prefixes from public GSM8K/MATH-500 prompts only.
- Evaluation: held-out generated prefixes plus AIME 2025+2026 prompt-boundary states; interventions use no evaluation donor activations.

## Results

- `liquid_12b` `thinking_induction` `aime_prompt_boundary`: effective `0.000` [`0.000`, `0.000`], donor win `0.033`, margin `-0.0052`, JS donor `0.6929`
- `liquid_12b` `thinking_induction` `heldout_public_generated_prefix`: effective `0.100` [`0.033`, `0.183`], donor win `0.450`, margin `0.0087`, JS donor `0.5099`
- `olmo3_7b` `thinking_induction` `aime_prompt_boundary`: effective `1.000` [`1.000`, `1.000`], donor win `1.000`, margin `0.6713`, JS donor `0.0213`
- `olmo3_7b` `thinking_induction` `heldout_public_generated_prefix`: effective `0.450` [`0.317`, `0.583`], donor win `0.600`, margin `0.1443`, JS donor `0.2663`
- `phi4_mini` `thinking_induction` `aime_prompt_boundary`: effective `0.000` [`0.000`, `0.000`], donor win `0.267`, margin `-0.0002`, JS donor `0.6931`
- `phi4_mini` `thinking_induction` `heldout_public_generated_prefix`: effective `0.017` [`0.000`, `0.050`], donor win `0.250`, margin `-0.0811`, JS donor `0.4705`
- `qwen35_4b` `thinking_induction` `aime_prompt_boundary`: effective `1.000` [`1.000`, `1.000`], donor win `1.000`, margin `0.4606`, JS donor `0.2028`
- `qwen35_4b` `thinking_induction` `heldout_public_generated_prefix`: effective `0.450` [`0.333`, `0.583`], donor win `0.883`, margin `0.1525`, JS donor `0.2136`

## Adapters

- `qwen35_4b` `thinking_induction` layer `15` alpha `2.0` norm `12.0334`: train effective `0.950`, donor win `1.000`
- `qwen35_4b` `thinking_induction` layer `15` alpha `2.0` norm `10.4575`: train effective `0.500`, donor win `0.900`
- `qwen35_4b` `thinking_induction` layer `15` alpha `4.0` norm `6.6448`: train effective `0.225`, donor win `0.850`
- `olmo3_7b` `thinking_induction` layer `8` alpha `1.0` norm `9.2858`: train effective `1.000`, donor win `1.000`
- `olmo3_7b` `thinking_induction` layer `8` alpha `4.0` norm `6.0997`: train effective `0.150`, donor win `0.350`
- `olmo3_7b` `thinking_induction` layer `8` alpha `4.0` norm `4.5996`: train effective `0.175`, donor win `0.225`
- `phi4_mini` `thinking_induction` layer `16` alpha `2.0` norm `39.4868`: train effective `0.000`, donor win `0.400`
- `phi4_mini` `thinking_induction` layer `16` alpha `2.0` norm `36.7717`: train effective `0.025`, donor win `0.075`
- `phi4_mini` `thinking_induction` layer `16` alpha `4.0` norm `26.6805`: train effective `0.075`, donor win `0.200`
- `liquid_12b` `thinking_induction` layer `12` alpha `4.0` norm `6.1318`: train effective `0.000`, donor win `0.000`
- `liquid_12b` `thinking_induction` layer `12` alpha `2.0` norm `1.3110`: train effective `0.150`, donor win `0.625`
- `liquid_12b` `thinking_induction` layer `12` alpha `4.0` norm `1.1137`: train effective `0.175`, donor win `0.800`
