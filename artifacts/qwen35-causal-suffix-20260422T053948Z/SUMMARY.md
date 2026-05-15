# qwen35-causal-suffix-20260422T053948Z

- Model: `mlx-community/Qwen3.5-4B-4bit`
- Prompt count: `12`

## Variant Aggregate

- `shared_prefix_only`: mean JS to think `0.6875`, mean JS to no-think `0.6924`, entropy `0.6550`, closer-to-think `8/12`, closer-to-no-think `4/12`
- `think_open_newline`: mean JS to think `0.0000`, mean JS to no-think `0.6119`, entropy `0.5348`, closer-to-think `12/12`, closer-to-no-think `0/12`
- `no_think_preclose`: mean JS to think `0.6933`, mean JS to no-think `0.6928`, entropy `0.0010`, closer-to-think `3/12`, closer-to-no-think `9/12`
- `no_think_closed_no_gap`: mean JS to think `0.6933`, mean JS to no-think `0.6928`, entropy `0.0002`, closer-to-think `3/12`, closer-to-no-think `9/12`
- `no_think_full`: mean JS to think `0.6119`, mean JS to no-think `0.0000`, entropy `0.4121`, closer-to-think `0/12`, closer-to-no-think `12/12`

## Activation Patch Aggregate

- `no_think_to_think` width `1` layer `0`: donor win rate `0.750`, mean JS to donor `0.6928`, mean JS to target `0.6933`
- `no_think_to_think` width `1` layer `4`: donor win rate `0.500`, mean JS to donor `0.2239`, mean JS to target `0.3578`
- `no_think_to_think` width `1` layer `8`: donor win rate `0.417`, mean JS to donor `0.2531`, mean JS to target `0.3460`
- `no_think_to_think` width `1` layer `12`: donor win rate `0.667`, mean JS to donor `0.2203`, mean JS to target `0.3666`
- `no_think_to_think` width `1` layer `16`: donor win rate `0.750`, mean JS to donor `0.1730`, mean JS to target `0.3946`
- `no_think_to_think` width `1` layer `20`: donor win rate `0.917`, mean JS to donor `0.1061`, mean JS to target `0.4303`
- `no_think_to_think` width `1` layer `24`: donor win rate `0.917`, mean JS to donor `0.0866`, mean JS to target `0.4511`
- `no_think_to_think` width `1` layer `28`: donor win rate `0.917`, mean JS to donor `0.0575`, mean JS to target `0.5002`
- `no_think_to_think` width `1` layer `32`: donor win rate `1.000`, mean JS to donor `0.0001`, mean JS to target `0.6122`
- `no_think_to_think` width `4` layer `0`: donor win rate `1.000`, mean JS to donor `0.0141`, mean JS to target `0.6234`
- `no_think_to_think` width `4` layer `4`: donor win rate `1.000`, mean JS to donor `0.0157`, mean JS to target `0.6118`
- `no_think_to_think` width `4` layer `8`: donor win rate `1.000`, mean JS to donor `0.0130`, mean JS to target `0.6106`
- `no_think_to_think` width `4` layer `12`: donor win rate `1.000`, mean JS to donor `0.0139`, mean JS to target `0.6119`
- `no_think_to_think` width `4` layer `16`: donor win rate `1.000`, mean JS to donor `0.0141`, mean JS to target `0.6155`
- `no_think_to_think` width `4` layer `20`: donor win rate `1.000`, mean JS to donor `0.0015`, mean JS to target `0.6122`
- `no_think_to_think` width `4` layer `24`: donor win rate `1.000`, mean JS to donor `0.0012`, mean JS to target `0.6131`
- `no_think_to_think` width `4` layer `28`: donor win rate `1.000`, mean JS to donor `0.0011`, mean JS to target `0.6137`
- `no_think_to_think` width `4` layer `32`: donor win rate `1.000`, mean JS to donor `0.0001`, mean JS to target `0.6122`
- `think_to_no_think` width `1` layer `0`: donor win rate `0.000`, mean JS to donor `0.5906`, mean JS to target `0.0403`
- `think_to_no_think` width `1` layer `4`: donor win rate `0.167`, mean JS to donor `0.4927`, mean JS to target `0.1129`
- `think_to_no_think` width `1` layer `8`: donor win rate `0.167`, mean JS to donor `0.3695`, mean JS to target `0.1537`
- `think_to_no_think` width `1` layer `12`: donor win rate `0.667`, mean JS to donor `0.2425`, mean JS to target `0.3144`
- `think_to_no_think` width `1` layer `16`: donor win rate `0.583`, mean JS to donor `0.1881`, mean JS to target `0.3381`
- `think_to_no_think` width `1` layer `20`: donor win rate `0.667`, mean JS to donor `0.1193`, mean JS to target `0.4275`
- `think_to_no_think` width `1` layer `24`: donor win rate `1.000`, mean JS to donor `0.0951`, mean JS to target `0.5028`
- `think_to_no_think` width `1` layer `28`: donor win rate `0.917`, mean JS to donor `0.0885`, mean JS to target `0.4926`
- `think_to_no_think` width `1` layer `32`: donor win rate `1.000`, mean JS to donor `0.0001`, mean JS to target `0.6116`
- `think_to_no_think` width `4` layer `0`: donor win rate `1.000`, mean JS to donor `0.0142`, mean JS to target `0.6012`
- `think_to_no_think` width `4` layer `4`: donor win rate `1.000`, mean JS to donor `0.0025`, mean JS to target `0.6042`
- `think_to_no_think` width `4` layer `8`: donor win rate `1.000`, mean JS to donor `0.0009`, mean JS to target `0.6086`
- `think_to_no_think` width `4` layer `12`: donor win rate `1.000`, mean JS to donor `0.0006`, mean JS to target `0.6112`
- `think_to_no_think` width `4` layer `16`: donor win rate `1.000`, mean JS to donor `0.0007`, mean JS to target `0.6145`
- `think_to_no_think` width `4` layer `20`: donor win rate `1.000`, mean JS to donor `0.0006`, mean JS to target `0.6132`
- `think_to_no_think` width `4` layer `24`: donor win rate `1.000`, mean JS to donor `0.0003`, mean JS to target `0.6110`
- `think_to_no_think` width `4` layer `28`: donor win rate `1.000`, mean JS to donor `0.0002`, mean JS to target `0.6106`
- `think_to_no_think` width `4` layer `32`: donor win rate `1.000`, mean JS to donor `0.0001`, mean JS to target `0.6116`

