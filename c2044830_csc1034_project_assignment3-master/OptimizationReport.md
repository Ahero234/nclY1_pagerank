CSC1034 Assignment 3 Optimization Report
========================================
### 1. Replaced for loop with dictionary comprehensions
In both the stochastic and distribution page rank functions, the initialization of the dictionaries (hit_count, node_prob and next_prob) 
have their for loops replaced with dictionary comprehensions. 
- ```hit_count = {node: 0 for node in graph}```
- ```node_prob = {node: 1 / len(graph) for node in graph}```
- ```next_prob = {node: 0 for node in graph}```

This change decreased the calculation time for the stochastic page rank from around 91.32 seconds to less than
67.15 seconds and the distribution page rank from around 0.32 seconds to 0.09 seconds.

### 2. Avoided attribute searches
Made sure that python does not search for a specific function in the module but instead only uses a single function imported from the module. This helped the stochastic page rank estimation 
run faster by only importing the ```choice``` function from the ```random``` module using the ```from random import choice``` statement. 
The calculation time went from 67.15 seconds to 49.18 seconds.

#### Calculations
The calculation time for the stochastic page rank improved by around 46% overall while the distribution page rank improved by 71%.
