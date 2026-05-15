# qwen-olmo-head-localization-20260423T231325Z

- Main prompts: `8`
- Alt prompts: `8`
- Patch width: `2`

## Full Donor-H Validation

- `qwen35_4b` `no_think_to_think` full donor-h patch best donor win `1.000` [`1.000`, `1.000`] at layer `15`
- `qwen35_4b` `think_to_no_think` full donor-h patch best donor win `1.000` [`1.000`, `1.000`] at layer `15`
- `olmo3_7b` `instruct_to_think` full donor-h patch best donor win `1.000` [`1.000`, `1.000`] at layer `8`
- `olmo3_7b` `think_to_instruct` full donor-h patch best donor win `1.000` [`1.000`, `1.000`] at layer `8`

## Strongest Single-Head Knockouts

- `qwen35_4b` `think_to_no_think` best layer `15` strongest knockout head `5`: margin drop `0.0123` [`0.0046`, `0.0222`], donor win after knockout `1.000`
- `qwen35_4b` `no_think_to_think` best layer `19` strongest knockout head `13`: margin drop `0.0041` [`0.0013`, `0.0077`], donor win after knockout `1.000`
- `olmo3_7b` `think_to_instruct` best layer `12` strongest knockout head `23`: margin drop `0.0096` [`0.0006`, `0.0207`], donor win after knockout `1.000`
- `olmo3_7b` `instruct_to_think` best layer `8` strongest knockout head `24`: margin drop `0.0076` [`0.0012`, `0.0153`], donor win after knockout `1.000`

## Top-K Donor Head Retention

- `qwen35_4b` `main` `no_think_to_think` keep top-`1` donor heads at layer `19`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `main` `no_think_to_think` keep top-`2` donor heads at layer `19`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `main` `no_think_to_think` keep top-`4` donor heads at layer `19`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `main` `no_think_to_think` keep top-`8` donor heads at layer `19`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `main` `no_think_to_think` keep top-`16` donor heads at layer `19`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `alt` `no_think_to_think` keep top-`1` donor heads at layer `19`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `alt` `no_think_to_think` keep top-`2` donor heads at layer `19`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `alt` `no_think_to_think` keep top-`4` donor heads at layer `19`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `alt` `no_think_to_think` keep top-`8` donor heads at layer `19`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `alt` `no_think_to_think` keep top-`16` donor heads at layer `19`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `main` `think_to_no_think` keep top-`1` donor heads at layer `15`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `main` `think_to_no_think` keep top-`2` donor heads at layer `15`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `main` `think_to_no_think` keep top-`4` donor heads at layer `15`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `main` `think_to_no_think` keep top-`8` donor heads at layer `15`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `main` `think_to_no_think` keep top-`16` donor heads at layer `15`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `alt` `think_to_no_think` keep top-`1` donor heads at layer `15`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `alt` `think_to_no_think` keep top-`2` donor heads at layer `15`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `alt` `think_to_no_think` keep top-`4` donor heads at layer `15`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `alt` `think_to_no_think` keep top-`8` donor heads at layer `15`: donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `alt` `think_to_no_think` keep top-`16` donor heads at layer `15`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `main` `instruct_to_think` keep top-`1` donor heads at layer `8`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `main` `instruct_to_think` keep top-`2` donor heads at layer `8`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `main` `instruct_to_think` keep top-`4` donor heads at layer `8`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `main` `instruct_to_think` keep top-`8` donor heads at layer `8`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `main` `instruct_to_think` keep top-`16` donor heads at layer `8`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `alt` `instruct_to_think` keep top-`1` donor heads at layer `8`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `alt` `instruct_to_think` keep top-`2` donor heads at layer `8`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `alt` `instruct_to_think` keep top-`4` donor heads at layer `8`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `alt` `instruct_to_think` keep top-`8` donor heads at layer `8`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `alt` `instruct_to_think` keep top-`16` donor heads at layer `8`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `main` `think_to_instruct` keep top-`1` donor heads at layer `12`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `main` `think_to_instruct` keep top-`2` donor heads at layer `12`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `main` `think_to_instruct` keep top-`4` donor heads at layer `12`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `main` `think_to_instruct` keep top-`8` donor heads at layer `12`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `main` `think_to_instruct` keep top-`16` donor heads at layer `12`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `alt` `think_to_instruct` keep top-`1` donor heads at layer `12`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `alt` `think_to_instruct` keep top-`2` donor heads at layer `12`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `alt` `think_to_instruct` keep top-`4` donor heads at layer `12`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `alt` `think_to_instruct` keep top-`8` donor heads at layer `12`: donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `alt` `think_to_instruct` keep top-`16` donor heads at layer `12`: donor win `1.000` [`1.000`, `1.000`]