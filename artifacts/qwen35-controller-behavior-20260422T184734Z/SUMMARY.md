# qwen35-controller-behavior-20260422T184734Z

- Behavior prompts: `12`
- Patch prompts: `12`
- Models: `mlx-community/Qwen3.5-4B-4bit, mlx-community/Qwen3.5-2B-4bit`

## Behavior Aggregates

- `qwen35_4b` `control_close_same_length`: accuracy `0.750`, reasoning-preface `0.000`, direct-answer `0.917`, self-correction `0.250`, mean words before first gold mention `37.27272727272727`, mean generated tokens `309.6`, mean JS to think `0.6021`, mean JS to no-think `0.5341`
- `qwen35_4b` `control_fake_close_tag`: accuracy `0.750`, reasoning-preface `0.000`, direct-answer `0.833`, self-correction `0.250`, mean words before first gold mention `95.08333333333333`, mean generated tokens `437.8`, mean JS to think `0.5698`, mean JS to no-think `0.2260`
- `qwen35_4b` `control_okay_same_length`: accuracy `0.833`, reasoning-preface `0.000`, direct-answer `0.250`, self-correction `0.250`, mean words before first gold mention `103.0909090909091`, mean generated tokens `351.6`, mean JS to think `0.5568`, mean JS to no-think `0.5723`
- `qwen35_4b` `control_thinkword_same_length`: accuracy `0.667`, reasoning-preface `0.000`, direct-answer `0.333`, self-correction `0.250`, mean words before first gold mention `118.33333333333333`, mean generated tokens `531.5`, mean JS to think `0.6041`, mean JS to no-think `0.5594`
- `qwen35_4b` `control_whitespace_only`: accuracy `0.833`, reasoning-preface `0.000`, direct-answer `0.917`, self-correction `0.250`, mean words before first gold mention `65.83333333333333`, mean generated tokens `358.8`, mean JS to think `0.5699`, mean JS to no-think `0.4304`
- `qwen35_4b` `no_think_closed_no_gap`: accuracy `0.667`, reasoning-preface `0.000`, direct-answer `0.833`, self-correction `0.000`, mean words before first gold mention `96.83333333333333`, mean generated tokens `348.8`, mean JS to think `0.6935`, mean JS to no-think `0.6933`
- `qwen35_4b` `no_think_full`: accuracy `0.833`, reasoning-preface `0.000`, direct-answer `0.833`, self-correction `0.000`, mean words before first gold mention `100.0`, mean generated tokens `354.0`, mean JS to think `0.6822`, mean JS to no-think `0.0000`
- `qwen35_4b` `no_think_preclose`: accuracy `0.667`, reasoning-preface `0.000`, direct-answer `0.000`, self-correction `0.000`, mean words before first gold mention `94.33333333333333`, mean generated tokens `336.2`, mean JS to think `0.6935`, mean JS to no-think `0.6934`
- `qwen35_4b` `shared_prefix_only`: accuracy `0.333`, reasoning-preface `0.417`, direct-answer `0.000`, self-correction `0.333`, mean words before first gold mention `85.75`, mean generated tokens `550.8`, mean JS to think `0.6801`, mean JS to no-think `0.6926`
- `qwen35_4b` `think_open_newline`: accuracy `0.333`, reasoning-preface `0.667`, direct-answer `0.000`, self-correction `0.500`, mean words before first gold mention `97.5`, mean generated tokens `715.8`, mean JS to think `0.0000`, mean JS to no-think `0.6822`

## Block Patch Highlights

