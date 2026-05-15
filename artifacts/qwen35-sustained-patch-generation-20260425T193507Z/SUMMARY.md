# qwen35-sustained-patch-generation-20260425T193507Z

- Model: `mlx-community/Qwen3.5-4B-4bit`
- Prompts: `6` (`3` GSM8K, `3` numeric MATH-500)
- Sustained patch steps: `64`
- Max generation tokens: `512`
- Each sustained step recomputes donor and target full traces with the same visible generated prefix, patches the target tail residual, and greedily emits the next token.

## Overall Behavior

- `canonical_no` `baseline`: accuracy `0.667`, reasoning-preface `0.000`, direct-answer `0.833`, self-correction `0.000`, mean tokens `345.2`, truncation `0.167`
- `canonical_think` `baseline`: accuracy `0.167`, reasoning-preface `0.833`, direct-answer `0.167`, self-correction `0.000`, mean tokens `504.7`, truncation `0.833`
- `sustained_full_then_free` `no_think_to_think`: accuracy `0.333`, reasoning-preface `0.000`, direct-answer `0.833`, self-correction `0.000`, mean tokens `465.0`, truncation `0.833`
- `sustained_full_then_free` `think_to_no_think`: accuracy `0.000`, reasoning-preface `0.833`, direct-answer `0.167`, self-correction `0.500`, mean tokens `497.0`, truncation `0.833`
- `sustained_rank2_then_free` `no_think_to_think`: accuracy `0.333`, reasoning-preface `0.000`, direct-answer `1.000`, self-correction `0.167`, mean tokens `494.2`, truncation `0.833`
- `sustained_rank2_then_free` `think_to_no_think`: accuracy `0.333`, reasoning-preface `0.167`, direct-answer `0.833`, self-correction `0.167`, mean tokens `444.5`, truncation `0.500`

## Sustained Step JS

- `sustained_full` `no_think_to_think`: mean JS donor `0.0159`, mean JS target `0.0347`, steps `384`
- `sustained_rank2` `no_think_to_think`: mean JS donor `0.0523`, mean JS target `0.0104`, steps `384`
- `sustained_full` `think_to_no_think`: mean JS donor `0.0149`, mean JS target `0.0302`, steps `384`
- `sustained_rank2` `think_to_no_think`: mean JS donor `0.0603`, mean JS target `0.0074`, steps `384`

## Manual Prefix Samples

- `gsm8k_0` `canonical_think` `baseline` style `reasoning_preface` correct `0` prefix ``
- `gsm8k_0` `canonical_no` `baseline` style `direct_answer` correct `1` prefix ``
- `gsm8k_0` `sustained_full_then_free` `think_to_no_think` style `reasoning_preface` correct `0` prefix `Here's a thinking process that leads to the solution:

1.  **Analyze the Request`
- `gsm8k_0` `sustained_rank2_then_free` `think_to_no_think` style `direct_answer` correct `1` prefix `Here is the step-by-step breakdown to solve the problem:

**1. Calculate the tot`
- `gsm8k_0` `sustained_full_then_free` `no_think_to_think` style `direct_answer` correct `1` prefix `Here is the step-by-step breakdown to solve the problem:

1.  **Calculate the to`
- `gsm8k_0` `sustained_rank2_then_free` `no_think_to_think` style `direct_answer` correct `1` prefix `To solve this problem, I need to determine the number of eggs Janet sells at the`
- `gsm8k_1` `canonical_think` `baseline` style `reasoning_preface` correct `1` prefix ``
- `gsm8k_1` `canonical_no` `baseline` style `direct_answer` correct `1` prefix ``
- `gsm8k_1` `sustained_full_then_free` `think_to_no_think` style `reasoning_preface` correct `0` prefix `Thinking Process:
1.  **Analyze the Request:** The user is asking for the total `
- `gsm8k_1` `sustained_rank2_then_free` `think_to_no_think` style `reasoning_preface` correct `0` prefix `Thinking Process:
1.  **Analyze the Request:** The user is asking for the total `
- `gsm8k_1` `sustained_full_then_free` `no_think_to_think` style `direct_answer` correct `1` prefix `Here is the step-by-step breakdown to solve the problem:

1.  **Identify the amo`
- `gsm8k_1` `sustained_rank2_then_free` `no_think_to_think` style `direct_answer` correct `1` prefix `To solve this problem, I need to determine the total number of bolts of fiber re`
- `gsm8k_2` `canonical_think` `baseline` style `reasoning_preface` correct `0` prefix ``
- `gsm8k_2` `canonical_no` `baseline` style `direct_answer` correct `1` prefix ``
- `gsm8k_2` `sustained_full_then_free` `think_to_no_think` style `reasoning_preface` correct `0` prefix `Here's a thinking process that leads to the solution:

1.  **Analyze the Request`
- `gsm8k_2` `sustained_rank2_then_free` `think_to_no_think` style `direct_answer` correct `1` prefix `Here is the step-by-step calculation to determine Josh's profit:

### Step 1: Ca`
- `gsm8k_2` `sustained_full_then_free` `no_think_to_think` style `direct_answer` correct `0` prefix `To find Josh's profit, I need to calculate the total cost and the final selling `
- `gsm8k_2` `sustained_rank2_then_free` `no_think_to_think` style `direct_answer` correct `0` prefix `To solve this problem, I need to calculate the total cost of the house and then `
- `math500_numeric_2` `canonical_think` `baseline` style `direct_answer` correct `0` prefix ``
- `math500_numeric_2` `canonical_no` `baseline` style `direct_answer` correct `0` prefix ``
- `math500_numeric_2` `sustained_full_then_free` `think_to_no_think` style `direct_answer` correct `0` prefix `Here's a step-by-step solution to find the value of $f(-2) + f(-1) + f(0)$.

**1`
- `math500_numeric_2` `sustained_rank2_then_free` `think_to_no_think` style `direct_answer` correct `0` prefix `Here is the step-by-step evaluation of the function $f(x) = \frac{3x-2}{x-2}$ fo`
- `math500_numeric_2` `sustained_full_then_free` `no_think_to_think` style `direct_answer` correct `0` prefix `To find the value of $f(-2) + f(-1) + f(0)$ for the function $f(x) = \frac{3x-2}`
- `math500_numeric_2` `sustained_rank2_then_free` `no_think_to_think` style `direct_answer` correct `0` prefix `To find the value of $f(-2) + f(-1) + f(0)$, I need to evaluate the function $f(`
