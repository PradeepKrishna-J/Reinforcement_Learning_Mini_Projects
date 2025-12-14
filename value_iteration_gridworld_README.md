# Value Iteration - Grid World

## Overview
Implementation of value iteration algorithm on a grid world environment. Demonstrates how value iteration finds optimal policies through iterative value function updates.

## Environment Description
- **Grid Size**: Configurable (e.g., 4×4 or 5×5)
- **Start State**: Typically top-left corner
- **Goal State**: Typically bottom-right corner
- **Obstacles**: Optional walls or blocked cells
- **Actions**: Up, Down, Left, Right
- **Rewards**: 
  - Large positive at goal
  - Negative per step (encourages efficiency)
  - Large negative for obstacles (if any)

## Algorithm Used
- **Value Iteration**: Direct computation of optimal value function
- **Bellman Optimality Equation**: V*(s) = max_a E[r + γV*(s')]
- **Synchronous Updates**: Update all states each iteration
- **Convergence**: Stop when max value change < threshold

## Key Concepts
- **Value Function V(s)**: Maximum expected return from state s
- **Q-Values Q(s,a)**: Expected return for taking action a in state s
- **Optimal Policy**: Greedy policy w.r.t. optimal value function
- **Discount Factor γ**: Controls horizon of planning
- **Convergence Guarantee**: Contraction mapping theorem

## Implementation Details
1. Initialize V(s) = 0 for all states
2. Repeat until convergence:
   - For each state s:
     - For each action a:
       - Calculate expected value considering:
         - Immediate reward
         - Discounted value of next states
         - Transition probabilities
     - V(s) = max_a expected_value(s,a)
   - Track maximum change δ
3. Extract policy: π(s) = argmax_a expected_value(s,a)
4. Visualize:
   - Value function heatmap
   - Policy arrows
   - Convergence plot

## Learning Outcomes
- Value iteration mechanics
- Optimal value function properties
- Policy extraction from values
- Impact of discount factor
- Visualization techniques for policies

## Visualization
- **Value Heatmap**: Color-coded state values
- **Policy Arrows**: Optimal action per state
- **Convergence Curve**: Value changes over iterations
- **Optimal Path**: Trajectory from start to goal

## Usage
```python
jupyter notebook value_iteration_Grid_world.ipynb
```

## Expected Results
- Values decrease with distance from goal
- Policy points toward goal from all states
- Convergence in relatively few iterations
- Clear visualization of optimal paths
- Understanding of value propagation