- `qwen35_4b` `think_to_no_think` `tail_w1` best donor win `1.000` at layer `32`
- `qwen35_4b` `think_to_no_think` `tail_w2` best donor win `1.000` at layer `0`
- `qwen35_4b` `think_to_no_think` `tail_w4` best donor win `1.000` at layer `0`
- `qwen35_4b` `think_to_no_think` `nontail_w2` best donor win `0.000` at layer `0`
- `qwen35_4b` `think_to_no_think` `nontail_w4` best donor win `0.000` at layer `0`
- `qwen35_4b` `no_think_to_think` `tail_w1` best donor win `1.000` at layer `16`
- `qwen35_4b` `no_think_to_think` `tail_w2` best donor win `1.000` at layer `0`
- `qwen35_4b` `no_think_to_think` `tail_w4` best donor win `1.000` at layer `0`
- `qwen35_4b` `no_think_to_think` `nontail_w2` best donor win `0.000` at layer `0`
- `qwen35_4b` `no_think_to_think` `nontail_w4` best donor win `0.000` at layer `0`
- `qwen35_2b` `think_to_no_think` `tail_w1` best donor win `1.000` at layer `24`
- `qwen35_2b` `think_to_no_think` `tail_w2` best donor win `1.000` at layer `0`
- `qwen35_2b` `think_to_no_think` `tail_w4` best donor win `1.000` at layer `0`
- `qwen35_2b` `think_to_no_think` `nontail_w2` best donor win `0.000` at layer `0`
- `qwen35_2b` `think_to_no_think` `nontail_w4` best donor win `0.000` at layer `0`
- `qwen35_2b` `no_think_to_think` `tail_w1` best donor win `1.000` at layer `4`
- `qwen35_2b` `no_think_to_think` `tail_w2` best donor win `1.000` at layer `0`
- `qwen35_2b` `no_think_to_think` `tail_w4` best donor win `1.000` at layer `0`
- `qwen35_2b` `no_think_to_think` `nontail_w2` best donor win `0.000` at layer `0`
- `qwen35_2b` `no_think_to_think` `nontail_w4` best donor win `0.000` at layer `0`

## Module Patch Highlights

- `qwen35_4b` `think_to_no_think` `attention_only` width `1` best donor win `1.000` at layer `28`
- `qwen35_4b` `think_to_no_think` `attention_only` width `2` best donor win `1.000` at layer `16`
- `qwen35_4b` `think_to_no_think` `mlp_only` width `1` best donor win `0.000` at layer `16`
- `qwen35_4b` `think_to_no_think` `mlp_only` width `2` best donor win `0.000` at layer `16`
- `qwen35_4b` `think_to_no_think` `full_layer` width `1` best donor win `1.000` at layer `28`
- `qwen35_4b` `think_to_no_think` `full_layer` width `2` best donor win `1.000` at layer `16`
- `qwen35_4b` `no_think_to_think` `attention_only` width `1` best donor win `1.000` at layer `16`
- `qwen35_4b` `no_think_to_think` `attention_only` width `2` best donor win `1.000` at layer `16`
- `qwen35_4b` `no_think_to_think` `mlp_only` width `1` best donor win `0.000` at layer `16`
- `qwen35_4b` `no_think_to_think` `mlp_only` width `2` best donor win `0.167` at layer `20`
- `qwen35_4b` `no_think_to_think` `full_layer` width `1` best donor win `1.000` at layer `16`
- `qwen35_4b` `no_think_to_think` `full_layer` width `2` best donor win `1.000` at layer `16`

## Manual Samples

