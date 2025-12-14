# Frozen Lake - SARSA

## Overview
Implementation of SARSA (State-Action-Reward-State-Action), an on-policy TD control algorithm, applied to the Frozen Lake environment.

## Environment Description
- **Grid**: 4x4 frozen lake with slippery ice
- **Objective**: Navigate from start to goal avoiding holes
- **Stochastic Actions**: Intended action succeeds only part of the time
- **Sparse Rewards**: Only at goal state

## Algorithm Used
- **SARSA**: On-policy TD control algorithm
- **On-Policy Learning**: Learns value of policy being followed
- **ε-greedy Policy**: For exploration
- **Bootstrapping**: Updates use estimated values

## Key Concepts
- **SARSA Update**: Q(s,a) ← Q(s,a) + α[r + γQ(s',a') - Q(s,a)]
- **On-Policy**: Learns about policy it's executing
- **Action Selection**: Next action chosen by current policy
- **Conservative Learning**: More cautious than Q-Learning
- **SARSA vs Q-Learning**: Different in how they handle next action

## Implementation Details
1. Initialize Q(s,a) arbitrarily
2. For each episode:
   - Initialize state s
   - Choose action a using ε-greedy from Q
   - While s is not terminal:
     - Take action a, observe r, s'
     - Choose a' from s' using ε-greedy
     - Update: Q(s,a) += α[r + γQ(s',a') - Q(s,a)]
     - s ← s', a ← a'
3. Decay epsilon over time

## Learning Outcomes
- Understanding on-policy learning
- SARSA algorithm mechanics
- Comparison with Q-Learning
- Handling stochastic transitions

## Usage
```python
jupyter notebook frozen_lake_sarsa.ipynb
```

## Expected Results
- SARSA learns safer policy than Q-Learning
- Q-values converge more conservatively
- Success rate improves steadily
- Policy accounts for exploration during learning
