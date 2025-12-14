# 5x5 Grid World - Optimal Policy

## Overview
This project implements finding the optimal policy for a 5x5 grid world environment using dynamic programming methods.

## Environment Description
- **State Space**: 25 states (5x5 grid)
- **Actions**: Up, Down, Left, Right
- **Goal**: Navigate from start position to goal position
- **Rewards**: Negative reward for each step, positive reward at goal

## Algorithm Used
- **Dynamic Programming**: Policy Iteration or Value Iteration
- Iteratively improves the value function
- Extracts optimal policy from converged value function

## Key Concepts
- **State Value Function V(s)**: Expected return from each state
- **Policy π(a|s)**: Probability of taking action a in state s
- **Bellman Equation**: Recursive relationship for value functions
- **Convergence**: Policy stabilizes when no improvements possible

## Implementation Details
1. Initialize value function and policy
2. Policy Evaluation: Calculate V(s) for current policy
3. Policy Improvement: Update policy greedily
4. Repeat until convergence
5. Visualize optimal policy with arrows

## Learning Outcomes
- Understanding grid world environments
- Dynamic programming for MDP solutions
- Policy iteration vs value iteration
- Visualization of optimal policies

## Usage
```python
jupyter notebook "5X5grid_world(optimal policy).ipynb"
```

## Expected Results
- Optimal value function for each state
- Optimal policy showing best action per state
- Visualization of policy with directional arrows
