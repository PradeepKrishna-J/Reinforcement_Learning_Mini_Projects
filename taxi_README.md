# Taxi Pick-Drop

## Overview
Q-Learning implementation on OpenAI Gym's Taxi-v3 environment. The agent learns to pick up passengers and drop them at destinations efficiently.

## Environment Description
- **Grid**: 5x5 grid with 4 special locations (R, G, Y, B)
- **Passenger**: Starts at one location, wants to go to another
- **Taxi**: Must navigate, pick up, and drop off passenger
- **Actions**: 6 actions - North, South, East, West, Pickup, Dropoff
- **States**: 500 discrete states (25 positions × 5 passenger locations × 4 destinations)

### Rewards
- +20: Successful dropoff at correct location
- -1: Each time step
- -10: Illegal pickup or dropoff

## Algorithm Used
- **Q-Learning**: Off-policy TD control
- **Q-Table**: 500 states × 6 actions
- **ε-greedy Exploration**: Decaying epsilon
- **Experience-based Learning**: Trial and error

## Key Concepts
- **Large State Space**: 500 discrete states
- **Hierarchical Task**: Navigate → Pickup → Navigate → Dropoff
- **Sparse Rewards**: Main reward only at successful completion
- **Illegal Actions**: Penalty for wrong pickup/dropoff
- **Exploration Importance**: Must try different strategies

## Implementation Details
1. Initialize Q-table with zeros
2. For each episode:
   - Reset environment (random start)
   - While not done:
     - Choose action (ε-greedy)
     - Execute action
     - Receive reward and next state
     - Update Q-value: Q(s,a) += α[r + γ max Q(s',a') - Q(s,a)]
   - Decay epsilon
3. Track cumulative rewards and penalties
4. Test learned policy

## Learning Outcomes
- Q-Learning in complex environment
- Handling hierarchical tasks
- Large state space management
- Balancing exploration in sparse reward problems
- Understanding illegal action penalties

## Usage
```python
jupyter notebook taxi_pick_drop.ipynb
```

## Expected Results
- Successful pick-up and drop-off strategy
- Q-table converges to optimal values
- Episode length decreases over training
- Penalties (illegal actions) decrease
- Consistent high rewards after convergence
