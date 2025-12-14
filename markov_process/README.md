# Markov Process

## Overview
Introduction to Markov Processes and Markov Decision Processes (MDPs), the mathematical foundation of reinforcement learning. This notebook covers the essential theory before diving into RL algorithms.

## Concepts Covered

### 1. Markov Property
- **Memoryless Property**: Future depends only on present, not past
- **Mathematical Definition**: P(s'|s) = P(s'|s,s_{t-1},...,s_0)
- **State Transition**: Probability of moving between states

### 2. Markov Chain
- **States**: Set of possible states
- **Transition Matrix**: P[i,j] = P(s'=j|s=i)
- **Stationary Distribution**: Long-term state probabilities
- **Example**: Weather patterns, random walks

### 3. Markov Reward Process (MRP)
- **Rewards**: Values associated with states
- **Return**: Cumulative discounted reward
- **Discount Factor γ**: Present vs future value
- **Value Function**: Expected return from each state

### 4. Markov Decision Process (MDP)
- **Actions**: Agent's decisions
- **Policy π(a|s)**: Probability of taking actions
- **State Transition**: P(s'|s,a)
- **Reward Function**: R(s,a,s')
- **Optimal Policy**: Maximizes expected return

## Implementation Details
- Visual representation of Markov chains
- Transition matrix calculations
- Bellman equation demonstrations
- Value function computations
- Policy evaluation examples

## Learning Outcomes
- Foundation of RL theory
- Understanding MDPs formally
- Bellman equations intuition
- Value function concepts
- Prerequisites for RL algorithms

## Key Equations

**Value Function (MRP)**:
$$V(s) = E[R_{t+1} + \gamma V(s_{t+1}) | s_t = s]$$

**Bellman Equation (MDP)**:
$$V^\pi(s) = \sum_a \pi(a|s) \sum_{s',r} p(s',r|s,a)[r + \gamma V^\pi(s')]$$

## Usage
```python
jupyter notebook Markov_process.ipynb
```

## Expected Results
- Visual Markov chain examples
- Transition matrix analysis
- Value function calculations
- Understanding of MDP components
