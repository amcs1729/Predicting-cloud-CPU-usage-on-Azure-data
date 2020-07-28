# Predicting Microsoft Azure cloud VM CPU Usage
## Project Name
Predicting Microsoft Azure cloud VM CPU Usage

## Objective
Predicting the CPU usage of cloud VM using data from the past.
## Why this might be worth considering?
Well, Cloud services are becoming increasingly popular day by day.  Server racks can be split between multiple users, with each user having anisolated sandbox (a virtual machine) for their application.A user can even have an application running across multiple VMs on separate machines.\ 
 \
 
**Proactively allocating VMs can increase usage efficiency of underlying resources. If a computing cluster predicts the future resource usage of a user service will increase, it can preemptively scale up to accommodate a higher load. If it predicts that usage will decrease, it can deallocate VMs and save computing resources. **

## Dataset
The Dataset contains the CPU Usage data of Microsoft Azure, which is a cloud service, samoled every 5 minutes. The data has three attributes - \
* Max CPU Utilization
* Average CPU Utilization
* Minimum CPU Utilization

A glimpse into the data -




## References
<a id="1">[1]</a> 
Independently Recurrent Neural Network (IndRNN): Building A Longer and Deeper RNN
(https://arxiv.org/abs/1803.04831)
 
 <a id="2">[2]</a>
 Keras implementation of IndRNN
(https://github.com/titu1994/Keras-IndRNN)
