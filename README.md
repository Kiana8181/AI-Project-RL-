# AI Project: SmartFlappyBird(RL)

## Overview

This project aims to develop an AI agent capable of playing the Flappy Bird game using Q-learning, a popular reinforcement learning algorithm. The objective is to maximize the agent's score by navigating through continuously moving pipes. The agent observes the environment, takes actions to keep the bird flying, and receives rewards based on its performance.

## Requirements

- Python 3.8.0
- `flappy_bird_gym` library

## Q-Learning Explanation

Q-Learning is a model-free reinforcement learning algorithm used to find the optimal action-selection policy for a given finite Markov decision process. Key components include the Q-table, state, action, reward, learning rate (α), and discount factor (γ).

## Project Development Process

1. **Initial Setup**: Define the environment using `flappy_bird_gym` and initialize parameters like Q-values, learning rate, exploration rate, and discount factor. Discretize the continuous state space into bins.
2. **Policy Definition**: Implement an epsilon-greedy policy to balance exploration and exploitation.
3. **State Conversion**: Convert continuous observations into discrete states using predefined bins.
4. **Reward Calculation**: Design a custom reward function to provide meaningful feedback to the agent.
5. **Action Selection and Q-Table Update**: Select actions based on the current state using the epsilon-greedy policy and update the Q-table accordingly.
6. **Training and Evaluation**: Train the agent over multiple iterations, continuously updating the Q-table and reducing the exploration rate over time. Evaluate the agent's performance using the learned policy.

## Effects of Parameter Changes

- **Learning Rate (α)**: A high α leads to quick adaptation but erratic behavior, while a moderate α balances learning new information and retaining old knowledge.
- **Exploration Rate (ε)**: A high ε promotes extensive exploration initially but often results in suboptimal actions. A decaying ε starting at 0.9 and reducing gradually allows effective exploration initially and stable exploitation later.

## Challenges and Solutions

1. **Reward Function Design**: Initial reward function adjustments to encourage meaningful improvement.
2. **State Space Discretization**: Discretizing continuous state space into bins for feasible Q-table management.
3. **Exploration vs. Exploitation**: Balancing using an epsilon-greedy policy with a decaying ε.
4. **Parameter Tuning**: Experimentation to find optimal values for α, γ, and ε.

## Conclusion

The project successfully developed a Q-learning-based agent for Flappy Bird. Key aspects included discretizing the state space, implementing a meaningful reward function, and balancing exploration and exploitation. Iterative training and parameter tuning significantly improved the agent’s performance. The final parameter settings (learning rate of 0.5 and a decaying exploration rate starting at 0.9) proved most effective, resulting in a stable and high-performing agent.

## Live Demo

Check out the live demo [here](https://kiana8181.github.io/AI-Project-RL-/).

## Note

This project uses `flappy_bird_gym`, which requires Python 3.8.0 for compatibility.
