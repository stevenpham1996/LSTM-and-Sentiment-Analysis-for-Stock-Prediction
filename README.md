# Numerical-and-Textual-Analysis-for-Stock-Prediction
This is one of the project tasks from the @GRIP Internship Program of **[The Spark Foundation](https://in.linkedin.com/company/the-sparks-foundation)**

## Objective:
Predict the Indian Stock Exchange Sensitive Index - `SENSEX` from historical stock price and news headlines data from 2015/01/01-31/03/2022.  
#### The dataset used in this project:  
-[SENSEX](https://www.bing.com/search?q=sensex+yahoo+finance&aqs=edge.1.0j69i59j0l6j69i64.4119j0j1&FORM=ANAB01&PC=EDGEDBB)  
-[News headlines](https://bit.ly/36fFPI6)

## Methodology:
- Transform Daily Close prices into logarithmic returns to attain better statistical properties, then used along side with Yesterday Close prices as numerical feature inputs.
- Utilize the Huggingface pretrained RoBERTa `cardiffnlp/twitter-roberta-base-sentiment-latest` model for Sentiment Analysis on news headlines.
- The `LSTM` was trained on numerical data only and used as a Baseline to contrast with the `LightGBM` which was trained on both numerical and textual analyzed data.

## Result:
- The `LightGBM Regressor` model as expected was able to fit and generalize better than the `LSTM` model with significantly lower `RMSE` (Root Mean Square Error).  
- The `LightGBM Classifier` was able to correctly predict the next day stock market's general movement (Buliish or Bearish) by **56.10%**.

## References:
- [Stock Price Prediction using Sentiment Analysis and Deep Learning for Indian Markets](https://arxiv.org/abs/2204.05783) 
