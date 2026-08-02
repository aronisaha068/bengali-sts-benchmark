# Bengali STS Benchmark

A human-annotated Semantic Textual Similarity (STS) evaluation benchmark for
Bengali: 295 sentence pairs drawn from native Bengali news, each scored on the
SemEval 0–5 scale by three independent native annotators after a calibration
round.

Inter-annotator agreement is strong: Krippendorff's α = 0.863 (interval) /
0.833 (ordinal); ICC(2,k) = 0.950, 95% CI [0.93, 0.96]; mean pairwise
Pearson = 0.885.

## Contents

- `data/bn_sts_gold_test.csv` — the benchmark: 295 pairs with gold scores
  (mean of three annotators), score standard deviation, and annotator count.
- `data/A1.csv`, `data/A2.csv`, `data/A3.csv` — the three annotators' individual
  0–5 ratings.
- `code/` — evaluation code for the reported experiments.

## Recommended use

This is an **evaluation** set, not a training set. We recommend reporting both
Pearson and Spearman correlation with bootstrap confidence intervals. The
distribution is dissimilar-heavy (165 of 295 pairs in the 0–1 band), reflecting
the news domain; treat fine-grained high-similarity conclusions with care.

## Data sources and licensing

The sentence pairs were derived from publicly available Bengali news articles
published by Anandabazar Patrika and Zee News Bengali. Only short,
sentence-level excerpts are included, solely for non-commercial research use.
All rights to the original text remain with the respective publishers. If you
are a rights holder and wish to have any content removed, please open an issue
in this repository or contact the authors, and we will promptly comply.

- **Annotations and gold scores:** released under CC BY 4.0.
- **Evaluation code:** released under the MIT License.

