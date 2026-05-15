# qwen35-bf16-residual-subspace-20260425T014455Z

- Main prompts: `10`
- Alt prompts: `20`
- Patch width: `2`
- Subspace dims: `[1, 2, 4, 8]`

## Learned Spectrum

- `qwen35_4b_bf16` `think_to_no_think` cumulative energy top-1 `0.827`, top-2 `0.888`, top-4 `0.943`
- `qwen35_4b_bf16` `no_think_to_think` cumulative energy top-1 `0.803`, top-2 `0.866`, top-4 `0.929`

## Held-Out Alt Prompts

- `qwen35_4b_bf16` `think_to_no_think` full patch donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b_bf16` `think_to_no_think` mean-direction donor win `0.900` [`0.750`, `1.000`], margin retention `0.838` [`0.681`, `0.966`]
- `qwen35_4b_bf16` `think_to_no_think` svd-`1` donor win `0.900` [`0.750`, `1.000`], margin retention `0.836` [`0.676`, `0.967`], random-`1` donor win `0.000`, random margin retention `-1.000`
- `qwen35_4b_bf16` `think_to_no_think` svd-`2` donor win `1.000` [`1.000`, `1.000`], margin retention `0.940` [`0.877`, `0.989`], random-`2` donor win `0.000`, random margin retention `-1.000`
- `qwen35_4b_bf16` `think_to_no_think` svd-`4` donor win `1.000` [`1.000`, `1.000`], margin retention `0.986` [`0.917`, `1.068`], random-`4` donor win `0.000`, random margin retention `-1.000`
- `qwen35_4b_bf16` `think_to_no_think` svd-`8` donor win `1.000` [`1.000`, `1.000`], margin retention `1.031` [`0.985`, `1.102`], random-`8` donor win `0.000`, random margin retention `-1.000`
- `qwen35_4b_bf16` `no_think_to_think` full patch donor win `1.000` [`1.000`, `1.000`]
- `qwen35_4b_bf16` `no_think_to_think` mean-direction donor win `0.950` [`0.850`, `1.000`], margin retention `0.817` [`0.676`, `0.936`]
- `qwen35_4b_bf16` `no_think_to_think` svd-`1` donor win `0.950` [`0.850`, `1.000`], margin retention `0.814` [`0.669`, `0.935`], random-`1` donor win `0.000`, random margin retention `-1.028`
- `qwen35_4b_bf16` `no_think_to_think` svd-`2` donor win `1.000` [`1.000`, `1.000`], margin retention `0.910` [`0.840`, `0.967`], random-`2` donor win `0.000`, random margin retention `-1.033`
- `qwen35_4b_bf16` `no_think_to_think` svd-`4` donor win `1.000` [`1.000`, `1.000`], margin retention `0.975` [`0.925`, `1.015`], random-`4` donor win `0.000`, random margin retention `-1.033`
- `qwen35_4b_bf16` `no_think_to_think` svd-`8` donor win `1.000` [`1.000`, `1.000`], margin retention `1.006` [`0.994`, `1.022`], random-`8` donor win `0.000`, random margin retention `-1.018`