# MCDC Summer 2026 tutorials

Python notebooks and rendered HTML lessons for the Metropolitan Chicago Data Science Corps, with source data, analysis outputs, and an interactive Chicago TIF explorer.

## Lessons

| Lesson | Notebook | Rendered HTML | Notes |
| --- | --- | --- | --- |
| Chicago TIF PDF extraction | [Notebook](chicago_tif_pdf_extraction_tutorial.ipynb) | [HTML](chicago_tif_pdf_extraction_tutorial.html) | Setup and source notes are in the notebook |
| Morton root traits and PCA | [Notebook](morton_root_traits_pca_tutorial.ipynb) | [HTML](morton_root_traits_pca_tutorial.html) | [Guide](README_root_traits_pca.md) |
| Morton grouped cross-validation | [Notebook](morton_grouped_cross_validation_tutorial.ipynb) | [HTML](morton_grouped_cross_validation_tutorial.html) | [Guide](README_grouped_cross_validation.md) |
| Chicago TIF data explorer | [Notebook](chicago_tif_data_explorer_tutorial.ipynb) | [HTML](chicago_tif_data_explorer_tutorial.html) | [Guide](README_tif_data_explorer.md) |

Download or clone this repository and open the HTML files locally in a browser. Open [chicago_tif_explorer.html](chicago_tif_explorer.html) for the interactive explorer.

## Run and render

Open the notebooks in Jupyter using a Python environment with the packages listed in the corresponding `requirements_*.txt` file. The PDF extraction notebook lists its dependencies in its setup cell. Run notebooks from this folder so relative paths to `data/` and `images/` resolve correctly.

With Quarto installed, render a notebook using its saved outputs:

```bash
quarto render chicago_tif_data_explorer_tutorial.ipynb --to html
```

Each notebook includes matching Quarto styling and PDF configuration using Tectonic. To render PDF, install Tectonic and use `--to pdf`. The headers disable code execution during rendering; run and save the notebooks in Jupyter first when updating results. Interactive HTML features are intended for a browser.

## Data and attribution

Original data and source records are in `data/raw/`; derived tables and analysis provenance are in `data/processed/`. Preserve source attribution and consult the source records and original project terms when reusing data or materials. The TIF explorer describes a frozen 2010–2023 snapshot.
