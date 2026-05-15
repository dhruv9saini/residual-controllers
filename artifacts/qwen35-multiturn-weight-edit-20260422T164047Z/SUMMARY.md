# qwen35-multiturn-weight-edit-20260422T164047Z

- Model: `mlx-community/Qwen3.5-4B-4bit`
- Prompt count: `24`
- Condition count: `6`
- Patch layers: `[0, 4, 8, 12, 16, 20, 24, 28, 32]`

## Multi-Turn Condition Aggregates

- `multiturn_clean_1`: mean think/no-think next-token JS `0.6891`, mean final hidden cosine distance `0.6522`
- `multiturn_empty_history_1`: mean think/no-think next-token JS `0.6572`, mean final hidden cosine distance `0.6086`
- `multiturn_empty_history_3`: mean think/no-think next-token JS `0.6110`, mean final hidden cosine distance `0.6169`
- `multiturn_reasoning_history_1`: mean think/no-think next-token JS `0.5152`, mean final hidden cosine distance `0.4877`
- `multiturn_reasoning_history_3`: mean think/no-think next-token JS `0.4291`, mean final hidden cosine distance `0.3231`
- `single_turn`: mean think/no-think next-token JS `0.6841`, mean final hidden cosine distance `0.6303`

## History Shift Vs Single Turn

- `multiturn_clean_1`: mean think JS to single-turn `0.1748`, mean no-think JS to single-turn `0.0285`, think top-1 match `0.542`, no-think top-1 match `0.917`
- `multiturn_empty_history_1`: mean think JS to single-turn `0.1264`, mean no-think JS to single-turn `0.0305`, think top-1 match `0.667`, no-think top-1 match `0.917`
- `multiturn_empty_history_3`: mean think JS to single-turn `0.3026`, mean no-think JS to single-turn `0.0966`, think top-1 match `0.375`, no-think top-1 match `0.875`
- `multiturn_reasoning_history_1`: mean think JS to single-turn `0.3827`, mean no-think JS to single-turn `0.0811`, think top-1 match `0.125`, no-think top-1 match `0.875`
- `multiturn_reasoning_history_3`: mean think JS to single-turn `0.6536`, mean no-think JS to single-turn `0.1189`, think top-1 match `0.000`, no-think top-1 match `0.875`
- `single_turn`: mean think JS to single-turn `0.0000`, mean no-think JS to single-turn `0.0000`, think top-1 match `1.000`, no-think top-1 match `1.000`

## Raw Logit Lens Highlights

- `single_turn` `think` earliest same-mode win rate >= 0.9: layer `0`
- `single_turn` `no_think` earliest same-mode win rate >= 0.9: layer `13`
- `multiturn_clean_1` `think` earliest same-mode win rate >= 0.9: layer `25`
- `multiturn_clean_1` `no_think` earliest same-mode win rate >= 0.9: layer `13`
- `multiturn_empty_history_1` `think` earliest same-mode win rate >= 0.9: layer `26`
- `multiturn_empty_history_1` `no_think` earliest same-mode win rate >= 0.9: layer `19`
- `multiturn_reasoning_history_1` `think` earliest same-mode win rate >= 0.9: layer `0`
- `multiturn_reasoning_history_1` `no_think` earliest same-mode win rate >= 0.9: layer `24`
- `multiturn_empty_history_3` `think` earliest same-mode win rate >= 0.9: layer `26`
- `multiturn_empty_history_3` `no_think` earliest same-mode win rate >= 0.9: layer `23`
- `multiturn_reasoning_history_3` `think` earliest same-mode win rate >= 0.9: layer `0`
- `multiturn_reasoning_history_3` `no_think` earliest same-mode win rate >= 0.9: layer `24`

## Width Patch Highlights

