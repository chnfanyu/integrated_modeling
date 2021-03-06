# Braess network
## Concepts

Braess' paradox is the observation that adding one or more roads to a road network can slow down overall traffic flow through it. The paradox was postulated in 1968 by German mathematician Dietrich Braess, who noticed that adding a road to a particular congested road traffic network would increase overall journey time.

<img src="https://github.com/chnfanyu/integrated_modeling/blob/main/dataset/02_Braess_Paradox/img/Capture.PNG" width="320" height="200"> Original network
<img src="https://github.com/chnfanyu/integrated_modeling/blob/main/dataset/02_Braess_Paradox/img/Capture1.PNG" width="320" height="200"> Modified network

## Contents
#### Input files:
 - `node.csv`  Node  
 - `link.csv`  Link
 - `demand.csv`  Demand  
 - `settings.csv`  Simulation settings
#### Output files:
 - `agent.csv`  Path performance   
 - `link_performance.csv`  Link performance 

## Network dimensions 

| | Original Network | Modified Network 
------------ | ------------- | ------------- 
Zones | 2 | 2 
Nodes | 4 | 4 
Links | 4 | 5 
Paths | 2 | 3 


## Network parameters 

Parameters | Link a & b | Link c & d | Link e
------------ | ------------- | ------------- | -------------
Free flow travel time| 1 | 45 | 0.01
Lane capacity | 100 | 1900 | 1900
Number of Lane | 1 | 3 | 3
BPR alpha | 1 | 0 | 0.15
BPR beta | 1 | 0 | 4


## Modeling summary 

<img src="https://github.com/chnfanyu/integrated_modeling/blob/main/dataset/02_Braess_Paradox/img/Capture2.PNG" width="450" height="250">

#### Overall system statistics summary

| | Original Network | Modified Network 
------------ | ------------- | ------------- 
Total number of vehicles | 4000 | 4000 
System-wide total travel time | 264,080 | 328,084 
Average travel time for each vehicle | 66 | 82 

#### Path performance 

| | Original Network | Modified Network 
------------ | ------------- | ------------- 
Path 1 volume | 2004 | 0 
Path 1 travel time | 66.06 | 0 
Path 2 volume | 1996 | 0 
Path 2 travel time | 65.98 | 0 
Path 3 volume | 0 | 82.2 
Path 3 travel time | 0 | 4000


#### Link performance 

| |Original Network | Modified Network 
------------ | ------------- | ------------- 
Link a volume | 2004 | 4000
Link a travel time | 21.04 | 41 
Link b volume | 1996 | 4000
Link b travel time | 20.96 | 41 
Link c volume | 1996 | 0
Link c travel time | 45 | 0
Link d volume | 2004 | 0
Link d travel time | 45 | 0
Link e volume | - - | 4000
Link e travel time | - - | 0.001
