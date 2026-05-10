# NBA Player Statistics PCA & Dimensionality Reduction

> Exploring high-dimensional sports and student-performance datasets using PCA, SVD, MDS, t-SNE, and UMAP

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue)](https://www.python.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange)](https://jupyter.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Analytics-013243)](https://numpy.org/)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-ML-F7931E)](https://scikit-learn.org/)

## Overview

This project demonstrates hands-on implementation of dimensionality reduction techniques applied to real-world datasets. Rather than relying on black-box library calls, the analysis builds PCA from the ground up using covariance matrices and SVD, then compares results against nonlinear methods including MDS, t-SNE, and UMAP.

The project analyzes two distinct datasets:
- **NBA Player Statistics**: 562 players across 17 standardized per-minute performance metrics
- **Student Performance**: Academic and lifestyle factors predicting final grades

## What This Project Demonstrates

- **Mathematical Foundation**: Manual computation of covariance matrices and SVD for PCA
- **Feature Engineering**: Per-minute normalization and z-score standardization
- **Dimensionality Reduction**: Implementation and comparison of PCA, MDS, t-SNE, and UMAP
- **Statistical Analysis**: Eta-squared and R² metrics for quantifying pattern clarity
- **Data Storytelling**: Interpreting principal components through feature loadings and visualization
- **Hyperparameter Tuning**: Systematic exploration of t-SNE perplexity and UMAP parameters

## Methods Used

| Method | Type | Use Case |
|--------|------|----------|
| **PCA** | Linear | Variance-maximizing projection; interpretable loadings |
| **MDS** | Linear | Distance-preserving embedding |
| **t-SNE** | Nonlinear | Local neighborhood structure; cluster visualization |
| **UMAP** | Nonlinear | Balanced local/global structure preservation |

## Datasets

### NBA Player Statistics
- **Source**: Tab-delimited text file with 2023-24 season statistics
- **Size**: 562 players × 21 features
- **Features**: Points, rebounds, assists, shooting percentages, advanced metrics
- **Preprocessing**: Per-minute normalization, z-score standardization

### Student Performance Dataset
- **Source**: [UCI Machine Learning Repository / Kaggle](https://www.kaggle.com/datasets/larsen0966/student-performance-data-set)
- **Size**: 395 students × 33 features
- **Features**: Demographics, family background, study habits, social activities, grades
- **Preprocessing**: One-hot encoding, standardization

## Key Technical Steps

### 1. Linear Algebra Fundamentals
- Matrix multiplication (YX^T)
- Matrix inversion and identity verification
- Foundation for understanding PCA mechanics

### 2. NBA Data Pipeline
```
Raw Statistics → Per-Minute Normalization → Z-Score Standardization → Covariance Matrix
    ↓
SVD Decomposition → Principal Components → 2D Projection → Visualization
```

### 3. Manual PCA Implementation
- Covariance matrix: `Cov(X,Y) = Σ(X_i - X̄)(Y_i - Ȳ)/(N-1)`
- Singular Value Decomposition to extract eigenvectors
- Projection onto top 2 principal directions

### 4. Quantitative Pattern Analysis
- **Eta-squared (η²)**: Categorical separation (player position, team tier)
- **R²**: Continuous correlation (games played)
- Winner: Position showed strongest separation (η² indicates clearest clustering)

### 5. Explained Variance Analysis
- **PC1**: 25.1% of variance (scoring volume, shooting attempts, free throws)
- **PC2**: 17.2% of variance (secondary statistical patterns)
- **Combined**: 42.3% variance captured in 2D

## Results and Interpretation

### NBA Analysis
**PC1 Loadings** (Top Contributors):
- PTS (points), FGM (field goals made), FGA (field goals attempted)
- Captures overall scoring volume and offensive involvement
- Negative loadings suggest PC1 represents "offensive activity intensity"

**Visualization Insights**:
- Player positions form distinguishable clusters in PCA space
- Guards vs. centers separate along different principal directions
- t-SNE with perplexity=30 provided clearest position clustering
- UMAP balanced local cluster detail with global structure

### Student Performance Analysis
**PC1**: Academic Preparedness Axis
- High loadings: Prior grades (G1, G2), study time
- Negative loadings: Number of failures
- Strong correlation with final grade (G3)

**PC2**: Lifestyle/Social Axis
- High loadings: Going out frequency, alcohol consumption, free time
- Orthogonal to grades—students vary in lifestyle regardless of academic performance

**Key Finding**: Final grades align primarily with the academic axis (PC1), while lifestyle factors form a secondary dimension with weaker predictive power.

## Example Visualizations

> **Note**: Visualizations are generated within the Jupyter notebook. Key plots include:
> - PCA scatter plots colored by player position, team tier, and games played
> - Scree plot and cumulative variance curve
> - t-SNE perplexity comparison grid (5, 10, 20, 30, 40, 50)
> - UMAP projections with multiple coloring schemes
> - Student performance PC1 vs PC2 colored by final grade

*TODO: Export key plots to `images/` directory for inline display*

## Repository Structure

```
.
├── README.md                          # This file
├── PROJECT_SUMMARY.md                 # Concise project summary for portfolio
├── notebooks/
│   ├── dimensionality_reduction_hw1.ipynb   # Main analysis notebook
│   └── README.md                      # Notebook documentation
├── data/
│   ├── README.md                      # Data sources and descriptions
│   ├── nba_statistics.txt             # NBA player stats (tab-delimited)
│   └── student_performance_dataset.csv # Student performance data
├── images/                            # Exported visualizations
├── reports/                           # PDF exports if available
├── requirements.txt                   # Python dependencies
└── .gitignore                         # Git ignore patterns
```

## How to Run

### Prerequisites
- Python 3.8 or higher
- Jupyter Notebook or JupyterLab

### Installation

1. Clone the repository:
```bash
git clone https://github.com/yourusername/nba-pca-dimensionality-reduction.git
cd nba-pca-dimensionality-reduction
```

2. Create a virtual environment (recommended):
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

3. Install dependencies:
```bash
pip install -r requirements.txt
```

4. Launch Jupyter:
```bash
jupyter notebook notebooks/dimensionality_reduction_hw1.ipynb
```

5. Run all cells or step through the analysis sequentially

## Skills Demonstrated

**Mathematical & Statistical**:
- Linear algebra (matrix operations, eigendecomposition)
- Covariance and correlation analysis
- SVD and PCA theory
- Statistical hypothesis testing (eta-squared, R²)

**Programming & Tools**:
- NumPy for numerical computation
- pandas for data manipulation
- Matplotlib for visualization
- scikit-learn for ML algorithms
- UMAP library for advanced dimensionality reduction

**Data Science Workflow**:
- Feature engineering and normalization strategies
- Standardization for scale-invariant analysis
- Hyperparameter tuning and method comparison
- Interpretability analysis through feature loadings
- Data storytelling and visualization design

## Project Context

This project was completed as part of **Harvard Extension School CSCI E-82: Advanced Machine Learning**. The assignment focused on applying dimensionality reduction techniques to real datasets while building understanding of the underlying mathematics.

**Academic Integrity Note**: The project includes GenAI-assisted plotting boilerplate and explanatory text in specific sections (Problems 2d–2g and 6b). All modeling decisions, data preprocessing, parameter choices, and interpretations are original work.

## Why This Matters

Dimensionality reduction is essential in modern machine learning and data science:

- **Visualization**: Makes high-dimensional data interpretable through 2D/3D projections
- **Noise Reduction**: Captures signal while filtering out noise in high-dimensional spaces
- **Feature Discovery**: Reveals latent structure and relationships in complex datasets
- **Computational Efficiency**: Reduces dataset size while preserving critical information
- **Preprocessing**: Often used before clustering, classification, or regression tasks

Understanding PCA from first principles—rather than treating it as a black box—builds intuition for when and how to apply dimensionality reduction techniques effectively.

## Future Improvements

- [ ] Export high-quality visualizations to `images/` directory
- [ ] Add interactive Plotly visualizations for web viewing
- [ ] Implement kernel PCA for nonlinear data
- [ ] Compare with autoencoders for dimensionality reduction
- [ ] Add statistical significance testing for component loadings
- [ ] Create streamlit or gradio demo for interactive exploration
- [ ] Expand analysis to multiple NBA seasons for temporal patterns

## Author

**Reid Sendroff**  
Harvard Extension School | Advanced Machine Learning

---

*This project demonstrates practical implementation of dimensionality reduction techniques with emphasis on mathematical understanding, proper preprocessing, and interpretable results.*
