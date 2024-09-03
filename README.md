# **Stock Market Predictor: S&P 500 Index**

## **Overview**

This project is divided into two main parts: **Exploratory Data Analysis (EDA)** and **Prediction Modeling**. The goal is to understand the historical behavior of the S&P 500 index through EDA and then apply machine learning techniques to predict its future movements. This README focuses on the EDA component, with the Prediction Modeling documentation to be added soon.

## **Project Structure**

- `README.md`: Project documentation.
- `requirements.txt`: List of dependencies needed to run the project.
- `StockMarketEDA.ipynb`: Jupyter notebook containing the Exploratory Data Analysis of the S&P 500 data.
- `StockMarketPredictor.ipynb`: Jupyter notebook for the Prediction Modeling (final and documentation coming soon).
- `stock_predictor_env/`: Virtual environment directory.

## **Exploratory Data Analysis (EDA)**

### **Purpose**
The EDA phase helps us uncover key patterns, trends, and insights from the S&P 500 data, which are essential for building a robust predictive model.

### **Key Insights**

1. **Time Series Analysis of Closing Prices**:
   - Long-term upward trends, with notable growth acceleration from the 1980s onwards.
   - Identification of major downturns like the 2000 dot-com bubble and the 2008 financial crisis.

2. **Distribution Analysis**:
   - The distribution shows a left-skew, reflecting the historical growth of the market with higher price levels becoming more frequent in recent decades.

3. **Volume Trend Analysis**:
   - Significant increase in trading volume starting in the late 1980s, often correlating with major market events.

4. **Rolling Mean and Standard Deviation**:
   - Rolling mean reveals long-term trends, while rolling standard deviation indicates periods of market volatility.

5. **Daily Returns and Risk Analysis**:
   - Analysis of daily returns shows the market’s tendency to gain more often than it loses, with occasional extreme movements indicating higher risk.

6. **Cumulative Returns**:
   - Illustrates the exponential growth of long-term investments in the S&P 500.

7. **Bollinger Bands for Volatility Analysis**:
   - Bollinger Bands help in identifying overbought and oversold market conditions, providing potential trading signals.

8. **Autocorrelation Analysis**:
   - Highlights patterns and cycles in the market, valuable for predictive modeling.

### **How to Run EDA**

1. **Clone the Repository**:
    ```bash
    git clone https://github.com/Nazaboy/StockMarketPredictor.git
    cd StockMarketPredictor
    ```

2. **Set Up a Virtual Environment**:
    ```bash
    python -m venv stock_predictor_env
    source stock_predictor_env/bin/activate  # On Windows: stock_predictor_env\Scripts\activate
    ```

3. **Install Dependencies**:
    ```bash
    pip install -r requirements.txt
    ```

4. **Run the EDA Notebook**:
    Start the Jupyter notebook server:
    ```bash
    jupyter notebook
    ```
    Open the `StockMarketEDA.ipynb` file to explore the data and insights.

## **Prediction Modeling (Coming Soon)**

The Prediction Modeling phase, detailed in `StockMarketPredictor.ipynb`, will use the insights gained from EDA to train and test a machine learning model. Documentation for this phase will be added soon.

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
