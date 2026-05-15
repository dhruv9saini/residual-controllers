# qwen35-public-benchmark-behavior-20260424T104510Z

- Model: `mlx-community/Qwen3.5-4B-4bit`
- Prompts: `24` (`12` GSM8K, `12` numeric MATH-500)
- Max generation tokens: `4096`
- Public data loaded from Hugging Face dataset server rows API.

## Overall Behavior

- `no_think_closed_no_gap`: accuracy `0.708`, reasoning-preface `0.000`, direct-answer `0.875`, self-correction `0.167`, mean tokens `1028.0`, truncation `0.125`
- `no_think_full`: accuracy `0.708`, reasoning-preface `0.000`, direct-answer `0.875`, self-correction `0.250`, mean tokens `1071.7`, truncation `0.125`
- `no_think_preclose`: accuracy `0.708`, reasoning-preface `0.000`, direct-answer `0.875`, self-correction `0.167`, mean tokens `984.4`, truncation `0.125`
- `shared_prefix_only`: accuracy `0.500`, reasoning-preface `0.208`, direct-answer `0.708`, self-correction `0.500`, mean tokens `2022.2`, truncation `0.375`
- `think_open_newline`: accuracy `0.417`, reasoning-preface `0.750`, direct-answer `0.167`, self-correction `0.917`, mean tokens `3585.9`, truncation `0.750`

## By Benchmark

- `gsm8k` `no_think_closed_no_gap`: accuracy `0.750`, reasoning-preface `0.000`, direct-answer `1.000`, self-correction `0.083`, mean tokens `659.2`, truncation `0.083`
- `gsm8k` `no_think_full`: accuracy `0.750`, reasoning-preface `0.000`, direct-answer `1.000`, self-correction `0.167`, mean tokens `677.0`, truncation `0.083`
- `gsm8k` `no_think_preclose`: accuracy `0.750`, reasoning-preface `0.000`, direct-answer `1.000`, self-correction `0.083`, mean tokens `660.2`, truncation `0.083`
- `gsm8k` `shared_prefix_only`: accuracy `0.750`, reasoning-preface `0.083`, direct-answer `0.917`, self-correction `0.167`, mean tokens `632.8`, truncation `0.000`
- `gsm8k` `think_open_newline`: accuracy `0.500`, reasoning-preface `1.000`, direct-answer `0.000`, self-correction `0.833`, mean tokens `3135.4`, truncation `0.583`
- `math500_numeric` `no_think_closed_no_gap`: accuracy `0.667`, reasoning-preface `0.000`, direct-answer `0.750`, self-correction `0.250`, mean tokens `1396.7`, truncation `0.167`
- `math500_numeric` `no_think_full`: accuracy `0.667`, reasoning-preface `0.000`, direct-answer `0.750`, self-correction `0.333`, mean tokens `1466.4`, truncation `0.167`
- `math500_numeric` `no_think_preclose`: accuracy `0.667`, reasoning-preface `0.000`, direct-answer `0.750`, self-correction `0.250`, mean tokens `1308.7`, truncation `0.167`
- `math500_numeric` `shared_prefix_only`: accuracy `0.250`, reasoning-preface `0.333`, direct-answer `0.500`, self-correction `0.833`, mean tokens `3411.6`, truncation `0.750`
- `math500_numeric` `think_open_newline`: accuracy `0.333`, reasoning-preface `0.500`, direct-answer `0.333`, self-correction `1.000`, mean tokens `4036.4`, truncation `0.917`

## Style Counts

- `think_open_newline`: `{'reasoning_preface': 18, 'direct_answer': 4, 'other': 2}`
- `shared_prefix_only`: `{'direct_answer': 17, 'reasoning_preface': 5, 'other': 2}`
- `no_think_preclose`: `{'direct_answer': 21, 'other': 3}`
- `no_think_closed_no_gap`: `{'direct_answer': 21, 'other': 3}`
- `no_think_full`: `{'direct_answer': 21, 'other': 3}`
