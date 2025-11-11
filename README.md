# 🏆 Performance of MARL Algorithms in Cooperative and Asymmetric Soccer Environments

## 👥 Authors  
- **Pratik Chakraborty (220962350)**  
- **Priyanka Pathak (220962276)**  
- **Aryan Bhargava (220962129)**  

---

## 📘 Project Overview  
This project presents a comparative study of **Multi-Agent Reinforcement Learning (MARL)** algorithms — **IPPO**, **MAPPO**, and **MADDPG** — implemented in the **Unity ML-Agents SoccerTwos** environment.  

The goal is to evaluate how different MARL algorithms perform under **cooperative** and **competitive** multi-agent settings, measuring their ability to learn coordinated strategies, maintain training stability, and achieve consistent performance.

---

## ⚙️ Environment Setup  

### 🧩 Requirements  

All implementations were executed on **Google Colab** using the following dependencies:

```bash
pip install torch torchvision torchaudio
pip install mlagents==0.30.0
pip install numpy matplotlib seaborn
pip install gym
```

---

## 🕹️ Environment Details  

### Simulator  
- **Unity ML-Agents (SoccerTwos)**

### Observation Space  
- **Continuous** — includes positions, velocities, and ball state

### Action Space  
- **Discrete** — includes movement, kick, and direction

### Reward Structure  
- **Team-based cooperative rewards**  
  - Rewards for scoring and possession control

### Training Platform  
- **Google Colab GPU Runtime**

---

## 🤖 Algorithms Implemented  

### 1. Independent Proximal Policy Optimization (IPPO)  
- Independent actor–critic networks per agent  
- No shared parameters; decentralized training  
- Encourages independent exploration  
- Achieved steady policy improvement and balanced learning trajectories  

### 2. Multi-Agent Proximal Policy Optimization (MAPPO)  
- Uses a centralized critic with decentralized actors  
- Aggregates global state information for coordinated learning  
- Reduced policy oscillations and improved convergence stability  
- Demonstrated the most stable convergence among the three algorithms  

### 3. Multi-Agent Deep Deterministic Policy Gradient (MADDPG)  
- Actor–critic structure with a shared critic  
- Optimized for continuous policy improvement  
- Agents learn coordinated offensive and defensive strategies  
- Exhibited rapid adaptability and high reward peaks  

---

## 📂 Repository Structure  

```
MARL-SoccerTwos/
│
├── 📁 scripts/
│   ├── IPPO.ipynb        # Independent Proximal Policy Optimization implementation
│   ├── MAPPO.ipynb       # Multi-Agent Proximal Policy Optimization implementation
│   ├── MADDPG.ipynb      # Multi-Agent Deep Deterministic Policy Gradient implementation
│
├── 📄 RL_Project_Final_Report.pdf   # Project report with results and analysis
│
└── README.md                        # Project documentation (this file)
```

---

## 🚀 How to Use  

### 🔹 Step 1: Clone the Repository  

```bash
git clone https://github.com/your-username/MARL-SoccerTwos.git
cd MARL-SoccerTwos
```

### 🔹 Step 2: Open in Google Colab  

You can directly open the notebook files from the `scripts/` directory in **Google Colab**.

- Open `scripts/IPPO.ipynb` for Independent PPO  
- Open `scripts/MAPPO.ipynb` for Multi-Agent PPO  
- Open `scripts/MADDPG.ipynb` for Multi-Agent DDPG  

### 🔹 Step 3: Run the Training  

Each notebook contains:
- Environment setup and initialization  
- Actor–critic network definitions  
- Training loop and policy updates  
- Visualization of rewards, losses, and win rates  

Execute the cells sequentially to train agents in the SoccerTwos environment.

---

## 📊 Results Summary  

| Algorithm | Architecture Type                   | Convergence | Coordination | Adaptability | Remarks                        |
|-----------|-------------------------------------|-------------|--------------|--------------|--------------------------------|
| IPPO      | Decentralized Actor–Critic          | Moderate    | Medium       | Moderate     | Stable but slower learning     |
| MAPPO     | Centralized Critic, Decentralized Actors | Excellent   | High         | High         | Most stable and cooperative    |
| MADDPG    | Shared Critic (Continuous)          | High        | High         | Very High    | Most adaptive and responsive   |

---

## 💡 Strengths  

- Fully functional multi-agent setup using Unity ML-Agents and PyTorch  
- Consistent training pipeline for all algorithms  
- Reproducible workflow on Google Colab  
- Comparative visualization of learning curves (rewards, policy loss, critic loss, win rates)  

---

## ⚠️ Limitations  

- Limited training duration due to Colab GPU timeouts  
- Only the SoccerTwos environment implemented (Strikers vs Goalie pending)  
- Minimal hyperparameter tuning due to compute constraints  

---

## 🔮 Future Improvements  

- Extend training to larger episode counts for full convergence  
- Include asymmetric environments (e.g., Strikers vs Goalie)  
- Add advanced evaluation metrics such as entropy and coordination score  
- Visualize agent trajectories and heatmaps for interpretability
