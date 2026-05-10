# Reports Directory

This directory contains PDF exports and rendered versions of the analysis.

## Expected Files

### `SendroffReidHW1.pdf`
- PDF export of the original notebook submission
- Includes all code, outputs, and visualizations
- Submitted version for Harvard Extension CSCI E-82

## Generating PDF Exports

To create a PDF from the Jupyter notebook:

### Method 1: Jupyter nbconvert
```bash
jupyter nbconvert --to pdf notebooks/dimensionality_reduction_hw1.ipynb
mv notebooks/dimensionality_reduction_hw1.pdf reports/
```

### Method 2: Print to PDF from Browser
1. Open notebook in Jupyter
2. File → Print Preview
3. Use browser's Print → Save as PDF
4. Save to `reports/` directory

### Method 3: LaTeX-based (requires LaTeX installation)
```bash
jupyter nbconvert --to latex notebooks/dimensionality_reduction_hw1.ipynb
cd notebooks
pdflatex dimensionality_reduction_hw1.tex
mv dimensionality_reduction_hw1.pdf ../reports/
```

## Usage

The PDF version is useful for:
- Quick review without running the notebook
- Sharing with non-technical stakeholders
- Portfolio presentations
- Academic submission archives

**Note**: The PDF is a static snapshot. For interactive exploration or code modification, use the Jupyter notebook directly.

## Current Status

If `SendroffReidHW1.pdf` is not present, it can be regenerated using the methods above or obtained from the original course submission.
