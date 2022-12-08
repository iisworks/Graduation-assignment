# Forecasting Spot Exchange Rates 

## Absrtact

Due to the interesting financial moment we are living, my motivation to write the this work has mostly been the behavior of foreign exchange rates and models that can be used to predict them. Thus, in htis assignment I have presented 2 models: the Autoregressive Integrated Moving Average (ARIMA) and tensorflow.keras models so they can be used to 

## Introduction

An exchange rate is a rate at which one currency will be exchanged for another currency and affects trade and the movement of money between countries.

Exchange rates are impacted by both the domestic currency value and the foreign currency value. In July 2022, the exchange rate from U.S. Dollars to the Euro was 1.02, meaning it takes $1.02 to buy €1.

While most exchange rates are floating and will rise or fall based on the supply and demand in the market, some exchange rates are pegged or fixed to the value of a specific country's currency. Exchange rate changes affect businesses and the cost of supplies and demand for their products in the international marketplace. 

Because of the unpredictability and volatility of currency rates, the exchange rate prediction has become one of the most challenging applications of financial time series forecasting.

## Data Description

Data were collected from an authentic source from the European Central Bank (https://www.ecb.europa.eu/stats/policy_and_exchange_rates/euro_reference_exchange_rates/html/index.en.html). This information comprises 42 variables. The data have a duration from 4 January 1999 to 29 November 2022. The period is based on daily observations, having two components, one is the dependent variable, and the other one is an independent variable as the exchange rate is part of the economic time series, which is considered as a dependent variable. By contrast, time is said to be an independent variable.

## Agenda

Part 1: Explanatory Data Analysis (EDA) & Data Visualisation of the raw dataset.

Part 2: Machine Learning: Time Series Forecasting with ARIMA.

Part 3: Machine Learning: Tensorflow.keras.

Part 4: Future recomendations: Econometric Models and Purchasing Power Parity (PPP)


## Autoregressive Integrated Moving Average (ARIMA) Model

A specific procedure, autoregressive integrated moving average (ARIMA) under time series forecasting, was introduced by Box and Jenkins.

Stationary is the basic assumption to be fulfilled for the time series forecasting, while other specified conditions are the mean should be independent over time  and the variance among consecutive observations should be constant .

![image](https://user-images.githubusercontent.com/112239284/206434851-ec1a471f-b25f-46ac-802c-9e2fc5ae0d70.png)

Here, the AR (p) model is represented by equation (1) with p parameters, and MA (q) model is represented by equation (2) with q parameters. Hence, the combination of both models ARMA (p, q) can be illustrated as (1) with p and q parameters.
This equation is applied when the original series is not stationary at its level. A transformation is needed, such as differencing. Further, if the series is ensured stationary at the first difference, then it provides that the original series is comprised of unit root and defined as I (1). Generally, if it is stationary at more than 1 difference, it is represented by d parameters. In such a case, equation (4) specifies the ARIMA (p, d, q) model with , d, and q parameters

![image](https://user-images.githubusercontent.com/112239284/206435068-12cde27a-fc44-4e45-aec6-9c062576ce28.png)


## Purchasing Power Parity (PPP)

The PPP forecasting approach is based on the theoretical law of one price, which states that identical goods in different countries should have identical prices.The PPP approach forecasts that the exchange rate will change to offset price changes due to inflation based on this underlying principle.

One of the most well-known applications of the PPP method is illustrated by the Big Mac Index, compiled and published by The Economist. This lighthearted index attempts to measure whether a currency is undervalued or overvalued based on the price of Big Macs in various countries. Since Big Macs are nearly universal in all the countries they are sold, a comparison of their prices serves as the basis for the index. (https://www.economist.com/big-mac-index)


## Econometric Models of Forecasting Exchange Rates

Another common method used to predict exchange rates involves gathering factors that might affect currency movements and creating a model that relates these variables to the exchange rate. The factors used in econometric models are typically based on economic theory, but any variable can be added if it is believed to significantly influence the exchange rate.

For example:

USD/EUR(1 - Year)=z+a(INT)+b(GDP)+c(IGR)

where:
z=Constant baseline exchange rate
a,b and c=Coefficients representing relative
weight of each factor
INT=Difference in interest rates between
U.S. and Canada
GDP=Difference in GDP growth rates
IGR=Difference in income growth rates
