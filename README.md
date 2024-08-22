# Predictive Modeling and Analysis of Stock Price Movements Using NYSE Historical Data
## Project Overview
### This project was part of the requirements for an M.Sc in Data Science at the University of Hertfordshire. It concentrated on predicting stock price movements based on historical New York Stock Exchange (NYSE) data. The main goal of this work is to assess how well three types of machine learning models, Long-Short-Term Memory (LSTM), Recurrent Neural Networks (RNN), and extreme Gradient Boosting (XGBoost), can perform when applied to the use case of forecasting stock prices.
## Motivation
### The Stock Market is never as simple or easy to predict, but it can be highly rewarding. Many times, the traditional methods fail because financial markets are non-linear. This project employs complex machine learning algorithms to enhance the precision of forecasting stock prices, which can help investors better understand their investment strategies.
## Dataset
### The dataset used in this project includes historical stock price data of S&P 500 companies listed on the NYSE from 2010 to 2016. The major features in this data set are:
### • prices.csv: Raw daily stock prices.
### •	prices-split-adjusted.csv: Daily stock prices adjusted for stock splits.
### •	securities.csv: Descriptive information about each company, including sector classifications.
### •	fundamentals.csv: Financial metrics derived from SEC 10-K filings, such as earnings, margins, and financial ratios.
## Data Preprocessing
### •	Data Cleaning: The datasets were merged based on common columns, missing values were handled, and the data was rescaled using MinMaxScaler.
### •	Feature Engineering: Technical indicators, including Moving Averages, Relative Strength Index (RSI), and Bollinger Bands, were calculated to improve the capability of our models.
### •	Normalization: Feature scaling was applied to ensure that all variables were on a consistent scale, facilitating better model performance.
## Models Developed
## 1. Long Short-Term Memory (LSTM)
### •	Architecture: One LSTM layer followed by a dropout layer and dense output Layer. The model was trained using the Adam optimizer with a learning rate of 1e-4.
### •	Performance: A R² value of 0.9883, a very good capture of the Temporal Patterns in stock prices.
## 2. Recurrent Neural Network (RNN)
### •	Architecture: Two SimpleRNN layers followed by dropout and a dense output layer were trained using the Adam optimizer.
### •	Performance: Could get 0.6415 of R² value, good results but not strongly capture long-term dependencies as LSTM does.
## 3. eXtreme Gradient Boosting (XGBoost)
### •	Architecture: XGBoost Regressor GridSearchCV using hyperparameters such as n_estimators, learning_rate, max_depth architecture.
### •	Performance: Had R² of 1.0 on the training set but overfitted a little when tested with the test data set.
## Results and Discussion
### The LSTM broke the record and was more predictive and accurate than other models like RNN or XGBoost. Although XGBoost was very good in training, it began to overfit from the test set. The RNN model, contrary to the Keras LSTM layer, worked well but achieved considerably less accuracy because it could not capture temporal dependencies in stock price data.
## Model Performance Comparison
### Model	MAE	MSE	RMSE	R²
### LSTM	0.0012	0.0000	0.0171	0.9883
### RNN	0.0064	0.0006	0.0079	0.6415
### XGBoost	0.3400	5.2500	2.2900	1.0000
## Future Work
### •	Advanced Architectures: Use more complex LSTM architectures like stacked or bidirectional LSTMs to make even better forecasts.
### •	Incorporating External Data: Add variables like macroeconomic indicators or news sentiment analysis to enhance the model's prediction.
### •	Alternative Models: Experiment with different machine learning methods, such as Transformer models or hybrid models, to see if they provide benefits over the above techniques.
## Acknowledgements
### This project was part of Niall Miller's MSc Data Science research module at the University of Hertfordshire. Thanks to NYSE Data for making this dataset available and to the open-source community, which has done a great job with tools and resources.
	
