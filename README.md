# Dublin Traffic Volume Prediction (Smart Dublin SCATS Data)

This repository contains a machine learning project focused on predicting hourly traffic volume in Dublin using the SCATS (Sydney Coordinated Adaptive Traffic System) sensor dataset.
The project demonstrates end-to-end skills in data cleaning, exploratory analysis, feature engineering, model development, and evaluation using Python and Scikit-Learn.

## Overview
Urban traffic forecasting is essential for improving congestion management and road network efficiency.
This project applies supervised regression algorithms to estimate hourly vehicle counts recorded by Dublin City Council’s SCATS sensors.

The workflow includes:
- Exploratory Data Analysis (EDA) of 500k+ hourly traffic observations
- Feature preprocessing using pipelines (imputation, encoding, scaling)
- Model comparison using Linear Regression, Random Forest, and Gradient Boosting
- Feature selection via RFECV and Sequential Forward Selection (SFS)
- Model evaluation with 10-fold cross-validation using MAE, RMSE, and R² metrics

## Key Results
| Model | R² | MAE | RMSE |
|--------|----|-----|------|
| Linear Regression | 0.28 | 50.8 | 86.0 |
| Random Forest | 0.43 | 35.4 | 77.1 |
| Gradient Boosting | 0.46 | 34.4 | 74.7 |

Gradient Boosting achieved the best performance, explaining approximately 46% of the variance in hourly traffic volume.
Temporal (Hour, DayOfWeek) and spatial (Region, Site, Detector) features were the most predictive.
Feature selection improved computational efficiency without sacrificing model accuracy.

## Repository Structure
```
Dublin-Traffic-ML/
│
├── Code/
│   ├── FINALESCAT.ipynb          → Main notebook: data preprocessing, model training, feature selection, evaluation.
│   └── SCATSMINIMINSING.ipynb    → Dataset reduction script (from 1.05M to ~500k records for efficient modeling).
│
├── Data/
│   ├── Filtered/                 → Cleaned dataset subset used for training.
│   └── Raw/                      → Original dataset (excluded due to GitHub file size limits).
│
└── README.md                     → Project documentation.
```
## Tools and Libraries
- Python
- Pandas / NumPy
- Matplotlib / Seaborn
- Scikit-Learn
- Jupyter Notebook

## Insights and Applications
This project demonstrates how machine learning can support data-driven traffic forecasting for smart city initiatives.
By predicting hourly traffic volume, city authorities can better anticipate congestion, adjust signal timings, and plan infrastructure improvements.

The methodology can be extended to real-time traffic prediction systems for adaptive transport management.

## Author
Laith Ahmed  
Bachelor of Science (Honours) in Data Science – National College of Ireland  
Email: laith.mactari@gmail.com  
LinkedIn: https://www.linkedin.com/in/laithwm/  
GitHub: https://github.com/Laithwm  

## License
This repository is intended for educational and portfolio purposes.  
Dataset © Dublin City Council / Smart Dublin (Open Data License).
