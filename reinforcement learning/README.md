# Reinforcement Learning
![image](https://user-images.githubusercontent.com/89811204/145855970-3fe624aa-df34-4147-a144-59f208d318ed.png)

Reinforcement learning doesn't use an existing dataset. Instead, the algorithm learns through "self-training" using reward and punishment to take the best action/path that maximizes rewards and minimizes punishment, using reinforcement theory from psychology. Decisionmaking is sequential, in response to delayed feedback, which makes reinforcement algorithms take a long time to run.

To do this, we create a learning system, called an **agent**, that can collect its own data through trial-and-error in an **environment** in which the agent makes observations, selects and perform actions, and is reinforced with a **reward** (positive) or **penalty** (negative). It then determines the best strategy, called a **policy** to maximize rewards over time that defines which actions the agent should choose in a given situation.

e.g. robots learning to walk, DeepMind's AlphaGo program playing Go, playing Dota, or playing Mario (with rewards for collecting coins and a penalty for walking into a Goomba)

Common vocabulary in reinforcement learning:
- Agent: sole decision-maker and learner
- Environment: physical world in which the agent learns and decides actions to perform (you can see a list of several different kinds of environments [here](https://medium.com/@mauriciofadelargerich/reinforcement-learning-environments-cff767bc241f))
- Action: a list of outcomes/actions the agent can decide to take
- State: the current situation/setting of the agent in the environment
- Reward: for each action the agent selects, the environment issues feedback in the form of a reward (it's usually just a scalar value)
- Policy: the agent's decision-making strategy that determines which actions they will choose in which situations
- Value function: cumulative reward as the policy is executed
- Model: the agent maps state-action pairs over a probability distribution for each state (not included in every reinforcement learning agent)

![image](https://editor.analyticsvidhya.com/uploads/229274.jpg)
goal: find a suitable action model that increases total cumulative reward
steps:
1) Create the environment (including actions and states)
2) Define the reward(s)
3) Create the agent
4) Train and validate the agent
5) Execute the policy

Common algorithms are: Q-Learning, SARSA, DQN, DDPG, REINFORCE

List of reinforcement learning in this repository:
  - [Q-Learning algorithm](https://github.com/Madison-Bunting/INDE-577/tree/main/reinforcement%20learning/1%20-%20q-learning)
  - [Graph Theory](https://github.com/Madison-Bunting/INDE-577/tree/main/reinforcement%20learning/2%20-%20graph%20theory) - this is not an explicit "algorithm" of reinforcement learning. Rather, this is an area of new development and overlap between a mathematical field and data science

If you are interested in further learning [this video](https://www.youtube.com/watch?v=wVXXLLT6srY) provides a more detailed explanation.

The notebooks in this folder are in the context of HR analyltics. For more information about the use of reinforcement learning in HR, you can look at the articles below:
- https://arxiv.org/pdf/2012.00583.pdf
- https://medium.com/geekculture/reinforcement-machine-learning-the-next-big-step-for-hr-ccc3ea908bd7
