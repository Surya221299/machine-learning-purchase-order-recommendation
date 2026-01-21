# Machine Learning–Based Purchase Order Recommendation
Understanding Machine Learning-Based Purchase Order Recommendation in Motorcycle Spare Parts Warehouse

## Project Motivation
In many inventory management systems, Purchase Order decisions are still driven by simple rule-based approaches, such as moving averages of past sales. While easy to implement, these methods often fail to capture complex demand patterns, especially when dealing with fast-moving and slow-moving spare parts.

This project investigates how different machine learning models learn from sales and stock data, and how their recommendations differ from traditional rule-based methods.

## Objectives
- Understand how machine learning models map sales and inventory features to PO recommendations
- Compare rule-based baseline, Linear Regression, and Random Forest approaches
- Analyze and interpret model behavior using coefficients and feature importance
- Highlight strengths and limitations of each approach in an operational warehouse context

## Dataset Overview
The dataset consists of 50 motorcycle spare parts, where each row represents one item with the following features:

## Methodology
1. Rule-Based Baseline

Uses a 3-month moving average of historical sales

2. Machine Learning Models

- Linear Regression
  - High interpretability via coefficients
  - Captures linear relationships

- Random Forest Regressor
  - Captures non-linear relationships and feature interactions
  - Interpreted using feature importance

The target variable for both models is the baseline PO quantity, used as a proxy label to study how models replicate decision logic.

## Experiments & Evaluation
- Train-test split: time-based (to avoid data leakage)
- Evaluation metric: Mean Absolute Error (MAE)
- Focus on behavioral comparison, not model optimization

## Key Findings
- Linear Regression produces more stable and interpretable recommendations
- Random Forest achieves lower MAE and is more adaptive to demand variability
- Recent sales data has the strongest influence on PO recommendations
- Stock level consistently acts as a limiting factor
- Fast-moving classification affects Linear Regression more strongly than Random Forest

## Tools & Libraries
- Python
- Pandas & NumPy
- Matplotlib
- Scikit-learn
- Google Colab

## Project Scope & Limitations
- Limited dataset size and time horizon
- External factors (promotions, seasonality, supplier lead time) are not considered
- Models are used for analysis and understanding, not direct deployment

## Future Work
- Extend dataset with longer time periods and seasonal effects
- Incorporate external signals (promotions, events, vehicle types)
- Explore advanced models (Gradient Boosting, Time Series, Deep Learning)
- Compare decision quality beyond baseline replication

## Related Work
This project is aligned with academic studies on:

- Inventory management
- Demand forecasting
- Interpretable machine learning
- Decision support systems

## Author
Surya Ramadhani
Apple Developer Academy Graduate.
Former Part Inventory Officer.
