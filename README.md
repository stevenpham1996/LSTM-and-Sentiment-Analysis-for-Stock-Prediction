# Numerical-and-Textual-Analysis-for-Stock-Prediction
This is one of the project tasks from the @GRIP Internship Program of **The Spark Foundation**

## Objective:
Predict the Indian Stock Exchange Sensitive Index - `SENSEX` from historical stock price and news headlines data from 2015/01/01-31/03/2022.  
#### The dataset used in this project:  
-[SENSEX](https://www.bing.com/search?q=sensex+yahoo+finance&aqs=edge.1.0j69i59j0l6j69i64.4119j0j1&FORM=ANAB01&PC=EDGEDBB)  
-[News headlines](https://bit.ly/36fFPI6)

## Methodology:
- Transform numerical stock price into logarithmic returns for better statistical modelling.
- Utilize the Huggingface pretrained RoBERTa `cardiffnlp/twitter-roberta-base-sentiment-latest` model for Sentiment Analysis on news headlines.
- 2 machine learning models `LSTM` and `Random Forest Regressor` are used and compared.
## Result:
The `Random Forest Regressor` model has signigficantly lower Root Mean Square Error `RMSE` in both training and testing outputs than the `LSTM` model's.  
However, this is merely a simple demonstration, the conclusion should not be taken without further research.

### References:
- [Stock Price Prediction using Sentiment Analysis and Deep Learning for Indian Markets](https://arxiv.org/abs/2204.05783) 
