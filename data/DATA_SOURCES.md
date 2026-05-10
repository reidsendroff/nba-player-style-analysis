# Data Sources & Acquisition

## Required Data Files

This project requires two datasets that are **not included in the repository**. You must download them separately before running the notebook.

### 1. NBA Player Statistics (`nba_statistics.txt`)

**Status:** ✅ INCLUDED

**Format:** Tab-delimited text file (`.txt`)

**Location:** `data/nba_statistics.txt`

**Source:** CSCI E-82 homework materials

**Details:**
- **Season**: 2023-24 NBA regular season
- **Rows**: 563 (including header)
- **Players**: 562
- **Features**: 21 columns

**Expected Format:**
```
NAME    POS    GP    MIN    PTS    FGM    FGA    FG%    ...
Luka Doncic DAL    PG    70    37.5    33.9    11.5    23.6    48.7    ...
```

---

### 2. Student Performance Dataset (`student_performanceData.csv`)

**Status:** ✅ Publicly Available

**Format:** CSV file

**Expected Location:** `data/student_performanceData.csv`

**Where to Obtain:**
- **Primary Source:** [Kaggle - Student Performance Data Set](https://www.kaggle.com/datasets/larsen0966/student-performance-data-set)
- **Alternative:** [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/student+performance)

**Download Instructions:**
1. Visit the Kaggle link above
2. Click "Download" (may require free Kaggle account)
3. Unzip the downloaded file
4. Rename to `student_performanceData.csv` if needed
5. Place in `data/` directory

**Note:** The dataset contains student achievement in secondary education, including demographics, family factors, and academic grades.

---

## Quick Setup

After obtaining both files, your `data/` directory should look like:

```
data/
├── README.md
├── DATA_SOURCES.md (this file)
├── nba_statistics.txt
└── student_performanceData.csv
```

Verify with:
```bash
ls -lh data/
```

You should see both `.txt` and `.csv` files present before running the notebook.

---

## Alternative: Use Your Own Data

If you cannot obtain the exact datasets, you can modify the notebook to use alternative datasets with similar structure:

**For NBA Analysis:**
- Any sports statistics dataset with multiple numeric features
- Requires: Player identifiers, position, and 10+ numeric stats

**For Student Performance:**
- Any educational dataset with demographics and grades
- Requires: Mix of categorical and numeric features, plus outcome variable

You'll need to adjust the column names in the notebook to match your data.

---

## Data Privacy

Both datasets should be:
- ✅ Publicly available or obtained through proper academic channels
- ✅ Anonymized (no personally identifiable information)
- ✅ Used for educational/portfolio purposes

Do not commit large data files (>10MB) to git. Consider adding them to `.gitignore` if they exceed GitHub's recommended limits.
