# universal-controller-olmo-large-20260428T054337Z

- Intervention: one universal recipe per model family: learn a mean think-minus-direct width-2 tail vector on public training prompts, use fixed pre-registered layer/alpha/active-step settings from prior controller sweeps, then evaluate held-out public generations without donor activations.
- Train prompts: `24`; eval prompts: `100` per model.
- Eval max tokens: `1024`; selection max tokens: `768`.

## Selected Controllers

- `olmo3_7b` layer `8` alpha `1.0` active steps `1`: selection reasoning `preset`, accuracy `preset`, truncation `preset`, degeneration `preset`

## Held-Out Generation

- `olmo3_7b` `canonical_target`: reasoning `0.528`, accuracy `0.730` CI [`0.640`, `0.820`], truncation `0.140`, degeneration `0.000`, tokens `474.4`, self-correction `0.110`
- `olmo3_7b` `canonical_think`: reasoning `0.900`, accuracy `0.280` CI [`0.190`, `0.370`], truncation `0.990`, degeneration `0.000`, tokens `1023.9`, self-correction `0.990`
- `olmo3_7b` `universal_controller`: reasoning `0.898`, accuracy `0.650` CI [`0.560`, `0.740`], truncation `0.320`, degeneration `0.000`, tokens `591.6`, self-correction `0.290`
