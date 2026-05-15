# Qwen adversarial branch-state audit

- Model: `mlx-community/Qwen3.5-4B-4bit`.
- Prompts: `30` train, `10` held-out test.
- Residual classifier is a canonical think/no-think centroid projection at the learned width-2 tail state.
- Patch rows use train-learned fixed residual controllers on paired adversarial prompt variants.

## Classifier aggregate
- `concise_one_sentence` `no`: residual `1.000`, visible `1.000`, top1 `0.400`, score `-0.235`.
- `concise_one_sentence` `think`: residual `1.000`, visible `0.000`, top1 `1.000`, score `0.438`.
- `plain` `no`: residual `1.000`, visible `0.000`, top1 `0.900`, score `-0.498`.
- `plain` `think`: residual `1.000`, visible `0.000`, top1 `0.900`, score `0.500`.
- `user_fake_closed` `no`: residual `1.000`, visible `1.000`, top1 `0.700`, score `-0.384`.
- `user_fake_closed` `think`: residual `1.000`, visible `0.000`, top1 `1.000`, score `0.413`.
- `user_fake_think_tags` `no`: residual `1.000`, visible `0.000`, top1 `0.900`, score `-0.354`.
- `user_fake_think_tags` `think`: residual `1.000`, visible `1.000`, top1 `0.900`, score `0.315`.
- `user_says_direct` `no`: residual `1.000`, visible `1.000`, top1 `0.100`, score `-0.141`.
- `user_says_direct` `think`: residual `1.000`, visible `0.000`, top1 `1.000`, score `0.453`.
- `user_says_think` `no`: residual `1.000`, visible `0.000`, top1 `0.000`, score `-0.351`.
- `user_says_think` `think`: residual `1.000`, visible `1.000`, top1 `1.000`, score `0.451`.
- `verbose_step_by_step` `no`: residual `1.000`, visible `0.000`, top1 `0.900`, score `-0.456`.
- `verbose_step_by_step` `think`: residual `1.000`, visible `1.000`, top1 `1.000`, score `0.486`.

## Patch aggregate
- `concise_one_sentence` `no_think_to_think`: donor win `0.000`, effective `0.000`, JS donor `0.6934`.
- `concise_one_sentence` `think_to_no_think`: donor win `1.000`, effective `1.000`, JS donor `0.2094`.
- `plain` `no_think_to_think`: donor win `0.900`, effective `0.300`, JS donor `0.6206`.
- `plain` `think_to_no_think`: donor win `1.000`, effective `0.900`, JS donor `0.0502`.
- `user_fake_closed` `no_think_to_think`: donor win `0.300`, effective `0.100`, JS donor `0.6496`.
- `user_fake_closed` `think_to_no_think`: donor win `1.000`, effective `1.000`, JS donor `0.0469`.
- `user_fake_think_tags` `no_think_to_think`: donor win `0.200`, effective `0.000`, JS donor `0.6883`.
- `user_fake_think_tags` `think_to_no_think`: donor win `1.000`, effective `1.000`, JS donor `0.0759`.
- `user_says_direct` `no_think_to_think`: donor win `0.000`, effective `0.000`, JS donor `0.6920`.
- `user_says_direct` `think_to_no_think`: donor win `1.000`, effective `1.000`, JS donor `0.0733`.
- `user_says_think` `no_think_to_think`: donor win `0.600`, effective `0.000`, JS donor `0.6876`.
- `user_says_think` `think_to_no_think`: donor win `1.000`, effective `0.000`, JS donor `0.0220`.
- `verbose_step_by_step` `no_think_to_think`: donor win `1.000`, effective `0.300`, JS donor `0.6033`.
- `verbose_step_by_step` `think_to_no_think`: donor win `1.000`, effective `1.000`, JS donor `0.0143`.
