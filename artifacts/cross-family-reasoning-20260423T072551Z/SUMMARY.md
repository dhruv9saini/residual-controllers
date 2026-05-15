# cross-family-reasoning-20260423T072551Z

- Prompt count: `12`

## Template Notes

- `liquid_12b` think suffix `'<|im_start|>assistant\n'` vs instruct suffix `'<|im_start|>assistant\n'`
- `olmo3_7b` think suffix `'<|im_start|>assistant\n<think>'` vs instruct suffix `'<|im_start|>assistant\n'`

## Step-0 Divergence

- `liquid_12b`: mean JS instruct->think `0.6932`, top-1 match `0.000`, think entropy `0.0006`, instruct entropy `0.9746`
- `olmo3_7b`: mean JS instruct->think `0.6932`, top-1 match `0.000`, think entropy `0.3943`, instruct entropy `0.5009`

## Trace Transplant

- `liquid_12b` `instruct_plus_other_think_trace` step `0`: mean JS to same-trace think `0.6932`, top-1 match `0.000`
- `liquid_12b` `instruct_plus_own_think_trace` step `0`: mean JS to same-trace think `0.6932`, top-1 match `0.000`
- `liquid_12b` `instruct_plus_other_think_trace` step `8`: mean JS to same-trace think `0.6264`, top-1 match `0.000`
- `liquid_12b` `instruct_plus_own_think_trace` step `8`: mean JS to same-trace think `0.5419`, top-1 match `0.083`
- `liquid_12b` `instruct_plus_other_think_trace` step `32`: mean JS to same-trace think `0.6203`, top-1 match `0.083`
- `liquid_12b` `instruct_plus_own_think_trace` step `32`: mean JS to same-trace think `0.2942`, top-1 match `0.500`
- `liquid_12b` `instruct_plus_other_think_trace` step `64`: mean JS to same-trace think `0.6918`, top-1 match `0.000`
- `liquid_12b` `instruct_plus_own_think_trace` step `64`: mean JS to same-trace think `0.1362`, top-1 match `0.833`
- `olmo3_7b` `instruct_plus_other_think_trace` step `0`: mean JS to same-trace think `0.6932`, top-1 match `0.000`
- `olmo3_7b` `instruct_plus_own_think_trace` step `0`: mean JS to same-trace think `0.6932`, top-1 match `0.000`
- `olmo3_7b` `instruct_plus_other_think_trace` step `8`: mean JS to same-trace think `0.2352`, top-1 match `0.667`
- `olmo3_7b` `instruct_plus_own_think_trace` step `8`: mean JS to same-trace think `0.0041`, top-1 match `1.000`
- `olmo3_7b` `instruct_plus_other_think_trace` step `32`: mean JS to same-trace think `0.5992`, top-1 match `0.167`
- `olmo3_7b` `instruct_plus_own_think_trace` step `32`: mean JS to same-trace think `0.1601`, top-1 match `0.750`
- `olmo3_7b` `instruct_plus_other_think_trace` step `64`: mean JS to same-trace think `0.6926`, top-1 match `0.000`
- `olmo3_7b` `instruct_plus_own_think_trace` step `64`: mean JS to same-trace think `0.0929`, top-1 match `0.917`

## OLMo Template Ablation

- `instruct_model_canonical`: mean JS to OLMo think canonical `0.6932`, to OLMo instruct canonical `0.0000`
- `instruct_model_think_suffix`: mean JS to OLMo think canonical `0.5005`, to OLMo instruct canonical `0.6007`
- `think_model_canonical`: mean JS to OLMo think canonical `0.0000`, to OLMo instruct canonical `0.6932`
- `think_model_instruct_suffix`: mean JS to OLMo think canonical `0.6929`, to OLMo instruct canonical `0.6036`

## Manual Samples

