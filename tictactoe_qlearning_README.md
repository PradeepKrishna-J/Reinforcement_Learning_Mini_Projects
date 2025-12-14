# Tic-Tac-Toe - Q-Learning

## Overview
Q-Learning implementation for Tic-Tac-Toe, using state-action values instead of state values. Demonstrates Q-Learning in a two-player adversarial game environment.

## Game Description
- **Board**: 3×3 grid
- **Players**: RL agent (X) vs opponent (O)
- **Goal**: Win, or at minimum draw
- **State-Action Pairs**: Board configuration + move position

## Algorithm Used
- **Q-Learning**: Learn Q(s,a) for each board state and action
- **Off-Policy TD Control**: Learn optimal while exploring
- **ε-greedy Policy**: Balance exploration and exploitation
- **Opponent Modeling**: Learn against various opponent strategies

## Key Concepts
- **Q-Table**: State-action value function
- **State Encoding**: Convert board to unique identifier
- **Action Space**: 9 possible positions (filtered by legal moves)
- **Reward Structure**:
  - Win: +1
  - Loss: -1
  - Draw: 0
  - Intermediate: 0 or small penalty
- **Exploration**: Critical for discovering winning strategies

## Implementation Details
1. Initialize Q(s,a) for all state-action pairs
2. For each episode (game):
   - Start with empty board
   - Agent's turn:
     - Choose action using ε-greedy
     - Place mark
     - Check win/loss/draw
   - Opponent's turn:
     - Place mark (various strategies)
     - Check win/loss
   - Update Q-values: Q(s,a) += α[r + γ max Q(s',a') - Q(s,a)]
3. Decay epsilon over episodes
4. Test final policy

## Opponent Strategies
- **Random**: Chooses random legal moves
- **Minimax**: Optimal opponent (good for evaluation)
- **Heuristic**: Blocks obvious wins
- **Another Q-Learning Agent**: Self-play

## Learning Outcomes
- Q-Learning in adversarial games
- Handling variable action spaces (legal moves)
- Opponent strategy impact on learning
- State encoding techniques
- Multi-agent considerations

## Usage
```python
jupyter notebook tic-tac-toe_qlearning.ipynb
```

## Expected Results
- Q-values converge to optimal play
- Agent learns to:
  - Take center if available
  - Block opponent wins
  - Create winning opportunities
  - Force draws against optimal play
- Win rate improves significantly
