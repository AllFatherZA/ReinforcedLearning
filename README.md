Q-Learning with Blob Environment
This repository contains Python code that demonstrates Q-learning in a simple 2D environment called the Blob game. The goal is to train an agent using Q-learning to navigate and collect food while avoiding enemies.

Dependencies
numpy
PIL (Python Imaging Library)
cv2 (OpenCV)
matplotlib
You can install the required packages using the following command:

Copy code
pip install numpy pillow opencv-python matplotlib
Environment Setup
The environment is a 10x10 grid, where the agent (player) starts at a random position, and there are two other entities - food and enemy, also placed randomly on the grid.

Parameters
The following parameters are used in the Q-learning process:

SIZE: Size of the grid (10x10 in this case).
HM_EPISODES: Number of episodes for training.
MOVE_PENALTY: Penalty for each move the agent makes.
ENEMY_PENALTY: Penalty when the agent collides with an enemy.
FOOD_REWARD: Reward when the agent collects food.
epsilon: Initial exploration rate for the agent.
EPS_DECAY: The decay rate for exploration (decreases exploration over time).
SHOW_EVERY: How often to show the environment visually (e.g., every 3000 episodes).
Q-Table Initialization
A Q-table is used to store Q-values for different states and actions. If no pre-trained Q-table is provided, a new one is initialized with random values.

Training and Visualization
The agent is trained using Q-learning over the specified number of episodes. During training, the agent learns to navigate the environment to collect food and avoid enemies. The Q-table is updated based on the rewards received during each action.

The code also includes visualization capabilities using cv2 to show the agent's progress in the environment during training.

Results
The training results are visualized using a moving average of the rewards obtained by the agent over the specified number of episodes. The plot shows how the agent's performance improves with training.

Usage
To run the code, execute the Python script, and it will start the training process. The trained Q-table will be saved to a pickle file (qtable-<timestamp>.pickle).

License
This project is licensed under the MIT License.
