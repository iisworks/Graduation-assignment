# Forecasting Spot Exchange Rates 

## Absrtact

Due to the interesting financial moment we are living, my motivation to write the this work has mostly been the behavior of foreign exchange rates and models that can be used to predict them. Thus, in htis assignment I have presented 2 models: the Autoregressive Integrated Moving Average (ARIMA) and tensorflow.keras models so they can be used to 

## Introduction

An exchange rate is a rate at which one currency will be exchanged for another currency and affects trade and the movement of money between countries.

Exchange rates are impacted by both the domestic currency value and the foreign currency value. In July 2022, the exchange rate from U.S. Dollars to the Euro was 1.02, meaning it takes $1.02 to buy €1.

While most exchange rates are floating and will rise or fall based on the supply and demand in the market, some exchange rates are pegged or fixed to the value of a specific country's currency. Exchange rate changes affect businesses and the cost of supplies and demand for their products in the international marketplace. 

Because of the unpredictability and volatility of currency rates, the exchange rate prediction has become one of the most challenging applications of financial time series forecasting.

## Data Description

Data were collected from an authentic source from the European Central Bank. This information comprises 42 variables. The data have a duration from 4 January 1999 to 29 November 2022. The period is based on daily observations, having two components, one is the dependent variable, and the other one is an independent variable as the exchange rate is part of the economic time series, which is considered as a dependent variable. By contrast, time is said to be an independent variable.

## Agenda

Part 1: Explanatory Data Analysis (EDA) & Data Visualisation of the raw dataset.

Part 2: Machine Learning: Time Series Forecasting with ARIMA.

Part 3: Machine Learning: Tensorflow.keras.


## Autoregressive Integrated Moving Average (ARIMA) Model

A specific procedure, autoregressive integrated moving average (ARIMA) under time series forecasting, was introduced by Box and Jenkins.

Stationary is the basic assumption to be fulfilled for the time series forecasting, while other specified conditions are the mean should be independent over time  and the variance among consecutive observations should be constant .

![image](https://user-images.githubusercontent.com/112239284/206434851-ec1a471f-b25f-46ac-802c-9e2fc5ae0d70.png)

Here, the AR (p) model is represented by equation (1) with p parameters, and MA (q) model is represented by equation (2) with q parameters. Hence, the combination of both models ARMA (p, q) can be illustrated as (1) with p and q parameters.
This equation is applied when the original series is not stationary at its level. A transformation is needed, such as differencing. Further, if the series is ensured stationary at the first difference, then it provides that the original series is comprised of unit root and defined as I (1). Generally, if it is stationary at more than 1 difference, it is represented by d parameters. In such a case, equation (4) specifies the ARIMA (p, d, q) model with , d, and q parameters

![image](https://user-images.githubusercontent.com/112239284/206435068-12cde27a-fc44-4e45-aec6-9c062576ce28.png)


## Purchasing Power Parity (PPP)

The PPP forecasting approach is based on the theoretical law of one price, which states that identical goods in different countries should have identical prices.
