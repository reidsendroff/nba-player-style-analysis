# Images Directory

This directory contains exported visualizations from the dimensionality reduction analysis.

## Recommended Figures to Export

The following high-value visualizations should be exported from the notebook and included in the main README:

### NBA Analysis

1. **`pca_by_position.png`**
   - PCA scatter plot colored by player position (POS)
   - Shows position-based clustering in reduced space
   - Generated in Problem 2d

2. **`pca_by_team_tier.png`**
   - PCA colored by team tier (top 6 / playoff bubble / bottom 5)
   - Reveals team performance patterns
   - Generated in Problem 2d

3. **`pca_by_games_played.png`**
   - PCA colored by games played (continuous scale)
   - Shows relationship between playing time and statistical profile
   - Generated in Problem 2d

4. **`scree_plot.png`**
   - Bar plot of explained variance per principal component
   - Includes cumulative variance line
   - Shows elbow around PC 4-6
   - Generated in Problem 2e

5. **`tsne_perplexity_comparison.png`**
   - 2×3 grid comparing t-SNE with perplexity values: 5, 10, 20, 30, 40, 50
   - Demonstrates effect of local neighborhood size
   - Generated in Problem 4b

6. **`umap_projection.png`**
   - UMAP embedding colored by position
   - Comparison with PCA and t-SNE
   - Generated in Problem 5a

### Student Performance Analysis

7. **`student_performance_pca.png`**
   - PC1 vs PC2 colored by final grade (G3)
   - Gradient shows academic preparedness (PC1) vs lifestyle (PC2)
   - Generated in Problem 6

## How to Export

Add these lines to the appropriate notebook cells:

```python
# After creating a matplotlib figure
plt.savefig('../images/pca_by_position.png', dpi=300, bbox_inches='tight')
plt.show()
```

## Image Guidelines

- **Format**: PNG (recommended) or SVG for vector graphics
- **Resolution**: 300 DPI for publication quality
- **Size**: Reasonable dimensions (typically 8-12 inches wide)
- **Transparency**: Use `transparent=True` if needed for presentations

## Current Status

**TODO**: Export key figures from notebook

Once exported, update the main README.md to include inline images:

```markdown
### PCA by Player Position
![PCA by Position](images/pca_by_position.png)

### Scree Plot
![Scree Plot](images/scree_plot.png)
```

This will make the GitHub repository page much more visually compelling for recruiters and technical reviewers.
