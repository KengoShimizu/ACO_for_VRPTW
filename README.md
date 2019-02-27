# ACO_for_VRPTW
This code is written in JAVA, and this Ant Colony Optimization (ACO) method is written for solving VRPTW.  
To solve VRPTW, this code loads a txt file from [Solomon benchmark](https://www.sintef.no/projectweb/top/vrptw/solomon-benchmark/).

&emsp; Procedure of this ACO (**Ant_colony_opt.java**):  
&emsp; &emsp; initialize pheromone using NN method (**Nearest_neighbor_heuristic.java**)  
&emsp; &emsp; loop until meet a stop criterion{  
&emsp; &emsp; &emsp; for each <img src="https://latex.codecogs.com/gif.latex?k&space;\in&space;\{1,2,...,m\}" />(<img src="https://latex.codecogs.com/gif.latex?m" /> is the number of ant){  
&emsp; &emsp; &emsp; &emsp; ant <img src="https://latex.codecogs.com/gif.latex?k" /> constructs solution <img src="https://latex.codecogs.com/gif.latex?\psi&space;^k" /> (**Build_tour.java**)  
&emsp; &emsp; &emsp; &emsp; if <img src="https://latex.codecogs.com/gif.latex?\psi&space;^k" /> is non-deminated solution{  
&emsp; &emsp; &emsp; &emsp; &emsp; <img src="https://latex.codecogs.com/gif.latex?P&space;=&space;P&space;\cup&space;\psi&space;^k" /> (<img src="https://latex.codecogs.com/gif.latex?P" /> is Pareto optimal set)  
&emsp; &emsp; &emsp; &emsp; }  
&emsp; &emsp; &emsp; }  
&emsp; &emsp; &emsp; if <img src="https://latex.codecogs.com/gif.latex?P" /> does NOT improve{  
&emsp; &emsp; &emsp; &emsp; perform global pheromone update  
&emsp; &emsp; &emsp; &emsp; }  
&emsp; &emsp; }  
  
The detail of this code is written in the paper.