- `single_turn` `think_to_no_think` width `1` best donor win `1.000` at layer `32`
- `single_turn` `think_to_no_think` width `2` best donor win `1.000` at layer `0`
- `single_turn` `think_to_no_think` width `4` best donor win `1.000` at layer `0`
- `single_turn` `no_think_to_think` width `1` best donor win `1.000` at layer `24`
- `single_turn` `no_think_to_think` width `2` best donor win `1.000` at layer `0`
- `single_turn` `no_think_to_think` width `4` best donor win `1.000` at layer `0`
- `multiturn_clean_1` `think_to_no_think` width `1` best donor win `1.000` at layer `20`
- `multiturn_clean_1` `think_to_no_think` width `2` best donor win `1.000` at layer `0`
- `multiturn_clean_1` `think_to_no_think` width `4` best donor win `1.000` at layer `0`
- `multiturn_clean_1` `no_think_to_think` width `1` best donor win `1.000` at layer `4`
- `multiturn_clean_1` `no_think_to_think` width `2` best donor win `1.000` at layer `0`
- `multiturn_clean_1` `no_think_to_think` width `4` best donor win `1.000` at layer `0`
- `multiturn_empty_history_1` `think_to_no_think` width `1` best donor win `1.000` at layer `32`
- `multiturn_empty_history_1` `think_to_no_think` width `2` best donor win `1.000` at layer `0`
- `multiturn_empty_history_1` `think_to_no_think` width `4` best donor win `1.000` at layer `0`
- `multiturn_empty_history_1` `no_think_to_think` width `1` best donor win `1.000` at layer `4`
- `multiturn_empty_history_1` `no_think_to_think` width `2` best donor win `1.000` at layer `0`
- `multiturn_empty_history_1` `no_think_to_think` width `4` best donor win `1.000` at layer `0`
- `multiturn_reasoning_history_1` `think_to_no_think` width `1` best donor win `1.000` at layer `32`
- `multiturn_reasoning_history_1` `think_to_no_think` width `2` best donor win `1.000` at layer `0`
- `multiturn_reasoning_history_1` `think_to_no_think` width `4` best donor win `1.000` at layer `0`
- `multiturn_reasoning_history_1` `no_think_to_think` width `1` best donor win `1.000` at layer `4`
- `multiturn_reasoning_history_1` `no_think_to_think` width `2` best donor win `1.000` at layer `0`
- `multiturn_reasoning_history_1` `no_think_to_think` width `4` best donor win `1.000` at layer `0`
- `multiturn_empty_history_3` `think_to_no_think` width `1` best donor win `1.000` at layer `32`
- `multiturn_empty_history_3` `think_to_no_think` width `2` best donor win `1.000` at layer `0`
- `multiturn_empty_history_3` `think_to_no_think` width `4` best donor win `1.000` at layer `0`
- `multiturn_empty_history_3` `no_think_to_think` width `1` best donor win `1.000` at layer `8`
- `multiturn_empty_history_3` `no_think_to_think` width `2` best donor win `1.000` at layer `0`
- `multiturn_empty_history_3` `no_think_to_think` width `4` best donor win `1.000` at layer `0`
- `multiturn_reasoning_history_3` `think_to_no_think` width `1` best donor win `1.000` at layer `32`
- `multiturn_reasoning_history_3` `think_to_no_think` width `2` best donor win `1.000` at layer `0`
- `multiturn_reasoning_history_3` `think_to_no_think` width `4` best donor win `1.000` at layer `0`
- `multiturn_reasoning_history_3` `no_think_to_think` width `1` best donor win `1.000` at layer `16`
- `multiturn_reasoning_history_3` `no_think_to_think` width `2` best donor win `1.000` at layer `0`
- `multiturn_reasoning_history_3` `no_think_to_think` width `4` best donor win `1.000` at layer `0`

## Weight Edit Search

- Best positive token candidate: `Thinking` (`90700`)
- Best negative token candidate: `To` (`1206`)
- `one_row` best train alpha `0.25` with train think-closer rate `1.000`
- `two_row` best train alpha `0.25` with train think-closer rate `1.000`
- `rank1` best train alpha `16.0` with train think-closer rate `1.000`

## Weight Edit Held-Out Transfer

- `one_row` on `multiturn_clean_1`: think-closer rate `1.000`, mean JS to think `0.0242`, top edited top-1 `Thinking`
- `one_row` on `multiturn_empty_history_3`: think-closer rate `1.000`, mean JS to think `0.2050`, top edited top-1 `Thinking`
- `one_row` on `single_turn`: think-closer rate `1.000`, mean JS to think `0.2507`, top edited top-1 `Thinking`
- `rank1` on `multiturn_clean_1`: think-closer rate `1.000`, mean JS to think `0.1023`, top edited top-1 `Thinking`
- `rank1` on `multiturn_empty_history_3`: think-closer rate `1.000`, mean JS to think `0.2744`, top edited top-1 `Thinking`
- `rank1` on `single_turn`: think-closer rate `1.000`, mean JS to think `0.3612`, top edited top-1 `Thinking`
- `two_row` on `multiturn_clean_1`: think-closer rate `1.000`, mean JS to think `0.0242`, top edited top-1 `Thinking`
- `two_row` on `multiturn_empty_history_3`: think-closer rate `1.000`, mean JS to think `0.2050`, top edited top-1 `Thinking`
- `two_row` on `single_turn`: think-closer rate `1.000`, mean JS to think `0.2507`, top edited top-1 `Thinking`

## Manual Checks

