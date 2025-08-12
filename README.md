# Trading Sentiment Analysis — README

## Overview

This project analyzes the relationship between Bitcoin market sentiment (Fear & Greed index) and historical trader performance data from Hyperliquid. The notebook performs data cleaning, feature engineering, exploratory analysis, hypothesis testing, clustering, and basic predictive modeling.

## Setup Instructions

### 1. Clone the repository

```bash
git clone <your-repo-url>
```

### 2. Install dependencies

This project requires Python 3.8+ and the following packages:

```bash
pip install pandas numpy matplotlib seaborn scipy scikit-learn statsmodels
```

### 3. Prepare the datasets

Place the following datasets in the project directory:

- **fear\_greed\_index.csv** — Bitcoin Market Sentiment data with `timestamp`, `value`, `classification`, and `date` columns.
- **historical\_data.csv** — Historical trader data with columns such as `account`, `symbol`, `execution price`, `size`, `side`, `time`, `closedPnL`, `leverage`, etc.

Ensure column names match expected formats or adjust parsing logic in the notebook.

### 4. Run the notebook

You can run the analysis in Jupyter or Google Colab:

```bash
jupyter notebook Assignment.ipynb
```

Or upload the notebook to [Google Colab](https://colab.research.google.com/) and run all cells.

### 5. Review outputs

The notebook produces:

- Statistical comparisons of trading metrics between sentiment phases.
- Cross-correlation plots and Granger causality tests.
- Trader segmentation clusters.
- Predictive model results.

---

## Notes

- **Timezone handling:** Trader timestamps are assumed to be in IST and converted to naive datetimes for daily aggregation.
- **Mixed date formats:** The Fear & Greed dataset is parsed to handle both `dd-mm-yyyy` and `yyyy-mm-dd` formats.
- **Data quality:** Missing or invalid numeric entries are coerced to NaN and ignored in statistical calculations.
- **Predictive limitations:** Current features provide limited predictive power for sentiment; integrating market price data may improve results.
- **Customization:** Adjust feature engineering and clustering parameters to suit your strategy focus.

---
