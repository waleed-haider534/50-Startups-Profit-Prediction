# 50 Startups Profit Prediction

Multiple Linear Regression model to predict startup profits using R&D, Administration and Marketing spend — built with Python and scikit-learn

---

## Project Overview

This project implements a **Multiple Linear Regression** model to predict startup profits based on various business expenses and location data. The model analyzes the relationship between R&D Spend, Administration costs, Marketing Spend, and State location to predict the Profit outcome for 50 startup companies.

### Objective

The primary goal is to build a predictive model that helps investors and business analysts understand which factors most significantly impact startup profitability, enabling data-driven investment decisions.

---

## Dataset Description

| Feature | Description | Type |
|---------|-------------|------|
| R&D Spend | Research & Development expenditure | Numeric |
| Administration | Administrative costs | Numeric |
| Marketing Spend | Marketing budget | Numeric |
| State | Location of the startup (Pakistan, California, Istanbul) | Categorical |
| Profit | Net profit earned | Numeric (Target) |

- **Total Records**: 50 startups
- **Target Variable**: Profit
- **Features**: 4 independent variables (3 numeric + 1 categorical)

---

## Technology Stack

- **Language**: Python 3.10+
- **Data Processing**: pandas, NumPy
- **Visualization**: Matplotlib, Seaborn
- **Machine Learning**: scikit-learn (LinearRegression)
- **Development Environment**: Jupyter Notebook

### Dependencies

```
pandas
numpy
matplotlib
seaborn
scikit-learn
```

Install all dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

---

## Project Structure

```
50-Startups-Profit-Prediction/
├── 50_startups_dataset.csv    # Dataset file
├── 50_startups_regression.ipynb  # Complete Jupyter Notebook
├── README.md                  # This documentation
└── pyproject.toml             # Project configuration
```

---

## Model Implementation

### Pipeline Overview

1. **Data Loading**: Import and explore the 50 Startups dataset
2. **Exploratory Data Analysis (EDA)**:
   - Statistical summary (mean, std, min, max)
   - Missing value detection
   - Correlation analysis
   - Distribution plots
3. **Data Preprocessing**:
   - One-hot encoding for categorical State variable
   - Feature/target separation
   - Train-test split (80/20)
4. **Model Training**: Multiple Linear Regression
5. **Model Evaluation**: R², MAE, MSE, RMSE metrics
6. **Visualization**: Actual vs Predicted plots, Feature importance

### Algorithm Details

**Multiple Linear Regression** uses the formula:

```
Profit = β₀ + β₁(R&D Spend) + β₂(Administration) + β₃(Marketing Spend) + β₄(State) + ε
```

Where:
- β₀ = Intercept
- β₁, β₂, β₃, β₄ = Coefficients
- ε = Error term

---

## Results & Evaluation

### Model Performance Metrics

| Metric | Value | Interpretation |
|--------|-------|-----------------|
| R² Score | ~0.85-0.95 | Model explains 85-95% of variance |
| MAE | ~$3,000-8,000 | Average prediction error |
| MSE | ~$50,000,000-150,000,000 | Squared error penalty |
| RMSE | ~$7,000-12,000 | Standard deviation of errors |

*Note: Actual values may vary based on random state*

### Key Findings

1. **R&D Spend** is the most influential factor affecting profit
2. **Marketing Spend** has a positive but smaller impact on profitability
3. **Administration costs** show minimal negative correlation with profit
4. **State location** has minimal impact on profit compared to spending factors

---

## Business Insights

### Top Investment Recommendations

Based on the model coefficients:

1. **Prioritize R&D Investment**: Every $1 increase in R&D spend correlates with approximately $0.80-0.85 increase in profit
2. **Moderate Marketing Spend**: Marketing has positive returns but with diminishing effectiveness
3. **Control Administrative Costs**: High administration overhead may reduce profit margins
4. **Location Flexibility**: State/city location is less critical than operational spending decisions

### Actionable Takeaways

- Startups should allocate significant budget to R&D activities
- Marketing spend should be optimized, not maximized
- Cost efficiency in administration improves profitability
- Geographic location decisions should consider other factors beyond tax incentives

---

## How to Run

### Using Jupyter Notebook

1. Open Jupyter Notebook:
   ```bash
   jupyter notebook
   ```

2. Open `50_startups_regression.ipynb`

3. Run all cells sequentially (Shift + Enter)

### Using Python Script

The notebook can also be converted to a Python script:
```bash
jupyter nbconvert --to script 50_startups_regression.ipynb
python 50_startups_regression.py
```

---

## Files Explained

### 50_startups_dataset.csv
Raw dataset containing 50 startup records with 5 columns: R&D Spend, Administration, Marketing Spend, State, and Profit.

### 50_startups_regression.ipynb
Complete Jupyter Notebook containing:
- Data loading and exploration
- Statistical analysis
- Data preprocessing
- Model training
- Evaluation metrics
- Visualizations
- Business insights

---

## Learning Outcomes

This project demonstrates:

- ✅ Data preprocessing and cleaning
- ✅ Exploratory Data Analysis (EDA)
- ✅ Feature engineering (one-hot encoding)
- ✅ Multiple Linear Regression implementation
- ✅ Model evaluation and validation
- ✅ Data visualization
- ✅ Business insight extraction

---

## Future Improvements

Potential enhancements for this project:

- **Regularization**: Add Ridge/Lasso regression to prevent overfitting
- **Cross-validation**: Implement k-fold cross-validation for robust evaluation
- **Feature Scaling**: Test with StandardScaler for normalized features
- **Additional Models**: Compare with Polynomial Regression or Random Forest
- **Hyperparameter Tuning**: Optimize model parameters

---

## License

This project is for educational purposes as part of a university Machine Learning assignment.

---

## Author

**Project**: 50 Startups Profit Prediction  
**Course**: Machine Learning Fundamentals  
**Institution**: Corvit Assignment  
**Date**: 2026

---

## Contact

For questions or suggestions, please reach out regarding this project implementation.