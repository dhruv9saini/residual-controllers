# Nemotron same-checkpoint localization

- Model: `mlx-community/Llama-3.1-Nemotron-Nano-4B-v1.1-4bit`.
- Prompts: `12`.
- Modes are the public same-checkpoint system-prompt switch: `detailed thinking on` vs `detailed thinking off`.

## Tail and control patching
- `off_to_think` `tail_w1`: first perfect layer `16`, best donor win `1.000`.
- `off_to_think` `tail_w2`: first perfect layer `16`, best donor win `1.000`.
- `off_to_think` `tail_w4`: first perfect layer `16`, best donor win `1.000`.
- `off_to_think` `nontail_w2`: first perfect layer `None`, best donor win `0.000`.
- `off_to_think` `nontail_w4`: first perfect layer `None`, best donor win `0.000`.
- `off_to_think` `prefix_w4`: first perfect layer `None`, best donor win `0.000`.
- `think_to_off` `tail_w1`: first perfect layer `16`, best donor win `1.000`.
- `think_to_off` `tail_w2`: first perfect layer `12`, best donor win `1.000`.
- `think_to_off` `tail_w4`: first perfect layer `12`, best donor win `1.000`.
- `think_to_off` `nontail_w2`: first perfect layer `None`, best donor win `0.000`.
- `think_to_off` `nontail_w4`: first perfect layer `None`, best donor win `0.000`.
- `think_to_off` `prefix_w4`: first perfect layer `None`, best donor win `0.000`.

## Module patching best donor win
- `off_to_think` `attention_only` width `1`: best donor win `1.000`.
- `off_to_think` `attention_only` width `2`: best donor win `1.000`.
- `off_to_think` `full_layer` width `1`: best donor win `1.000`.
- `off_to_think` `full_layer` width `2`: best donor win `1.000`.
- `off_to_think` `mlp_only` width `1`: best donor win `0.000`.
- `off_to_think` `mlp_only` width `2`: best donor win `0.000`.
- `think_to_off` `attention_only` width `1`: best donor win `1.000`.
- `think_to_off` `attention_only` width `2`: best donor win `1.000`.
- `think_to_off` `full_layer` width `1`: best donor win `1.000`.
- `think_to_off` `full_layer` width `2`: best donor win `1.000`.
- `think_to_off` `mlp_only` width `1`: best donor win `0.000`.
- `think_to_off` `mlp_only` width `2`: best donor win `0.000`.
