# universal-controller-qwen-aime60-direct-20260428T144728Z

- Intervention: one universal recipe per model family: route each public reasoning model to its paired direct public mode using the same held-out prompts.
- Eval suite: `aime2526`.
- Train prompts: `0`; eval prompts: `60` per model.
- Eval max tokens: `4096`; selection max tokens: `768`.

## Selected Controllers

- `qwen35_4b` direct-donor controller using mode `no`.

## Held-Out Generation

- `qwen35_4b` `canonical_donor`: reasoning `0.145`, accuracy `0.233` CI [`0.133`, `0.350`], truncation `0.733`, degeneration `0.000`, tokens `3480.7`, self-correction `0.733`
- `qwen35_4b` `universal_controller`: reasoning `0.145`, accuracy `0.233` CI [`0.133`, `0.350`], truncation `0.733`, degeneration `0.000`, tokens `3480.7`, self-correction `0.733`
