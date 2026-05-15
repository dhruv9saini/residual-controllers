# Qwen broad thinking-induction grid scan

- Direction: think donor into no-think target.
- Train prompts: 30 GSM8K + 30 MATH-500 numeric public prompts.
- Eval prompts: 30 broad non-AIME prompts.

## Train-selected controller
- layer `32`, width `1`, alpha `2.0`
- `opposite_mean`: donor win `0.033`, effective `0.000`, JS donor `0.6928`, margin `-0.1309`
- `random_norm_matched`: donor win `0.033`, effective `0.011`, JS donor `0.6703`, margin `-0.2139`
- `train_selected_fixed_mean`: donor win `0.400`, effective `0.233`, JS donor `0.4983`, margin `-0.1588`

## Best eval-grid rows
- layer `32`, width `1`, alpha `4.0`: donor win `0.733`, effective `0.600`, JS donor `0.4219`, margin `0.1671`
- layer `32`, width `2`, alpha `4.0`: donor win `0.733`, effective `0.600`, JS donor `0.4219`, margin `0.1671`
- layer `32`, width `4`, alpha `4.0`: donor win `0.733`, effective `0.600`, JS donor `0.4219`, margin `0.1671`
- layer `32`, width `8`, alpha `4.0`: donor win `0.733`, effective `0.600`, JS donor `0.4219`, margin `0.1671`
- layer `32`, width `1`, alpha `16.0`: donor win `0.900`, effective `0.567`, JS donor `0.5033`, margin `0.1823`
- layer `32`, width `2`, alpha `16.0`: donor win `0.900`, effective `0.567`, JS donor `0.5033`, margin `0.1823`
- layer `32`, width `4`, alpha `16.0`: donor win `0.900`, effective `0.567`, JS donor `0.5033`, margin `0.1823`
- layer `32`, width `8`, alpha `16.0`: donor win `0.900`, effective `0.567`, JS donor `0.5033`, margin `0.1823`
- layer `32`, width `1`, alpha `8.0`: donor win `0.833`, effective `0.567`, JS donor `0.4666`, margin `0.2063`
- layer `32`, width `2`, alpha `8.0`: donor win `0.833`, effective `0.567`, JS donor `0.4666`, margin `0.2063`

- HF upload: `{'repo_id': 'oof-baroomf/reasoning-switch-research-artifacts', 'repo_type': 'dataset', 'commit_url': CommitInfo(commit_url='https://huggingface.co/datasets/oof-baroomf/reasoning-switch-research-artifacts/commit/559dfb8d5d8a60e705de0920ebce06e653e62abe', commit_message='Upload qwen35-broad-induction-grid-scan-20260507T030000Z', commit_description='', oid='559dfb8d5d8a60e705de0920ebce06e653e62abe', pr_url=None, repo_url=RepoUrl('https://huggingface.co/datasets/oof-baroomf/reasoning-switch-research-artifacts', endpoint='https://huggingface.co', repo_type='dataset', repo_id='oof-baroomf/reasoning-switch-research-artifacts'), pr_revision=None, pr_num=None)}`
