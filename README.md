# 🐦 Flappy Bird AI — Reinforcement Learning

An interactive implementation of the classic Flappy Bird game built to train, evaluate, and visualize an intelligent autonomous agent using **Reinforcement Learning (RL)**. The agent learns to navigate through obstacle gaps over successive iterations by optimizing its decision-making policy.

---

## 🚀 Project Overview

This repository bridges classical arcade game physics with machine learning. By framing Flappy Bird as a Markov Decision Process (MDP), an RL agent learns optimal timing for its "flap" action purely through trial and error, relying on an algorithmic reward structure.

### 🧠 Core Reinforcement Learning Concepts
* **State Space ($S$):** The environment tracks key spatial variables, including the horizontal distance to the next upcoming pipe gap, the vertical distance to the top/bottom pipes, and the bird's current velocity.
* **Action Space ($A$):** A discrete set containing two actions: `0` (do nothing/let gravity pull the bird down) or `1` (flap/apply upward velocity).
* **Reward Function ($R$):** 
  * `+1` (or `+0.1`) for every frame survived or pipe successfully cleared.
  * `-100` (or a heavy penalty) if the bird collides with a pipe boundary or crashes into the ground.

---

## 🛠️ Tech Stack & Key Modules

* **Frontend / Simulation Layer:** JavaScript (HTML5 Canvas) / Python (Pygame) for rendering real-time game physics, collision logic, and responsive frame rates.
* **RL Agent Engine:** 
  * **Q-Learning (Tabular):** Discretizes continuous spatial states into a state-action matrix table for lightweight, efficient training directly in-browser or terminal.
  * **Deep Q-Networks (DQN):** Utilizes deep neural networks (via TensorFlow / PyTorch) to approximate the optimal action-value function directly from high-dimensional or continuous state feature vectors.

---

## 📊 Performance & Training Workflow

1. **Exploration Phase ($\epsilon$-Greedy):** The agent initially makes random moves ($\epsilon \approx 1.0$) to map out the consequences of actions within the state space coordinates.
2. **Exploitation Phase:** As the exploration decay rate takes effect, the agent relies progressively more on its learned values ($Q$-values) to choose actions maximizing long-term cumulative rewards.
3. **Convergence:** Over hundreds of training episodes, the agent achieves flawless policy execution, indefinitely avoiding obstacle collisions.

---

## 💻 Getting Started

### Prerequisites
Ensure you have the required runtime or dependencies installed:
```bash
# Example if using Python/Pygame/PyTorch stack:
pip install pygame torch numpy
