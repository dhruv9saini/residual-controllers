# Branch-entry paper audit
Derived from stored row-level artifacts; no new model activations were generated.
## Non-math public prompt audit
- no_think_to_think: 102/108 donor-win on non-math/algorithmic/language test prompts; mean JS donor 0.0714.
- think_to_no_think: 94/108 donor-win on non-math/algorithmic/language test prompts; mean JS donor 0.1947.
## Math public prompt audit
- no_think_to_think: 72/72 donor-win on math/counting/probability test prompts; mean JS donor 0.0969.
- think_to_no_think: 72/72 donor-win on math/counting/probability test prompts; mean JS donor 0.4245.
## Visible-prompt/logit baselines
- canonical_no_think: mean JS to think 0.6132, mean JS to no-think 0.0000, closer-to-think 0.000.
- canonical_think: mean JS to think 0.0000, mean JS to no-think 0.6132, closer-to-think 1.000.
- fake_close_tag: mean JS to think 0.6016, mean JS to no-think 0.4709, closer-to-think 0.117.
- moved_close_then_inert_tail: mean JS to think 0.5731, mean JS to no-think 0.3748, closer-to-think 0.067.
- real_close_outside_empty_block: mean JS to think 0.5936, mean JS to no-think 0.0534, closer-to-think 0.000.
- same_len_okay: mean JS to think 0.6519, mean JS to no-think 0.6713, closer-to-think 0.833.
- same_len_think_word: mean JS to think 0.6767, mean JS to no-think 0.6774, closer-to-think 0.600.
- same_len_whitespace: mean JS to think 0.6618, mean JS to no-think 0.6702, closer-to-think 0.733.
## Missing-analysis status
- Full token-masked JS cannot be reconstructed from stored artifacts because full probability vectors were not retained; top-k/argmax proxy files are included.
- A trained verbosity/style residual vector is not present in stored artifacts; visible style/suffix controls are included as a weaker baseline.
