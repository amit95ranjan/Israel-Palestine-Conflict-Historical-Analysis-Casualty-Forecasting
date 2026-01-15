# 🌍 Israel-Palestine Conflict: Historical Analysis & Casualty Forecasting (2000-2021)

## 📌 Project Overview
This project performs a comprehensive data analysis of the Israeli-Palestinian conflict using dataset records from 2000 to 2021. The analysis focuses on temporal trends of injuries and fatalities for both sides, correlation analysis between casualty types, and the implementation of machine learning models (Linear Regression, Random Forest, ARIMA, and LSTM) to forecast future casualty trends.

## 🛠️ Tech Stack
* **Language:** Python 3.x
* [cite_start]**Data Manipulation:** Pandas, NumPy [cite: 3]
* [cite_start]**Visualization:** Matplotlib, Seaborn [cite: 52]
* [cite_start]**Machine Learning:** Scikit-Learn (Linear Regression, Random Forest) [cite: 461, 727]
* [cite_start]**Time Series & Deep Learning:** Statsmodels, PMDarima, TensorFlow/Keras (LSTM) [cite: 606, 697, 725]

## 📊 Data Pipeline & Preprocessing
The raw dataset contained information on year, month, and casualty counts (killed/injured) for both groups.
* **Data Cleaning:**
    * [cite_start]Handled missing values (NaN) in injury columns by imputing the mean of the respective column[cite: 14].
    * [cite_start]Converted the 'Month' column from string strings (e.g., "JANUARY") to numeric values (1-12)[cite: 14].
    * [cite_start]Ensured all numerical columns were converted to proper integer/float types for analysis[cite: 42].
* **Feature Engineering:**
    * Created time-series indices for temporal decomposition.
    * [cite_start]Calculated moving averages to smooth volatile data points[cite: 608].

## 📈 Key Insights (EDA)
* [cite_start]**Casualty Distribution:** The dataset covers approximately 162,967 total incidents (injuries + deaths)[cite: 52].
    * [cite_start]Palestinians account for **88.7%** of total reported deaths[cite: 130].
    * [cite_start]Palestinians account for **93.6%** of total reported injuries[cite: 146].
* **Peak Conflict Periods:**
    * [cite_start]**2014** was the year with the maximum injuries for both Palestinians (13,735) and Israelis (2,347)[cite: 95, 100].
    * [cite_start]**2002** was the year with the maximum deaths for Israelis (122)[cite: 103].
* **Correlations:**
    * [cite_start]There is a moderate positive correlation (**0.59**) between Palestinian Injuries and Israeli Injuries, suggesting conflict escalation often results in casualties on both sides simultaneously[cite: 420].
    * [cite_start]There is a strong positive correlation (**0.75**) between Palestinian Injuries and Israeli Deaths[cite: 420].

## 🤖 Machine Learning & Forecasting
The project implemented multiple models to predict casualty figures:

### 1. Linear Regression
* **Goal:** Predict the number of "Palestinians Killed" based on "Palestinians Injuries".
* [cite_start]**Performance:** Achieved a Mean Squared Error (MSE) of **2531.88**[cite: 515].
* [cite_start]**Insight:** The model found that for every additional injury, the death count increases by approximately 0.02[cite: 547].

### 2. Time Series Analysis
* [cite_start]**Decomposition:** Decomposed the "Palestinians Injuries" data into Trend, Seasonal, and Residual components to understand underlying patterns[cite: 609].
* [cite_start]**ARIMA:** Implemented `auto_arima` to forecast future trends in fatalities[cite: 699].

### 3. Random Forest Regressor
* **Goal:** Predict injuries based on multivariate data.
* **Performance:**
    * [cite_start]**Mean Absolute Error (MAE):** 117.05 [cite: 890]
    * [cite_start]**Root Mean Squared Error (RMSE):** 579.01 [cite: 892]

### 4. Deep Learning (LSTM)
* [cite_start]**Architecture:** Implemented a Sequential LSTM model with Dense layers using TensorFlow/Keras[cite: 746].
* [cite_start]**Training:** Trained over 50 epochs to capture long-term dependencies in the casualty time-series data[cite: 748].

## Model summary
- Short description: A model used for historical analysis and demonstration purposes. This repository provides reproducible analysis and a demo; it is not intended for automated high-stakes decision-making.

## Primary intended use
- Intended: research, exploratory analysis, stakeholder reporting, educational demonstration.
- Not intended: automated operational decisions that materially affect individuals or policy without human oversight.

## 🚀 Future Scope
* **Feature Expansion:** Incorporate geopolitical events or news sentiment data to improve prediction accuracy.
* **Model Tuning:** Perform Hyperparameter tuning on the LSTM and Random Forest models to reduce RMSE.
* **Granularity:** Break down analysis by specific regions (e.g., West Bank vs. Gaza) if data permits.

---
## 🚀 How to Run
1. **Clone the repository:**
   ```bash
   git clone: https://github.com/amit95ranjan/Israel-Palestine-Conflict-Historical-Analysis-Casualty-Forecasting
---
*Created By  Amit Ranjan - Data Analyst*
