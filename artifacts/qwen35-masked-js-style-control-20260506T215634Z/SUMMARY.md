# Qwen masked-JS and style-vector audit

- Model: `mlx-community/Qwen3.5-4B-4bit`.
- Prompts: `40` total, `30` train, `10` test.
- Branch fixed vector is the normal train-learned donor-minus-target residual-tail adapter.
- Style vector is trained from visible verbose-vs-concise prompt pairs under the no-think suffix.
- Masked JS rows renormalize after removing special/whitespace tokens, canonical opener tokens, or the broader non-template vocabulary.

## Test aggregate
- `no_think_to_think` `branch_fixed_mean`: donor win none `1.000`, special `1.000`, openers `1.000`, non-template `1.000`, JS donor none `0.6203`.
- `no_think_to_think` `random_norm_matched_17`: donor win none `0.500`, special `0.500`, openers `0.700`, non-template `0.700`, JS donor none `0.6918`.
- `no_think_to_think` `random_norm_matched_31`: donor win none `0.500`, special `0.500`, openers `0.800`, non-template `0.800`, JS donor none `0.6916`.
- `no_think_to_think` `random_norm_matched_43`: donor win none `0.400`, special `0.400`, openers `0.500`, non-template `0.500`, JS donor none `0.6930`.
- `no_think_to_think` `style_verbosity_vector`: donor win none `0.600`, special `0.600`, openers `0.500`, non-template `0.500`, JS donor none `0.6881`.
- `think_to_no_think` `branch_fixed_mean`: donor win none `1.000`, special `1.000`, openers `1.000`, non-template `1.000`, JS donor none `0.0502`.
- `think_to_no_think` `random_norm_matched_17`: donor win none `0.700`, special `0.700`, openers `0.600`, non-template `0.600`, JS donor none `0.6922`.
- `think_to_no_think` `random_norm_matched_31`: donor win none `1.000`, special `1.000`, openers `0.600`, non-template `0.600`, JS donor none `0.2035`.
- `think_to_no_think` `random_norm_matched_43`: donor win none `0.800`, special `0.800`, openers `0.400`, non-template `0.400`, JS donor none `0.6890`.
- `think_to_no_think` `style_verbosity_vector`: donor win none `0.700`, special `0.700`, openers `0.500`, non-template `0.500`, JS donor none `0.5825`.
