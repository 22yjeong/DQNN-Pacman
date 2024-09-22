# Deep Convolutional Q-Learning for Pac-Man

## Overview

This project utilizes a Deep Convolutional Q-Learning (DCQN) approach to train an agent to play Pac-Man. The agent learns to interpret visual input from the game and make decisions that maximize its score, demonstrating the use of convolutional neural networks (CNNs) in a reinforcement learning context.

## System Components

### Neural Network Architecture
The core of the agent's decision-making process is a CNN with multiple layers designed to process the spatial hierarchies in the game's visual input. The network architecture includes:
- **Convolutional Layers**: Extract spatial features from the game frames.
- **Batch Normalization**: Stabilizes and accelerates learning.
- **Fully Connected Layers**: Transform the learned spatial features into action values.

### Agent Dynamics
The `Agent` class manages interactions with the game environment through:
- **Action Selection**: Decides the best action based on the current policy, using an epsilon-greedy strategy for exploration.
- **Learning Mechanism**: Updates the policy based on observed rewards and transitions, using a target network to stabilize the updates.

## Functionality

### Environment Interaction
The environment, built with `gymnasium`, is a wrapper around the classic Atari game Ms. Pac-Man. The agent interacts with this environment by:
- **Observing States**: Receives game frames as input.
- **Performing Actions**: Executes actions which are translated into game movements.
- **Receiving Rewards**: Obtains feedback in the form of scores from the game.

### Training Process
Training involves running multiple episodes where the agent:
- **Collects Experience**: Gathers data about state transitions and rewards.
- **Learns from Experience**: Uses batches of collected data to update the neural network weights.

### Results Visualization
The project includes functionality to record and display the agent's gameplay, allowing users to visually assess the agent's performance and improvement over time.


## Usage

To run this project:
1. Install all required dependencies.
2. Execute the Python script to start training the agent.
3. Use the visualization functions to view the agent's gameplay.
