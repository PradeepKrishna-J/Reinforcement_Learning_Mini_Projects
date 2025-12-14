# Gambler's Problem

## Overview
Classic dynamic programming problem from Sutton & Barto. A gambler bets on coin flips to reach a goal amount, demonstrating value iteration for finite MDPs.

## Problem Description
- **Initial Capital**: $0 to $100
- **Goal**: Reach $100 (win)
- **Actions**: Bet any amount from $1 to min(capital, 100-capital)
- **Coin**: Probability p of heads (typically p=0.4)
- **Win**: Get bet amount added
- **Lose**: Lose bet amount
- **Terminal States**: $0 (lose) or $100 (win)

## Algorithm Used
- **Value Iteration**: Dynamic programming for optimal policy
- **Bellman Optimality Equation**: V*(s) = max_a E[r + γV*(s')]
- **Iterative Updates**: Sweep through state space
- **Convergence**: Until values stabilize

## Key Concepts
- **Finite MDP**: Discrete states and actions
- **Value Function**: Expected return from each capital level
- **Optimal Policy**: Best betting strategy
- **Risk Management**: Balancing bet sizes
- **Convergence Guarantee**: Value iteration converges to optimal

## Implementation Details
1. Initialize value function V(s) = 0 for all states
2. Repeat until convergence:
   - For each state (capital):
     - For each possible action (bet):
       - Calculate expected value
       - Track maximum
     - Update V(s)
3. Extract policy: argmax over actions
4. Visualize value function and policy

## Learning Outcomes
- Value iteration algorithm
- Dynamic programming principles
- Optimal decision making under uncertainty
- Policy extraction from value function
- Understanding convergence criteria

## Usage
```python
jupyter notebook gamblers_problem.ipynb
```

## Expected Results
- Value function showing expected probability of winning
- Optimal betting policy (often aggressive bets)
- Visualization of how policy changes with capital
- Convergence plots showing iterations
