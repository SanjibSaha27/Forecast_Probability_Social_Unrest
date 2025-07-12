**Objective:**
- To develop a predictive model that forecasts the likelihood of societal unrest one month in advance across 50 regions using economic, environmental, and sociopolitical indicators.

**Approach & Methodology:**
- Data Preparation:
    - Dataset: unrest.csv
    - Handled missing values and performed basic feature engineering (e.g., extracting month/year).
    - Visualized class distribution and correlation with target (unrest_event).

**Model Development:**
- Target variable: unrest_event (binary classification).
- Features: All other relevant indicators, excluding identifiers and temporal fields.
- SMOTE was applied to balance the class distribution.
- Model: RandomForestClassifier within a pipeline (with StandardScaler).
- Training/Test Split: 70/30 stratified.

**Model Evaluation:**

- Reported performance with:
    - classification_report
    - ROC AUC Score
    - Average Precision Score

- Feature importance was visualized to identify influential indicators.

**Model Calibration:**

- Used CalibratedClassifierCV (isotonic regression) to improve probability estimates.
- Compared uncalibrated vs calibrated models with calibration curves.

**Results:**

- The Random Forest model performed well with balanced class treatment via SMOTE.
- ROC AUC and precision-recall metrics indicated good discriminatory power.
- Top features were clearly identified through importance analysis.
- Calibration improved the reliability of probability predictions.

**1. Distibution of Unrest Events**
![1. Distibution of Unrest Events](https://github.com/SanjibSaha27/Forecast_Probability_Social_Unrest/blob/main/1%20Distibution%20of%20Unrest%20Events.png)

**2 Correlation with Unrest Event**
![2 Correlation with Unrest Event](https://github.com/SanjibSaha27/Forecast_Probability_Social_Unrest/blob/main/2%20Correlation%20with%20Unrest%20Event.png)

**3 Feature Importance**
![3 Feature Importance](https://github.com/SanjibSaha27/Forecast_Probability_Social_Unrest/blob/main/3%20Feature%20Importance.png)

**4 Calibration Curve**
![4 Calibration Curve](https://github.com/SanjibSaha27/Forecast_Probability_Social_Unrest/blob/main/4%20Calibration%20Curve.png)

**5 Calibration Curve Comparision**
![5 Calibration Curve Comparision](https://github.com/SanjibSaha27/Forecast_Probability_Social_Unrest/blob/main/5%20Calibration%20Curve%20Comparision.png)


**Recommendations:**

- Use the calibrated model for more trustworthy risk probabilities in decision-making.
- Monitor the most important features over time for trend analysis.
- Incorporate real-time or updated data feeds for live prediction integration.
- Consider testing additional models (e.g., Gradient Boosting, XGBoost) for comparison.
- Explore temporal models (e.g., LSTM) if time sequence patterns are critical.

**Power BI Interactive Dashboard**
https://app.powerbi.com/groups/me/reports/0e063933-fef6-4daa-a435-0d58dcca20b6/20d9865034acea96453a?experience=power-bi