- `liquid_12b` `count_strawberries_r` `think_canonical`: `<think> Okay, let's see. The question is asking how many 'r' letters are in the word "strawberries". Hmm, first I need to make sure I understand the problem correctly. They want the count of the letter 'r' in the spellin`
- `liquid_12b` `count_strawberries_r` `instruct_canonical`: `Let's count the number of **R** letters in the word **"strawberries"**.  The word is: **strawberries**  Counting the letters: - s t r a w b e r r s t s  Now, let's look for the letter **R**:  - The word has **two** R's: `
- `liquid_12b` `count_committee_m` `think_canonical`: `<think> Okay, let's see. The question is asking how many m letters are in the word "committee". Wait, hold on, actually, the question says "how many m letters are in the word committee?" Hmm, maybe I need to parse that a`
- `liquid_12b` `count_committee_m` `instruct_canonical`: `To determine how many **m** letters are in the word **"committee"**, we need to analyze the word and count the number of letters.  ### Step 1: Write down the word The word is: **committee**  ### Step 2: Count the number `
- `liquid_12b` `mul_317_248` `think_canonical`: `<think> Okay, let me see. I need to compute 317 multiplied by 248 and give the exact result. Hmm, so first, I should just multiply these two numbers together. But how? Maybe the straightforward way is just to do the mult`
- `liquid_12b` `mul_317_248` `instruct_canonical`: `We are asked to compute the product of 317 and 248.  We can compute this using standard multiplication:  $$ 317 \times 248 $$  We can break this down using the distributive property:  $$ 317 \times 248 = 317 \times (200 `
- `liquid_12b` `count_strawberries_r` `instruct_plus_own_think_trace`: `need to count the letters in "strawberries" and see how many of them are 'r'.  Let's break it down:  **Word:** strawberries  Count the letters: - s t r a w s t r i s t s  Now, let's look at each letter and check for 'r':`
- `liquid_12b` `count_strawberries_r` `instruct_plus_other_think_trace`: `word is **"strawberries"**.  Let's count the letters in "strawberries" and identify the number of **r** letters.  **Step 1: Write the word and count the letters.**  "strawberries" has 11 letters.  Now, let's count the nu`
- `liquid_12b` `count_committee_m` `instruct_plus_own_think_trace`: `word is "committee", which has 9 letters. But the question is about how many of those letters are m's.  Let's count the letters in "committee": - c - o - m - m - i - t - t - e - t  Now let's count the m's: - The first le`
- `liquid_12b` `count_committee_m` `instruct_plus_other_think_trace`: `count the letters in "committee".  Counting the letters: c, o, m, m, m, i, t, t, i, t, e, s.  Let's break it down: - c (1) - o (2) - m (3, 4, 5) - i (6) - t (7, 8) - i (9) - t (10) - e (11) - s`
- `liquid_12b` `mul_317_248` `instruct_plus_own_think_trace`: `recall how to multiply these two numbers efficiently.  We can break this down using the distributive property:  317 × 248 = 317 × (200 + 40 + 8)  Now compute each part:  1. 317 × 200 = 63,400   2. 317 × 40 = 12,680   3. `
- `liquid_12b` `mul_317_248` `instruct_plus_other_think_trace`: `break down 317 × 248.  We can write 317 × 248 as 317 × (200 + 40 + 8).  First, compute 317 × 200 = 63,400.  Next, 317 × 40 = 12,680.  Then, 317 × 8 = 2,536.  Now add them together: 63,400 + 12,680 = 76,080   76,080`
- `olmo3_7b` `count_strawberries_r` `think_canonical`: `Okay, so the question is asking how many r letters are in the word "strawberries". Let me think. First, I need to make sure I spell the word correctly in my head. S-T-R-A-W-B-E-R-R-I-E-S. Wait, let me break it down lette`
- `olmo3_7b` `count_strawberries_r` `instruct_canonical`: `Let's break down the word **"strawberries"** and count the letter **"r"** (case-insensitive, assuming all letters are lowercase as in the word itself):  s t r a w b e r r i e s  Let's go through each letter and count the`
- `olmo3_7b` `count_committee_m` `think_canonical`: `Okay, so the question is asking how many letters are in the word "committee." Let me think. First, I need to make sure I spell the word correctly in my head. C-O-M-M-I-T-T-E-E. Let me break it down letter by letter.  Sta`
- `olmo3_7b` `count_committee_m` `instruct_canonical`: `The word **"committee"** has **9 letters**.   Let's break it down: C-O-M-M-I-T-T-E-E  Count them: 1. C 2. O 3. M 4. M 5. I 6. T 7. T 8. E 9. E  So, there are **9 m (or, more accurately, 9 letters in total)** in the word `
- `olmo3_7b` `mul_317_248` `think_canonical`: `Okay, so I need to compute 317 multiplied by 248. Hmm, let me think about how to approach this. I remember that multiplying large numbers can be done by breaking them down into smaller parts, maybe using the distributive`
- `olmo3_7b` `mul_317_248` `instruct_canonical`: `Let's compute \( 317 \times 248 \) step by step.  **Method 1: Distributive Property (Breaking down 248)**  First, express 248 as \( 200 + 40 + 8 \):  \[ 317 \times 248 = 317 \times (200 + 40 + 8) \]  Now multiply 317 by `
- `olmo3_7b` `count_strawberries_r` `instruct_plus_own_think_trace`: `'m spelling the word correctly in my mind. S-T-R-A-W-B-E-R-R-I-E-S. Let me write it out letter by letter and count the Rs.  S (1), T (2), R (3), A (4), W (5), B (6), E (7), R (8), R (9), I (10), E (11), S (12).  Wait, le`
- `olmo3_7b` `count_strawberries_r` `instruct_plus_other_think_trace`: `correctly in my mind. The word is "strawberries." Let me break it down letter by letter:  S - T - R - A - W - B - E - R - R - I - E - S  Now, let's count each letter one by one:  1. S   2. T   3. R   4. A   5. W   6. B  `
- `olmo3_7b` `count_committee_m` `instruct_plus_own_think_trace`: `correctly in my mind: C-O-M-M-I-T-T-E-E. Let's count each letter one by one:  1. C   2. O   3. M   4. M   5. I   6. T   7. T   8. E   9. E    Let me double-check to make sure I didn't skip any or count any twice. Sometim`
- `olmo3_7b` `count_committee_m` `instruct_plus_other_think_trace`: `be done by breaking them into parts and using the distributive property. Let me try that.  First, let's break down 317 into 300 + 17. So, the problem becomes:  (300 + 17) × 248  Now, I'll distribute 248 to each part:  = `
- `olmo3_7b` `mul_317_248` `instruct_plus_own_think_trace`: `be done by breaking them into parts and using the distributive property. Let me try that.  First, I can break 248 into 200 + 40 + 8. Then, multiply each part by 317 and add the results together.  Let's start with 317 × 2`
- `olmo3_7b` `mul_317_248` `instruct_plus_other_think_trace`: `breaking numbers into parts can make multiplication easier. Let me try that.  First, let's break 248 into 200 + 40 + 8. Then, multiply each part by 317 and add the results together.  **Step 1: Multiply 317 by 200** 317 ×`