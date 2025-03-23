# CNN-LSTM Stock Price Prediction

## Overview
This project implements a **CNN-LSTM model** to predict stock prices using historical stock market data. The model combines **Convolutional Neural Networks (CNNs)** for feature extraction and **Long Short-Term Memory (LSTMs)** for learning temporal dependencies in stock price trends.

## Dataset
We use publicly available stock price datasets, such as **Yahoo Finance** data. The dataset includes features like:
- Open Price
- High Price
- Low Price
- Close Price
- Trading Volume

## Installation
To run the project, install the required dependencies:
```bash
pip install yfinance pandas numpy scikit-learn tensorflow matplotlib
```

## Steps to Run
1. **Download Stock Data**  
   Fetch historical stock prices using `yfinance`.
2. **Preprocess the Data**  
   - Normalize stock prices.
   - Convert data into sequences suitable for LSTM.
3. **Build the CNN-LSTM Model**  
   - CNN extracts features from stock price sequences.
   - LSTM learns historical trends.
4. **Train the Model**  
   - Split data into training and testing sets.
   - Train the model using `Adam` optimizer and `MSE` loss function.
5. **Make Predictions**  
   - Evaluate the model on test data.
   - Plot actual vs. predicted prices.

## Model Architecture
- **CNN Layer:** Extracts important stock price patterns.
- **MaxPooling:** Reduces dimensionality.
- **LSTM Layer:** Captures long-term dependencies in stock trends.
- **Dense Layer:** Outputs the final predicted stock price.

## Example Usage
```python
import yfinance as yf

# Download Apple stock data
data = yf.download('AAPL', start='2010-01-01', end='2020-01-01')
print(data.head())
```

## Disclaimer
Stock price prediction is inherently uncertain and influenced by multiple external factors. This model is for **educational purposes only** and **should not be used for actual trading or investment decisions**.

## References
- [Yahoo Finance API](https://pypi.org/project/yfinance/)
- [TensorFlow Keras Documentation](https://www.tensorflow.org/guide/keras)

