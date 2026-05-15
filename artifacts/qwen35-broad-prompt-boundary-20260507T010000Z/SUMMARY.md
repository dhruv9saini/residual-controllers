# Qwen broad held-out prompt-boundary audit

- Model: `mlx-community/Qwen3.5-4B-4bit`.
- Train prompts: `30` GSM8K + `30` MATH-500 numeric public prompts.
- Evaluation prompts: `30` non-AIME prompts across general instruction, coding, factual QA, multi-turn chat, and non-English prompts.
- Intervention: fixed train-mean width-2 residual-tail controller; no evaluation donor activations or donor-target differences are used by the deployed fixed-vector intervention.

## Selection
- `thinking_induction` layer `15`, width `2`, alpha `1.0`, train prompts `60`.
- `direct_erasure` layer `19`, width `2`, alpha `2.0`, train prompts `60`.

## Aggregate
- `direct_erasure` `fixed_mean`: donor win `0.900`, effective `0.533`, JS donor `0.5058`, margin `0.1452`.
- `direct_erasure` `opposite_mean`: donor win `0.400`, effective `0.000`, JS donor `0.6918`, margin `0.0004`.
- `direct_erasure` `random_norm_matched`: donor win `0.589`, effective `0.044`, JS donor `0.6694`, margin `0.0066`.
- `thinking_induction` `fixed_mean`: donor win `0.500`, effective `0.433`, JS donor `0.3546`, margin `0.0575`.
- `thinking_induction` `opposite_mean`: donor win `0.033`, effective `0.000`, JS donor `0.6280`, margin `-0.5662`.
- `thinking_induction` `random_norm_matched`: donor win `0.033`, effective `0.022`, JS donor `0.6192`, margin `-0.5501`.

## Category aggregate
- `coding` `direct_erasure` fixed: donor win `1.000`, effective `0.500`, JS donor `0.4564`.
- `coding` `thinking_induction` fixed: donor win `0.333`, effective `0.167`, JS donor `0.5109`.
- `factual_qa` `direct_erasure` fixed: donor win `1.000`, effective `0.167`, JS donor `0.6054`.
- `factual_qa` `thinking_induction` fixed: donor win `1.000`, effective `1.000`, JS donor `0.0774`.
- `general_instruction` `direct_erasure` fixed: donor win `0.500`, effective `0.500`, JS donor `0.4971`.
- `general_instruction` `thinking_induction` fixed: donor win `0.500`, effective `0.500`, JS donor `0.1963`.
- `multi_turn_chat` `direct_erasure` fixed: donor win `1.000`, effective `1.000`, JS donor `0.4588`.
- `multi_turn_chat` `thinking_induction` fixed: donor win `0.333`, effective `0.333`, JS donor `0.4355`.
- `non_english` `direct_erasure` fixed: donor win `1.000`, effective `0.500`, JS donor `0.5116`.
- `non_english` `thinking_induction` fixed: donor win `0.333`, effective `0.167`, JS donor `0.5528`.

- HF upload: `{'repo_id': 'oof-baroomf/reasoning-switch-research-artifacts', 'repo_type': 'dataset', 'commit_url': CommitInfo(commit_url='https://huggingface.co/datasets/oof-baroomf/reasoning-switch-research-artifacts/commit/a3d72049bbbabfeb1cc0c62d4070edf0ada08b34', commit_message='Upload qwen35-broad-prompt-boundary-20260507T010000Z', commit_description='', oid='a3d72049bbbabfeb1cc0c62d4070edf0ada08b34', pr_url=None, repo_url=RepoUrl('https://huggingface.co/datasets/oof-baroomf/reasoning-switch-research-artifacts', endpoint='https://huggingface.co', repo_type='dataset', repo_id='oof-baroomf/reasoning-switch-research-artifacts'), pr_revision=None, pr_num=None)}`
