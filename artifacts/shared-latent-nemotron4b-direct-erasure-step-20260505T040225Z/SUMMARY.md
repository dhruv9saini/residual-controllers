# shared-latent-nemotron4b-direct-erasure-step-20260505T040225Z

- Controller: shared latent branch codes (`direct_erasure`, `thinking_induction`) with model-specific residual adapters.
- Adapter training: generated prefixes from public GSM8K/MATH-500 prompts only.
- Evaluation: held-out generated prefixes plus AIME 2025+2026 prompt-boundary states; interventions use no evaluation donor activations.

## Results

- `nemotron_nano_4b` `direct_erasure` `fixed_latent_adapter` `aime_prompt_boundary`: effective `0.950` [`0.883`, `1.000`], donor win `1.000`, margin `0.5235`, JS donor `0.1697`
- `nemotron_nano_4b` `direct_erasure` `fixed_latent_adapter` `heldout_public_generated_prefix`: effective `0.300` [`0.217`, `0.383`], donor win `0.892`, margin `0.1610`, JS donor `0.3597`

## Adapters

- `nemotron_nano_4b` `direct_erasure` `fixed` step `0` layer `28` alpha `2.0` norm `37.2268`: train effective `0.850`, donor win `1.000`
- `nemotron_nano_4b` `direct_erasure` `fixed` step `1` layer `28` alpha `4.0` norm `39.9531`: train effective `0.000`, donor win `0.775`
- `nemotron_nano_4b` `direct_erasure` `fixed` step `2` layer `28` alpha `4.0` norm `24.0782`: train effective `0.000`, donor win `0.800`
