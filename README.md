## Blackjack: A Cards Game

This repository contains an implementation of a Blackjack card game environment, designed to explore reinforcement learning techniques such as Monte Carlo Control and Sarsa(λ). The project showcases how these algorithms can be used to optimize decision-making in the game.

### Game Rules:
1. **Card Values:** Cards are valued between 1 and 13, with face cards (Jack, Queen, King) assigned values of 11, 12, and 13, respectively.
2. **Game Start:** Both the player and the dealer start with one card. Players can draw additional cards (hit) or keep their current total (stick).
3. **Objective:** The player's goal is to accumulate a card value as close to 21 as possible without exceeding it or dropping below 1 (busting).
4. **Dealer Behavior:** The dealer must stick if their card total is 17 or higher and hit otherwise.
5. **Rewards:** The game rewards +1 for a player win, -1 for a player loss, and 0 for a draw.

### Implementation Details:
- **Monte Carlo Control:**
  - The value function (Q) is initialized to zero.
  - The algorithm uses a time-varying step-size and ϵ-greedy exploration to evaluate and improve the player's strategy.
  - The method accumulates rewards over episodes to estimate the value of actions in various states.

- **Sarsa(λ) Algorithm:**
  - This algorithm is an extension of the Sarsa method, incorporating eligibility traces.
  - It initializes the value function (Q) to zero and utilizes similar step sizes and exploration schedules as in Monte Carlo Control.
  - The parameter λ is varied between 0 and 1 to explore its impact on learning efficiency.

### Analysis and Results:
- **Value Function Visualization:** The notebook includes plots that visualize the value functions learned by the Monte Carlo and Sarsa(λ) algorithms.
- **Error Analysis:** Error functions are plotted to show the convergence of the algorithms over time.
- **Experimental Runs:** Multiple experiments are conducted to compare the performance of the two algorithms under different conditions.

### Dependencies:
- Python libraries required include `numpy`, `matplotlib`, and `random`. Ensure these are installed in your environment before running the notebook.

### How to Run:
1. Clone the repository to your local machine.
2. Install the required dependencies using `pip install -r requirements.txt`.
3. Open the notebook in Jupyter and run the cells sequentially to reproduce the results.

This project serves as a comprehensive demonstration of applying reinforcement learning techniques to solve a classic card game problem. It's a great starting point for anyone interested in game AI and reinforcement learning.
