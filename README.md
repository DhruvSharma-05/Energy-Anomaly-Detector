# Energy-Anomaly-Detector

[![dashboard](https://img.shields.io/badge/Dashboard_Link-000?style=for-the-badge&logo=ko-fi&logoColor=white)](https://dhruvsharma-05.github.io/)
## Introduction
This project focuses on predicting electrical energy output from a Combined Cycle Power Plant (CCPP) using ambient variables. The dataset is sourced from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/dataset/294/combined+cycle+power+plant) and contains 9568 data points collected from a Combined Cycle Power Plant over 6 years (2006-2011), when the plant was set to work with full load.

## Project Overview
A combined cycle power plant integrates gas and steam turbines to generate electricity with enhanced efficiency. The plant's performance depends heavily on environmental conditions. This project implements various machine learning models to predict net hourly electrical energy output based on ambient variables.

### Dataset Features
- **Temperature (AT)**: 1.81°C to 37.11°C
- **Ambient Pressure (AP)**: 992.89-1033.30 mbar
- **Relative Humidity (RH)**: 25.56% to 100.16%
- **Exhaust Vacuum (V)**: 25.36-81.56 cm Hg
- **Target Variable**: Net hourly electrical energy output (PE)

## Requirements


Install required packages:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn xgboost shap openpyxl
```

## Implementation Features

### Data Processing
- Data cleaning and normalization
- Feature scaling
- Train-test split implementation
- Cross-validation setup

### Models Implemented
1. Linear Regression
   - Baseline model implementation
   - Standard scaling of features
   - Cross-validation evaluation

2. Bagging with REPTree
   - Ensemble method implementation
   - Reduced error pruning
   - Optimized parameters

3. XGBoost
   - Gradient boosting implementation
   - Hyperparameter tuning
   - Feature importance analysis

### Performance Metrics
| Model                | MAE      | RMSE     |
|---------------------|----------|----------|
| Linear Regression   | 3.622570 | 4.518926 |
| Bagging + REPTree   | 0.391552 | 0.873753 |
| XGBoost             | 2.052544 | 2.747258 |

## Key Results
1. **Best Performing Model**: Bagging with REPTree
   - Lowest MAE: 0.391552
   - Lowest RMSE: 0.873753
   - Significant improvement over baseline

2. **Model Comparison**
   - Bagging + REPTree shows superior performance
   - XGBoost performs better than Linear Regression
   - Linear Regression provides baseline metrics

3. **Error Analysis**
   - Bagging + REPTree reduces error by ~89% compared to Linear Regression
   - XGBoost shows ~43% improvement over Linear Regression
   - Consistent performance across different data splits

## Usage

1. Update dataset path:
```python
"path/to/your/Folds5x2_pp.xlsx"
```

2. Run the script:
```bash
python your_script.py
```
