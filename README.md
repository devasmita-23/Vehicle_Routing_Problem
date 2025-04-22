## 2. Vehicle Routing Problem using Genetic Algorithm (VRP-GA)

Solves a simplified version of the VRP using evolutionary algorithms with route balancing.

###  Technologies Used

- Python
- DEAP (Genetic Algorithm)
- NumPy
- Matplotlib

###  Problem Setup

- **Depot**: `[50, 50]`  
- **Locations**: 10 randomly generated (x, y) coordinates  
- **Vehicles**: 3

###  Genetic Algorithm Steps

1. **Population Representation**  
   - Each individual is a permutation of delivery locations

2. **Fitness Function**  
   - Minimizes total distance  
   - Penalizes route imbalance using standard deviation across vehicle routes

3. **Genetic Operators**
   - **Crossover**: `cxPartialyMatched`
   - **Mutation**: `mutShuffleIndexes`
   - **Selection**: `selRoulette`

###  Visualization

- Each vehicle's route is plotted starting and ending at the depot
- Shows optimal route balancing across the fleet
