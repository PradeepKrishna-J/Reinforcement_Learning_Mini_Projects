# Tic-Tac-Toe (Exercise 5a)

## Overview
Implementation of reinforcement learning for Tic-Tac-Toe, likely corresponding to Exercise 5a from Sutton & Barto's textbook. Focuses on value function approximation and policy learning.

## Game Description
- **Board**: 3×3 grid
- **Players**: X and O
- **Win Condition**: Three in a row (horizontal, vertical, diagonal)
- **States**: All possible board configurations
- **Actions**: Place mark in empty cell

## RL Approach
- **State Representation**: Board configuration
- **Value Function**: Estimated probability of winning from each state
- **Policy**: Greedy with respect to value function
- **Opponent**: Can be deterministic or probabilistic

## Key Concepts
- **State Space**: Exponential growth (3^9 possible boards)
- **Symmetry**: Board rotations and reflections
- **Afterstate Values**: Value of state after agent's move
- **Temporal Difference Learning**: Update values during play
- **Self-Play**: Learn by playing against itself

## Implementation Details
1. Initialize state values (e.g., V(s) = 0.5)
2. Special cases: Win = 1, Loss = 0, Draw = 0.5
3. For each game:
   - Start with empty board
   - Agent moves greedily (with exploration)
   - Opponent moves (various strategies)
   - Update values: V(s) += α[V(s') - V(s)]
4. Track win/loss/draw rates
5. Test against optimal player

## Learning Outcomes
- TD learning in board games
- Afterstate representation
- Self-play training
- Exploitation of symmetries
- Value function for zero-sum games

## Usage
```python
jupyter notebook "tic-tac-toe_5(a).ipynb"
```

## Expected Results
- Agent learns to block opponent threats
- Discovers winning strategies
- Improves win rate over training
- Near-optimal play against various opponents
