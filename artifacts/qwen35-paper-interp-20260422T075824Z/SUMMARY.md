# qwen35-paper-interp-20260422T075824Z

- Model: `mlx-community/Qwen3.5-4B-4bit`
- Prompt count: `60`

## Key Aggregates

- variant `no_think_closed_no_gap`: mean JS to think `0.6933`, mean JS to no-think `0.6933`, entropy `0.0001`, think-closer `30/60`, no-think-closer `30/60`
- variant `no_think_full`: mean JS to think `0.6252`, mean JS to no-think `0.0000`, entropy `0.2983`, think-closer `0/60`, no-think-closer `60/60`
- variant `no_think_preclose`: mean JS to think `0.6933`, mean JS to no-think `0.6934`, entropy `0.0010`, think-closer `31/60`, no-think-closer `29/60`
- variant `shared_prefix_only`: mean JS to think `0.6828`, mean JS to no-think `0.6928`, entropy `0.6856`, think-closer `48/60`, no-think-closer `12/60`
- variant `think_open_newline`: mean JS to think `0.0000`, mean JS to no-think `0.6252`, entropy `0.4647`, think-closer `60/60`, no-think-closer `0/60`

## Raw Logit Lens Highlights

- `think`: earliest layer with same-mode win rate >= 0.9 is `26`; best layer `28` with win rate `1.000`
- `no_think`: earliest layer with same-mode win rate >= 0.9 is `19`; best layer `31` with win rate `1.000`

## Single-Position Patch Highlights

- `think_to_no_think` best single-position patch: rel pos `-1`, layer `31`, donor win rate `1.000`, mean JS donor `0.0005`, mean JS target `0.6236`
- `no_think_to_think` best single-position patch: rel pos `-2`, layer `0`, donor win rate `1.000`, mean JS donor `0.1578`, mean JS target `0.6021`

## Width Patch Highlights

- `think_to_no_think` width `1` best layer `31` donor win rate `1.000`
- `think_to_no_think` width `2` best layer `3` donor win rate `1.000`
- `think_to_no_think` width `4` best layer `0` donor win rate `1.000`
- `no_think_to_think` width `1` best layer `21` donor win rate `1.000`
- `no_think_to_think` width `2` best layer `0` donor win rate `1.000`
- `no_think_to_think` width `4` best layer `0` donor win rate `1.000`

## Manual Checks

### `count_strawberries_r`

