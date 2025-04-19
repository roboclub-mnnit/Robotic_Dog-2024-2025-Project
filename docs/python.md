
# Robotic Dog Python Simulations

This folder contains Python scripts for simulating and calculating the kinematics of a four-legged robotic dog. The scripts provide 3D visualizations and inverse kinematics calculations for leg movements, using interactive tools to adjust joint angles.

## Files

- `InverseKinematics.py`: Computes joint angles (T1, T2, T3) for left and right legs based on (x, y, z) inputs.
- `4-Legs-Simulation.py`: Simulates all four legs with sliders for angle adjustments and a chassis model.
- `Right-Leg-Simulation.py`: Visualizes a single right leg with interactive angle controls.
- `Left-Leg-Simulation.py`: Visualizes a single left leg with interactive angle controls.

## Dependencies

- Python 3.x
- `numpy` (for matrix operations)
- `matplotlib` (for 3D plotting and widgets)

## Installation

1. Install Python 3.x from python.org.
2. Install dependencies:
   ```bash
   pip install numpy matplotlib
   ```
3. Run scripts from this folder.

## Usage

- **InverseKinematics.py**: 
  - Run: `python InverseKinematics.py`
  - Input leg (0 for right, 1 for left) and coordinates (x, y, z) to get angles.
- **4-Legs-Simulation.py**: 
  - Run: `python 4-Legs-Simulation.py`
  - Use sliders to adjust T1, T2, T3 for each leg; click XY, YZ, XZ buttons to change views.
- **Right-Leg-Simulation.py**: 
  - Run: `python Right-Leg-Simulation.py`
  - Adjust T1 (-90° to 90°), T2 (0° to 180°), T3 (0° to 180°) with sliders.
- **Left-Leg-Simulation.py**: 
  - Run: `python Left-Leg-Simulation.py`
  - Adjust T1 (90° to 270°), T2 (0° to 180°), T3 (0° to 180°) with sliders.

## Kinematics

- Segment lengths: a1=4.5 cm, a2=6 cm, a3=5.4 cm (InverseKinematics); a1=5 cm, a2=6 cm, a3=5.5 cm (Simulations).
- Offsets: ±1 cm (x), ±8.5 cm (z) for four-leg simulation.
- Angles in degrees, calculated using transformation matrices.

## Notes

- Simulations display end effector coordinates.
- Ensure inputs are within the workspace (L ≤ a1 + a2 + a3).
