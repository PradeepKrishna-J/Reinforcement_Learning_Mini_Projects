# Frozen Lake - Q-Learning

## Overview
Implementation of Q-Learning algorithm on OpenAI Gym's Frozen Lake environment, a classic grid world problem with stochastic dynamics.

## Environment Description
- **Grid**: 4x4 frozen lake
- **States**: Start (S), Frozen (F), Hole (H), Goal (G)
- **Actions**: Left, Down, Right, Up
- **Stochastic**: Ice is slippery - actions have uncertainty
- **Reward**: +1 for reaching goal, 0 otherwise

## Algorithm Used
- **Q-Learning**: Off-policy TD control
- **Temporal Difference**: Learn from each step
- **ε-greedy Exploration**: Gradually decay epsilon
- **Experience Replay**: Optional enhancement

## Key Concepts
- **Q-Table**: Matrix storing Q(s,a) values
- **Temporal Difference Error**: δ = r + γ max Q(s',a') - Q(s,a)
- **Learning Rate α**: Controls update magnitude
- **Discount Factor γ**: Future reward importance
- **Stochastic Environment**: Actions don't always work as intended

## Implementation Details
1. Initialize Q-table with zeros
2. For each episode:
   - Start at initial state
   - While not terminal:
     - Select action using ε-greedy
     - Execute action, observe reward and next state
     - Update: Q(s,a) += α[r + γ max Q(s',a') - Q(s,a)]
     - Decay epsilon
3. Track success rate

## Learning Outcomes
- Q-Learning in stochastic environments
- Handling environment randomness
- Hyperparameter tuning (α, γ, ε)
- Off-policy TD control

## Usage
```python
jupyter notebook frozen_lake_Qlearning.ipynb
```

## Expected Results
- Q-table converges to optimal values
- Success rate increases with training
- Policy handles slippery ice effectively
- Comparison of hyperparameter effects
