# Morton root-traits PCA lesson

Open `morton_root_traits_pca_tutorial.ipynb` in Jupyter from this directory. An HTML companion provides a reading version. The lesson follows the summer 2026 TIF notebook's structure: context, learning objectives, short worked steps, validation, exercises, reflection, and source notes.

Install the packages in `requirements_root_traits_pca.txt` in the Python environment selected by your notebook. The existing TIF environment may not yet include scikit-learn, matplotlib, or openpyxl.

## Data

Save the original Dryad workbook as `data/raw/morton_root_traits/final_exudate_data_submission.xlsx`. See that directory's `SOURCE.md` for the DOI, original links, checksum, license, and acquisition steps. The notebook verifies the original release and never overwrites it. Once the data and packages are installed, analysis can run offline.

Derived CSV tables and an analysis manifest are generated in `data/processed/morton_root_traits_pca/`. The notebook selects the worksheet by required columns, audits conversion and missingness, and preserves source row indexes.

## Teaching sequence

- Session 1 (75 minutes): source and schema, data audit, unscaled PCA, standardization.
- Session 2 (75 minutes): unit experiment, variance retention, component coefficients, score plot, reconstruction, reporting.
- Homework: interpretation, alternative retention thresholds, and transformation sensitivity.

## Current verification status

The supplied original workbook matches the published SHA-256 checksum. All 17 code cells executed successfully against the actual data. Checks cover scaling, positive unit conversion invariance, score reconstruction, full PCA reconstruction, explained variance, and CSV round-trip values. Figures were inspected. The release contains 60 rows, 11 species, and no missing values in the six selected traits. Standardized PC1 and PC2 retain 82.80% of variance. The executed notebook includes results; the HTML includes embedded figures.

Tested Python and package versions are recorded in `data/processed/morton_root_traits_pca/analysis_provenance.json`. The original research dataset is CC0, and source attribution is included in the notebook and source record.
