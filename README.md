# RLBellmanEquation
Value Iteration algorithm for a 4x4 Grid World problem using Bellman Equation
# Grid World Value Iteration

This repository contains a Jupyter notebook implementation of the Value Iteration algorithm for a 4x4 Grid World problem.

## Description

The notebook `new_grid.ipynb` implements a value iteration algorithm for solving a Grid World problem with the following specifications:

- 4x4 grid where an agent starts at the top-left corner
- Goal is to reach the bottom-right corner (terminal state)
- Actions: Up, Down, Left, Right (equal probability)
- Rewards: -1 for each move, 0 for reaching the terminal state
- Discount factor (gamma) = 1.0
- Convergence threshold = 1e-4

## Requirements

- Python 3.x
- NumPy
- Jupyter Notebook

To install the required packages:
```bash
pip install numpy jupyter
```

## Usage

1. Clone the repository
2. Launch Jupyter Notebook:
```bash
jupyter notebook
```
3. Open `new_grid.ipynb`
4. Run the cells in sequence

## Features

- **Value Iteration Implementation**: Complete implementation of the value iteration algorithm
- **File Logging**: Detailed logging of iterations to `output.txt`
- **State Value Tracking**: Tracks and displays:
  - Position in grid
  - New and old values for each state
  - Delta (change in values)
  - Convergence information

## Output Files

- `output.txt`: Contains detailed iteration logs
- `grid.txt`: Contains grid state information

## Functions

### `print_to_file(content, filename="output.txt", mode="a")`
- Writes content to a specified file
- Handles both numpy arrays and regular content
- Parameters:
  - `content`: Content to write
  - `filename`: Output file name (default: "output.txt")
  - `mode`: File opening mode (default: append)

### `value_iteration(grid_size=4, gamma=1.0, theta=1e-4)`
- Implements the value iteration algorithm
- Parameters:
  - `grid_size`: Size of the grid (default: 4)
  - `gamma`: Discount factor (default: 1.0)
  - `theta`: Convergence threshold (default: 1e-4)
- Returns:
  - Optimal value function matrix

## Results

The notebook outputs:
- Final value function matrix
- Detailed iteration logs in output.txt
- State values showing the optimal path to the goal

## Example Output

```python
Final Value Function:
[[-59.42367735 -57.42387125 -54.2813141  -51.71012579]
 [-57.42387125 -54.56699476 -49.71029394 -45.13926711]
 [-54.2813141  -49.71029394 -40.85391609 -29.99766609]
 [-51.71012579 -45.13926711 -29.99766609   0.        ]]
```

## Notes

- The values represent the expected cumulative reward from each state
- More negative values indicate states further from the goal
- The optimal path can be traced by following increasing values

## Contributing

Feel free to submit issues and enhancement requests!

## License

This project is open source and available under the [MIT License](LICENSE). 
