# Task 4.4 bonus

## Task 1
### Create network with 2 or mo routers

[link](https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/tree/master/m4/task4.2) for newtwork (network 3)

## Task 2
### Create network with dns

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m4/task4.4/screenshotsh/topology.png" witdh="50%">

### Set IP for PC

PC|IP|GateWay|DNS
--|--|-------|---
PC0|192.168.1.1|192.168.1.100|192.168.1.254
PC1|192.168.1.2|192.168.1.100|192.168.1.254
PC2|192.168.0.1|192.168.0.100|192.168.0.254
PC3|192.168.0.2|192.168.0.100|192.168.0.254
Server0|192.168.1.254|192.168.1.100|0.0.0.0
Server1|192.168.0.254|192.168.0.100|0.0.0.0

### Set DNS address for server0 and server1

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m4/task4.4/screenshotsh/dns_config.png" witdh="50%">

### Request to the server from 2 subnets

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m4/task4.4/screenshotsh/check_dns.png" witdh="50%">

### Check connection 

<img src="https://github.com/vlddryga2233/DevOps_online_Kyiv_2020_Q42021Q1/blob/master/m4/task4.4/screenshotsh/ping%20network.png" witdh="50%">

