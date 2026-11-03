# SVT_research
This repository contains files need to run the simulations of traffic in Zurich city center, including implementation of the traffic signal priority for trams.

## Contained files:
- `merged_fixed.net.xml`: File of the network with fixed-time signal plans
- `merged_actuated.net.xml`: File of the network with actuated signal plans
- `merged.rou.xml`: File containing the network demand
- `DODE.sumocfg`: Template file containing the SUMO configuration
- `DODE_new.add.xml`: Template file containing additional elements
- `config.py`: File defining variables for the simulation
- `model.py`: File containing functions used for implementation of the priority and data processing
- `main_1.py`: Main script

## How to run:
1. Make sure the environment variable '$SUMO_HOME' on your device is set
2. Download or clone the whole repository
3. Set up the `config.py` file with variables that you need. Following variables can be changed:
     - `number`: Number that is used on folders, generated simulation files and output files to differentiate different scenarios.
     - `cooldownTime`: Cooldown duration in seconds
     - `red_min_duration_coefficient`: Minimum phase duration ratio
     - `way`: Priority strategy, 3 options are available:
          - `nopriority`, base case without priority implemented
          - `nspnc`: active priority logic, no compensation mechanism
          - `ǹspc`: active priority logic, with a compensation mechanism
     - `mode`: Traffic signal schedule, either `fixed` or `actuated`
     - `simulationTime`: In-simulation time until when to run the simulation, default value *39600*
     - `seed`: Random seed, used seeds: 23423, 23424, ....5, ....6, ....7
4. After setting up the variables, run the main_1.py either in an IDE or terminal
5. The simulation should be running :) 
6. Two folders are generated, `simulations` containing folders for each separated run, containing modified files used for the simulation. `outputs` contains folders with outputs for each run.
7. The `outputs` folder contains `variables_{number}.csv` which contains the variables used for the particular run.
If you wish to run more simulations, make sure to change the variable `number` in the `config.py` file, otherwise your previous outputs and generated simulation files will be overwritten.