- `qwen35_4b` `count_strawberries_r` `shared_prefix_only`: `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'r' (case-insensitive usually, but I should check the specific casing in the word provided) in the word "strawberries".  2.  `
- `qwen35_4b` `count_strawberries_r` `think_open_newline`: `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'r' (case-insensitive usually, but I should check the specific casing in the word provided) in the word "strawberries".  2.  `
- `qwen35_4b` `count_strawberries_r` `no_think_preclose`: `</think>  To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  t 3.  **r** (1) 4.  a 5.  w 6.  b 7.  e 8.  **r** (2) 9.  r 10. i 11. e 12. s  There are **3** "r`
- `qwen35_4b` `count_strawberries_r` `no_think_closed_no_gap`: `To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  t 3.  **r** (1) 4.  a 5.  w 6.  b 7.  e 8.  **r** (2) 9.  r 10. i 11. e 12. s  There are **3** "r" letters `
- `qwen35_4b` `count_strawberries_r` `no_think_full`: `To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  t 3.  **r** (1) 4.  a 5.  w 6.  b 7.  e 8.  **r** (2) 9.  r 10. i 11. e 12. s  There are **3** "r" letters `
- `qwen35_4b` `count_strawberries_r` `control_okay_same_length`: `The word **strawberries** contains **2** r letters.  Here is the breakdown: s - **t** - **r** - **a** - **w** - **b** - **e** - **r** - **r** - **i** - **e** - **s**  Wait, let me recount carefully.  s - t - **r** - a - `
- `qwen35_4b` `count_strawberries_r` `control_close_same_length`: `The word **strawberries** contains **2** r letters.  Here is the breakdown: s - **t** - **r** - **a** - **w** - **b** - **e** - **r** - **r** - **i** - **e** - **s**  Wait, let me recount carefully.  s - t - **r** - a - `
- `qwen35_4b` `count_strawberries_r` `control_thinkword_same_length`: `There are **2** "r" letters in the word "strawberries".  Here is the breakdown: 1.  s 2.  **r** 3.  a 4.  w 5.  b 6.  e 7.  **r** 8.  r 9.  i 10. e 11. s  Wait, let me recount carefully.  Word: **s t r a w b e r r i e s*`
- `qwen35_4b` `count_strawberries_r` `control_whitespace_only`: `There are **3** "r" letters in the word "strawberries".  Here is the breakdown: 1.  s**t**r**a**w**b**e**r**r**i**e**s 2.  s**t**r**a**w**b**e**r**r**i**e**s 3.  s**t**r**a**w**b**e**r**r**i**e**s  Wait, let me recount c`
- `qwen35_4b` `count_strawberries_r` `control_fake_close_tag`: `The word **strawberries** contains **2** r letters.  Here is the breakdown: s - **t** - **r** - **a** - **w** - **b** - **e** - **r** - **r** - **i** - **e** - **s**  Wait, let me recount carefully. s - t - **r** - a - w`
- `qwen35_4b` `count_committee_m` `shared_prefix_only`: `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'm' (case-insensitive usually, but I should check the specific casing in the word) in the word "committee".  2.  **Analyze th`
- `qwen35_4b` `count_committee_m` `think_open_newline`: `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'm' (case-insensitive usually, but I should check the specific casing in the word) in the word "committee".  2.  **Analyze th`
- `qwen35_4b` `count_committee_m` `no_think_preclose`: `</think>  To find the number of "m" letters in the word **committee**, let's break down the spelling letter by letter:  1.  c 2.  o 3.  m 4.  m 5.  i 6.  t 7.  t 8.  e  There are **2** "m" letters in the word "committee"`
- `qwen35_4b` `count_committee_m` `no_think_closed_no_gap`: `To find the number of "m" letters in the word **committee**, let's break down the spelling letter by letter:  1.  c 2.  o 3.  m 4.  m 5.  i 6.  t 7.  t 8.  e  There are **2** "m" letters in the word "committee".`
- `qwen35_4b` `count_committee_m` `no_think_full`: `To find the number of "m" letters in the word **committee**, let's break down the spelling letter by letter:  1.  c 2.  o 3.  m 4.  m 5.  i 6.  t 7.  t 8.  e  There are **2** "m" letters in the word "committee".`
- `qwen35_4b` `count_committee_m` `control_okay_same_length`: `The word **committee** contains **1** letter "m".  Here is the breakdown: c - o - m - m - i - t - t - e  Wait, let me recount carefully. c - o - **m** - **m** - i - t - t - e  There are **2** "m" letters in the word "com`
- `qwen35_4b` `count_committee_m` `control_close_same_length`: `The word **committee** contains **1** letter "m".  Here is the breakdown: c - o - m - m - i - t - t - e  Wait, I miscounted. Let me look again.  c - o - **m** - m - i - t - t - e  There are **2** "m" letters in the word `
- `qwen35_4b` `count_committee_m` `control_thinkword_same_length`: `There is **1** "m" letter in the word "committee".  Here is the breakdown: c - o - m - m - i - t - t - e  Wait, I miscounted. Let me look again.  c - o - **m** - **m** - i - t - t - e  There are **2** "m" letters in the `
- `qwen35_4b` `count_committee_m` `control_whitespace_only`: `There is **1** "m" letter in the word "committee".  Here is the breakdown: c - o - m - m - i - t - t - e  Wait, I miscounted. Let me look again.  c - o - **m** - **m** - i - t - t - e  There are **2** "m" letters in the `
- `qwen35_4b` `count_committee_m` `control_fake_close_tag`: `The word **committee** contains **1** letter "m".  Here is the breakdown: c - o - m - m - i - t - t - e  Wait, let me recount carefully. c - o - **m** - **m** - i - t - t - e  There are **2** "m" letters in the word "com`
- `qwen35_4b` `mul_317_248` `shared_prefix_only`: `Thinking Process:  1.  **Analyze the Request:** The user wants to compute the product of 317 and 248. The result must be exact.  2.  **Identify the Operation:** Multiplication ($317 \times 248$).  3.  **Choose a Method:*`
- `qwen35_4b` `mul_317_248` `think_open_newline`: `Thinking Process:  1.  **Analyze the Request:** The user wants to compute the product of 317 and 248. The result must be exact.  2.  **Identify the Operation:** Multiplication ($317 \times 248$).  3.  **Choose a Method:*`
- `qwen35_4b` `mul_317_248` `no_think_preclose`: `</think>  To compute the product of $317$ and $248$, we can use the standard long multiplication method or the distributive property. Here is the step-by-step calculation:  ### Method: Long Multiplication  We set up the `
- `qwen35_4b` `mul_317_248` `no_think_closed_no_gap`: `To compute the product of $317$ and $248$, we can use the standard long multiplication method.  ### Step-by-Step Deduction  **1. Set up the multiplication:** $$ \begin{array}{r}   317 \\ \times 248 \\ \hline \end{array} `
- `qwen35_4b` `mul_317_248` `no_think_full`: `To compute the product of $317$ and $248$, we can use the standard long multiplication method.  ### Step-by-Step Deduction  **1. Set up the multiplication:** $$ \begin{array}{r}   317 \\ \times 248 \\ \hline \end{array} `
- `qwen35_4b` `mul_317_248` `control_okay_same_length`: `</think>  To compute the product of $317$ and $248$, we can use the standard long multiplication method or the distributive property.  **Method: Distributive Property** We can break down $248$ into $200 + 40 + 8$:  $$317`
- `qwen35_4b` `mul_317_248` `control_close_same_length`: `The exact result of 317 multiplied by 248 is 78616.  Here is the step-by-step calculation:  1.  **Set up the multiplication:**     ```       317     x 248     -----     ```  2.  **Multiply 317 by 8 (the ones digit of 248`
- `qwen35_4b` `mul_317_248` `control_thinkword_same_length`: `</think>  To compute the product of $317$ and $248$, we can use the standard long multiplication method or the distributive property. Here is the step-by-step calculation:  ### Method: Long Multiplication  We set up the `
- `qwen35_4b` `mul_317_248` `control_whitespace_only`: `317 * 248 = 78616  Here is the step-by-step calculation:  1.  **Set up the multiplication:**     ```       317     x 248     -----     ```  2.  **Multiply 317 by 8 (the ones digit of 248):**     *   $8 \times 7 = 56$ (wr`
- `qwen35_4b` `mul_317_248` `control_fake_close_tag`: `To compute $317 \times 248$, we can use the standard multiplication algorithm or the distributive property.  **Method 1: Standard Multiplication**  $$ \begin{array}{r}   317 \\ \times 248 \\ \hline \end{array} $$  1.  **`
- `qwen35_4b` `mul_126_94` `shared_prefix_only`: `Thinking Process:  1.  **Analyze the Request:** The user wants to compute the product of 126 and 94. The result must be exact.  2.  **Identify the Operation:** Multiplication: $126 \times 94$.  3.  **Choose a Method:**  `
- `qwen35_4b` `mul_126_94` `think_open_newline`: `Thinking Process:  1.  **Analyze the Request:** The user wants to compute the product of 126 and 94. The result must be exact.  2.  **Identify the Operation:** Multiplication ($126 \times 94$).  3.  **Choose a Method:** `