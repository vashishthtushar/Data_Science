# 📘 Assignment 1 — Reinforcement Learning

## 🔍 Overview

This project is a complete implementation of three foundational Reinforcement Learning (RL) algorithms trained on the OpenAI Gym environment **CartPole-v1**. The objective is to study and compare how different learning strategies perform in solving a control problem.

Implemented algorithms:
- Deep Q-Network (DQN)
- Policy Gradient (REINFORCE)
- Actor-Critic (A2C)

---

## 🧠 Algorithms Summary

### 1️⃣ Deep Q-Network (DQN)
A value-based method that approximates Q-values using a neural network. It uses experience replay and a target network to improve training stability.

### 2️⃣ Policy Gradient (REINFORCE)
A Monte Carlo policy-based approach that updates the policy using complete episode returns and log-probabilities of actions.

### 3️⃣ Actor-Critic (A2C)
A hybrid method that maintains both a policy (Actor) and a value function (Critic), enabling step-wise updates using TD error.

---

## ⚙️ Environment

All three models were trained on the **CartPole-v1** environment provided by OpenAI Gym.

Observation space: 4-dimensional continuous  
Action space: 2 discrete actions (left, right)  
Reward: +1 for every time step the pole remains balanced

---

## 🏗️ Project Structure


Assignment1_RL/
│
├── DQN/
│ ├── dqn.py
│ ├── dqn_cartpole.pt
│ ├── dqn_reward_plot.png
│
├── REINFORCE/
│ ├── reinforce.py
│ ├── reinforce_cartpole.pt
│ ├── reinforce_reward_plot.png
│
├── A2C/
│ ├── a2c.py
│ ├── a2c_actor_cartpole.pt
│ ├── a2c_critic_cartpole.pt
│ ├── a2c_reward_plot.png
│
├── report.pdf
├── README.md


---

## 📊 Outputs

Each model produces:
- A `.pt` file containing trained model weights
- A `.png` plot showing episode rewards and moving averages
- Logs for performance tracking over episodes

---

## 📝 Instructions to Run

1. Install dependencies:

```bash
pip install torch gym matplotlib numpy

2. Choose the algorithm you want to run:

bash
Copy code
python dqn.py          # For DQN
python reinforce.py    # For REINFORCE
python a2c.py          # For A2C

3. After training, check:

Saved model file (.pt)
Reward plot image (.png)

📈 Evaluation Metrics
Each model was evaluated based on:

Total reward per episode
Moving average (over 50 episodes)
Convergence behavior
Final average reward (last 100 episodes)

