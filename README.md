# DASC 41103 - Reinforcement Learning Honors Project
## Temporal Difference Learning with SARSA

This repository contains the work of the following three undergraduate Data Science students from the University of Arkansas:
- Lawson Levin
- Myli Brown
- Lucas Jones

### Inspiration
This project was inspired by:
	•	Classic Reinforcement Learning literature, especially “Reinforcement Learning: An Introduction” by Richard S. Sutton and Andrew G. Barto, which first introduced SARSA as an on-policy temporal-difference learning algorithm.
	•	The OpenAI Gym environment design, which standardizes how agents and environments interact through a simple reset() / step() interface.
	•	Educational examples from the “Python Machine Learning” and “Deep Reinforcement Learning Hands-On” books, which emphasize clarity and transparency in small-scale RL simulations.
	•	The idea of building from scratch — rather than relying on prebuilt Gym environments — to help visualize how reinforcement learning actually unfolds step by step.

This version of Gridworld is intentionally minimalist and console-based to make the algorithm’s inner workings visible, explainable, and teachable — perfect for classroom demonstration.

### Overview

This project implements SARSA (State–Action–Reward–State–Action) — an on-policy reinforcement learning algorithm — in a simple 4×4 Gridworld environment built from scratch using Python + Gym-style design.

The agent starts in the top-left corner and must reach the bottom-right terminal cell while minimizing steps.
Each step gives a small penalty (-0.01) to encourage efficiency, and reaching the goal gives a reward of +1.0.
