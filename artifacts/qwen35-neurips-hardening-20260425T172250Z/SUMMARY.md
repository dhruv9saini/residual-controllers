# qwen35-neurips-hardening-20260425T172250Z

- Model: `mlx-community/Qwen3.5-4B-4bit`
- Prompt count: `180`
- Patch width: `2`

## Cross-Validated Low-Rank And Controls

- `think_to_no_think` `full_patch` dim `5120`: donor win `1.000`, margin retention `1.000`, JS donor `0.0036`, JS target `0.6102`, top5 donor overlap `0.922`
- `think_to_no_think` `mean_direction` dim `1`: donor win `0.939`, margin retention `0.795`, JS donor `0.0412`, JS target `0.5849`, top5 donor overlap `0.830`
- `think_to_no_think` `svd_subspace` dim `1`: donor win `0.939`, margin retention `0.786`, JS donor `0.0419`, JS target `0.5826`, top5 donor overlap `0.832`
- `think_to_no_think` `svd_subspace` dim `2`: donor win `1.000`, margin retention `0.994`, JS donor `0.0669`, JS target `0.6173`, top5 donor overlap `0.862`
- `think_to_no_think` `svd_subspace` dim `4`: donor win `0.972`, margin retention `0.885`, JS donor `0.0420`, JS target `0.6072`, top5 donor overlap `0.896`
- `think_to_no_think` `random_subspace` dim `2`: donor win `0.000`, margin retention `-1.064`, JS donor `0.6108`, JS target `0.0001`, top5 donor overlap `0.268`
- `think_to_no_think` `signed_shuffle_subspace` dim `2`: donor win `1.000`, margin retention `0.994`, JS donor `0.0669`, JS target `0.6173`, top5 donor overlap `0.862`
- `think_to_no_think` `wrong_prompt_exact_diff` dim `5120`: donor win `0.956`, margin retention `0.698`, JS donor `0.1327`, JS target `0.5867`, top5 donor overlap `0.853`
- `no_think_to_think` `full_patch` dim `5120`: donor win `1.000`, margin retention `1.000`, JS donor `0.0050`, JS target `0.6025`, top5 donor overlap `0.874`
- `no_think_to_think` `mean_direction` dim `1`: donor win `0.967`, margin retention `0.827`, JS donor `0.0889`, JS target `0.6085`, top5 donor overlap `0.700`
- `no_think_to_think` `svd_subspace` dim `1`: donor win `0.967`, margin retention `0.821`, JS donor `0.0924`, JS target `0.6094`, top5 donor overlap `0.701`
- `no_think_to_think` `svd_subspace` dim `2`: donor win `1.000`, margin retention `0.922`, JS donor `0.0623`, JS target `0.6076`, top5 donor overlap `0.777`
- `no_think_to_think` `svd_subspace` dim `4`: donor win `1.000`, margin retention `0.991`, JS donor `0.0255`, JS target `0.6117`, top5 donor overlap `0.824`
- `no_think_to_think` `random_subspace` dim `2`: donor win `0.000`, margin retention `-1.026`, JS donor `0.6109`, JS target `0.0001`, top5 donor overlap `0.264`
- `no_think_to_think` `signed_shuffle_subspace` dim `2`: donor win `1.000`, margin retention `0.922`, JS donor `0.0623`, JS target `0.6076`, top5 donor overlap `0.777`
- `no_think_to_think` `wrong_prompt_exact_diff` dim `5120`: donor win `0.994`, margin retention `0.805`, JS donor `0.1379`, JS target `0.6193`, top5 donor overlap `0.536`

## Token Controls

- `canonical_no_think`: closer-to-think `0.000`, JS think `0.6132`, JS no-think `0.0000`
- `canonical_think`: closer-to-think `1.000`, JS think `0.0000`, JS no-think `0.6132`
- `fake_close_tag`: closer-to-think `0.117`, JS think `0.6016`, JS no-think `0.4709`
- `moved_close_then_inert_tail`: closer-to-think `0.067`, JS think `0.5731`, JS no-think `0.3748`
- `real_close_outside_empty_block`: closer-to-think `0.000`, JS think `0.5936`, JS no-think `0.0534`
- `same_len_okay`: closer-to-think `0.833`, JS think `0.6519`, JS no-think `0.6713`
- `same_len_think_word`: closer-to-think `0.600`, JS think `0.6767`, JS no-think `0.6774`
- `same_len_whitespace`: closer-to-think `0.733`, JS think `0.6618`, JS no-think `0.6702`

## Rank-2 Attribution Head

- `think_to_no_think` component `1` promoted #1: `Thinking` delta `15.925`
- `think_to_no_think` component `1` promoted #2: ` user` delta `13.469`
- `think_to_no_think` component `1` promoted #3: `用户` delta `13.208`
- `think_to_no_think` component `1` promoted #4: `用户在` delta `12.139`
- `think_to_no_think` component `1` promoted #5: `思考` delta `11.722`
- `think_to_no_think` component `1` promoted #6: ` thinking` delta `11.529`
- `think_to_no_think` component `1` promoted #7: ` Thinking` delta `11.309`
- `think_to_no_think` component `1` promoted #8: `/user` delta `11.226`
- `think_to_no_think` component `1` promoted #9: `thinking` delta `10.930`
- `think_to_no_think` component `1` promoted #10: `User` delta `10.914`
- `think_to_no_think` component `1` promoted #11: `-user` delta `10.746`
- `think_to_no_think` component `1` promoted #12: `我现在` delta `10.611`
- `think_to_no_think` component `1` promoted #13: `ユーザー` delta `10.482`
- `think_to_no_think` component `1` promoted #14: `用戶` delta `10.475`
- `think_to_no_think` component `1` promoted #15: `用户的` delta `10.339`
- `think_to_no_think` component `1` promoted #16: ` users` delta `10.321`
- `think_to_no_think` component `1` promoted #17: ` User` delta `10.083`
- `think_to_no_think` component `1` promoted #18: ` thinker` delta `9.984`
- `think_to_no_think` component `1` promoted #19: ` usuario` delta `9.879`
- `think_to_no_think` component `1` promoted #20: `用户对` delta `9.874`
- `think_to_no_think` component `1` suppressed #1: ` To` delta `-9.307`
- `think_to_no_think` component `1` suppressed #2: `To` delta `-8.778`
- `think_to_no_think` component `1` suppressed #3: `###` delta `-8.713`
- `think_to_no_think` component `1` suppressed #4: `_to` delta `-8.327`
