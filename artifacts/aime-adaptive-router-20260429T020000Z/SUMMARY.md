# aime-adaptive-router-20260429T020000Z

- Controller: adaptive multi-model public-mode router.
- Routing rule: run direct public mode for OLMo, Qwen, Liquid, and Phi; choose the first non-truncated completion in the fixed order `olmo3_7b`, `qwen35_4b`, `liquid_12b`, `phi4_mini`; if all truncate, use OLMo.
- Eval suite: AIME 2025+2026, 60 total questions.

## Aggregate

- `universal_controller`: accuracy `0.333` CI [`0.217`, `0.450`], truncation `0.000`, tokens `2266.7`

## By Year

- `aime2025` `universal_controller`: correct `10/30`, accuracy `0.333`, truncation `0.000`
- `aime2026` `universal_controller`: correct `10/30`, accuracy `0.333`, truncation `0.000`
