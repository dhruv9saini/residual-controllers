# gemma-nemotron-broad-prompt-boundary-20260507T020000Z

- Controller: train-learned fixed width-2 prompt-boundary residual vectors.
- Training prompts: public GSM8K/MATH-500 only.
- Evaluation prompts: 30 non-AIME prompts across general instruction, coding, factual QA, multi-turn transcript, and non-English categories.
- Evaluation is next-token branch control with no broad-eval donor activations in the deployed fixed-vector controller.

## Broad Prompt-Boundary Control

- `gemma4_e2b` `off_to_think` `fixed_mean`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6609`, JS donor `0.0204`
- `gemma4_e2b` `off_to_think` `full_tail_patch`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6798`, JS donor `0.0000`
- `gemma4_e2b` `off_to_think` `opposite_mean`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.5172`, JS donor `0.6825`
- `gemma4_e2b` `off_to_think` `random_norm_matched`: donor win `0.011` [`0.000`, `0.033`], effective `0.000` [`0.000`, `0.000`], margin `-0.1756`, JS donor `0.6886`
- `gemma4_e2b` `think_to_off` `fixed_mean`: donor win `0.800` [`0.667`, `0.933`], effective `0.733` [`0.567`, `0.900`], margin `0.2840`, JS donor `0.2916`
- `gemma4_e2b` `think_to_off` `full_tail_patch`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6799`, JS donor `0.0001`
- `gemma4_e2b` `think_to_off` `opposite_mean`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.6891`, JS donor `0.6927`
- `gemma4_e2b` `think_to_off` `random_norm_matched`: donor win `0.011` [`0.000`, `0.033`], effective `0.011` [`0.000`, `0.033`], margin `-0.6538`, JS donor `0.6723`
- `nemotron_nano_4b` `off_to_think` `fixed_mean`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6932`, JS donor `0.0001`
- `nemotron_nano_4b` `off_to_think` `full_tail_patch`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6926`, JS donor `0.0000`
- `nemotron_nano_4b` `off_to_think` `opposite_mean`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.0116`, JS donor `0.6931`
- `nemotron_nano_4b` `off_to_think` `random_norm_matched`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.0169`, JS donor `0.6930`
- `nemotron_nano_4b` `think_to_off` `fixed_mean`: donor win `1.000` [`1.000`, `1.000`], effective `0.100` [`0.000`, `0.233`], margin `0.0478`, JS donor `0.6449`
- `nemotron_nano_4b` `think_to_off` `full_tail_patch`: donor win `1.000` [`1.000`, `1.000`], effective `1.000` [`1.000`, `1.000`], margin `0.6880`, JS donor `0.0046`
- `nemotron_nano_4b` `think_to_off` `opposite_mean`: donor win `0.000` [`0.000`, `0.000`], effective `0.000` [`0.000`, `0.000`], margin `-0.6932`, JS donor `0.6932`
- `nemotron_nano_4b` `think_to_off` `random_norm_matched`: donor win `0.011` [`0.000`, `0.033`], effective `0.000` [`0.000`, `0.000`], margin `-0.6540`, JS donor `0.6891`

## Selected Controllers

- `gemma4_e2b` `off_to_think` layer `35` alpha `0.25`: train donor win `0.000`, effective `0.000`, margin `-0.6211`
- `gemma4_e2b` `off_to_think` layer `35` alpha `0.5`: train donor win `0.183`, effective `0.167`, margin `-0.3453`
- `gemma4_e2b` `off_to_think` layer `35` alpha `1.0`: train donor win `0.983`, effective `0.983`, margin `0.6042`
- `gemma4_e2b` `off_to_think` layer `35` alpha `2.0`: train donor win `1.000`, effective `1.000`, margin `0.6739`
- `gemma4_e2b` `off_to_think` layer `35` alpha `4.0`: train donor win `1.000`, effective `1.000`, margin `0.5454`
- `gemma4_e2b` `off_to_think` layer `35` alpha `8.0`: train donor win `1.000`, effective `0.000`, margin `0.0193`
- `gemma4_e2b` `think_to_off` layer `35` alpha `0.25`: train donor win `0.250`, effective `0.217`, margin `-0.4124`
- `gemma4_e2b` `think_to_off` layer `35` alpha `0.5`: train donor win `0.483`, effective `0.450`, margin `-0.0588`
- `gemma4_e2b` `think_to_off` layer `35` alpha `1.0`: train donor win `0.950`, effective `0.817`, margin `0.4273`
- `gemma4_e2b` `think_to_off` layer `35` alpha `2.0`: train donor win `0.950`, effective `0.783`, margin `0.4320`
- `gemma4_e2b` `think_to_off` layer `35` alpha `4.0`: train donor win `0.950`, effective `0.767`, margin `0.4372`
- `gemma4_e2b` `think_to_off` layer `35` alpha `8.0`: train donor win `0.950`, effective `0.717`, margin `0.3243`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `0.25`: train donor win `0.000`, effective `0.000`, margin `-0.6394`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `0.5`: train donor win `0.467`, effective `0.467`, margin `-0.0143`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `1.0`: train donor win `1.000`, effective `1.000`, margin `0.6936`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `2.0`: train donor win `1.000`, effective `1.000`, margin `0.6936`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `4.0`: train donor win `1.000`, effective `1.000`, margin `0.6936`
- `nemotron_nano_4b` `off_to_think` layer `28` alpha `8.0`: train donor win `1.000`, effective `1.000`, margin `0.6936`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `0.25`: train donor win `0.000`, effective `0.000`, margin `-0.6875`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `0.5`: train donor win `0.150`, effective `0.150`, margin `-0.4094`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `1.0`: train donor win `0.983`, effective `0.783`, margin `0.4745`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `2.0`: train donor win `1.000`, effective `0.833`, margin `0.4629`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `4.0`: train donor win `1.000`, effective `0.033`, margin `0.0175`
- `nemotron_nano_4b` `think_to_off` layer `28` alpha `8.0`: train donor win `1.000`, effective `0.033`, margin `0.0113`

- HF upload: `{'repo_id': 'oof-baroomf/reasoning-switch-research-artifacts', 'repo_type': 'dataset', 'commit_url': CommitInfo(commit_url='https://huggingface.co/datasets/oof-baroomf/reasoning-switch-research-artifacts/commit/eabdd2dfa10a96e59f1c965f3b1ddcab287f1210', commit_message='Upload gemma-nemotron-broad-prompt-boundary-20260507T020000Z', commit_description='', oid='eabdd2dfa10a96e59f1c965f3b1ddcab287f1210', pr_url=None, repo_url=RepoUrl('https://huggingface.co/datasets/oof-baroomf/reasoning-switch-research-artifacts', endpoint='https://huggingface.co', repo_type='dataset', repo_id='oof-baroomf/reasoning-switch-research-artifacts'), pr_revision=None, pr_num=None)}`
