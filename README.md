# **Stock Market Predictor: S&P 500 Index**

## **Overview**

This project is divided into two main parts: **Exploratory Data Analysis (EDA)** and **Prediction Modeling**. The goal is to understand the historical behavior of the S&P 500 index through EDA and then apply machine learning techniques to predict its future movements.

## **Project Structure**

- `README.md`: Project documentation.
- `requirements.txt`: List of dependencies needed to run the project.
- `StockMarketEDA.ipynb`: Jupyter notebook containing the Exploratory Data Analysis of the S&P 500 data.
- `StockMarketPredictor.ipynb`: Jupyter notebook for the Prediction Modeling.
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

## **Prediction Modeling**

### **Purpose**
The Prediction Modeling phase builds on the insights gained from the EDA phase to develop machine learning models capable of predicting whether the S&P 500 will move up or down on the next day.

### **Key Steps in Prediction Modeling**

1. **Feature Engineering**:
   - We create features such as **RSI**, **MACD**, **Moving Averages**, and other technical indicators to help the model learn the patterns in stock price movements.

2. **Machine Learning Models**:
   - We train several models, including:
     - **HistGradientBoostingClassifier**
     - **RandomForestClassifier**
     - **LogisticRegression**
     - **Support Vector Classifier (SVC)**

3. **Model Tuning and Comparison**:
   - The models are evaluated based on accuracy, precision, recall, and F1-score.
   - The best-performing model is selected after hyperparameter tuning using **GridSearchCV**.

4. **Evaluation**:
   - The best model is evaluated on unseen test data, with detailed metrics including confusion matrix, precision, recall, and F1-score.

### **How to Run the Prediction Model**

1. **Open the Prediction Notebook**:
    Open the `StockMarketPredictor.ipynb` file to view the prediction model steps and outputs.

2. **Run the Notebook**:
    Run each cell step-by-step to train and evaluate the machine learning models on the S&P 500 data.

## **Contributing**

1. Fork the repo.
2. Create a new branch (`git checkout -b feature-branch-name`).
3. Commit your changes (`git commit -m 'Add some feature'`).
4. Push to the branch (`git push origin feature-branch-name`).
5. Create a Pull Request.
