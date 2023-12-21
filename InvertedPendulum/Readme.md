# Soft Actor-Critic (SAC) for InvertedPendulum-v4 in OpenAI Gym

## Overview
This repository contains an implementation of the Soft Actor-Critic (SAC) algorithm applied to the "InvertedPendulum-v4" environment from OpenAI Gym. SAC is a state-of-the-art reinforcement learning algorithm that combines off-policy learning with deep learning and entropy maximization.

## About InvertedPendulum-v4 Environment
The InvertedPendulum-v4 task requires an agent to balance a pole on a cart that moves along a frictionless track. The challenge is to prevent the pole from falling over by moving the cart.

## Soft Actor-Critic (SAC) Explained
SAC is an advanced reinforcement learning algorithm designed for environments with continuous action spaces. It introduces an entropy term to the objective function, encouraging the agent to explore more diverse policies.

### Key Components of SAC
1. **Off-Policy Learning**: SAC learns from past experiences stored in a replay buffer, allowing for efficient use of past data.
2. **Actor-Critic Architecture**: The algorithm uses two models, an actor that suggests actions and a critic that evaluates them.
3. **Entropy Maximization**: By maximizing entropy, SAC encourages the agent to explore a variety of actions, leading to more robust learning.
4. **Automatic Entropy Tuning**: The algorithm can automatically adjust the entropy coefficient, balancing exploration and exploitation.

## Implementation Details

### Configuration
- The SAC algorithm is configured with specific hyperparameters like learning rates, buffer size, and exploration settings.
- The neural network architecture for the actor and critic uses fully connected layers with ReLU activation.

### Training Process
- The agent is trained for a defined number of iterations, with metrics like mean reward tracked and plotted.
- The training rewards over time are visualized using Matplotlib to assess performance.

### Testing and Visualization
- The trained model is tested in the environment, and the agent's performance is captured in a video.
- The video creation uses OpenCV for processing and saving frames.

### Running the Code
Ensure all dependencies (Gym, Ray RLlib, OpenCV, etc.) are installed before running the Jupyter Notebook.

## Conclusion
This implementation showcases the effectiveness of the SAC algorithm in a classic control task, demonstrating its ability to learn complex policies in continuous action spaces.

