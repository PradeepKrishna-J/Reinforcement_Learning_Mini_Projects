# Jack's Car Rental - Value Iteration

## Overview
Alternative solution to Jack's Car Rental using value iteration instead of policy iteration. Compares efficiency and convergence properties of both dynamic programming methods.

## Problem Description
Same as policy iteration version:
- Two rental locations with stochastic demand
- Move cars overnight to optimize availability
- Maximize rental revenue minus moving costs
- Poisson-distributed requests and returns

## Algorithm Used
- **Value Iteration**: Direct optimization of value function
- **Bellman Optimality Operator**: Combine evaluation and improvement
- **Single Sweep**: Update values by maximizing over actions
- **Policy Extraction**: Derive policy from converged values

## Key Concepts
- **Value Iteration vs Policy Iteration**: Comparison of approaches
- **Computational Efficiency**: Fewer policy evaluation sweeps
- **Convergence**: Guaranteed to optimal value function
- **Implicit Policy**: No explicit policy until end
- **Stopping Criterion**: δ < θ for value changes

## Implementation Details
1. Initialize V(s) arbitrarily (e.g., zeros)
2. Repeat until convergence:
   - For each state:
     - Calculate Q(s,a) for all actions
     - V(s) = max_a Q(s,a)
     - Track maximum change δ
3. Extract greedy policy: π(s) = argmax_a Q(s,a)
4. Visualize final policy and values

## Learning Outcomes
- Value iteration mechanics
- Efficiency comparison with policy iteration
- When to choose value vs policy iteration
- Convergence properties
- Same optimal solution, different path

## Usage
```python
jupyter notebook "Jacks'_Car_Rental_value_iteration.ipynb"
```

## Expected Results
- Same optimal policy as policy iteration
- Potentially faster convergence
- Value function showing expected profits
- Comparison metrics with policy iteration
