# Cliff Walking - Off-Policy Q-Learning

## Overview
Demonstrates the difference between on-policy (SARSA) and off-policy (Q-Learning) methods in a cliff walking environment where falling off the cliff results in large negative rewards.

## Environment Description
- **Grid**: 4x12 grid world with cliff along bottom row
- **Start**: Bottom-left corner
- **Goal**: Bottom-right corner
- **Cliff**: Bottom row (except start and goal)
- **Reward**: -1 per step, -100 for falling off cliff

## Algorithm Used
- **Q-Learning (Off-Policy)**: Learns optimal policy while following exploratory policy
- **Temporal Difference Learning**: Updates after each step
- **ε-greedy Exploration**: For behavior policy
- **Greedy Target**: Target policy is greedy w.r.t. Q

## Key Concepts
- **Off-Policy Learning**: Behavior policy ≠ target policy
- **Q-Learning Update**: Q(s,a) ← Q(s,a) + α[r + γ max Q(s',a') - Q(s,a)]
- **Optimal Path vs Safe Path**: Q-learning finds risky optimal path
- **Comparison with SARSA**: Different paths due to on/off-policy

## Implementation Details
1. Initialize Q(s,a) for all state-action pairs
2. For each episode:
   - Choose action using ε-greedy
   - Take action, observe reward and next state
   - Update Q using max over next actions
3. Track rewards per episode
4. Visualize learned policy

## Learning Outcomes
- Understanding off-policy learning
- Q-Learning algorithm mechanics
- Risk-seeking behavior of Q-Learning
- Comparison of TD methods

## Usage
```python
jupyter notebook "cliff walking_offpolicy_qlearning.ipynb"
```

## Expected Results
- Q-Learning finds path close to cliff (optimal but risky)
- Convergence to optimal Q-values
- Episode rewards improve over time
- Visual comparison of learned path
