This code builds a stock price prediction model using a hybrid deep learning approach that combines Convolutional Neural Networks (CNN) and LSTM networks with Keras.

## What the Code Does

## Data Loading & Preprocessing

It reads historical stock data from a CSV file and extracts closing prices. The values are scaled between 0 and 1 using MinMaxScaler to improve model performance.

## Sequence Creation (Time Series)
A sliding window of 60 days is used to create input sequences, where each sequence predicts the next day’s price.

## Train-Test Split
The dataset is split into 80% training and 20% testing data.

## Model Architecture (CNN + LSTM)
CNN layer captures short-term patterns in the data

## MaxPooling reduces dimensionality
LSTM layer learns long-term dependencies in time series

## Dropout helps prevent overfitting
Dense layer outputs the predicted stock price

## Training
The model is trained using the Adam optimizer and mean squared error loss.

## Prediction & Evaluation
The model predicts stock prices on test data, then converts them back to original scale for comparison with actual prices.

The model combines CNN (for feature extraction) and LSTM (for temporal learning) to improve prediction accuracy on sequential stock data. This is a hybrid deep learning pipeline that processes historical stock prices, learns patterns over time, and predicts future values though results depend heavily on data quality and market unpredictability.