- `think` top next token `Thinking` sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'r' (case-insensitive usually, but I should check the casing in the word provided) in the word "strawberries".  2.  **Analyze`
- `no_think` top next token `To` sample `To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  **r** (1) 3.  a 4.  w 5.  b 6.  e 7.  **r** (2) 8.  **r** (3) 9.  i 10. e 11. s  There are **3** "r" letter`
- variant `shared_prefix_only` closer to `think` top token `
` sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'r' (case-insensitive usually, but I should check the specific casing in the word) in`
- variant `think_open_newline` closer to `think` top token `Thinking` sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'r' (case-insensitive usually, but I should check the specific casing in the word pro`
- variant `no_think_preclose` closer to `no_think` top token `</think>` sample `</think>  To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  t 3.  **r** (1) 4.  a 5.  w 6.  b 7.  e 8.  **r** (2) 9. `
- variant `no_think_closed_no_gap` closer to `no_think` top token `

` sample `To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  **r** (1) 3.  a 4.  w 5.  b 6.  e 7.  **r** (2) 8.  **r** (3) 9.  i`
- variant `no_think_full` closer to `no_think` top token `To` sample `To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  **r** (1) 3.  a 4.  w 5.  b 6.  e 7.  **r** (2) 8.  r 9.  i 10. e 1`

### `count_committee_m`

- `think` top next token `Thinking` sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'm' (case-insensitive usually, but here it's lowercase in the query) in the word "committee".  2.  **Analyze the Target Word:`
- `no_think` top next token `To` sample `To determine the number of the letter **m** in the word **committee**, let's break down the word letter by letter:  1.  **c** 2.  **o** 3.  **m** (1) 4.  **m** (2) 5.  **i** 6.  **t** 7.  **t** 8.  **e**  The letter **m*`
- variant `shared_prefix_only` closer to `think` top token `
` sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'm' (case-insensitive usually, but I should check the specific casing in the word pro`
- variant `think_open_newline` closer to `think` top token `Thinking` sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'm' in the word "committee".  2.  **Analyze the Target Word:** The word is "committee`
- variant `no_think_preclose` closer to `think` top token `</think>` sample `</think>  To find the number of the letter **m** in the word **committee**, let's break down the spelling:  1.  c 2.  o 3.  m 4.  m 5.  i 6.  t 7.  t 8.  e  You can see that the le`
- variant `no_think_closed_no_gap` closer to `think` top token `

` sample `To find the number of "m" letters in the word **committee**, let's break down the spelling:  1.  **c** 2.  **o** 3.  **m** (First occurrence) 4.  **m** (Second occurrence) 5.  **i*`
- variant `no_think_full` closer to `no_think` top token `To` sample `To find the number of the letter **m** in the word **committee**, let's break it down letter by letter:  1.  c 2.  o 3.  m (1) 4.  m (2) 5.  i 6.  t 7.  t 8.  e  The letter **m** a`

### `count_balloon_l`

- `think` top next token `Thinking` sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'l' (case-insensitive usually, but I should check the specific casing in the word) in the word "balloon".  2.  **Analyze the `
- `no_think` top next token `To` sample `To find the number of the letter **"l"** (case-insensitive) in the word **balloon**, let's break down the spelling:  1.  **b** 2.  **a** 3.  **l** (1) 4.  **l** (2) 5.  **o** 6.  **o** 7.  **n**  The letter "l" appears t`
- variant `shared_prefix_only` closer to `think` top token `
` sample `</think>  To find the number of "l" letters in the word **balloon**, let's break it down letter by letter:  1.  **b** 2.  **a** 3.  **l** (1) 4.  **l** (2) 5.  **o** 6.  **o** 7.  `
- variant `think_open_newline` closer to `think` top token `Thinking` sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'l' (case-insensitive usually, but I should check the specific casing in the word) in`
- variant `no_think_preclose` closer to `think` top token `</think>` sample `</think>  To find the number of the letter **"l"** in the word **balloon**, let's break it down letter by letter:  1.  **b** 2.  **a** 3.  **l** (1) 4.  **l** (2) 5.  **o** 6.  **o`
- variant `no_think_closed_no_gap` closer to `think` top token `

` sample `To find the number of the letter **"l"** in the word **balloon**, let's break down the word letter by letter:  1.  **b** 2.  **a** 3.  **l** (This is the first "l") 4.  **l** (This`
- variant `no_think_full` closer to `no_think` top token `To` sample `Let's break down the word **b-a-l-l-o-o-n** to count the letter "l":  1.  b 2.  a 3.  **l** (1st occurrence) 4.  **l** (2nd occurrence) 5.  o 6.  o 7.  n  There are **2** "l" lette`

### `count_mississippi_s`

- `think` top next token `Thinking` sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 's' in the word "mississippi".  2.  **Analyze the Target Word:** The word is "mississippi".  3.  **Break Down the Word:**    `
- `no_think` top next token `To` sample `To find the number of "s" letters in the word **mississippi**, let's break down the word letter by letter:  1.  m 2.  **i** 3.  **s** (1) 4.  s**s**i (2, 3) 5.  p 6.  p 7.  i 8.  p 9.  i  The word contains **4** "s" lett`
- variant `shared_prefix_only` closer to `think` top token `
` sample `</think>  To find the number of "s" letters in the word **mississippi**, let's break it down letter by letter:  1.  **m** 2.  **i** 3.  **s** (1) 4.  **s** (2) 5.  **i** 6.  **p** `
- variant `think_open_newline` closer to `think` top token `Thinking` sample `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 's' in the word "mississippi".  2.  **Examine the Word:** The word is "mississippi". `
- variant `no_think_preclose` closer to `no_think` top token `</think>` sample `</think>  To find the number of "s" letters in the word **mississippi**, let's break it down letter by letter:  1.  m 2.  **i** 3.  **s** (1) 4.  **s** (2) 5.  i 6.  p 7.  p 8.  i `
- variant `no_think_closed_no_gap` closer to `no_think` top token `

` sample `To find the number of **s** letters in the word **mississippi**, let's break down the word letter by letter:  1.  **m** 2.  **i** 3.  **s** (1) 4.  **s** (2) 5.  **i** 6.  **p** 7.`
- variant `no_think_full` closer to `no_think` top token `To` sample `To find the number of "s" letters in the word **mississippi**, let's break down the word letter by letter:  1.  m 2.  **i** 3.  **s** (1) 4.  **s** (2) 5.  i 6.  p 7.  p 8.  i 9.  `
