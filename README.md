# Corn-Futres-Capstone
My capstone project at Galvanize, I aimed to predict a range of potential corn prices using data on the corn market and the weather in key producing states. I was able to achieve sufficient results for implementing a hedging strategy, although overall returns would not be high enough to warrant speculation.  For current predictions and a prettier presentation, please visit my website: cooperscorn.com

# Summary
Going into the project, I had two main goals:
* Predict the direction of the price movement to lend farmers confidence for hedging their crop production
* Develop a model that would earn acceptable investment returns for traders

To achieve these objectives, I developed several neural networks, which relied on market data as inputs.  While I largely accomplished my goal of predicting direction, investment returns would be substandard for all but those with a very low cost of capital.

# Technology Used
* Python Packages
    * Keras
    * Pandas
    * Numpy
    * SciPy
    * StatsModels
    * IbPy
    * Flask

* AWS EC2

# Data
While not all datasets collected were used as features for the final models, the following was collected.

### Interactive Brokers (Daily Data)
* Corn Futures Prices
* Soybean Futures Prices
* Oil Futures Prices
* $USD Exchange Rate Index

### USDA (Yearly and Quarterly Data)
* Corn Supply Levels
* Acreage Planted
* Yield Estimates

### NOAA (Daily Data)
* Precipitation and Temperatures for Iowa, Illinois, Nebraska, Minnesota, and Indiana
* ONI Index

# Model
The final models I developed are feed-forward neural networks, which use either 6-month or 3-month lagged data as features.  The structure of the nets is quite simple, consisting of 3 layers, the hidden layer having a linear activation function and the output layer having a sigmoid activation function.  I used the lagged features rather than current data to simulate forecasting 3 or 6 months out with the information that is readily available.

# Website
After finishing the modeling phase of the project, I developed a website, cooperscorn.com, to display the results of my research as well as current predictions.  The website was built using flask bootstrapping and is hosted on an Amazon EC2 instance.

# Future Steps
* Monitor my predictions to ensure outcomes are comparable with current out-of-sample forecasts
* Speak with futures traders to identify other potentially import features
