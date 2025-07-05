# Gasoline Prediction

This repository presents a comprehensive data analysis project built around fuel price data obtained from Tankerkönig. Due to licensing restrictions, the raw datasets are not included in this repository but can be made available upon request.

## Directory Structure & Notebook Descriptions

### 01\_Data\_Pipeline.ipynb

In the first notebook, the focus is on establishing a robust data pipeline that brings together fuel price information from Tankerkönig and supplementary oil price series retrieved via the `yfinance` library. The notebook loads the raw datasets, validates their integrity by identifying missing or inconsistent records, and applies systematic cleaning procedures to standardize formats and handle outliers. The cleaned and structured data are then exported in formats optimized for downstream analysis, ensuring reproducibility and transparency throughout the preparation phase.

### 02\_Summary.ipynb

The second notebook offers a descriptive overview of the preprocessed data, providing insights into their central tendencies and distributional characteristics. After importing the cleaned datasets produced in the pipeline, key metrics such as mean prices, medians, and quantiles are computed and presented in concise tables. To complement these statistics, informative visualizations— including histograms, box plots, and time series plots—are generated to highlight notable patterns and anomalies in the fuel price movements, setting the stage for deeper, model-driven exploration.

### 03\_Univariate\_Analysis.ipynb

In the third notebook, univariate time series models are developed to forecast fuel prices based solely on their historical behavior. Beginning with an exploration of trend, seasonality, and stationarity, the notebook then transitions to the construction of simple yet effective forecasting techniques such as ARIMA and Exponential Smoothing models. Each model’s configuration is assessed using standardized metrics and cross-validation. The notebook concludes by interpreting the forecasting outcomes.

### 04\_Multivariate\_Analysis.ipynb

The fourth notebook expands the analytical scope by introducing external explanatory variables into the forecasting framework. Building on the insights from the univariate analysis, this section explores the relationship between fuel prices and oil price indices sourced via `yfinance`, examining correlation structures and potential lead-lag effects. The structure of the entire notebook is identical to 03\_Univariate\_Analysis.ipynb.

## Data

Raw data are available upon request. The primary data source consists of Tankerkönig fuel station price data, supplemented by global oil price series downloaded via `yfinance`.

## Requirements & Installation

To run the analysis notebooks, ensure you have Python 3.8 or higher and Jupyter Notebook or JupyterLab installed. Install required libraries using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn yfinance
```

## Usage

Clone the repository and execute the notebooks in sequential order (01 → 02 → 03 → 04) to reproduce the full analysis:

```bash
git clone https://github.com/username/repository.git
cd repository
jupyter notebook
```

## Notes

Please update the **Data Source** section with any additional details or links as needed. For questions or feedback, feel free to open an issue in this repository.
