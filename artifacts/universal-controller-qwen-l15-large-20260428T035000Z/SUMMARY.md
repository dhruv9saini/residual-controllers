# universal-controller-qwen-l15-large-20260428T035000Z

- Intervention: one universal recipe per model family: learn a mean think-minus-direct width-2 tail vector on public training prompts, use fixed pre-registered layer/alpha/active-step settings from prior controller sweeps, then evaluate held-out public generations without donor activations.
- Train prompts: `24`; eval prompts: `100` per model.
- Eval max tokens: `1024`; selection max tokens: `768`.

## Selected Controllers

- `qwen35_4b` layer `15` alpha `1.0` active steps `1`: selection reasoning `preset`, accuracy `preset`, truncation `preset`, degeneration `preset`

## Held-Out Generation

- `qwen35_4b` `canonical_target`: reasoning `0.257`, accuracy `0.790` CI [`0.710`, `0.870`], truncation `0.120`, degeneration `0.000`, tokens `493.9`, self-correction `0.050`
- `qwen35_4b` `canonical_think`: reasoning `0.522`, accuracy `0.220` CI [`0.140`, `0.300`], truncation `0.890`, degeneration `0.000`, tokens `997.7`, self-correction `0.750`
- `qwen35_4b` `universal_controller`: reasoning `0.671`, accuracy `0.820` CI [`0.740`, `0.890`], truncation `0.110`, degeneration `0.000`, tokens `503.9`, self-correction `0.060`
