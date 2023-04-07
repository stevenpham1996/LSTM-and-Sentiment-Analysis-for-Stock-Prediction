# Numerical-and-Textual-Analysis-for-Stock-Prediction
This is one of the project tasks from the @GRIP Internship Program of **The Spark Foundation**

## Objective:
Predict the Indian Stock Exchange Sensitive Index - `SENSEX` from historical stock price and news headlines data from 2015/01/01-31/03/2022.  
#### The dataset used in this project:  
-[SENSEX](https://www.bing.com/search?q=sensex+yahoo+finance&aqs=edge.1.0j69i59j0l6j69i64.4119j0j1&FORM=ANAB01&PC=EDGEDBB)  
-[News headlines](https://bit.ly/36fFPI6)

## Methodology:
- Transform Daily Close prices into logarithmic returns to attain better statistical properties, then used along side with Yesterday Close prices as numerical feature inputs.
- Utilize the Huggingface pretrained RoBERTa `cardiffnlp/twitter-roberta-base-sentiment-latest` model for Sentiment Analysis on news headlines.
- 2 machine learning models `LSTM` and `LightGBM` are used and contrasted.  

## Result:
The `LSTM` model was able to generalize better in testing data than the 'LightGBM' model with significant lower `RMSE` (Root Mean Square Error).  

## References:
- [Stock Price Prediction using Sentiment Analysis and Deep Learning for Indian Markets](https://arxiv.org/abs/2204.05783) 
