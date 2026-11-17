# Fragility Gap: dataset list

## Contents

- `datasets.csv`: the 59 OpenML datasets used in the paper.
  - Columns: `Dataset` (name), `OpenML_ID`, `Set`.
  - `Set = primary`: the 30 datasets of the main evaluation (Table 1 of the paper).
  - `Set = supplementary`: the 29 additional datasets used only in the supplementary 59-dataset analysis.

The 59 datasets are 40 numeric-only, 13 mixed-type and 6 categorical-only.

## Getting a dataset

All datasets are public on OpenML. Each `OpenML_ID` is the dataset ID on https://www.openml.org/d/<ID>.

    from sklearn.datasets import fetch_openml
    data = fetch_openml(data_id=31, as_frame=True)   # German Credit

## Protocol used in the paper

- Missing values: median (numeric) and most frequent value (categorical), fitted on the training set only.
- Numeric features scaled; categorical features one-hot encoded.
- Stratified 70% train / 30% test split, random seed 42.
- Python with scikit-learn.

The datasets themselves are not redistributed here; each keeps its own licence on OpenML.

## Contact

Amritha Sai S - amrithasai.s2025@vitstudent.ac.in
