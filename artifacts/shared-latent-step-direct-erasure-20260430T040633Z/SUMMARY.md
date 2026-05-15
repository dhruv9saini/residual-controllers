# shared-latent-step-direct-erasure-20260430T040633Z

- Controller: shared latent branch codes (`direct_erasure`, `thinking_induction`) with model-specific residual adapters.
- Adapter training: generated prefixes from public GSM8K/MATH-500 prompts only.
- Evaluation: held-out generated prefixes plus AIME 2025+2026 prompt-boundary states; interventions use no evaluation donor activations.

## Results

- `liquid_12b` `direct_erasure` `aime_prompt_boundary`: effective `1.000` [`1.000`, `1.000`], donor win `1.000`, margin `0.5879`, JS donor `0.1051`
- `liquid_12b` `direct_erasure` `heldout_public_generated_prefix`: effective `0.850` [`0.750`, `0.933`], donor win `1.000`, margin `0.3472`, JS donor `0.3455`
- `olmo3_7b` `direct_erasure` `aime_prompt_boundary`: effective `1.000` [`1.000`, `1.000`], donor win `1.000`, margin `0.4019`, JS donor `0.2887`
- `olmo3_7b` `direct_erasure` `heldout_public_generated_prefix`: effective `0.617` [`0.500`, `0.733`], donor win `0.933`, margin `0.2305`, JS donor `0.1680`
- `phi4_mini` `direct_erasure` `aime_prompt_boundary`: effective `1.000` [`1.000`, `1.000`], donor win `1.000`, margin `0.5829`, JS donor `0.1103`
- `phi4_mini` `direct_erasure` `heldout_public_generated_prefix`: effective `0.917` [`0.850`, `0.983`], donor win `1.000`, margin `0.3564`, JS donor `0.3366`
- `qwen35_4b` `direct_erasure` `aime_prompt_boundary`: effective `0.967` [`0.917`, `1.000`], donor win `0.983`, margin `0.5069`, JS donor `0.1295`
- `qwen35_4b` `direct_erasure` `heldout_public_generated_prefix`: effective `1.000` [`1.000`, `1.000`], donor win `1.000`, margin `0.4988`, JS donor `0.0789`

## Adapters

- `qwen35_4b` `direct_erasure` layer `19` alpha `2.0` norm `15.8384`: train effective `1.000`, donor win `1.000`
- `qwen35_4b` `direct_erasure` layer `19` alpha `1.0` norm `14.4115`: train effective `0.850`, donor win `0.900`
- `qwen35_4b` `direct_erasure` layer `19` alpha `4.0` norm `12.2796`: train effective `0.800`, donor win `0.950`
- `olmo3_7b` `direct_erasure` layer `12` alpha `4.0` norm `12.8170`: train effective `0.975`, donor win `1.000`
- `olmo3_7b` `direct_erasure` layer `12` alpha `2.0` norm `11.7715`: train effective `0.000`, donor win `0.875`
- `olmo3_7b` `direct_erasure` layer `12` alpha `4.0` norm `10.0905`: train effective `0.975`, donor win `1.000`
- `phi4_mini` `direct_erasure` layer `28` alpha `1.0` norm `203.1257`: train effective `1.000`, donor win `1.000`
- `phi4_mini` `direct_erasure` layer `28` alpha `2.0` norm `210.1079`: train effective `0.975`, donor win `1.000`
- `phi4_mini` `direct_erasure` layer `28` alpha `2.0` norm `208.1498`: train effective `0.875`, donor win `1.000`
- `liquid_12b` `direct_erasure` layer `16` alpha `1.0` norm `5.4648`: train effective `1.000`, donor win `1.000`
- `liquid_12b` `direct_erasure` layer `16` alpha `1.0` norm `6.4401`: train effective `1.000`, donor win `1.000`
- `liquid_12b` `direct_erasure` layer `16` alpha `2.0` norm `6.1197`: train effective `0.525`, donor win `1.000`
