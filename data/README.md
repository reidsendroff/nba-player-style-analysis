# Data Directory

This directory contains the datasets used in the dimensionality reduction analysis.

## Datasets

### 1. NBA Player Statistics (`nba_statistics.txt`)

**Format**: Tab-delimited text file  
**Season**: 2023-24 NBA season  
**Size**: 562 players × 21 features

**Features Include**:
- **Identification**: NAME, POS (position), GP (games played), MIN (minutes per game)
- **Scoring**: PTS, FGM, FGA, FG%, 3PM, 3PA, 3P%, FTM, FTA, FT%
- **Other Stats**: REB (rebounds), AST (assists), STL (steals), BLK (blocks), TO (turnovers)
- **Advanced**: DD2 (double-doubles), TD3 (triple-doubles)

**Preprocessing Applied**:
- Per-minute normalization (divided by MIN column)
- Z-score standardization across all numeric features
- Features from PTS through TD3 used for analysis (17 features)

**Data Limitations**:
- Single season snapshot (no temporal analysis)
- Team names appear as abbreviated codes in NAME column
- Some players have limited games played (affects statistical reliability)

---

### 2. Student Performance Dataset (`student_performance_dataset.csv`)

**Source**: [UCI Machine Learning Repository / Kaggle](https://www.kaggle.com/datasets/larsen0966/student-performance-data-set)  
**Format**: CSV  
**Size**: 395 students × 33 features

**Feature Categories**:
- **Demographics**: Age, sex, urban/rural residence
- **Family**: Parent education, family size, parent's job
- **Academic**: Study time, failures, extra educational support
- **Lifestyle**: Going out frequency, alcohol consumption, free time
- **Grades**: G1 (first period), G2 (second period), G3 (final grade - target variable)

**Preprocessing Applied**:
- One-hot encoding of categorical variables
- Standardization (z-score) of all features
- G3 (final grade) used as target for interpretation
- Encoded features used for PCA dimensionality reduction

---

## Usage Notes

Both datasets are loaded directly in the Jupyter notebook:

```python
# NBA data
df = pd.read_csv("nba_statistics.txt", sep="\t", encoding="utf-8")

# Student performance data
student_df = pd.read_csv('student_performance_dataset.csv')
```

If the data files are not present in this directory, the notebook will fail to run. Ensure both files are downloaded and placed here before execution.

## Data Privacy & Attribution

- **NBA Statistics**: Publicly available sports statistics (no privacy concerns)
- **Student Performance**: Anonymized educational data from UCI repository (no personally identifiable information)

Both datasets are used for educational and portfolio demonstration purposes under fair use.
