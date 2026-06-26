# 🎰 Casino Challenge — Multi-Armed Bandits & ε-Greedy (Gamified Workshop)

## 📘 Overview
This workshop introduces **exploration–exploitation trade-offs** in **Reinforcement Learning** through a gamified **Multi-Armed Bandit (MAB)** challenge.  
Students will implement ε-greedy policies, compete for the highest rewards, and analyze their strategies in both stationary and non-stationary environments.

---

## 🧠 Learning Objectives
By completing this workshop, students will be able to:
- Explain the **exploration vs. exploitation dilemma**.
- Implement **ε-greedy** and **decaying ε-greedy** algorithms.
- Compare the effects of different ε values on performance.
- Adapt policies for **non-stationary bandits** using constant step-size (α).
- Reflect critically on their strategies and outcomes.

---

## 🏗️ Workshop Structure

| Phase | Activity | Description |
|-------|-----------|-------------|
| 1 | **Setup & Introduction** | Review MAB concepts and workshop goals. |
| 2 | **Round 1 – Stationary Casino** | Students compete using ε-greedy strategies. |
| 3 | **Leaderboard & Reflection** | Submit scores, compare results, and discuss strategies. |
| 4 | **Round 2 – Non-Stationary Casino** | Adapt to drifting reward probabilities using constant α. |
| 5 | **Final Discussion** | Relate bandit learning to real-world systems (A/B testing, ads, recommendations). |

---

## 🎮 Gamified Components
- **Leaderboards:** Students submit results to CSV files (`submissions_round1.csv`, `submissions_round2.csv`) and view rankings.
- **Badges / Awards:**
  - 🥇 *Efficient Exploiter* — Highest reward with low ε.
  - 🧭 *Risk Taker* — High ε with competitive performance.
  - 🔄 *Adaptive Strategist* — Best performance in non-stationary round.
- **Reflection Prompts:** Encourage analysis of exploration behavior and real-world parallels.

---

## 💻 Technical Notes
- Works in **Jupyter Notebook** or **Google Colab**.
- Dependencies: `numpy`, `matplotlib`, `pandas`, `IPython.display`
- Each student runs locally; the instructor collects leaderboard CSVs for aggregation.

---

## 🧩 Files Included
| File | Description |
|------|--------------|
| `Casino_Challenge_MAB_Workshop.ipynb` | Main notebook with competition, code, and reflection prompts. |
| `MultiArmedBandit_Workshop.ipynb` | Introductory notebook demonstrating ε-greedy bandits and basic visualizations. |
| `My_MAB_Reflection_Notebook.ipynb` | Student submission notebook with both rounds, visualizations, CSV readbacks, and reflections. |
| `submissions_round1.csv` | Generated leaderboard CSV for Round 1: Stationary Casino. |
| `submissions_round2.csv` | Generated leaderboard CSV for Round 2: Non-Stationary Casino. |
| `mab_figures/` | Figures used by the student reflection notebook. |
| `README.md` | This summary document. |

---

## 📝 Student Submission Notes
For grading or review, start with `My_MAB_Reflection_Notebook.ipynb`.

That notebook summarizes:
- Round 1: Stationary Casino results and ε comparison.
- Round 2: Non-Stationary Casino results and constant-α comparison.
- Exploration–exploitation reflections.
- Why ε matters.
- Why constant step-size α helps in non-stationary settings.
- Optional UCB and Thompson Sampling extensions for both rounds.
- The generated CSV files from both competition rounds.

The original workshop notebooks are kept as reference material.

---

## 💬 Talking Points Summary

My main takeaway is that a bandit problem is really about learning while acting. If I only exploit too early, I may get stuck with a bad machine. If I explore too much, I waste chances to use the machine that already looks good.

- In **Round 1**, the casino is stationary, so the machines' reward probabilities stay fixed. That means old data is still useful, and sample-average estimates make sense.
- In **Round 2**, the casino is non-stationary, so the reward probabilities drift. In that case, old data can become misleading, and constant α helps because it gives more weight to recent rewards.
- I also clarified that **stationary/non-stationary** describes the environment, while **static/adaptive** describes the policy. A policy can keep updating even if the environment is stationary.
- A real regulated casino is usually closer to stationary because RTP settings are not normally changed all the time. Short winning or losing streaks can look like change, but they are often just randomness.
- In real applications like ads, recommendations, A/B testing, and markets, non-stationarity is more realistic because users, trends, and conditions keep changing.
- UCB and Thompson Sampling are useful extensions because they explore based on uncertainty instead of random guessing.
- For non-stationary problems, even UCB or Thompson Sampling need adaptive versions, such as sliding-window UCB or discounted Thompson Sampling.

Key generated outputs:
- `submissions_round1.csv`
- `submissions_round2.csv`
- `mab_figures/round1_epsilon_comparison.png`
- `mab_figures/round2_alpha_comparison.png`
- `mab_figures/round1_ucb_thompson_comparison.png`
- `mab_figures/round2_ucb_thompson_comparison.png`

---

## 🧭 Instructor Tips
- Keep the same random seed (`SEED_ENV`) for fairness.
- Hide true means during competition.
- Encourage students to explain *why* their chosen ε performed as it did.
- Optionally extend to **UCB** or **Thompson Sampling**.

---

## 🧾 License
For educational use in academic settings.  
Developed with support from OpenAI’s ChatGPT (GPT‑5) as part of CSCN8020 Machine Learning Education Tools.
