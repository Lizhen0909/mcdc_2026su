# Chicago TIF data explorer lesson — Summer 2026

This fourth lesson turns CivicLab–MCDC project data into an interactive tool for comparing districts and communicating results. It follows the PDF extraction lesson and runs independently.

## Start here

- Open `chicago_tif_data_explorer_tutorial.html` to read the executed lesson.
- Open `chicago_tif_explorer.html` in a browser to use the completed explorer. Its charts and data are embedded; no server or internet connection is required.
- Open `chicago_tif_data_explorer_tutorial.ipynb` in Jupyter to work through and modify the Python analysis.
- Keep `tif_explorer_template.html`, `data/`, and `images/` beside the notebook.

Install the packages in `requirements_tif_explorer.txt` into your teaching environment. Run the notebook from its own folder. The supplied original CSV enables offline execution; the acquisition cell can retrieve and verify it if it is absent.

## Teaching sequence

Allow two 75-minute sessions. Students audit district-year records, distinguish flows from balances and cumulative measures, reshape data, rank districts, build Plotly charts, preserve missing years, and export an explorer. Six exercises and a dashboard extension support further practice. The supplied HTML template handles browser controls so students can focus on Python analysis and communication.

## Data and reproducibility

Source: https://github.com/philipayates/chicago2022TIF

Frozen revision: `a7dba68a484f49c682a823a023b6ee7f5cf20473`.

File: `TIF_PDF_Parsing/csvs/master_TIF_2023.csv`, retrieved September 5, 2026. It contains 2,049 district-year rows, 178 districts, and reporting years 2010–2023. Acquisition instructions and checksum verification are included in Part 1. Original data and README are preserved in `data/raw/mcdc_tif/`; exports and machine-readable provenance are in `data/processed/tif_explorer/`.

The source contains project-parsed financial figures, not a newly audited dataset. Coverage varies by year. Screening flags identify 28 annual/cumulative tax discrepancies and 58 rows with a negative value among the four selected measures. Values are retained unchanged. Dollar values are nominal. Missing records are not zero; balances and cumulative values must not be summed across years.

## Validation

The complete notebook executed successfully. Exported data were checked against the analysis table. Browser checks matched the saved expected values for spending, ending balance, an absent district-year, and a flagged zero value. Static charts and the explorer layout were visually inspected. The browser reported no JavaScript errors during those checks.

Package versions used for execution are recorded in `analysis_provenance.json`. Preserve source attribution and consult the original repository's terms before broader republication.
