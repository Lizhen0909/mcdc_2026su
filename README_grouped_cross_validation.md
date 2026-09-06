# Morton grouped cross-validation lesson

Open `morton_grouped_cross_validation_tutorial.ipynb` in Jupyter from this directory. The HTML companion includes executed results and embedded figures.

The lesson uses the same unchanged Dryad workbook as the PCA lesson and starts from raw traits. It does not reuse full-data PCA scores or scaling parameters. Install the packages in `requirements_grouped_cv.txt` in your notebook environment if needed.

## Contents

- Original data and provenance: `data/raw/morton_root_traits/`
- Out-of-fold predictions, scores, species errors, fold assignments, and analysis provenance: `data/processed/morton_grouped_cv/`
- 11-fold shuffled-row evaluation and leave-one-species-out evaluation
- Training-median baseline and fixed-alpha scaled ridge model
- Five figures, six exercises, nested group-aware tuning challenge, and reflection questions

## Validation

All 15 code cells executed successfully on the verified 60-row, 11-species dataset. Checks cover the source checksum, unique IDs, no train/test row overlap, no species overlap in grouped folds, exactly one test prediction per row per model/design, training-only scaler means, finite predictions, and CSV round-trip values. All five figures were visually inspected.

Ridge MAE is 952.87 for shuffled rows and 1043.40 for held-out species. The held-out-species baseline MAE is 884.00. The lesson reports these limitations directly. Exact settings and package versions are saved in the analysis provenance JSON. No hyperparameters were selected from test errors.

## Teaching plan

Two 75-minute sessions: data and split design first, then prediction auditing and interpretation. The lesson can stand alone or follow the Morton PCA lesson. For any predictive PCA extension, fit PCA inside the training-fold pipeline.
