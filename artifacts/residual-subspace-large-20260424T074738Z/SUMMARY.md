# residual-subspace-large-20260424T074738Z

- Main prompts: `20`
- Alt prompts: `40`
- Patch width: `2`
- Subspace dims: `[1, 2, 4, 8]`

## Learned Spectrum

- `qwen35_4b` `think_to_no_think` cumulative energy top-1 `0.814`, top-2 `0.875`, top-4 `0.934`
- `qwen35_4b` `no_think_to_think` cumulative energy top-1 `0.794`, top-2 `0.855`, top-4 `0.922`
- `olmo3_7b` `think_to_instruct` cumulative energy top-1 `0.825`, top-2 `0.865`, top-4 `0.923`
- `olmo3_7b` `instruct_to_think` cumulative energy top-1 `0.889`, top-2 `0.919`, top-4 `0.953`

## Held-Out Alt Prompts

- `qwen35_4b` `think_to_no_think` full patch donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `think_to_no_think` mean-direction donor win `0.900` [`0.800`, `0.975`], margin retention `0.770` [`0.609`, `0.901`]
- `qwen35_4b` `think_to_no_think` svd-`1` donor win `0.900` [`0.800`, `0.975`], margin retention `0.765` [`0.601`, `0.898`], random-`1` donor win `0.000`, random margin retention `-1.036`
- `qwen35_4b` `think_to_no_think` svd-`2` donor win `1.000` [`1.000`, `1.000`], margin retention `0.974` [`0.899`, `1.071`], random-`2` donor win `0.000`, random margin retention `-1.036`
- `qwen35_4b` `think_to_no_think` svd-`4` donor win `1.000` [`1.000`, `1.000`], margin retention `1.000` [`0.940`, `1.082`], random-`4` donor win `0.000`, random margin retention `-1.036`
- `qwen35_4b` `think_to_no_think` svd-`8` donor win `1.000` [`1.000`, `1.000`], margin retention `1.021` [`0.949`, `1.116`], random-`8` donor win `0.000`, random margin retention `-1.036`
- `qwen35_4b` `no_think_to_think` full patch donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `no_think_to_think` mean-direction donor win `0.925` [`0.825`, `1.000`], margin retention `0.829` [`0.714`, `0.923`]
- `qwen35_4b` `no_think_to_think` svd-`1` donor win `0.925` [`0.825`, `1.000`], margin retention `0.825` [`0.706`, `0.922`], random-`1` donor win `0.000`, random margin retention `-1.022`
- `qwen35_4b` `no_think_to_think` svd-`2` donor win `1.000` [`1.000`, `1.000`], margin retention `0.918` [`0.869`, `0.963`], random-`2` donor win `0.000`, random margin retention `-1.024`
- `qwen35_4b` `no_think_to_think` svd-`4` donor win `1.000` [`1.000`, `1.000`], margin retention `0.958` [`0.923`, `0.989`], random-`4` donor win `0.000`, random margin retention `-1.030`
- `qwen35_4b` `no_think_to_think` svd-`8` donor win `1.000` [`1.000`, `1.000`], margin retention `0.977` [`0.943`, `1.004`], random-`8` donor win `0.000`, random margin retention `-1.020`
- `olmo3_7b` `think_to_instruct` full patch donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `think_to_instruct` mean-direction donor win `0.950` [`0.875`, `1.000`], margin retention `0.767` [`0.667`, `0.853`]
- `olmo3_7b` `think_to_instruct` svd-`1` donor win `0.950` [`0.875`, `1.000`], margin retention `0.770` [`0.670`, `0.856`], random-`1` donor win `0.000`, random margin retention `-1.265`
- `olmo3_7b` `think_to_instruct` svd-`2` donor win `1.000` [`1.000`, `1.000`], margin retention `0.876` [`0.825`, `0.925`], random-`2` donor win `0.000`, random margin retention `-1.265`
- `olmo3_7b` `think_to_instruct` svd-`4` donor win `1.000` [`1.000`, `1.000`], margin retention `1.007` [`0.950`, `1.085`], random-`4` donor win `0.000`, random margin retention `-1.265`
- `olmo3_7b` `think_to_instruct` svd-`8` donor win `1.000` [`1.000`, `1.000`], margin retention `0.993` [`0.967`, `1.019`], random-`8` donor win `0.000`, random margin retention `-1.265`
- `olmo3_7b` `instruct_to_think` full patch donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `instruct_to_think` mean-direction donor win `1.000` [`1.000`, `1.000`], margin retention `1.012` [`0.948`, `1.076`]
- `olmo3_7b` `instruct_to_think` svd-`1` donor win `1.000` [`1.000`, `1.000`], margin retention `1.014` [`0.950`, `1.078`], random-`1` donor win `0.000`, random margin retention `-6.591`
- `olmo3_7b` `instruct_to_think` svd-`2` donor win `1.000` [`1.000`, `1.000`], margin retention `0.972` [`0.924`, `1.016`], random-`2` donor win `0.000`, random margin retention `-6.591`
- `olmo3_7b` `instruct_to_think` svd-`4` donor win `1.000` [`1.000`, `1.000`], margin retention `0.958` [`0.924`, `0.989`], random-`4` donor win `0.000`, random margin retention `-6.590`
- `olmo3_7b` `instruct_to_think` svd-`8` donor win `1.000` [`1.000`, `1.000`], margin retention `0.954` [`0.928`, `0.977`], random-`8` donor win `0.000`, random margin retention `-6.590`