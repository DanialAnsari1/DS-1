# Practical Data Science (COSC2670) — Assignment 2: Data Modelling

Practice re-do of Assignment 2 (Semester 2, 2026) on the Dry Bean dataset, PG version (COSC2670).
Student: Danial Ansari (s4119075).

## Submission files (`Assignment2/`)

| File | What it is |
|---|---|
| `COSC2670-s4119075-A2code.ipynb` | Jupyter notebook with all code, comments and outputs (executed with Restart & Run All) |
| `COSC2670-s4119075-A2report.pdf` | The report (9 pages, text-searchable PDF built from the provided Word template) |
| `COSC2670-s4119075-A2SampleOne.csv` | Task 1 random sample (300 rows) |
| `COSC2670-s4119075-A2SampleTwo.csv` | Task 2 random sample (2,000 rows) |
| `COSC2670-s4119075-A2SampleThree.csv` | Task 3 random sample (2,000 rows) |

Not for submission: `COSC2670-s4119075-A2report.docx` (editable report), `A2data.csv` (input data),
`figures/` (graphs saved by the notebook and used in the report).

## Tasks covered (PG)

- **Task 1** – scatter plot and simple linear regression (Perimeter ~ MajorAxisLength).
- **Task 2.1** – kNN with standardisation and k chosen by repeated stratified CV.
- **Task 2.2B** – local mean-based kNN (LMKNN) and its pseudo-NN extension (LMPNN), implemented from scratch.
- **Task 2.3** – Decision tree tuned on depth, leaf size and criterion; compared with kNN.
- **Task 3.1 / 3.2** – k-Means (k chosen from internal indices) and DBSCAN (MinPts = 2·D, eps from the k-distance knee).
- **Task 3.3B** – PCA analysis and its effect on k-Means clustering.

## Re-running

```bash
pip install pandas numpy scikit-learn matplotlib jupyter python-docx
cd Assignment2 && jupyter nbconvert --to notebook --execute --inplace COSC2670-s4119075-A2code.ipynb
```

The samples are created only if their CSV files do not exist, so re-running re-uses the saved samples.
`tools/build_notebook.py` regenerates the notebook source and `tools/build_report.py` regenerates the
report `.docx` from `tools/A2report-Template.docx` (convert to PDF with LibreOffice Writer).
