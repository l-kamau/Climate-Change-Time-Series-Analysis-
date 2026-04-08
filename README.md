# Climate Change Time Series Analysis

## Project Overview
This project focuses on analyzing climate change data (2020–2024) to identify historical trends and forecast future climate variables. By employing robust data cleaning, exploratory analysis, and machine learning, this study highlights the critical relationships between atmospheric conditions and global temperature shifts.

## Key Sections & Results

### 1. Data Cleaning & Pre-processing
* **Missing Data Strategy**: Successfully handled missing values using **Linear Interpolation** for long-term trends (like CO2) and **Seasonal Mean Imputation** for weather-dependent variables (Temperature and Humidity) to preserve natural cyclical patterns.
* **Outlier Management**: Identified and corrected placeholder values (e.g., `99999.0`) that would have otherwise skewed the statistical validity of the models.
* **Feature Engineering**: Implemented **Lag Features** (past values) to enable the models to understand temporal dependencies and historical momentum in climate shifts.

### 2. Exploratory Data Analysis (EDA)
* **Correlation Findings**: Heatmap analysis confirmed a strong positive correlation between **CO2 Concentration** and **Average Temperature**, quantifying the impact of greenhouse gases within the dataset.
* **Temporal Trends**: Visualization revealed consistent seasonal oscillations, with temperature peaks aligning closely with recorded **ENSO (El Niño–Southern Oscillation)** cycles.
* **Geospatial Localization**: Analysis of coordinates localized the data source to an urban environment at approximately **40.71° N, -74.01° W**.

### 3. Time Series Forecasting & Modeling
* **ARIMA Model (5, 1, 0)**:
    * Achieved stationarity through first-order differencing (`d=1`).
    * Utilized an AutoRegressive order of `p=5` to capture the influence of the previous five time steps on future predictions.
* **Random Forest Regressor**:
    * Effectively captured non-linear relationships between humidity, wind speed, CO2 levels, and the target temperature.
* **Performance Evaluation**: Models were validated using **Root Mean Squared Error (RMSE)** to ensure that the forecasts remain accurate when applied to out-of-sample test data.

## Technical Stack
* **Language**: Python
* **Libraries**: 
    * **Data Manipulation**: `pandas`, `numpy`
    * **Visualization**: `matplotlib`, `seaborn`, `plotly`
    * **Statistical Modeling**: `statsmodels` (ARIMA)
    * **Machine Learning**: `scikit-learn` (Random Forest)

## Project Structure
* `Climate_Change_Analysis.ipynb`: The primary interactive notebook containing all code, visualizations, and detailed documentation.
* `climate_change_dataset.csv`: The raw climate dataset used for training and analysis.
