# Branch-State Broad-Claim Evidence

This is a derived meta-analysis over existing row-level artifacts. It does not rerun model inference.

## Headline

- Fixed train-learned residual vectors induce the thinking branch on 240/240 AIME prompt/model cases across Qwen, OLMo, Gemma, and Nemotron.
- Opposite-sign controls induce it on 0/240 cases; norm-matched random controls are far weaker (19/720).
- The shared direct-erasure branch code transfers to held-out generated-prefix states on 239/360 model/prefix cases across five families.
- Blind rollout deployment hurts aggregate accuracy (197/300 vs 205/300), but policy-gated deployment improves the point estimate (213/300); paired delta 0.027 CI [-0.010, 0.063].

## Interpretation

The broad positive claim supported by these artifacts is not that a residual vector solves semantic reasoning. It is that public thinking switches create compact, reusable branch states that can be causally controlled across model families, audited with strong controls, and converted into behavior changes when deployment is gated by model/task fit.