### `count_strawberries_r`

- Single-turn think top-1 `Thinking`
- Single-turn no-think top-1 `To`
- Edited no-think sample (`one_row`, alpha `0.25`): `Thinking Process:  Thinking Process:Thinking ProcessThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinking`
- `single_turn` think sample: `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'r' (case-insensitive usually, but I should check the specific casing in the word pro`
- `single_turn` no-think sample: `To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  t 3.  **r** (1) 4.  a 5.  w 6.  b 7.  e 8.  **r** (2) 9.  r 10. i 1`
- `multiturn_empty_history_3` think sample: `The user is asking for a count of the letter "r" in the word "strawberries".  1.  **Analyze the word:** "strawberries" 2.  **Break it down:** s - t - r - a - w - b - e - r - r - i `
- `multiturn_empty_history_3` no-think sample: `The word **strawberries** contains **3** "r" letters.  Here is the breakdown: 1.  s 2.  t 3.  **r** (1) 4.  a 5.  w 6.  **b** 7.  e**r** (2) 8.  r (3) 9.  r (4) 10. i 11. e`

### `count_committee_m`

- Single-turn think top-1 `Thinking`
- Single-turn no-think top-1 `To`
- Edited no-think sample (`one_row`, alpha `0.25`): `Thinking Process: Thinking process:Thinking processThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingThinkingT`
- `single_turn` think sample: `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'm' (case-insensitive usually, but I should check the specific casing in the word pro`
- `single_turn` no-think sample: `To find the number of "m" letters in the word **committee**, let's break down the word letter by letter:  1.  c 2.  o 3.  m  (1) 4.  m m (2, 3) 5.  t 6.  t 7.  e  There are **3** "`
- `multiturn_empty_history_3` think sample: `The user is asking to count the occurrences of the letter "m" in the word "committee". I need to carefully analyze the word "committee" to determine the count.  1.  **Break down th`
- `multiturn_empty_history_3` no-think sample: `The word **committee** contains **2** "m" letters.  Here is the breakdown: c - o - m - m - i - t - t - e           ^ ^           (1) (2)<|im_end|>`

### `count_balloon_l`

- Single-turn think top-1 `Thinking`
- Single-turn no-think top-1 `To`
- Edited no-think sample (`one_row`, alpha `0.25`): `Thinking Process: Thinking Process:Thinking Process:Thinking Process:Thinking Process:Thinking Process:Thinking ProcessThinking ProcessThinking ProcessThinking ProcessThinking ProcessThinking ProcessThinking ProcessThink`
- `single_turn` think sample: `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter "l" (case-insensitive usually, but I should check the casing in the word provided) in`
- `single_turn` no-think sample: `To find the number of the letter **"l"** (case-insensitive) in the word **balloon**:  1.  Break down the word: **b** - **a** - **l** - **l** - **o** - **o** - **n**. 2.  Count the `
- `multiturn_empty_history_3` think sample: `The user is asking a riddle that requires counting the letter "l" in the word "balloon". Let's break it down: 1.  **Word:** "balloon" 2.  **Target letter:** "l" (case-insensitive, `
- `multiturn_empty_history_3` no-think sample: `There is **1** "l" in the word "balloon".  Here is the breakdown: b - **a** - **l** - **l** - o - o - n  Wait, let me recount carefully. B-a-**l**-**l**-o-o-n. Yes, there are **2**`

### `mul_317_248`

- Single-turn think top-1 `Thinking`
- Single-turn no-think top-1 `To`
- Edited no-think sample (`one_row`, alpha `0.25`): `Thinking Process:  1.  **Identify the operation:** The user wants to compute the product of two integers: $317$ and $248$.     Equation: $317 \times 248$  2.  **Set up the multiplication:**       ```           317       `
- `single_turn` think sample: `Thinking Process:  1.  **Analyze the Request:** The user wants to compute the product of two integers, 317 and 248, and provide the exact result.  2.  **Identify the Operation:** M`
- `single_turn` no-think sample: `To compute the product of $317$ and $248$, we can use the standard long multiplication method.  ### Step-by-Step Calculation  **1. Set up the multiplication:** $$ \begin{array}{r} `
- `multiturn_empty_history_3` think sample: `The user wants me to compute 317 multiplied by 248.  Let me calculate this step by step:  317 × 248  I can break this down: 317 × 248 = 317 × (200 + 40 + 8) = 317 × 200 + 317 × 40 `
- `multiturn_empty_history_3` no-think sample: `To compute $317 \times 248$, we can break it down using the distributive property or perform standard long multiplication.  Let's use the breakdown method: $$317 \times 248 = 317 \`
