# BlackJack - Monte Carlo Methods

## Overview
Implementation of Monte Carlo methods to learn optimal BlackJack playing strategy without prior knowledge of the game dynamics.

## Environment Description
- **Game**: Standard BlackJack (21)
- **Player Actions**: Hit (draw card) or Stick (stop drawing)
- **State**: (player sum, dealer showing card, usable ace)
- **Goal**: Get closer to 21 than dealer without going over

## Algorithm Used
- **Monte Carlo Control**: Learning from complete episodes
- **First-Visit MC** or **Every-Visit MC**
- **ε-greedy Policy**: Balance exploration and exploitation
- **On-Policy Learning**: Learn while following the policy

## Key Concepts
- **Episode-Based Learning**: Complete games from start to finish
- **Sample Returns**: Average returns from states visited
- **State-Action Value Q(s,a)**: Expected return for taking action a in state s
- **Exploration vs Exploitation**: ε-greedy ensures both
- **No Model Required**: Learn directly from experience

## Implementation Details
1. Generate episodes following ε-greedy policy
2. For each state-action pair in episode:
   - Calculate return (sum of rewards)
   - Update Q(s,a) with average return
3. Update policy to be greedy w.r.t. Q
4. Repeat for many episodes

## Learning Outcomes
- Monte Carlo methods for model-free learning
- Importance of exploration in learning
- Value function estimation from samples
- Strategy learning without game rules

## Usage
```python
jupyter notebook blackJack_montecarlo.ipynb
```

## Expected Results
- Optimal policy for hitting/sticking
- Q-value surface plots
- Win rate improvements over episodes
- Strategy tables for different situations
