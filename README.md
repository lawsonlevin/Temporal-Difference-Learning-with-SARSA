# DASC 41103 - Reinforcement Learning Honors Project
## Temporal Difference Learning with SARSA

This repository contains the work of the following three undergraduate Data Science students from the University of Arkansas:
- Lawson Levin
- Myli Brown
- Lucas Jones

To run this prject on your own machine, you will need to install the following Python libraries.
- numpy
- gymnasium

### Inspiration
This project was inspired by:
- Classic Reinforcement Learning literature, especially _Reinforcement Learning: An Introduction_ by Richard S. Sutton and Andrew G. Barto, which first introduced SARSA as an on-policy temporal-difference learning algorithm.
- The OpenAI Gym environment design, which standardizes how agents and environments interact through a simple reset() / step() interface.
- Educational examples from the _Machine Learning with PyTorch and Scikit-Learn_ by Sebastian Raschka, Yuxi (Hayden) Liu, and Vahid Mirjalili
- The idea of building from scratch — rather than relying on prebuilt Gym environments — to help visualize how reinforcement learning actually unfolds step by step.

This version of Gridworld is intentionally minimalist and console-based to make the algorithm’s inner workings visible, explainable, and teachable — perfect for classroom demonstration.

### Overview

This project implements SARSA (State–Action–Reward–State–Action) — an on-policy reinforcement learning algorithm — in a simple 4×4 Gridworld environment

The agent starts in the top-left corner and must reach the bottom-right terminal cell while minimizing steps.
Each step gives a small penalty (-0.01) to encourage efficiency, and reaching the goal gives a reward of +1.0.

### How the algorithm is trained and evaluated

- A Q-table of zeros is initialized with shape [n_states × n_actions], representing the expected reward value of taking each action in each state.
- During training, the agent runs through 500 episodes, updating its Q-values using the SARSA algorithm.
- Early episodes are exploratory, allowing the agent to experience different paths.
- Over time, as Q-values stabilize, the agent converges on an optimal policy, finding the fastest and most reliable route to the goal.

The trained agent is evaluated by following the greedy policy derived from its learned Q-table (no exploration).
- Each episode starts from the top-left corner and ends when the terminal state is reached or when the step limit is exceeded.

**Performance Metrics**
- Success Rate – Percentage of episodes where the goal was reached.
- Average Steps – Mean number of steps taken per episode.
- Average Reward – Mean total reward accumulated during each episode.
- Min/Max Steps – Shortest and longest episode lengths observed.

**Baseline Comparison**
- A random baseline is also run, where the agent takes random actions with no learning.
- Comparing SARSA results to the random policy demonstrates the impact of learning on efficiency and consistency.

**Visualization**
- To illustrate the learned policy, one episode is played out step-by-step in the console.
- The grid is printed after each move using env.draw():
	•	A marks the agent’s position.
	•	T marks the terminal goal.
	•	. marks empty cells.
- This allows observers to watch the agent’s path as it successfully navigates from start to goal.
