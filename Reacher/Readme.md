# Soft Actor-Critic (SAC) for Reacher-v4 in OpenAI Gym

## Overview
This repository contains an implementation of the Soft Actor-Critic (SAC) algorithm for the "Reacher-v4" environment in OpenAI Gym. SAC is an advanced reinforcement learning algorithm designed for continuous action spaces, leveraging off-policy learning, actor-critic architecture, and entropy maximization.

## About Reacher-v4 Environment
The "Reacher-v4" environment is a robotic control task where an agent must move a robotic arm to reach a target location. The challenge is to control the arm precisely, balancing the need for accurate movements and efficient actions.

## Soft Actor-Critic (SAC) Explained
SAC is a model-free reinforcement learning method that incorporates entropy into the reward structure, promoting exploration and robust policy development.

### Key Components of SAC
1. **Actor-Critic Framework**: Utilizes separate networks for policy (actor) and value estimation (critic).
2. **Entropy Maximization**: Encourages the agent to explore diverse actions, improving policy robustness.
3. **Off-Policy Learning**: Learns from past experiences stored in a replay buffer for efficient learning.
4. **Automatic Entropy Tuning**: Adjusts the entropy coefficient automatically for a balance between exploration and exploitation.

## Implementation Details

### Configuration
- Multiple configuration dictionaries (`config_dict_1`, `config_dict_2`, `config_dict_3`, `config_dict_4`) are defined to experiment with different SAC settings.
- The configurations vary in terms of network architecture, learning rates, exploration strategies, and replay buffer capacities.

### Custom Environment Wrapper
- A custom wrapper `CustomReacherEnv` is implemented around the standard Gym environment to modify the reward function and potentially other environment dynamics.

### Training Process
- The SAC algorithm is initialized and trained for a specified number of iterations.
- Training performance and other metrics are logged for analysis.

### Testing and Visualization
- The trained model is evaluated in the environment.
- OpenCV is used to capture and save the agent's performance in a video format.

### Running the Code
Ensure all dependencies (Gym, Ray RLlib, OpenCV, etc.) are installed before executing the scripts.

## Conclusion
This repository demonstrates the application of SAC in a complex control task, highlighting its ability to learn efficient and nuanced policies in continuous action spaces.

