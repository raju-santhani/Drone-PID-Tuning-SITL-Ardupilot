# PID Tuning of Heavy-Payload Drones

### MATLAB/Simulink | ArduPilot SITL | Flight Control

**Model-Based PID Tuning and Simulation-to-Real Flight Validation**

## Project Overview

This project focuses on model-based PID tuning for a heavy-payload multirotor UAV with a payload capacity of 150 kg.

A physics-based drone model was developed in MATLAB/Simulink, incorporating aircraft mass, propulsion characteristics, and flight dynamics. The model was integrated with ArduPilot Software-In-The-Loop (SITL) to evaluate and tune PID controller gains before real-world flight testing.

The simulation-derived gains were used as initial controller parameters on the actual UAV, followed by flight-based fine-tuning to achieve stable autonomous flight.

## Project Objectives

- Develop a physics-based simulation model of a heavy-payload drone.
- Integrate MATLAB/Simulink with ArduPilot SITL.
- Tune PID gains in simulation before real-world testing.
- Reduce trial-and-error tuning and initial flight-test risks.
- Validate simulation-derived PID gains through actual flight testing.

## 1. Drone Physical Modelling

Developed a MATLAB-based physical model incorporating:

- Aircraft mass and inertia characteristics.
- Motor and propeller thrust characteristics.
- Aircraft translational and rotational dynamics.
- Control inputs and vehicle response.

The drone's physical model parameters were implemented in `hexsoon.mat`.

## 2. MATLAB/Simulink and ArduPilot SITL Integration

The simulation environment was configured using the ArduPilot JSON interface for MATLAB/Simulink.

**Implementation workflow:**

1. Cloned the ArduPilot repository in Windows and used the MATLAB Copter example as the starting point.
2. Configured Windows Subsystem for Linux (WSL).
3. Cloned ArduPilot in Linux and installed the required dependencies.
4. Launched ArduCopter SITL using the JSON simulation interface.
5. Connected Mission Planner on Windows through UDP port 14550.
6. Performed simulated flight tests and PID controller tuning.

**References:**

- [ArduPilot MATLAB Copter JSON Example](https://github.com/ArduPilot/ardupilot/tree/master/libraries/SITL/examples/JSON/MATLAB/Copter)
- [ArduPilot SITL Setup Documentation](https://ardupilot.org/dev/docs/sitl-simulator-software-in-the-loop.html)

## 3. PID Controller Tuning

The drone's physical model was used to evaluate flight response and tune PID controller gains in the simulation environment.

The simulation-based approach enabled controller evaluation before applying the gains to the actual heavy-payload UAV.

## 4. Real-World Flight Validation

The tuned PID gains obtained from simulation were used as initial values on the physical drone.

Further flight-based adjustments were performed to achieve stable autonomous flight.

## Project Results

- Developed a physics-based model for a 150 kg-payload UAV.
- Integrated MATLAB/Simulink with ArduPilot SITL.
- Validated simulation-derived PID gains through real-world flight testing.
- Achieved stable autonomous flight following controller fine-tuning.
- Saved approximately 20 hours of manual tuning effort.
- Reduced exposure to risky initial trial-and-error flight tests.

## Tools and Technologies

- **Physical Modelling:** MATLAB/Simulink
- **Flight Controller:** ArduPilot / ArduCopter
- **Simulation:** ArduPilot SITL, JSON Interface
- **Ground Control Station:** Mission Planner
- **Development Environment:** Windows, WSL, Linux
- **Control:** PID Tuning and Flight Dynamics

## Author

**Raju Santhani**  
IIT Hyderabad
