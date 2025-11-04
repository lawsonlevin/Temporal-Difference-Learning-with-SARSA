# DASC 41103 - Reinforcement Learning Honors Project
## Temporal Difference Learning with SARSA

This repository contains the work of the following three undergraduate Data Science students from the University of Arkansas:
- Lawson Levin
- Myli Brown
- Lucas Jones

SARSA Gridworld — Reinforcement Learning Demo

Overview

This project implements SARSA (State–Action–Reward–State–Action) — an on-policy reinforcement learning algorithm — in a simple 4×4 Gridworld environment built from scratch using Python + Gym-style design.

The agent starts in the top-left corner and must reach the bottom-right terminal cell while minimizing steps.
Each step gives a small penalty (-0.01) to encourage efficiency, and reaching the goal gives a reward of +1.0.
