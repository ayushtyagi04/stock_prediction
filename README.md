Stock Market Prediction Using Stacked LSTM
==========================================

This project predicts and forecasts stock prices using a Stacked LSTM (Long Short-Term Memory)
deep learning model. It focuses on Apple's stock (AAPL) data fetched from Tiingo API,
and it visualizes both actual and predicted trends.

Features
--------
• Fetches historical stock data from Tiingo (2015–2023)
• Preprocessing using MinMaxScaler
• Stacked LSTM neural network for sequence prediction
• RMSE evaluation of train and test predictions
• Forecasts stock price for the next 30 days
• Visualizes actual vs predicted stock price trends

Requirements
------------
Install dependencies before running:
pip install pandas_datareader pandas matplotlib scikit-learn numpy tensorflow

API Key
-------
This project uses the Tiingo API. Replace the API key in Main.py with your own:
key = 'your_api_key_here'

Get your free API key here: https://www.tiingo.com

Project Structure
-----------------
• Main.py - The main Python script containing the LSTM model and forecasting code
• AAPL.csv - CSV file containing fetched stock data (generated at runtime)

Model Architecture
------------------
• LSTM Layer (256 units)
• Dropout Layer (0.1)
• Dense Layer (256 units, tanh)
• Dropout Layer (0.1)
• Output Layer (Dense(5) with softmax)

Note: The model uses categorical_crossentropy which is typically for classification.
You might consider changing the output layer and loss function for regression-based forecasting.

Results
-------
Root Mean Squared Error (RMSE) is computed for both training and testing datasets.
Plots show both short-term and extended (30-day) forecasts.

Visualization
-------------
• Actual vs predicted values
• Extended 30-day forecast chart

Improvements
------------
• Optimize model architecture (e.g., loss function for regression)
• Try different stocks or use multivariate data
• Incorporate external financial indicators or news sentiment

License
-------
This project is open-source and available under the MIT License.
