# Weather-Electricity Consumption Analysis for TGERC

## Analyzing Weather Impact on Electricity Consumption in Telangana

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/downloads/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![Colab](https://img.shields.io/badge/Google-Colab-yellow.svg)](https://colab.research.google.com/)

A comprehensive data analysis project that investigates the relationship between weather parameters and electricity consumption patterns in Telangana, India. Developed for the Telangana Electricity Regulatory Commission (TGERC) to support evidence-based tariff design and demand management strategies.

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Data Requirements](#data-requirements)
- [Important Note on Sample Data](#important-note-on-sample-data)
- [Adapting for Real Datasets](#adapting-for-real-datasets)
- [Analysis Workflow](#analysis-workflow)
- [Key Results](#key-results)
- [Contributing](#contributing)
- [License](#license)
- [Contact](#contact)
- [Acknowledgments](#acknowledgments)

##  Overview

This project provides a complete analytical framework for understanding how weather conditions influence electricity consumption in Telangana. It combines traditional statistical methods with advanced machine learning techniques to deliver actionable insights for:

- **Seasonal tariff optimization**
- **Peak demand forecasting**
- **Infrastructure planning**
- **Risk assessment and anomaly detection**
- **Evidence-based regulatory decision-making**

### Key Objectives

1. Quantify the relationship between weather parameters (temperature, humidity, rainfall) and electricity consumption
2. Develop accurate forecasting models for operational planning
3. Identify critical temperature thresholds for demand response
4. Provide data-driven recommendations for seasonal tariff structures

## Features

### Core Analysis

- **Exploratory Data Analysis (EDA)** with comprehensive visualizations
- **Correlation Analysis** between weather parameters and consumption
- **Time Series Decomposition** for trend and seasonal patterns
- **Multiple Regression Models** (Linear, Polynomial, Ridge, Lasso)
- **Advanced Machine Learning** (XGBoost, Neural Networks, Random Forest)
- **Interactive Dashboards** using Plotly
- **Automated Report Generation** with key findings

### Advanced Methods

- **SARIMA** time series forecasting with weather regressors
- **Granger Causality** testing for directional relationships
- **Wavelet Analysis** for multi-scale pattern detection
- **Quantile Regression** for risk assessment
- **Regime Switching Models** for operational states
- **Extreme Value Analysis** for peak demand estimation
- **Mathematical Tariff Optimization**

### Operational Tools

- **Real-time Prediction System**
- **7-day Forecasting Dashboard**
- **Alert System** (GREEN/YELLOW/ORANGE/RED levels)
- **Monthly Report Generator**

## Technologies Used

### Core Libraries

```python
pandas==1.3.0          # Data manipulation
numpy==1.21.0          # Numerical computing
matplotlib==3.4.2      # Static visualizations
seaborn==0.11.1       # Statistical plots
plotly==5.1.0         # Interactive visualizations
scikit-learn==0.24.2  # Machine learning
```

### Advanced Analytics

```python
statsmodels==0.12.2   # Statistical modeling
xgboost==1.4.2       # Gradient boosting
lightgbm==3.2.1      # Fast gradient boosting
prophet==1.0         # Time series forecasting
pywavelets==1.1.1    # Wavelet analysis
scipy==1.7.0         # Scientific computing
```

##  Installation

### Option 1: Google Colab (Recommended)

No installation required! Simply:

1. Upload the notebooks to Google Colab
2. Run the first cell to install any missing packages

### Option 2: Local Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/weather-electricity-analysis.git
cd weather-electricity-analysis

# Create virtual environment
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

# Install requirements
pip install -r requirements.txt
```

## Project Structure

```
TGERC/
│
├── advanced/
│   └── TGERC_Repo_Advanced.ipynb           # Advanced analytics notebook
│
├── comparision/
│   └── TGERC_Compare.ipynb                 # Comparative analysis notebook
│
├── main/
│   ├── TGERC_Report.ipynb                  # Main report notebook
│   └── output/
│       └── content/
│           └── output/
│               ├── figures/                # Generated visualizations
│               │   ├── 3d_visualization.html
│               │   ├── analysis_summary_dashboard.png
│               │   ├── consumption_forecast_2025.png
│               │   ├── correlation_heatmap.png
│               │   ├── correlation_scatter_plots.png
│               │   ├── interactive_dashboard.html
│               │   ├── model_predictions.png
│               │   ├── polynomial_regression.png
│               │   ├── seasonal_analysis.png
│               │   ├── time_series_decomposition.png
│               │   └── time_series_overview.png
│               ├── models/
│               │   └── best_model_artifacts.pkl         # Saved model artifacts
│               └── reports/
│                   └── TGERC_Weather_Electricity_Analysis_Report.md  # Analysis report
│
├── sample_data/
│   └── content/
│       ├── telangana_combined_data_2019_2024.csv
│       ├── telangana_electricity_data_2019_2024.csv
│       ├── telangana_monthly_averages.csv
│       └── telangana_weather_data_2019_2024.csv
│
├── requirements.txt                        # Python dependencies
├── README.md                               # This file
```

##  Usage

### Quick Start with Sample Data

1. **Run Main Analysis Notebook**:

   - Open `main/TGERC_Report.ipynb` in Jupyter or Colab.
   - This notebook performs the full analysis pipeline using the sample data.

2. **Advanced Analysis**:

   - For advanced methods, use `advanced/TGERC_Repo_Advanced.ipynb`.

3. **Comparative Analysis**:

   - For comparison studies, use `comparision/TGERC_Compare.ipynb`.

4. **View Results**:
   - Check `main/output/content/output/figures/` for visualizations
   - Review `main/output/content/output/reports/` for detailed findings
   - Load `main/output/content/output/models/` for saved models

### For Custom/Production Use

- Adapt the notebooks to load your own data in place of the sample data.
- Update file paths and parameters as needed in the notebooks.

##  Data Requirements

### Electricity Consumption Data

Required columns:

- `Year`: Year of record
- `Month`: Month (1-12)
- `Energy_Requirement_MU`: Monthly electricity requirement in Million Units
- `Energy_Available_MU`: Monthly electricity available
- `Peak_Demand_MW`: Peak demand in Megawatts
- `Peak_Met_MW`: Peak demand met

### Weather Data

Required columns:

- `Year`: Year of record
- `Month`: Month (1-12)
- `Avg_Temperature_C`: Average monthly temperature in Celsius
- `Max_Temperature_C`: Maximum temperature
- `Min_Temperature_C`: Minimum temperature
- `Humidity_Percent`: Average humidity percentage
- `Rainfall_mm`: Total monthly rainfall in millimeters

### Optional Weather Parameters

- `Wind_Speed_kmh`: Average wind speed
- `Solar_Radiation_MJ_m2`: Solar radiation

##  Important Note on Sample Data

**This repository uses SAMPLE DATA for demonstration purposes.** The included datasets are synthetically generated to mimic realistic patterns but are NOT actual electricity consumption or weather data from Telangana.

### Why Sample Data?

- Protects sensitive infrastructure information
- Allows public sharing and collaboration
- Demonstrates methodology without confidentiality concerns
- Provides consistent baseline for testing

### Sample Data Characteristics

- **Time Period**: 2020-2024 (60 months)
- **Patterns**: Realistic seasonal variations and weather correlations
- **Correlations**: Temperature-consumption correlation ~0.75-0.85
- **Seasonality**: Summer peaks 35-45% higher than winter

## 🔧 Adapting for Real Datasets

To use this project with actual data, follow these steps:

### Step 1: Data Collection

#### Electricity Data Sources

1. **Central Electricity Authority (CEA)**

   - Visit: https://cea.nic.in/power-supply/?lang=en
   - Download monthly Power Supply Position reports
   - Extract Telangana state data

2. **National Power Portal**
   - Visit: https://npp.gov.in/
   - Access state-wise consumption data

#### Weather Data Sources

1. **India Meteorological Department (IMD)**
   - Register at: https://dsp.imdpune.gov.in/
   - Request historical weather data for Telangana
2. **Telangana State Development Planning Society**
   - Visit: https://tgdps.telangana.gov.in/
   - Download weather statistics

### Step 2: Data Preparation

1. **Create CSV files** with the required columns mentioned above

2. **Replace sample data paths** in notebooks:

```python
# Change this:
df = pd.read_csv('sample_data/telangana_combined_data_2019_2024.csv')

# To this:
df = pd.read_csv('real_data/your_actual_data.csv')
```

3. **Update date ranges** if your data covers different periods:

```python
# Modify in notebooks:
start_date = '2019-01-01'  # Change to your data start date
end_date = '2024-04-30'    # Change to your data end date
```

### Step 3: Configuration Updates

1. **Modify data validation thresholds** in `src/data_preprocessing.py`:

```python
# Adjust based on your region's characteristics
TEMP_MIN = 10    # Minimum valid temperature
TEMP_MAX = 45    # Maximum valid temperature
CONSUMPTION_MIN = 2000  # Minimum valid consumption
CONSUMPTION_MAX = 10000 # Maximum valid consumption
```

2. **Update model parameters** if needed:

```python
# In advanced models notebook
SEASONAL_PERIOD = 12  # Keep as 12 for monthly data
FORECAST_HORIZON = 12 # Adjust forecast period as needed
```

3. **Calibrate alert thresholds** for your grid:

```python
# In operational tool
ALERT_THRESHOLDS = {
    'consumption': {'warning': 5500, 'critical': 6500},  # Adjust these
    'temperature': {'warning': 33, 'critical': 38},      # Based on your region
    'peak_demand': {'warning': 10000, 'critical': 11500} # Grid capacity
}
```

### Step 4: Validation

After loading real data, run these validation checks:

```python
# Check data quality
python src/data_preprocessing.py --validate real_data/your_data.csv

# Verify correlations are reasonable
correlation = df['Temperature'].corr(df['Consumption'])
assert 0.5 < correlation < 0.95, "Unusual correlation detected"

# Ensure seasonal patterns exist
summer_avg = df[df['Month'].isin([4,5,6])]['Consumption'].mean()
winter_avg = df[df['Month'].isin([12,1,2])]['Consumption'].mean()
assert summer_avg > winter_avg, "Seasonal pattern validation failed"
```

##  Analysis Workflow

1. **Data Collection & Preprocessing**

   - Load electricity and weather data
   - Clean and merge datasets
   - Handle missing values
   - Create derived features

2. **Exploratory Data Analysis**

   - Time series visualization
   - Seasonal pattern analysis
   - Correlation assessment
   - Outlier detection

3. **Model Development**

   - Traditional regression models
   - Advanced machine learning
   - Time series forecasting
   - Model validation

4. **Insights & Recommendations**
   - Temperature threshold identification
   - Seasonal impact quantification
   - Peak demand forecasting
   - Tariff optimization suggestions

##  Key Results

Using the sample data, the analysis reveals:

- **Strong Correlation**: Temperature explains ~75-85% of consumption variation
- **Threshold Effect**: Consumption increases sharply above 28-30°C
- **Seasonal Impact**: Summer consumption 35-45% higher than winter
- **Best Model**: XGBoost achieves ~89% R² score
- **Consumption Sensitivity**: ~150 MU increase per degree Celsius

_Note: These are sample data results. Real data may show different patterns._

##  Contributing

Contributions are welcome! Please follow these steps:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Contribution Guidelines

- Maintain code quality and documentation
- Add unit tests for new features
- Update README for significant changes
- Follow PEP 8 style guidelines

##  License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

##  Acknowledgments

- Telangana Electricity Regulatory Commission (TGERC) for the project concept
- Central Electricity Authority (CEA) for data structure guidelines
- India Meteorological Department (IMD) for weather data formats
- Open source community for the excellent analytical libraries

---

**Disclaimer**: This project uses sample data for demonstration. Results and recommendations should be validated with actual data before implementation in production systems.

**Note for TGERC**: For the official version with real data, please contact the development team for secure data integration and customized deployment.
