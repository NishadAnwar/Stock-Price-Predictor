# Stock-Price-Predictor

This code is a Python script that creates a web application using the Streamlit framework to visualize stock data and predict future stock prices using various machine learning models. Here’s a breakdown of the code:

### 1. Imports
Libraries:
streamlit for creating the web interface.
pandas for data manipulation.
yfinance for downloading stock data.
ta for technical analysis indicators like Bollinger Bands, MACD, RSI, SMA, and EMA.
datetime for handling date and time.
scikit-learn libraries for data preprocessing, model selection, and evaluation.
xgboost for advanced gradient boosting models.

### 2. Streamlit Interface
The application title is set using st.title('Trading Price Predictor').
Main Functionality:
The sidebar allows users to choose between three options: Visualize, Recent Data, and Predict.
Depending on the user’s choice, the application will display different features.

### 3. Data Downloading
The download_data function fetches stock data using the Yahoo Finance API via yfinance.
The user inputs a stock symbol, start and end dates, and the duration to download the data.

### 4. Technical Indicators Visualization
The tech_indicators function displays various technical indicators like Close price, Bollinger Bands, MACD, RSI, SMA, and EMA based on the user’s choice.
The data is visualized using line charts for the selected indicator.

### 5. Displaying Recent Data
The dataframe function shows the most recent 10 rows of the downloaded stock data.

### 6. Prediction
The predict function allows users to choose a machine learning model from options like Linear Regression, Random Forest, Extra Trees, K-Nearest Neighbors, or XGBoost.
Users can input how many days into the future they want to forecast.
The model_engine function handles data preprocessing, training, and prediction:
It uses the closing prices of the stock.
The data is scaled, and the model is trained using the selected machine learning algorithm.
The model is evaluated using r2_score and mean_absolute_error.
It predicts future stock prices for the specified number of days.

### 7. Execution
The main function controls the flow based on user selections, and it is executed when the script is run.

### 8. Caching
The @st.cache_resource decorator is used to cache the download_data function to avoid redundant downloads.
This script offers an interactive platform for users to visualize stock data, examine technical indicators, and predict future prices using machine learning models.
