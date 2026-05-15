# qwen35-prefix-probe-20260422T045935Z

- Model: `mlx-community/Qwen3.5-4B-4bit`
- Prompt count: `12`
- Mean final-state cosine distance: `0.6206`
- Mean next-token JS divergence: `0.6120`
- Final-token leave-one-prompt-out linear probe accuracy: `1.000`

## Best Window Probe Cells

- Layer `0`, relative prompt position `-9`: accuracy `1.000`
- Layer `0`, relative prompt position `-8`: accuracy `1.000`
- Layer `0`, relative prompt position `-7`: accuracy `1.000`
- Layer `0`, relative prompt position `-6`: accuracy `1.000`
- Layer `0`, relative prompt position `-5`: accuracy `1.000`
- Layer `0`, relative prompt position `-4`: accuracy `1.000`
- Layer `0`, relative prompt position `-3`: accuracy `1.000`
- Layer `0`, relative prompt position `-2`: accuracy `1.000`
- Layer `0`, relative prompt position `-1`: accuracy `1.000`
- Layer `1`, relative prompt position `-10`: accuracy `1.000`
- Layer `1`, relative prompt position `-9`: accuracy `1.000`
- Layer `1`, relative prompt position `-8`: accuracy `1.000`

## Manual Output Checks

### `strawberries_r`

- Think top next token: `Thinking`
- No-think top next token: `To`
- Think sample: `Thinking Process:  1.  **Analyze the Request:** The user is asking for the count of the letter 'r' (case-insensitive usually, but I should check the specific casing in the target word) in the word "strawberries".  2.  **Analyze the Target W`
- No-think sample: `To find the number of "r" letters in the word **strawberries**, let's break it down letter by letter:  1.  s 2.  **r** (1) 3.  a 4.  w 5.  b 6.  e 7.  **r** (2) 8.  r 9.  i 10. e 11. s  There are **3** "r" letters in the word "strawberries"`

### `multiply_317_248`

- Think top next token: `Thinking`
- No-think top next token: `To`
- Think sample: `Thinking Process:  1.  **Analyze the Request:** The user wants to compute the product of two numbers: 317 and 248. The result should be exact.  2.  **Identify the Operation:** Multiplication ($317 \times 248$).  3.  **Perform the Calculatio`
- No-think sample: `To compute $317 \times 248$, we can use the standard long multiplication method or the distributive property. Here is the step-by-step calculation:  ### Method: Standard Long Multiplication  We multiply $317$ by $248$:  $$ \begin{array}{r} `

### `logic_siblings`

- Think top next token: `Here`
- No-think top next token: `Let`
- Think sample: `Here's a thinking process that leads to the answer:  1.  **Analyze the Request:** The user is asking to identify the second youngest person among four individuals (Ava, Ben, Cara, Dan) based on a set of comparative statements about their ag`
- No-think sample: `Let's break down the relationships given in the statement step by step:  1.  **Ava > Ben** (Ava is older than Ben) 2.  **Ben > Cara** (Ben is older than Cara) 3.  **Cara > Dan** (Cara is older than Dan)  Combining these chains, we get the f`

### `river_crossing`

- Think top next token: `Here`
- No-think top next token: `This`
- Think sample: `Here's a thinking process that leads to the solution:  1.  **Analyze the Request:**     *   **Problem:** The "River Crossing Problem" (specifically the Wolf, Goat, and Cabbage puzzle).     *   **Entities:** Farmer, Wolf, Goat, Cabbage.     `
- No-think sample: `This is a classic logic puzzle often referred to as the "River Crossing Problem." The key constraint is that the **wolf and the goat cannot be left alone together** (the wolf will eat the goat), and the **goat and the cabbage cannot be left`
