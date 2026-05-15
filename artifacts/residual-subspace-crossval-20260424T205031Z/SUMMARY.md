# residual-subspace-crossval-20260424T205031Z

- Folds: `3`
- Train prompts per fold: `40`
- Held-out prompts per fold: `20`
- Patch width: `2`
- Subspace dims: `[1, 2, 4, 8]`

## Mean Learned Spectrum Across Folds

- `qwen35_4b` `think_to_no_think` top-`1` cumulative energy mean `0.813`
- `qwen35_4b` `think_to_no_think` top-`2` cumulative energy mean `0.874`
- `qwen35_4b` `think_to_no_think` top-`4` cumulative energy mean `0.933`
- `qwen35_4b` `no_think_to_think` top-`1` cumulative energy mean `0.792`
- `qwen35_4b` `no_think_to_think` top-`2` cumulative energy mean `0.854`
- `qwen35_4b` `no_think_to_think` top-`4` cumulative energy mean `0.921`
- `olmo3_7b` `think_to_instruct` top-`1` cumulative energy mean `0.824`
- `olmo3_7b` `think_to_instruct` top-`2` cumulative energy mean `0.865`
- `olmo3_7b` `think_to_instruct` top-`4` cumulative energy mean `0.922`
- `olmo3_7b` `instruct_to_think` top-`1` cumulative energy mean `0.889`
- `olmo3_7b` `instruct_to_think` top-`2` cumulative energy mean `0.919`
- `olmo3_7b` `instruct_to_think` top-`4` cumulative energy mean `0.952`

## Held-Out Cross-Validation Results

- `qwen35_4b` `think_to_no_think` `mean_direction` dim `1`: donor win `0.917` [`0.833`, `0.983`], margin retention `0.755` [`0.616`, `0.869`], random donor win `0.000`
- `qwen35_4b` `think_to_no_think` `svd_subspace` dim `1`: donor win `0.917` [`0.833`, `0.983`], margin retention `0.749` [`0.608`, `0.865`], random donor win `0.000`
- `qwen35_4b` `think_to_no_think` `svd_subspace` dim `2`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.966` [`0.906`, `1.046`], random donor win `0.000`
- `qwen35_4b` `think_to_no_think` `svd_subspace` dim `4`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.974` [`0.928`, `1.028`], random donor win `0.000`
- `qwen35_4b` `think_to_no_think` `svd_subspace` dim `8`: donor win `0.983` [`0.950`, `1.000`], margin retention `0.991` [`0.934`, `1.057`], random donor win `0.000`
- `qwen35_4b` `no_think_to_think` `mean_direction` dim `1`: donor win `0.950` [`0.883`, `1.000`], margin retention `0.830` [`0.747`, `0.904`], random donor win `0.000`
- `qwen35_4b` `no_think_to_think` `svd_subspace` dim `1`: donor win `0.933` [`0.867`, `0.983`], margin retention `0.826` [`0.741`, `0.902`], random donor win `0.000`
- `qwen35_4b` `no_think_to_think` `svd_subspace` dim `2`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.910` [`0.869`, `0.948`], random donor win `0.000`
- `qwen35_4b` `no_think_to_think` `svd_subspace` dim `4`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.966` [`0.937`, `0.990`], random donor win `0.000`
- `qwen35_4b` `no_think_to_think` `svd_subspace` dim `8`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.987` [`0.963`, `1.005`], random donor win `0.000`
- `olmo3_7b` `think_to_instruct` `mean_direction` dim `1`: donor win `0.967` [`0.917`, `1.000`], margin retention `0.757` [`0.680`, `0.827`], random donor win `0.000`
- `olmo3_7b` `think_to_instruct` `svd_subspace` dim `1`: donor win `0.967` [`0.917`, `1.000`], margin retention `0.761` [`0.684`, `0.830`], random donor win `0.000`
- `olmo3_7b` `think_to_instruct` `svd_subspace` dim `2`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.862` [`0.811`, `0.908`], random donor win `0.000`
- `olmo3_7b` `think_to_instruct` `svd_subspace` dim `4`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.984` [`0.941`, `1.044`], random donor win `0.000`
- `olmo3_7b` `think_to_instruct` `svd_subspace` dim `8`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.993` [`0.970`, `1.018`], random donor win `0.000`
- `olmo3_7b` `instruct_to_think` `mean_direction` dim `1`: donor win `1.000` [`1.000`, `1.000`], margin retention `1.019` [`0.961`, `1.072`], random donor win `0.000`
- `olmo3_7b` `instruct_to_think` `svd_subspace` dim `1`: donor win `1.000` [`1.000`, `1.000`], margin retention `1.021` [`0.963`, `1.074`], random donor win `0.000`
- `olmo3_7b` `instruct_to_think` `svd_subspace` dim `2`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.967` [`0.925`, `1.006`], random donor win `0.000`
- `olmo3_7b` `instruct_to_think` `svd_subspace` dim `4`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.961` [`0.933`, `0.988`], random donor win `0.000`
- `olmo3_7b` `instruct_to_think` `svd_subspace` dim `8`: donor win `1.000` [`1.000`, `1.000`], margin retention `0.959` [`0.939`, `0.979`], random donor win `0.000`
