# Simple Monte Carlo Decay Chain Simulation
This Juypter notebook project was completed for PHYS 115(computational physics course). Within the notebook I go over the process of developing my simulation, then testing my simulation on Helium 8(smaller none transuranic radioisotope), before running it on Plutonium 238, 239, and 240 and doing an analysis.

## Running
1. Open it in an IDE that supports notebooks
2. make sure you are using Python 3.7 or later due to the difference in how the dictionary data structure works, which will only work properly in 3.7+
3. Run the cell that defines the library and the cell with the simulation before running any of the decay simulations
4. To run their own simulation, the user must define a decaying tree using a dictionary, with the first item being the starting isotope, and each isotope must have their decay products defined with their respective probability of occurring
   

## Issues
- The model is incredibly poorly optimized, due to the structure of how data is stored and operations are completed on the data
- There is a serious flaw with the run time, due to the complexity of the decay chains with varying decay times meaning that if I wanted to get everything my time step would be
- incredibly small and the period would have to be incredibly long, resulting in ridiculously long run times
- If diagrams of decay chains were viewed it could be observed I chose isotopes whose probability of being decayed is at least 1%(something that I noted within the notebook), this choice was partially due to the difficulty and inconsistency in finding accurate stats and information on certain decay products but also due to floating point calculations would become an issue with the incredibly small probabilities