## Manual Checks

### `strawberries_r`

- `think` top next token: `Thinking`
- `think` sample: `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'r' (case-insensitive usually, but I should check the casing in the word provided) in the word "strawberries".  2.  **Analyze the Target Word:** `
- `no_think` top next token: `To`
- `no_think` sample: `To find the number of "r" letters in the word **strawberries**, let's break down the spelling letter by letter:  1.  s 2.  **r** (1) 3.  a 4.  w 5.  b 6.  e 7.  **r** (2) 8.  r 9.  i 10. e 11. s  There are **3** "r" letters in the word "str`
- variant `shared_prefix_only` closer to `think` with top next token `
` and sample `</think>  To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  **r** (1) 3.  a 4.  w 5.  b 6.  e 7.  **r** (2) 8.  r 9.  i 10. e 11. s  Ther`
- variant `think_open_newline` closer to `think` with top next token `Thinking` and sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'r' (case-insensitive usually, but the word provided is lowercase) in the word "strawberries".  2.  **Ana`
- variant `no_think_preclose` closer to `no_think` with top next token `</think>` and sample `</think>  To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  t 3.  **r** (1) 4.  a 5.  w 6.  b 7.  e 8.  **r** (2) 9.  r 10. i 11. e 12. s`
- variant `no_think_closed_no_gap` closer to `no_think` with top next token `

` and sample `To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  **r** (1) 3.  a 4.  w 5.  b 6.  e 7.  **r** (2) 8.  r 9.  i 10. e 11. s  There are **3*`
- variant `no_think_full` closer to `no_think` with top next token `To` and sample `To find the number of "r" letters in the word **strawberries**, let's break down the word letter by letter:  1.  s 2.  t 3.  **r** (1) 4.  a 5.  w 6.  b 7.  e 8.  **r** (2) 9.  r**ies** -> wait, let's`