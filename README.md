# Vehicle_Routing_Problem using Genetic Algorithm (VRP-GA)
This project demonstrates the use of Genetic Algorithms (GA) to solve a simplified Vehicle Routing Problem (VRP) using Python and the DEAP evolutionary computation framework.

The goal is to efficiently assign a set of delivery locations to multiple vehicles starting and ending at a central depot, optimizing for both minimum total distance traveled and balanced workload across vehicles.

# Problem Description
Given:
 -A depot (fixed central location)
 -A list of randomly generated delivery locations
 -A fleet of vehicles

# The task is to:
  -Distribute the delivery points among the vehicles
  -Ensure each route starts and ends at the depot
  -Minimize the total travel distance
  -Balance the routes across vehicles to avoid overloading

# Technologies Used
  -Python
  -DEAP – for genetic algorithms
  -NumPy – for numerical computations
  -Matplotlib – for plotting and route visualization
  -Random – for generating location coordinates

# How It Works
# Initialization
  -Generate 10 random delivery locations on a 2D plane.
  -Depot is set at coordinate (50, 50).
  -Number of vehicles: 3.

# GA Setup
  Individual: a permutation of delivery locations
  Fitness: (total_distance, route_balance_penalty)
  Crossover: Partial Match Crossover (cxPartialyMatched)
  Mutation: Index shuffling (mutShuffleIndexes)
  Selection: Roulette Wheel Selection (selRoulette)

# Fitness Function
  - Calculates the total distance for each vehicle's route.
  - Computes the standard deviation of distances for route balance.
  - Objective: Minimize both total distance and imbalance.

# Output
  -Route for each vehicle is plotted with matplotlib.
  -Best individual is stored in Hall of Fame.

