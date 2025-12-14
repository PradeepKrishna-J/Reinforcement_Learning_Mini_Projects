# Recycling Robot

## Overview
Classic MDP example modeling a mobile robot that collects recyclable items. Demonstrates MDP formulation, state transitions, and decision-making under uncertainty.

## Problem Description
- **Robot States**: High battery, Low battery
- **Actions**: 
  - Search: Look for cans (energy-intensive)
  - Wait: Stay in place (low energy)
  - Recharge: Go to charging station
- **Rewards**: +1 for each can collected, 0 for waiting
- **Battery Dynamics**: Stochastic depletion based on actions
- **Rescue State**: Risk of complete battery drain

## MDP Formulation

### States
- **High**: Sufficient battery for search
- **Low**: Limited battery, risky to search

### Actions
- **Search (in High)**: High reward probability, depletes battery
- **Search (in Low)**: Lower reward, high risk of depletion
- **Wait**: Safe, no reward
- **Recharge**: Return to High state

### Transition Probabilities
- P(High | High, Search) = α
- P(Low | High, Search) = 1-α
- P(High | Low, Search) = β (low)
- P(Low | Low, Recharge) = 1
- Stochastic outcomes based on battery usage

## Algorithm Used
- **Policy Evaluation**: Calculate value of given policies
- **Value Iteration**: Find optimal policy
- **Policy Iteration**: Alternative optimization approach

## Key Concepts
- **Trade-offs**: Risk vs reward in decision making
- **State-Dependent Actions**: Different options in different states
- **Expected Utility**: Balancing immediate and future rewards
- **Conservative vs Aggressive**: Safe waiting vs risky searching

## Implementation Details
1. Define MDP parameters (states, actions, transitions, rewards)
2. Implement policy evaluation for fixed policies
3. Apply value iteration to find optimal policy
4. Compare different policies:
   - Always search
   - Always wait when low
   - Optimal policy
5. Visualize value functions and policies

## Learning Outcomes
- MDP modeling of real problems
- Risk-reward trade-offs in RL
- Impact of discount factor on policy
- Comparing multiple policies
- Understanding state-dependent decisions

## Usage
```python
jupyter notebook Recycling_Robot.ipynb
```

## Expected Results
- Optimal policy balances risk and reward
- Value functions for different battery states
- Policy comparison showing performance
- Sensitivity analysis on parameters
