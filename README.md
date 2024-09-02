# **Stock Market Predictor: S&P 500 Index**

## **Overview**

This project predicts the S&P 500 index using machine learning, specifically a Random Forest model. The analysis and modeling are performed in a Jupyter notebook, making it easy to visualize the workflow and results.

## **Features**

- **Data Sourcing**: Downloads historical S&P 500 data from Yahoo Finance.
- **Data Cleaning**: Prepares and cleans the dataset for analysis.
- **Model Training**: Trains a Random Forest model to predict stock price movements.
- **Backtesting**: Tests the model's accuracy using historical data.
- **Enhanced Predictions**: Adds features like rolling averages to improve prediction accuracy.

## **Key Insights**

- **Directionality**: Focuses on predicting whether the index will go up or down, rather than exact prices.
- **Machine Learning**: Random Forests help manage non-linear relationships in the data.
- **Backtesting**: Validates the model’s reliability by testing it on historical data.
- **Data Cleaning**: Ensures that the data is accurate and free of errors before modeling.
- **Feature Engineering**: Incorporates additional features like trends to enhance model performance.

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


## **Usage**

1. **Download Data**: The notebook automatically fetches the latest S&P 500 data.
2. **Train Model**: The Random Forest model is trained within the notebook.
3. **Backtest**: Backtesting is performed to evaluate the model's predictions.
4. **Predict**: Use the notebook to make future predictions.

## **Contributing**

1. Fork the repo.
2. Create a new branch (`git checkout -b feature-branch-name`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch-name`).
5. Create a Pull Request.


### Problem Fix Report: Jupyter Kernel Issue in VSCode

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



## **Contact**

- GitHub: [Nazaboy](https://github.com/Nazaboy)
