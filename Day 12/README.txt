Problem seems to be similar to a typical Travelling Salesman problem and is modelled as such.
There are two different solutions. One modelled in pyomo and solved using Gurobi and one using Google OR-tools.

For the one modelled in pyomo, sub-tour elimination  is done by adding a dummy 'time' variable. 
Excludingtime taken to generate model, time taken to solve for Gurobi version 11.0.3 is 2 mins.
Intrestingly, both HiGHS and CPLEX is unable to solve in 3 mins, but able to find best bounds of 2720

Optimal solution found by Gurobi is 2720.

As the problem is similar as TSP, I have copied the TSP example off Google OR-tools (https://developers.google.com/optimization/routing/tsp) to run and see how it goes.

Optimal Route found by OR-tools is 2763. Time taken is 7-8 seconds.

As I am not familiar with OR-tools, I am not sure why the 2 values found is different. I am open to feedback about this issue.
