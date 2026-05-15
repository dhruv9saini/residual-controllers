# universal-controller-phi-careful-large-20260428T101045Z

- Intervention: one universal recipe per model family: learn a mean think-minus-direct width-2 tail vector on public training prompts, use fixed pre-registered layer/alpha/active-step settings from prior controller sweeps, then evaluate held-out public generations without donor activations.
- Train prompts: `24`; eval prompts: `100` per model.
- Eval max tokens: `1024`; selection max tokens: `768`.

## Selected Controllers

- `phi4_mini` layer `28` alpha `0.25` active steps `0`: selection reasoning `preset`, accuracy `preset`, truncation `preset`, degeneration `preset`

## Held-Out Generation

- `phi4_mini` `canonical_target`: reasoning `0.025`, accuracy `0.530` CI [`0.430`, `0.620`], truncation `0.120`, degeneration `0.010`, tokens `293.6`, self-correction `0.000`
- `phi4_mini` `canonical_think`: reasoning `1.000`, accuracy `0.280` CI [`0.190`, `0.370`], truncation `1.000`, degeneration `0.000`, tokens `1024.0`, self-correction `1.000`
- `phi4_mini` `universal_controller`: reasoning `0.042`, accuracy `0.500` CI [`0.400`, `0.600`], truncation `0.230`, degeneration `0.040`, tokens `401.0`, self-correction `0.000`
