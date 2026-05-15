# Offline CQL HalfCheetah

Implementation of **Conservative Q-Learning (CQL)** for **Offline Reinforcement Learning** using the `HalfCheetah-medium-v0` dataset from Minari and the `d3rlpy` framework.

---

## 📌 Project Overview

This project demonstrates how an agent can learn optimal locomotion behavior **without interacting with the environment during training**.  
The model is trained entirely on pre-collected trajectory data using the **Conservative Q-Learning (CQL)** algorithm.

The implementation focuses on:
- Offline Reinforcement Learning
- Conservative Q-Learning
- Continuous Control Tasks
- MuJoCo HalfCheetah Environment

---

## 🧠 Algorithm Used

### Conservative Q-Learning (CQL)

CQL is an offline RL algorithm designed to reduce overestimation bias by learning conservative value functions.

Objective:

$$
L(Q) = \alpha \cdot \mathbb{E}[Q(s,a)] - \mathbb{E}[Q(s,a')] + L_{TD}(Q)
$$

Where:
- \(a\) → out-of-distribution actions
- \(a'\) → in-distribution actions
- \(L_{TD}\) → temporal difference loss

---

## 📂 Dataset

- **Dataset:** `mujoco/halfcheetah/medium-v0`
- **Source:** Minari
- **Environment:** HalfCheetah-v4
- **State Space:** 17-dimensional observations
- **Action Space:** 6 continuous action dimensions

---

## ⚙️ Tech Stack

- Python
- d3rlpy
- Gymnasium
- Minari
- MuJoCo
- PyTorch
- Google Colab

---

## 🚀 Features

- Offline RL training pipeline
- Conservative Q-Learning implementation
- GPU support with CUDA fallback
- Model checkpoint saving
- Policy evaluation in MuJoCo environment
- Episode rendering and video generation

---

## 📊 Training Configuration

| Parameter | Value |
|---|---|
| Algorithm | Conservative Q-Learning |
| Dataset | HalfCheetah-medium-v0 |
| Batch Size | 256 |
| Learning Rate | 3e-4 |
| Training Steps | 100,000 |
| Framework | d3rlpy |

---

## 📈 Results

- Successfully trained an offline RL agent on static trajectory data
- Learned stable locomotion behavior
- Achieved policy convergence through decreasing TD loss
- Generated evaluation rollouts for qualitative analysis

---

## 📁 Project Structure

```bash
offline-cql-halfcheetah/
│
├── train.py
├── evaluate.py
├── cheetah_agent.d3
├── videos/
├── requirements.txt
└── README.md
```

---

## 🛠️ Installation

Clone the repository:

```bash
git clone https://github.com/your-username/offline-cql-halfcheetah.git
cd offline-cql-halfcheetah
```

Install dependencies:

```bash
pip install -r requirements.txt
```

---

## ▶️ Training

Run training:

```bash
python train.py
```

---

## 🎮 Evaluation

Evaluate the trained agent:

```bash
python evaluate.py
```

---

## 📚 References

1. Conservative Q-Learning for Offline Reinforcement Learning — Kumar et al.
2. d3rlpy: An Offline Deep Reinforcement Learning Library
3. Minari Dataset Framework
4. MuJoCo Physics Engine

---

## 👨‍💻 Authors

- Abhinav Koushik

## 📜 License

This project is intended for academic and educational purposes.
