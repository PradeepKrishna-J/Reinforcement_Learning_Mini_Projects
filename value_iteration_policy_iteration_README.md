# Value Iteration and Policy Iteration Algorithms

## Overview
Comprehensive comparison of the two fundamental dynamic programming algorithms for solving MDPs. Demonstrates theoretical concepts and practical implementation differences.

## Algorithms Covered

### 1. Policy Iteration
**Process:**
1. **Policy Evaluation**: Solve Bellman equation for V^π(s)
2. **Policy Improvement**: Update π to be greedy w.r.t. V^π
3. **Repeat**: Until policy is stable

**Characteristics:**
- Each iteration: complete policy evaluation (multiple sweeps)
- Fewer iterations to converge
- More computation per iteration
- Guaranteed convergence to optimal

### 2. Value Iteration
**Process:**
1. **Value Update**: V(s) = max_a E[r + γV(s')]
2. **Repeat**: Until values converge
3. **Extract Policy**: π(s) = argmax_a E[r + γV(s')]

**Characteristics:**
- Single sweep per iteration
- More iterations to converge
- Less computation per iteration
- Combines evaluation and improvement

## Comparison Metrics
- **Convergence Speed**: Number of iterations
- **Computation Time**: Time per iteration and total
- **Memory Usage**: Storage requirements
- **Implementation Complexity**: Code simplicity

## Key Concepts
- **Bellman Optimality Principle**: Optimal policy has optimal subpolicies
- **Contraction Mapping**: Guaranteed convergence
- **Generalized Policy Iteration**: Framework encompassing both
- **Asynchronous Updates**: In-place vs synchronous
- **Stopping Criteria**: ε-convergence thresholds

## Implementation Details
1. Define common test environment (e.g., Grid World)
2. Implement Policy Iteration:
   - Policy evaluation subroutine
   - Policy improvement step
   - Track iterations and time
3. Implement Value Iteration:
   - Bellman optimality update
   - Track iterations and time
4. Compare results:
   - Final policies (should be identical)
   - Value functions (should converge to same)
   - Computation metrics

## Learning Outcomes
- Deep understanding of DP in RL
- When to use each algorithm
- Trade-offs: iterations vs computation
- Practical implementation skills
- Foundation for understanding approximate DP

## Usage
```python
jupyter notebook value_iteration_and_policy_iteration_algorithms.ipynb
```

## Expected Results
- Both converge to same optimal policy
- Value iteration: more iterations, faster per iteration
- Policy iteration: fewer iterations, slower per iteration
- Total time depends on problem structure
- Identical final value functions
