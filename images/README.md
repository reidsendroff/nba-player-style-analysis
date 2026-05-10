# Images Directory

This directory contains exported visualizations from the dimensionality reduction analysis.

## Key Visualizations to Export

The following high-value visualizations should be exported from the notebook and included in the main README:

### NBA PCA Analysis (Problem 2)

1. **`pca_by_position.png`**
   - **Description**: PCA scatter plot (PC1 vs PC2) colored by player position
   - **Key Finding**: Shows clear position-based clustering (PG, SG, SF, PF, C, F, G)
   - **Dimensions**: PC1 captures ~22% variance, PC2 captures ~19% variance
   - **Export command**: `plt.savefig('../images/pca_by_position.png', dpi=300, bbox_inches='tight')`

2. **`pca_by_standings.png`**
   - **Description**: PCA colored by team conference standings
   - **Categories**: EAST_TOP_6, EAST_MID, EAST_BOT_5, WEST_TOP_6, WEST_MID, WEST_BOT_5
   - **Key Finding**: Team performance tiers show moderate clustering
   - **Export command**: `plt.savefig('../images/pca_by_standings.png', dpi=300, bbox_inches='tight')`

3. **`pca_by_games_played.png`**
   - **Description**: PCA colored by games played (GP) using continuous scale
   - **Coloring**: Gradient from 0-9 games to 70+ games
   - **Key Finding**: Experience (GP) shows some correlation with PC dimensions
   - **Export command**: `plt.savefig('../images/pca_by_games_played.png', dpi=300, bbox_inches='tight')`

4. **`variance_explained.png`**
   - **Description**: Dual subplot showing (1) cumulative variance and (2) scree plot
   - **Key Finding**: First 2 PCs explain ~40.94% of variance
   - **Details**: Clear elbow visible around PC 4-6
   - **Export command**: `plt.savefig('../images/variance_explained.png', dpi=300, bbox_inches='tight')`

5. **`pc1_feature_loadings.png`**
   - **Description**: Bar chart showing top contributors to PC1
   - **Top Features**: PTS, FGM, FGA, FG%, 3PM, 3PA dominate PC1
   - **Interpretation**: PC1 represents overall offensive activity/scoring volume
   - **Export command**: `plt.savefig('../images/pc1_feature_loadings.png', dpi=300, bbox_inches='tight')`

6. **`correlation_circle.png`** *(Optional)*
   - **Description**: PCA correlation circle showing feature relationships
   - **Key Finding**: Identifies redundancy in NBA statistics
   - **Details**: PTS, FGM, FGA highly correlated; 3PM, 3PA form separate cluster
   - **Export command**: `plt.savefig('../images/correlation_circle.png', dpi=300, bbox_inches='tight')`

### MDS Analysis (Problem 3)

7. **`mds_by_position.png`**
   - **Description**: MDS 2D projection colored by player position
   - **Comparison**: Similar to PCA but with slight rotation
   - **Key Finding**: Position clustering preserved in MDS
   - **Export command**: `plt.savefig('../images/mds_by_position.png', dpi=300, bbox_inches='tight')`

### t-SNE Analysis (Problem 4)

8. **`tsne_default.png`**
   - **Description**: t-SNE with default perplexity=30, colored by position
   - **Key Finding**: Clearer position clusters than PCA/MDS
   - **Export command**: `plt.savefig('../images/tsne_default.png', dpi=300, bbox_inches='tight')`

9. **`tsne_perplexity_grid.png`**
   - **Description**: 2×3 grid comparing perplexity values: 5, 10, 20, 30, 40, 50
   - **Key Finding**: Perplexity=30 provides best balance of local/global structure
   - **Details**: Low perplexity (5-10) overly fragmented; high (40-50) over-smoothed
   - **Export command**: `plt.savefig('../images/tsne_perplexity_grid.png', dpi=300, bbox_inches='tight')`

### UMAP Analysis (Problem 5)

10. **`umap_by_position.png`**
    - **Description**: UMAP projection with default parameters (n_neighbors=15, min_dist=0.1)
    - **Key Finding**: Tightest position clustering of all methods
    - **Export command**: `plt.savefig('../images/umap_by_position.png', dpi=300, bbox_inches='tight')`

11. **`umap_by_standings.png`**
    - **Description**: UMAP colored by team standings
    - **Export command**: `plt.savefig('../images/umap_by_standings.png', dpi=300, bbox_inches='tight')`

12. **`umap_by_gp.png`**
    - **Description**: UMAP colored by games played
    - **Export command**: `plt.savefig('../images/umap_by_gp.png', dpi=300, bbox_inches='tight')`

### Student Performance Analysis (Problem 6)

13. **`student_performance_pca.png`**
    - **Description**: PC1 vs PC2 colored by final grade (G3)
    - **Key Finding**: PC1 = academic preparedness, PC2 = lifestyle/social factors
    - **Interpretation**: Grades align with PC1 (prior performance, study time, failures)
    - **Export command**: `plt.savefig('../images/student_performance_pca.png', dpi=300, bbox_inches='tight')`

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
