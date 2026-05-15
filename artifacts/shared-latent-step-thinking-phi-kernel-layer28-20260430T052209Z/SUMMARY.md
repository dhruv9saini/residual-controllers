# shared-latent-step-thinking-phi-kernel-layer28-20260430T052209Z

- Controller: shared latent branch codes (`direct_erasure`, `thinking_induction`) with model-specific residual adapters.
- Adapter training: generated prefixes from public GSM8K/MATH-500 prompts only.
- Evaluation: held-out generated prefixes plus AIME 2025+2026 prompt-boundary states; interventions use no evaluation donor activations.

## Results

- `phi4_mini` `thinking_induction` `kernel_latent_adapter` `aime_prompt_boundary`: effective `1.000` [`1.000`, `1.000`], donor win `1.000`, margin `0.6282`, JS donor `0.0570`
- `phi4_mini` `thinking_induction` `kernel_latent_adapter` `heldout_public_generated_prefix`: effective `0.367` [`0.250`, `0.500`], donor win `0.500`, margin `0.1224`, JS donor `0.1837`

## Adapters

- `phi4_mini` `thinking_induction` `kernel` step `0` layer `28` alpha `1.0` norm `203.1257`: train effective `0.950`, donor win `1.000`
- `phi4_mini` `thinking_induction` `kernel` step `1` layer `28` alpha `1.0` norm `205.4124`: train effective `0.425`, donor win `0.750`
- `phi4_mini` `thinking_induction` `kernel` step `2` layer `28` alpha `1.0` norm `154.8448`: train effective `0.150`, donor win `0.625`
