# closed-loop-shared-direct-erasure-reduced-20260505T041600Z

- Evaluation: closed-loop greedy decoding under the learned controller.
- Control uses only target-model activations and stored adapters; donor traces are computed only for auditing.

## Step Metrics

- `liquid_12b` `direct_erasure` `aime_closed_loop`: step donor win `0.250` [`0.125`, `0.375`], margin `-0.0234`, JS donor `0.3671`
- `liquid_12b` `direct_erasure` `heldout_public_closed_loop`: step donor win `0.250` [`0.125`, `0.375`], margin `-0.0295`, JS donor `0.3521`
- `olmo3_7b` `direct_erasure` `aime_closed_loop`: step donor win `0.354` [`0.229`, `0.479`], margin `-0.0045`, JS donor `0.3226`
- `olmo3_7b` `direct_erasure` `heldout_public_closed_loop`: step donor win `0.438` [`0.312`, `0.583`], margin `0.0264`, JS donor `0.3590`
- `phi4_mini` `direct_erasure` `aime_closed_loop`: step donor win `0.854` [`0.750`, `0.938`], margin `0.1410`, JS donor `0.4637`
- `phi4_mini` `direct_erasure` `heldout_public_closed_loop`: step donor win `0.854` [`0.750`, `0.938`], margin `0.2266`, JS donor `0.4535`
- `qwen35_4b` `direct_erasure` `aime_closed_loop`: step donor win `0.562` [`0.417`, `0.708`], margin `0.0895`, JS donor `0.2742`
- `qwen35_4b` `direct_erasure` `heldout_public_closed_loop`: step donor win `0.521` [`0.375`, `0.667`], margin `0.0655`, JS donor `0.2985`

## Text Metrics

- `liquid_12b` `direct_erasure` `aime_closed_loop`: donor think-presence match `1.000` [`1.000`, `1.000`], first-token donor match `1.000`, direct-like `1.000`, donor direct-style match `1.000`
- `liquid_12b` `direct_erasure` `heldout_public_closed_loop`: donor think-presence match `1.000` [`1.000`, `1.000`], first-token donor match `0.500`, direct-like `1.000`, donor direct-style match `0.667`
- `olmo3_7b` `direct_erasure` `aime_closed_loop`: donor think-presence match `1.000` [`1.000`, `1.000`], first-token donor match `0.167`, direct-like `0.833`, donor direct-style match `0.333`
- `olmo3_7b` `direct_erasure` `heldout_public_closed_loop`: donor think-presence match `1.000` [`1.000`, `1.000`], first-token donor match `0.333`, direct-like `0.333`, donor direct-style match `0.833`
- `phi4_mini` `direct_erasure` `aime_closed_loop`: donor think-presence match `1.000` [`1.000`, `1.000`], first-token donor match `0.833`, direct-like `0.333`, donor direct-style match `0.333`
- `phi4_mini` `direct_erasure` `heldout_public_closed_loop`: donor think-presence match `1.000` [`1.000`, `1.000`], first-token donor match `0.833`, direct-like `0.333`, donor direct-style match `0.333`
- `qwen35_4b` `direct_erasure` `aime_closed_loop`: donor think-presence match `1.000` [`1.000`, `1.000`], first-token donor match `0.833`, direct-like `1.000`, donor direct-style match `1.000`
- `qwen35_4b` `direct_erasure` `heldout_public_closed_loop`: donor think-presence match `1.000` [`1.000`, `1.000`], first-token donor match `0.667`, direct-like `1.000`, donor direct-style match `0.833`
