# Predicting Microsoft Azure cloud VM CPU Usage
## Project Name
Predicting Microsoft Azure cloud VM CPU Usage

## Objective
Predicting the CPU usage of cloud VM using data from the past.
## Why this might be worth considering?
Well, Cloud services are becoming increasingly popular day by day.  Server racks can be split between multiple users, with each user having anisolated sandbox (a virtual machine) for their application.A user can even have an application running across multiple VMs on separate machines.
 
 
**Proactively allocating VMs can increase usage efficiency of underlying resources. If a computing cluster predicts the future resource usage of a user service will increase, it can preemptively scale up to accommodate a higher load. If it predicts that usage will decrease, it can deallocate VMs and save computing resources.**

## Dataset
The Dataset contains the CPU Usage data of Microsoft Azure, which is a cloud service, sampled every 5 minutes. The data has three attributes -
* Max CPU Utilization
* Average CPU Utilization
* Minimum CPU Utilization

A glimpse into the data -
![Dataset](https://github.com/amcs1729/Predicting-cloud-CPU-usage-on-Azure-data/blob/master/Images/Dataset._graphpng.png)

## Models Used
Three different types of models were trained and their results were compared.
* LSTM Model ( 2 layers of 512 units each and a dense layer at the top)
* GRU Model  ( 2 layers of 512 units each and a dense layer at the top)
* Independent RNN Model ( 2 layers of 512 units each and a dense layer at the top)

## Results
### LSTM MODEL
##### CPU High
![LSTM_high](https://github.com/amcs1729/Predicting-cloud-CPU-usage-on-Azure-data/blob/master/Images/lstm.png)
##### CPU Average
![LSTM_avg](https://github.com/amcs1729/Predicting-cloud-CPU-usage-on-Azure-data/blob/master/Images/lstm1.png)
##### CPU Low
![LSTM_low](https://github.com/amcs1729/Predicting-cloud-CPU-usage-on-Azure-data/blob/master/Images/lstm2.png)
### GRU Model
##### CPU High
![GRU_high](https://github.com/amcs1729/Predicting-cloud-CPU-usage-on-Azure-data/blob/master/Images/gru.png)
##### CPU Avergae
![GRU_avg](https://github.com/amcs1729/Predicting-cloud-CPU-usage-on-Azure-data/blob/master/Images/gru(1).png)
##### CPU Low
![GRU_low](https://github.com/amcs1729/Predicting-cloud-CPU-usage-on-Azure-data/blob/master/Images/gru(2).png)
### Independent RNN Model
##### CPU High
![IndRNN_high](https://github.com/amcs1729/Predicting-cloud-CPU-usage-on-Azure-data/blob/master/Images/indrnn.png)
##### CPU Average
![IndRNN_avg](https://github.com/amcs1729/Predicting-cloud-CPU-usage-on-Azure-data/blob/master/Images/indrnn(1).png)
##### CPU Low
![IndRNN_low](https://github.com/amcs1729/Predicting-cloud-CPU-usage-on-Azure-data/blob/master/Images/indrnn(2).png)


## Model Performance

The Model was evaluated using rolling window forecasting method. The Root Mean Squared Error (RMSE) , Mean Absolute Error (MAE) and the Mean Average Percentage Error (MAPE) were chosen as evaluation metrices. 
##### LSTM Model

* Test Score: 23987.87 RMSE
* Test Score: 123.022565 MAE
* Test Score: 1.004987 MAPE
##### GRU Model

* Test Score: 24265.39 RMSE
* Test Score: 125.725532 MAE
* Test Score: 1.071244 MAPE

##### Independent RNN Model

* Test Score: 30128.65 RMSE
* Test Score: 131.286369 MAE
* Test Score: 1.120023 MAPE

## Inference
Based on the test scores, it is evident that the LSTM Model was better than the other two models. The error rate is only 1.004% which is quiet good and acceptable 

## References
<a id="1">[1]</a> 
Independently Recurrent Neural Network (IndRNN): Building A Longer and Deeper RNN
(https://arxiv.org/abs/1803.04831)
 
 <a id="2">[2]</a>
 Keras implementation of IndRNN
(https://github.com/titu1994/Keras-IndRNN)
