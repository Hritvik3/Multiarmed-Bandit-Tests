# Multi-Armed Bandit Evaluation for E-commerce Recommendations

This project demonstrates how to use **Multi-Armed Bandit (MAB)** algorithms to optimize product recommendations using historical logged data from the **ZOZO, Inc. Open Bandit Dataset**. It compares traditional offline evaluation methods with synthetic online simulations to safely evaluate and improve recommendation policies.

---

## Project Overview

- Use logged user interaction data to build action and user contexts.
- Map item IDs to indices and prepare data arrays for rewards, actions, and propensity scores.
- Implement simple MAB policies:  
  - Logged Policy (baseline)  
  - Random Policy  
  - Epsilon-Greedy  
  - UCB1 (Upper Confidence Bound)
- Run offline evaluation modes:  
  - Biased (always update policy)  
  - Replay (update only when chosen action matches logged)  
  - IPS (Inverse Propensity Scoring for unbiased off-policy evaluation)
- Run synthetic online simulations using estimated true click-through rates (CTRs).
- Visualize cumulative and average rewards to compare policy performance.

---

## Why This Matters

- **Offline evaluation** uses historical data to estimate how new recommendation policies would perform without risking live user experience.
- **Synthetic simulation** helps test policies in a controlled environment reflecting real-world variability.
- MAB algorithms dynamically balance exploration and exploitation to improve recommendations faster than fixed A/B/n tests.
- This approach supports smarter, fairer, and more effective personalization in e-commerce platforms.

---

## Getting Started

### Requirements

- Python 3.7+
- Packages: `numpy`, `pandas`, `matplotlib`

Install dependencies with:

```bash
pip install numpy pandas matplotlib
