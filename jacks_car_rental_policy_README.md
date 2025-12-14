# Jack's Car Rental - Policy Iteration

## Overview
Classic example of policy iteration algorithm applied to Jack's car rental business problem. Demonstrates dynamic programming for continuous state-action spaces with Poisson distributions.

## Problem Description
- **Two Locations**: Jack manages two rental locations
- **Daily Dynamics**: Cars rented and returned (Poisson distributed)
- **Actions**: Move up to 5 cars between locations overnight
- **Revenue**: $10 per rental
- **Cost**: $2 per car moved
- **Capacity**: Maximum 20 cars per location
- **Goal**: Maximize long-term profit

## Algorithm Used
- **Policy Iteration**: Alternate between policy evaluation and improvement
- **Policy Evaluation**: Solve Bellman equation for current policy
- **Policy Improvement**: Update policy greedily
- **Expected Returns**: Handle Poisson distributions

## Key Concepts
- **Stochastic Demand**: Rental requests follow Poisson(λ)
- **Stochastic Returns**: Car returns follow Poisson(λ)
- **State Space**: (cars at location 1, cars at location 2)
- **Action Space**: -5 to +5 (moves between locations)
- **Policy Representation**: Table mapping states to actions
- **Value Function**: Expected cumulative reward

## Implementation Details
1. Initialize policy arbitrarily (e.g., no moves)
2. Policy Evaluation:
   - Iteratively solve V^π(s) using Bellman equation
   - Handle Poisson probabilities for requests/returns
   - Consider all possible outcomes
3. Policy Improvement:
   - For each state, find action maximizing expected return
   - Update policy if improvement found
4. Repeat until policy stable
5. Visualize policy as heatmap

## Learning Outcomes
- Policy iteration algorithm
- Handling Poisson distributions in RL
- Large state-space problems
- Optimal resource allocation
- Visualization of multi-dimensional policies

## Usage
```python
jupyter notebook "Jacks'_Car_Rental_Policy_iteration.ipynb"
```

## Expected Results
- Optimal car movement policy
- Value function showing expected profits
- Policy converges in few iterations
- Asymmetric policy based on demand differences
