# residual-subspace-20260424T034506Z

- Main prompts: `8`
- Alt prompts: `8`
- Patch width: `2`
- Subspace dims: `[1, 2, 4, 8]`

## Learned Spectrum

- `qwen35_4b` `think_to_no_think` cumulative energy top-1 `0.833`, top-2 `0.896`, top-4 `0.956`
- `qwen35_4b` `no_think_to_think` cumulative energy top-1 `0.816`, top-2 `0.880`, top-4 `0.949`
- `olmo3_7b` `think_to_instruct` cumulative energy top-1 `0.835`, top-2 `0.883`, top-4 `0.939`
- `olmo3_7b` `instruct_to_think` cumulative energy top-1 `0.896`, top-2 `0.931`, top-4 `0.965`
- `phi4_mini` `think_to_instruct` cumulative energy top-1 `0.756`, top-2 `0.812`, top-4 `0.903`
- `phi4_mini` `instruct_to_think` cumulative energy top-1 `0.663`, top-2 `0.744`, top-4 `0.868`

## Held-Out Alt Prompts

- `qwen35_4b` `think_to_no_think` full patch donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `think_to_no_think` mean-direction donor win `0.625` [`0.250`, `0.875`], margin retention `0.187` [`-0.435`, `0.693`]
- `qwen35_4b` `think_to_no_think` svd-`1` donor win `0.625` [`0.250`, `0.875`], margin retention `0.169` [`-0.464`, `0.685`], random-`1` donor win `0.000`, random margin retention `-1.247`
- `qwen35_4b` `think_to_no_think` svd-`2` donor win `1.000` [`1.000`, `1.000`], margin retention `1.031` [`0.513`, `1.791`], random-`2` donor win `0.000`, random margin retention `-1.245`
- `qwen35_4b` `think_to_no_think` svd-`4` donor win `1.000` [`1.000`, `1.000`], margin retention `0.964` [`0.830`, `1.155`], random-`4` donor win `0.000`, random margin retention `-1.247`
- `qwen35_4b` `think_to_no_think` svd-`8` donor win `1.000` [`1.000`, `1.000`], margin retention `0.994` [`0.855`, `1.169`], random-`8` donor win `0.000`, random margin retention `-1.245`
- `qwen35_4b` `no_think_to_think` full patch donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b` `no_think_to_think` mean-direction donor win `0.875` [`0.625`, `1.000`], margin retention `0.685` [`0.323`, `0.938`]
- `qwen35_4b` `no_think_to_think` svd-`1` donor win `0.875` [`0.625`, `1.000`], margin retention `0.670` [`0.290`, `0.937`], random-`1` donor win `0.000`, random margin retention `-1.017`
- `qwen35_4b` `no_think_to_think` svd-`2` donor win `1.000` [`1.000`, `1.000`], margin retention `0.955` [`0.840`, `1.055`], random-`2` donor win `0.000`, random margin retention `-1.016`
- `qwen35_4b` `no_think_to_think` svd-`4` donor win `1.000` [`1.000`, `1.000`], margin retention `0.925` [`0.825`, `1.004`], random-`4` donor win `0.000`, random margin retention `-1.021`
- `qwen35_4b` `no_think_to_think` svd-`8` donor win `1.000` [`1.000`, `1.000`], margin retention `0.941` [`0.858`, `1.008`], random-`8` donor win `0.000`, random margin retention `-1.006`
- `olmo3_7b` `think_to_instruct` full patch donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `think_to_instruct` mean-direction donor win `1.000` [`1.000`, `1.000`], margin retention `0.529` [`0.204`, `0.862`]
- `olmo3_7b` `think_to_instruct` svd-`1` donor win `1.000` [`1.000`, `1.000`], margin retention `0.532` [`0.209`, `0.863`], random-`1` donor win `0.000`, random margin retention `-1.110`
- `olmo3_7b` `think_to_instruct` svd-`2` donor win `1.000` [`1.000`, `1.000`], margin retention `0.769` [`0.463`, `0.988`], random-`2` donor win `0.000`, random margin retention `-1.110`
- `olmo3_7b` `think_to_instruct` svd-`4` donor win `1.000` [`1.000`, `1.000`], margin retention `0.841` [`0.631`, `0.995`], random-`4` donor win `0.000`, random margin retention `-1.110`
- `olmo3_7b` `think_to_instruct` svd-`8` donor win `1.000` [`1.000`, `1.000`], margin retention `0.864` [`0.670`, `1.008`], random-`8` donor win `0.000`, random margin retention `-1.110`
- `olmo3_7b` `instruct_to_think` full patch donor win `1.000` [`1.000`, `1.000`]
- `olmo3_7b` `instruct_to_think` mean-direction donor win `1.000` [`1.000`, `1.000`], margin retention `0.777` [`0.575`, `0.944`]
- `olmo3_7b` `instruct_to_think` svd-`1` donor win `1.000` [`1.000`, `1.000`], margin retention `0.779` [`0.578`, `0.945`], random-`1` donor win `0.000`, random margin retention `-2.316`
- `olmo3_7b` `instruct_to_think` svd-`2` donor win `1.000` [`1.000`, `1.000`], margin retention `0.797` [`0.589`, `0.964`], random-`2` donor win `0.000`, random margin retention `-2.317`
- `olmo3_7b` `instruct_to_think` svd-`4` donor win `1.000` [`1.000`, `1.000`], margin retention `0.865` [`0.703`, `1.002`], random-`4` donor win `0.000`, random margin retention `-2.314`
- `olmo3_7b` `instruct_to_think` svd-`8` donor win `1.000` [`1.000`, `1.000`], margin retention `0.828` [`0.651`, `0.969`], random-`8` donor win `0.000`, random margin retention `-2.314`
- `phi4_mini` `think_to_instruct` full patch donor win `1.000` [`1.000`, `1.000`]
- `phi4_mini` `think_to_instruct` mean-direction donor win `0.750` [`0.375`, `1.000`], margin retention `0.508` [`-0.282`, `1.124`]
- `phi4_mini` `think_to_instruct` svd-`1` donor win `0.750` [`0.375`, `1.000`], margin retention `0.535` [`-0.257`, `1.136`], random-`1` donor win `0.000`, random margin retention `-1.899`
- `phi4_mini` `think_to_instruct` svd-`2` donor win `0.750` [`0.375`, `1.000`], margin retention `0.258` [`-0.948`, `1.107`], random-`2` donor win `0.000`, random margin retention `-1.899`
- `phi4_mini` `think_to_instruct` svd-`4` donor win `0.750` [`0.375`, `1.000`], margin retention `0.275` [`-1.070`, `1.184`], random-`4` donor win `0.000`, random margin retention `-1.899`
- `phi4_mini` `think_to_instruct` svd-`8` donor win `0.750` [`0.375`, `1.000`], margin retention `0.490` [`-0.558`, `1.220`], random-`8` donor win `0.000`, random margin retention `-1.899`
- `phi4_mini` `instruct_to_think` full patch donor win `1.000` [`1.000`, `1.000`]
- `phi4_mini` `instruct_to_think` mean-direction donor win `1.000` [`1.000`, `1.000`], margin retention `1.312` [`0.623`, `2.139`]
- `phi4_mini` `instruct_to_think` svd-`1` donor win `1.000` [`1.000`, `1.000`], margin retention `1.150` [`0.572`, `1.843`], random-`1` donor win `0.000`, random margin retention `-2.544`
- `phi4_mini` `instruct_to_think` svd-`2` donor win `0.875` [`0.625`, `1.000`], margin retention `1.130` [`0.563`, `1.762`], random-`2` donor win `0.000`, random margin retention `-2.544`
- `phi4_mini` `instruct_to_think` svd-`4` donor win `0.750` [`0.375`, `1.000`], margin retention `1.401` [`0.402`, `2.509`], random-`4` donor win `0.000`, random margin retention `-2.544`
- `phi4_mini` `instruct_to_think` svd-`8` donor win `0.750` [`0.375`, `1.000`], margin retention `0.758` [`0.217`, `1.206`], random-`8` donor win `0.000`, random margin retention `-2.544`