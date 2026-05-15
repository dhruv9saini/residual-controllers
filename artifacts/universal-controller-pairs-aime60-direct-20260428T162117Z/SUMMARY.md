# universal-controller-pairs-aime60-direct-20260428T162117Z

- Intervention: one universal recipe per model family: route each public reasoning model to its paired direct public mode using the same held-out prompts.
- Eval suite: `aime2526`.
- Train prompts: `0`; eval prompts: `60` per model.
- Eval max tokens: `4096`; selection max tokens: `768`.

## Selected Controllers

- `olmo3_7b` direct-donor controller using mode `instruct`.
- `phi4_mini` direct-donor controller using mode `instruct`.
- `liquid_12b` direct-donor controller using mode `instruct`.

## Held-Out Generation

- `liquid_12b` `canonical_donor`: reasoning `0.123`, accuracy `0.050` CI [`0.000`, `0.117`], truncation `0.033`, degeneration `0.000`, tokens `2043.8`, self-correction `0.867`
- `liquid_12b` `universal_controller`: reasoning `0.123`, accuracy `0.050` CI [`0.000`, `0.117`], truncation `0.033`, degeneration `0.000`, tokens `2043.8`, self-correction `0.867`
- `olmo3_7b` `canonical_donor`: reasoning `0.633`, accuracy `0.283` CI [`0.167`, `0.400`], truncation `0.567`, degeneration `0.000`, tokens `3374.7`, self-correction `0.933`
- `olmo3_7b` `universal_controller`: reasoning `0.633`, accuracy `0.283` CI [`0.167`, `0.400`], truncation `0.567`, degeneration `0.000`, tokens `3374.7`, self-correction `0.933`
- `phi4_mini` `canonical_donor`: reasoning `0.012`, accuracy `0.017` CI [`0.000`, `0.050`], truncation `0.717`, degeneration `0.017`, tokens `3111.5`, self-correction `0.000`
- `phi4_mini` `universal_controller`: reasoning `0.012`, accuracy `0.017` CI [`0.000`, `0.050`], truncation `0.717`, degeneration `0.017`, tokens `3111.5`, self-correction `0.000`
