# changi-airport-taxiway-planning
We want to solve the coupled routing and timing optimization problem in taxiway planning. There are many individual constraints such as push-back times, taxiway layouts, and separation rules all requiring considerations. The dynamic nature of this problem requires planning to be updated regularly. We propose to formulate the optimization problem in a Receding Horizon scheme, meaning that a plan is implemented in small execution horizons, before re-planning occurs.   We will have Changi Airport surface modelled as a graph containing nodes, each representing a junction of taxiways. We will construct the connectivity and distance matrix between nodes. Active aircrafts are then modelled as points moving along the arcs, subject to speed limit. Each aircraft moves from its origin node to its destination node, while observing taxiway rules.   The decision variables are therefore  1) the node at which an aircraft begins its kth move  2) the time at which an aircraft starts its kth move.   The objective is to minimize a weighted combination of total taxi time of all aircrafts and their total taxi distance. We will use Mixed Integer Linear Programming and CPLEX to solve the optimization problem.     As taxiway planning is coupled with runway scheduling and other operations, we made assumptions to simplify the problem in order to define a realistic scope given the time constraint. 