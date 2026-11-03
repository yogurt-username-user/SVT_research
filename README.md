# SVT_research
This repository contains files need to run the simulations of traffic in Zurich city center, including implementation of the traffic signal priority for trams.

## Contained files:
- 'merged_fixed.net.xml': File of the network with fixed-time signal plans
- 'merged_actuated.net.xml': File of the network with actuated signal plans
- 'merged.rou.xml': File containing the network demand
- 'DODE.sumocfg': Template file containing the SUMO configuration
- 'DODE_new.add.xml': Template file containing additional elements
- 'config.py': File defining variables for the simulation
- 'model.py': File containing functions used for implementation of the priority and data processing
- 'main_1.py': Main script

## How to run:
1. Make sure the environment variable '$SUMO_HOME' is set
2. Set up the 'config.py' file with variables that you need. Following variables can be changed:
     - '
