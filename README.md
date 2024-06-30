# Deep Q-Learning for Lunar Landing

![](https://github.com/anandkaranubc/deep_q/blob/main/lunarlander.gif)

This project implements a Deep Q-Learning algorithm to simulate lunar landing. The objective is to develop an AI agent capable of landing a lunar module safely on the moon's surface. The implementation is based on the Gymnasium library and utilizes PyTorch for the neural network architecture.

## Table of Contents

- [Installation](#installation)
- [Project Structure](#project-structure)
- [Usage](#usage)
- [Algorithm Explanation](#algorithm-explanation)
- [Results](#results)

## Installation

### Requirements

- Python 3.x
- Gymnasium
- PyTorch
- NumPy

To install the required packages, you can use the following commands:

```bash
pip install gymnasium
pip install "gymnasium[atari, accept-rom-license]"
apt-get install -y swig
pip install gymnasium[box2d]
pip install torch
pip install numpy
```

## Project Structure

The project consists of the following sections:

1. **Installing the required packages and importing the libraries**: This part includes commands to install necessary libraries and packages.
2. **Building the AI**: This part involves creating the architecture of the neural network.
3. **Training the AI**: This part covers the training loop, including how the agent interacts with the environment, stores experiences, and updates its knowledge through training.
4. **Evaluation**: This part evaluates the performance of the trained model.

## Usage

To run the project, execute the Python script:

```bash
python deep_q_learning_for_lunar_landing.py
```

Ensure you have all the required libraries installed as mentioned in the installation section.

## Algorithm Explanation

### Deep Q-Learning

Deep Q-Learning is a reinforcement learning algorithm that uses a neural network to approximate the Q-value function. The key components include:

- **Q-Value**: Represents the expected future rewards for an action taken in a given state.
- **Experience Replay**: Stores the agent's experiences to break the correlation between consecutive samples.
- **Target Network**: A separate network to stabilize training by keeping a fixed Q-value target.

### Neural Network Architecture

The neural network consists of:
- An input layer that takes the state representation.
- Hidden layers with activation functions.
- An output layer that outputs Q-values for each action.

### Training Process

1. **Initialize the environment and the network**.
2. **Interact with the environment** to collect experiences.
3. **Store experiences** in a replay buffer.
4. **Sample a mini-batch of experiences** from the replay buffer.
5. **Calculate the loss** using the difference between predicted Q-values and target Q-values.
6. **Backpropagate the loss** and update the network weights.
7. **Periodically update the target network**.

## Results

After training, the AI agent should be able to land the lunar module safely. The performance can be evaluated based on the average reward per episode and the number of successful landings.
