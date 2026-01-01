# Indic Languages Disinformation Datasets

Test sets for zero-shot cross-lingual disinformation detection in Indic languages.

- bangla_test.csv (2000 samples)
- hindi_test.csv (1500 samples)
- malayalam_test.csv (1200 samples)
- tamil_test.csv (1300 samples)

These are stratified random samples from larger curated datasets, used as test sets in the thesis (no training data provided for target languages).

Full source datasets available upon request.

License: CC BY 4.0 (attribution required)

## Reproducibility

The test splits used in the thesis can be exactly reproduced using the provided script:

```bash
python create_test_splits.py
