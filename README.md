# Self-Driving Car Simulation using NEAT
This repository contains a Python script that simulates a self-driving car using NeuroEvolution of Augmenting Topologies (NEAT) algorithm. NEAT is an evolutionary algorithm that evolves artificial neural networks to control the car's movements in a given environment. The car is trained to navigate a map, avoiding obstacles and staying within the borders.

## How the Script Works
The newcar.py script uses the Pygame library to create a graphical simulation of the self-driving car. The NEAT algorithm is used to evolve the neural network that controls the car's movements. The car is represented as a rectangle sprite that can rotate and move on the map.

The script includes the following key components:

1. Car Class: The Car class represents the self-driving car. It has methods to update the car's position, calculate distances to obstacles (radars), check for collisions with the map boundaries, and more.

2. NEAT Initialization: The script initializes the NEAT algorithm by loading the configuration from the config.txt file and setting up the population of genomes.

3. NEAT Evolution: The main simulation loop runs the NEAT algorithm. Each car in the population is associated with a genome and a neural network. The neural network receives input from the car's sensors (radars) and outputs actions (rotating left or right and adjusting speed). The genomes are evaluated based on the distance the car travels, and the fitness of each genome is updated accordingly.

4. Pygame Visualization: The simulation is displayed using Pygame. The map and car sprites are loaded, and the car's movements and sensor readings are drawn on the screen.

## Required Libraries
The following libraries are required to run the script: PyGame, Neat-Python
## Installation

Install the required libraries using pip. Open a terminal or command prompt and run the following commands:

```
pip install pygame
pip install neat-python
```

## How to Run the Simulation
1. Clone or download this repository to your local machine.

2. Open a terminal or command prompt and navigate to the directory where the newcar.py script is located.

3. Run the script using the following command:
```
python newcar.py
```
4. The simulation will start, and you will see a window showing the map and the self-driving car. The car will start learning to navigate the environment.

5. Wait for the simulation to finish. You can adjust the number of generations in the run_simulation function in the script if needed.

7. Once the simulation is complete, the best performing neural network will be saved in the neat-checkpoint-* file. This network represents the trained self-driving car.

## Controls
During the simulation, the car will learn and navigate on its own without any user input. The NEAT algorithm controls the car's movements.

