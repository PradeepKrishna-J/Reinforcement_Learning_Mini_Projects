# Reinforcement Learning Mini Projects

A collection of educational Reinforcement Learning implementations using various algorithms and environments. These projects demonstrate fundamental RL concepts and algorithms through practical examples.

## 📚 Projects Overview

Each project is organized in its own directory with the notebook and detailed README.

### Grid World & Navigation
- **[5X5 Grid World](5X5_grid_world/)** - Finding optimal policies in a 5x5 grid environment
- **[Frozen Lake Q-Learning](frozen_lake_qlearning/)** - Q-learning implementation on the Frozen Lake environment
- **[Frozen Lake SARSA](frozen_lake_sarsa/)** - SARSA algorithm applied to Frozen Lake
- **[Frozen Lake (Basic)](frozen_lake_basic/)** - Introductory Frozen Lake exploration
- **[Cliff Walking](cliff_walking/)** - Off-policy Q-learning in cliff walking environment
- **[Value Iteration Grid World](value_iteration_gridworld/)** - Value iteration implementation for grid world

### Classic RL Problems
- **[Gambler's Problem](gamblers_problem/)** - Dynamic programming solution to the gambler's problem
- **[Jack's Car Rental (Policy Iteration)](jacks_car_rental_policy/)** - Policy iteration for the car rental problem
- **[Jack's Car Rental (Value Iteration)](jacks_car_rental_value/)** - Value iteration approach to car rental
- **[Recycling Robot](recycling_robot/)** - MDP modeling and solution for a recycling robot

### Card Games & Strategy
- **[BlackJack Monte Carlo](blackjack/)** - Monte Carlo methods for BlackJack strategy
- **[Tic-Tac-Toe (Exercise 5a)](tictactoe_5a/)** - RL approach to Tic-Tac-Toe
- **[Tic-Tac-Toe Q-Learning](tictactoe_qlearning/)** - Q-learning implementation for Tic-Tac-Toe

### Advanced Environments
- **[Taxi Pick-Drop](taxi/)** - Q-learning for the Taxi environment

### Theoretical Foundations
- **[Markov Process](markov_process/)** - Introduction to Markov processes
- **[Value Iteration and Policy Iteration Algorithms](value_iteration_policy_iteration/)** - Comprehensive comparison of DP methods

## 🚀 Getting Started

### Prerequisites
```bash
pip install gymnasium numpy matplotlib jupyter
```

### Running the Projects
1. Clone this repository
   ```bash
   git clone https://github.com/PradeepKrishna-J/Reinforcement_Learning_Mini_Projects.git
   cd Reinforcement_Learning_Mini_Projects
   ```
2. Navigate to any project folder
   ```bash
   cd frozen_lake_qlearning  # or any other project
   ```
3. Read the project's README for specific details
4. Launch Jupyter Notebook:
   ```bash
   jupyter notebook
   ```
5. Open the `.ipynb` file to explore the implementation

## 📖 Learning Path

**Recommended order for beginners:**
1. Start with [Markov Process](markov_process/) for theoretical foundations
2. Explore [Value Iteration and Policy Iteration](value_iteration_policy_iteration/)
3. Try simpler environments: [Frozen Lake (Basic)](frozen_lake_basic/)
4. Progress to more complex problems: [Jack's Car Rental](jacks_car_rental_policy/)
5. Experiment with different algorithms on the same environment

## 📁 Repository Structure

```
Reinforcement_Learning_Mini_Projects/
├── README.md                           # This file
├── LICENSE                             # CC BY-NC-SA 4.0 License
├── 5X5_grid_world/                     # Grid world with optimal policy
├── blackjack/                          # Monte Carlo for BlackJack
├── cliff_walking/                      # Off-policy Q-learning
├── frozen_lake_basic/                  # Introduction to Frozen Lake
├── frozen_lake_qlearning/              # Q-learning on Frozen Lake
├── frozen_lake_sarsa/                  # SARSA on Frozen Lake
├── gamblers_problem/                   # DP for gambler's problem
├── jacks_car_rental_policy/            # Policy iteration
├── jacks_car_rental_value/             # Value iteration
├── markov_process/                     # Markov process foundations
├── recycling_robot/                    # MDP modeling
├── taxi/                               # Taxi environment Q-learning
├── tictactoe_5a/                       # Tic-Tac-Toe exercise
├── tictactoe_qlearning/                # Tic-Tac-Toe with Q-learning
├── value_iteration_gridworld/          # Value iteration demo
└── value_iteration_policy_iteration/   # Algorithm comparison

Each project folder contains:
- Jupyter notebook (.ipynb) with implementation
- README.md with detailed explanation
```

## 🎓 Educational Purpose

These projects are designed for:
- Students learning Reinforcement Learning
- Educators teaching RL concepts
- Self-learners exploring RL algorithms
- Academic research and study

## 📝 License

This project is licensed under the Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License - see the [LICENSE](LICENSE) file for details.

**Important:** This work is for educational purposes only. Commercial use is strictly prohibited.

## 🤝 Contributing

As this is an educational repository, contributions that improve clarity, fix bugs, or add educational value are welcome. Please ensure any contributions maintain the educational focus and non-commercial nature of the project.

## ⚠️ Disclaimer

These implementations are for educational purposes and may not be optimized for production use. They are designed to illustrate concepts and algorithms clearly rather than for maximum performance.

## 📧 Contact

For questions or discussions about these educational materials, please open an issue in the repository.

---

**Note:** All implementations are based on standard Reinforcement Learning textbooks and resources, including "Reinforcement Learning: An Introduction" by Sutton and Barto.
