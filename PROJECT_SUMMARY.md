# Project Summary: NBA Player Statistics PCA & Dimensionality Reduction

## Concise Summary

Built a dimensionality reduction analysis pipeline in Python for high-dimensional NBA player statistics and student performance data. The project implemented PCA using covariance matrices and SVD, compared PCA with MDS, t-SNE, and UMAP, and interpreted principal components through feature loadings, explained variance, and visualization patterns.

## Resume Bullets

- Implemented PCA-based dimensionality reduction on NBA player statistics using NumPy, pandas, covariance matrix construction, SVD, feature standardization, and 2D projection
- Compared PCA, MDS, t-SNE, and UMAP visualizations to analyze structure in high-dimensional sports data across position, team tier, and games played
- Applied PCA to a student performance dataset, using one-hot encoding and standardized features to interpret academic and lifestyle dimensions associated with final grades

## Technical Explanation

This project uses PCA to transform standardized high-dimensional data into lower-dimensional coordinates that preserve as much variance as possible. For the NBA dataset, per-game statistics were normalized by minutes played, standardized with z-scores, and used to manually compute a covariance matrix. SVD was then applied to identify principal directions, project players into two dimensions, and analyze feature loadings. Additional methods including MDS, t-SNE, and UMAP were used to compare linear and nonlinear dimensionality reduction approaches.

## Interview Version

In this project, I worked through dimensionality reduction from both the mathematical and applied sides. I manually built the covariance matrix for normalized NBA player statistics, used SVD to compute principal components, and projected the data into two dimensions for visualization. I also compared PCA to MDS, t-SNE, and UMAP to understand how different methods reveal different structure. Finally, I applied the same PCA storytelling approach to a student performance dataset, where I interpreted one component as academic preparedness and another as a lifestyle/social dimension.

## Why This Project Stands Out

This project demonstrates hands-on understanding of the math behind PCA and dimensionality reduction, including covariance matrices, SVD, standardization, explained variance, and feature loadings. Rather than simply calling a black-box library, the analysis builds key PCA steps manually and then compares the results against nonlinear visualization methods such as t-SNE and UMAP.

## Key Skills Demonstrated

**Mathematical Foundation:**
- Linear algebra (covariance matrices, SVD, eigendecomposition)
- Statistical analysis (eta-squared, R² for pattern quantification)
- Understanding of variance, standardization, and feature scaling

**Programming & Implementation:**
- NumPy for matrix operations and manual PCA implementation
- pandas for data manipulation and feature engineering
- scikit-learn for MDS and t-SNE
- UMAP library for advanced nonlinear dimensionality reduction

**Data Science Workflow:**
- Feature engineering (per-minute normalization)
- Proper preprocessing (z-score standardization)
- Hyperparameter tuning (t-SNE perplexity, UMAP parameters)
- Interpretability through feature loadings and explained variance
- Data storytelling and visualization design

## Project Outcomes

- **PC1 explained 25.1%** of NBA dataset variance, dominated by scoring and shooting volume
- **Position-based clustering** showed strongest separation (η² analysis confirmed)
- **Student performance PC1** captured academic preparedness (prior grades, study time, failures)
- **Student performance PC2** captured lifestyle factors (going out, alcohol use, free time)
- Systematic comparison across PCA, MDS, t-SNE, and UMAP revealed different structural insights

## Context

Completed as part of Harvard Extension School CSCI E-82: Advanced Machine Learning. The project emphasizes mathematical understanding over black-box application, building PCA from first principles before comparing against modern nonlinear methods.
