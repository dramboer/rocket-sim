# Rocket Launch Simulation Project

## Overview

This Python project simulates rocket launches and models the trajectory of rockets over time, factoring in forces like gravity and thrust. The simulation allows users to configure multiple rockets with different parameters such as mass, thrust, and burn time. The resulting rocket trajectories are displayed on a single plot, where altitude is shown in kilometers.

## Features

- **Customizable Rockets**: Users can input mass, engine thrust, burn time, and labels for multiple rockets.
- **Simulation of Rocket Flight**: The simulation computes rocket trajectories considering both thrust and gravitational forces.
- **Multiple Rocket Trajectories**: The simulation supports multiple rockets, each with its own configuration, and displays them on a single plot.
- **Visualization**: The trajectories of rockets are plotted in a single graph with altitude in kilometers and time in seconds. Each rocket has a different color and label.

## Project Structure

```yaml
rocket_sim/
    ├── rocket.py        # Defines the Rocket and Engine classes
    ├── simulation.py    # Contains the RocketSimulation class that handles the simulation logic
    ├── plotter.py       # Responsible for plotting the trajectories using Matplotlib
    ├── main.py          # Entry point of the program
```

## File Descriptions

- **`rocket.py`**: Contains the `Rocket` and `Engine` classes. These represent the physical properties of the rocket, including mass, thrust, and motion. The rocket's position is updated over time using simple kinematic equations.

- **`simulation.py`**: Implements the `RocketSimulation` class, which manages the simulation over time. It runs the simulation for each rocket and stores the altitude and velocity data for plotting.

- **`plotter.py`**: Contains the `Plotter` class, which is responsible for plotting the trajectories of rockets. The `plot_multiple_trajectories` method is used to plot multiple rockets' altitude over time, with the altitude shown in kilometers.

- **`main.py`**: The entry point of the program. It allows users to input multiple rockets' configurations, runs the simulation for each rocket, and then generates a plot of all trajectories.

## Running the Simulation

1. Clone or download the project.

2. Navigate to the project directory:

   ```yaml
   cd rocket_simulation
   ```

3. Make sure you have Python 3 installed, along with the required libraries and virtual environment setup:

   ```yaml
   python3 -m venv env
   source env/bin/activate
   pip install -r requirements.txt
   ```

4. Run the `main.py` file:

   ```yaml
   python3 main.py
   ```

5. Follow the prompts to input the number of rockets and configure each rocket's parameters:

   - Rocket mass (in kg)
   - Engine thrust (in N)
   - Burn time (in seconds)
   - Total simulation time (in seconds)
   - A label to distinguish each rocket's trajectory

6. After inputting the data for all rockets, the simulation will run, and the results will be saved to `sim.png`.

## Example Usage

```yaml
Enter the number of rockets to simulate: 2

Rocket 1 configuration:
Enter the rocket mass (kg): 500
Enter the engine thrust (N): 5000
Enter the engine burn time (seconds): 30
Enter the total simulation time (seconds): 120
Enter a label for this rocket: Rocket 1

Rocket 2 configuration:
Enter the rocket mass (kg): 300
Enter the engine thrust (N): 3500
Enter the engine burn time (seconds): 20
Enter the total simulation time (seconds): 100
Enter a label for this rocket: Rocket 2
```

### Output

The output plot, `sim.png`, will display the altitude (in kilometers) of each rocket over time (in seconds), with a different line and label for each rocket's trajectory.
