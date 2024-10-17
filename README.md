# Quantum Traffic Signal Management System

This project implements a Quantum Traffic Signal Management System using Variational Quantum Classifier (VQC) and quantum circuit optimization (QAOA) to manage traffic at intersections. The system accounts for factors like incoming traffic, congestion levels, and emergency vehicle prioritization. It uses a quantum machine learning model to predict signal states and dynamically optimize routes based on real-time data.

## Features
- **Traffic Prediction**: Predicts signal state (green/red) using VQC.
- **Route Optimization**: Uses QAOA to determine optimal vehicle routes.
- **Emergency Vehicle Priority**: Prioritizes routes for emergency vehicles.
- **Real-time Updates**: Simulates traffic updates at signals.

## Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/your-repo/quantum-traffic-system.git
    ```
2. create a virtual environment to install the dependancies
   ```back
   virtualenv prep_a_thon
   ```
    Activate the virtualenv
   ```bash
   source prep_a_thon/bin/activate
   ```
4. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage
1. Generate traffic data and train the VQC model for traffic signal predictions.
2. Run the system with dynamic traffic updates and simulate route optimization for vehicles, including emergency vehicle priority handling.

```python
from quantum_traffic_system import QuantumGPSManagementSystem, MockRoadNetwork

# Initialize road network and traffic data
road_network = MockRoadNetwork()
traffic_data = {...}  # Example traffic data
traffic_light_data = {...}  # Example traffic light data

# Initialize Quantum Traffic System
traffic_system = QuantumGPSManagementSystem(road_network, traffic_data, source='A', destination='E', traffic_light_data=traffic_light_data)

# Simulate and get optimized traffic routes
traffic_system.run_simulation()
```
3. Tutorial for this implementation is simulated in the Quantum-traffic-management.ipynb file.

## Data
The project uses simulated traffic data with the following structure:
- **Incoming Traffic**: Vehicle count approaching the signal.
- **Congestion Level**: Measures the level of congestion at the intersection.
- **Number of Outgoing Lanes**: Represents the number of available lanes for vehicles to exit.
- **Traffic Distribution**: Proportion of vehicles expected to take specific outgoing routes.

## Dependencies
- Python 3.x
- Qiskit
- NumPy
- Networkx

## Contributions
Feel free to submit issues and pull requests to improve the project.

