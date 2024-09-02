# **Stock Market Predictor: S&P 500 Index**

## **Overview**

This project focuses on predicting the S&P 500 index using a machine learning approach, specifically utilizing a Random Forest model. The entire process is conducted within a Jupyter notebook, which facilitates easy visualization of the workflow and results.

## **Features**

- **Data Sourcing**: Automatically downloads historical S&P 500 data from Yahoo Finance.
- **Data Cleaning**: Prepares and cleans the dataset to ensure accuracy and usability for analysis.
- **Exploratory Data Analysis (EDA)**: Provides deep insights into the dataset through various visualizations.
- **Model Training**: Implements a Random Forest model to predict stock price movements.
- **Backtesting**: Evaluates the model's accuracy using historical data to ensure reliability.
- **Enhanced Predictions**: Integrates advanced features like rolling averages and Bollinger Bands to improve prediction accuracy.

## **Exploratory Data Analysis (EDA)**

EDA is a crucial step in this project, helping to understand the data and prepare it for the modeling process. Below are the key visualizations and their insights:

1. **S&P 500 Closing Prices Over Time**:
   - Shows a clear long-term upward trend, with notable accelerations from the 1980s onwards. Occasional dips represent market corrections or economic downturns.

2. **Distribution of S&P 500 Closing Prices**:
   - The distribution is heavily left-skewed, reflecting the market's historically lower levels. Higher prices have become more common only in recent years.

3. **S&P 500 Volume Traded Over Time**:
   - Trading volume remained low until the late 1980s, after which it increased significantly. Spikes in volume often correspond to periods of high market activity.

4. **S&P 500 Rolling Mean and Standard Deviation**:
   - The 100-day rolling mean smooths out short-term fluctuations, revealing longer-term trends. The rolling standard deviation indicates periods of high volatility, often during market corrections.

5. **Distribution of S&P 500 Daily Returns**:
   - Daily returns are centered around 0%, with a slight positive skew, indicating the market generally gains more than it loses. The presence of fat tails highlights the risk of extreme market movements.

6. **S&P 500 Cumulative Returns Over Time**:
   - Demonstrates the exponential growth of an investment in the S&P 500, underscoring the power of long-term investments and compound growth.

7. **S&P 500 with Bollinger Bands**:
   - Visualizes market volatility with bands expanding during high volatility and contracting during stability. Prices near the upper band may indicate overbought conditions, while prices near the lower band suggest oversold conditions.

8. **Autocorrelation of S&P 500 Closing Prices**:
   - The autocorrelation plot shows how past values of the S&P 500 closing price influence future values, with autocorrelation decreasing over time. Periodic dips and peaks may indicate cycles or seasonality.

## **Installation**

To set up the project locally:

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/Nazaboy/StockMarketPredictor.git
    cd StockMarketPredictor
    ```

2. **Create a Virtual Environment**:
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```

3. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Run the Jupyter Notebook**:
    Start the Jupyter notebook server:
    ```bash
    jupyter notebook
    ```
    Open the `StockMarketPredictor.ipynb` file to run the analysis.

## **Project Structure**

- `README.md`: Project documentation.
- `requirements.txt`: List of dependencies.
- `StockMarketPredictor.ipynb`: The main Jupyter notebook containing the analysis and model.
- `venv/`: The virtual environment directory (not included in the repository; generated locally).

## **Usage**

1. **Download Data**: The notebook automatically fetches the latest S&P 500 data.
2. **EDA**: Explore the data with visualizations to understand trends, volatility, and patterns.
3. **Train Model**: The Random Forest model is trained within the notebook.
4. **Backtest**: Evaluate the model's predictions with historical data to assess accuracy.
5. **Predict**: Use the trained model to make future predictions based on new data.

## **Contributing**

1. Fork the repo.
2. Create a new branch (`git checkout -b feature-branch-name`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch-name`).
5. Create a Pull Request.

### **Problem Fix Report: Jupyter Kernel Issue in VSCode**

**Issue:**
- Kernel failed to start in VSCode: `/bin/python3.10: No module named ipykernel_launcher...`
- `ModuleNotFoundError` for `yfinance`.

**Cause:**
- Incorrect Python interpreter in VSCode.
- Missing or misconfigured `ipykernel`.

**Resolution:**
1. Activated virtual environment: `source stock_predictor_env/bin/activate`
2. Installed `ipykernel`: `pip install ipykernel`
3. Registered the environment as a Jupyter kernel:
   ```bash
   python -m ipykernel install --user --name=stock_predictor_env --display-name "Python (stock_predictor_env)"
