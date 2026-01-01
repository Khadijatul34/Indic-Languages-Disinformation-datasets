## English Source Dataset (Training/Validation)

The English dataset serves as the **source language** for knowledge transfer in zero-shot experiments. It is aggregated from multiple public sources and preprocessed for binary classification (Real = 0, Fake = 1).

### Dataset Structure

Each instance has the following columns:
- **text**: The main news content (headline and/or body text, cleaned and concatenated where necessary).
- **label**: Binary label (Real = 0, Fake = 1). Mapped from original multi-class labels in sources like LIAR.
- **language**: Fixed as "English".
- **source**: Original repository ("LIAR", "ISOT", or "FakeNewsNet").
- **domain**: Primary category (e.g., "Politics", "World News", "Entertainment"), inferred or retained from source metadata.

### Aggregation and Statistics

Total instances after aggregation, cleaning, and label unification: **51,422**

Stratified split (maintaining class balance):
- **Training**: 70% → 35,995 samples
- **Validation**: 15% → 7,713 samples
- **Test**: 15% → 7,714 samples

### Sources
- LIAR dataset: https://www.cs.ucsb.edu/~william/data/liar_dataset.zip
- ISOT Fake News Dataset: https://www.uvic.ca/engineering/ece/isot/datasets/fake-news/index.php
- FakeNewsNet: https://github.com/KaiDMML/FakeNewsNet

Due to size constraints, the full English splits are not hosted here. They can be reproduced using the sources above or are available from the author upon request.

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
