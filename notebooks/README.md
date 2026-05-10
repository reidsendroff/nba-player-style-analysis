# Notebooks Directory

## Main Notebook

### `dimensionality_reduction_hw1.ipynb`

This Jupyter notebook contains the complete dimensionality reduction analysis pipeline.

## Notebook Structure

The notebook is organized into the following major sections:

### 1. **Project Overview & Imports**
- Package imports (NumPy, pandas, matplotlib, scikit-learn, UMAP)
- Random seed setting for reproducibility
- Initial data loading

### 2. **Linear Algebra Warmup** (Problem 1)
- Matrix multiplication (YX^T)
- Matrix inversion computation
- Identity verification

### 3. **NBA Dataset Preprocessing** (Problem 2a)
- Load tab-delimited NBA statistics
- Per-minute normalization (divide by MIN column)
- Z-score standardization
- Feature selection (PTS through TD3)

### 4. **Manual PCA Implementation** (Problem 2b-c)
- Covariance matrix computation from scratch
- Singular Value Decomposition (SVD)
- Eigenvector extraction (principal directions)
- 2D projection onto first two principal components

### 5. **PCA Visualization & Interpretation** (Problem 2d-g)
- Scatter plots colored by:
  - Player position (POS)
  - Team tier (top 6, playoff bubble, bottom 5)
  - Games played (GP)
- Quantitative pattern analysis (eta-squared, R²)
- Scree plot and cumulative explained variance
- PC1 feature loadings interpretation
- Standardization importance explanation

### 6. **MDS Comparison** (Problem 3)
- Multidimensional Scaling applied to same data
- Comparison with PCA projection

### 7. **t-SNE Experiments** (Problem 4)
- Default t-SNE with perplexity=30
- Perplexity sweep (5, 10, 20, 30, 40, 50)
- Grid visualization of results
- Interpretation of local vs. global structure

### 8. **UMAP Projections** (Problem 5)
- Default UMAP parameters
- Visualizations colored by POS, team tier, GP
- Comparison with PCA and t-SNE

### 9. **Student Performance Analysis** (Problem 6)
- Dataset loading and exploration
- One-hot encoding of categorical features
- Standardization and PCA application
- PC1 vs PC2 visualization colored by final grade (G3)
- Interpretation:
  - PC1 = Academic preparedness (prior grades, study time)
  - PC2 = Lifestyle/social factors (going out, alcohol use)
- Data storytelling

### 10. **Conclusion**
- Time estimate and reflection

## How to Run

1. Ensure all dependencies are installed:
   ```bash
   pip install -r ../requirements.txt
   ```

2. Ensure data files are present in `../data/`:
   - `nba_statistics.txt`
   - `student_performance_dataset.csv`

3. Launch Jupyter:
   ```bash
   jupyter notebook dimensionality_reduction_hw1.ipynb
   ```

4. Execute cells sequentially or use "Run All"

## Key Outputs

The notebook generates numerous visualizations:
- PCA scatter plots (multiple coloring schemes)
- Scree plots and variance curves
- MDS projections
- t-SNE perplexity comparison grids
- UMAP embeddings
- Student performance PCA plots

**Note**: Visualizations are displayed inline. To export for use in README.md, add save commands:
```python
plt.savefig('../images/pca_by_position.png', dpi=300, bbox_inches='tight')
```

## Academic Integrity Note

This notebook was completed for Harvard Extension CSCI E-82. Specific sections (2d-2g, 6b) include GenAI-assisted plotting boilerplate and explanatory text. All modeling decisions, preprocessing, parameter choices, and interpretations are original work.

## Notebook Improvements (Future Work)

- [ ] Add project overview markdown cell at the top
- [ ] Improve section headers with clearer hierarchy
- [ ] Add "Methods Summary" cell
- [ ] Add "Key Takeaways" cell at end
- [ ] Export key visualizations to `../images/`
- [ ] Add markdown explanations between code cells
- [ ] Remove "Assignment #1 due 9/16" header for portfolio version
