# Q-Learning

Reinforcement learning is learning what to do; how to map situations to actions as to maximize a numerical reward signal. The learner, or agent, is not told which actions to take, but to instead discover which actions yield the most reward by trying them. This type of model can be thought of a specific instance of Markov decision processes (MDP's). The learner and action maker is called the **agent**. The thing that the agent interacts with is called the **environment**, which can be thought of as everything outside the agent. 

The agent and environment interact in a looping process, where the agent observes some portion of the environment and takes an action, after which, the environment responds and presents a new situation to the agent. More specifically, the agent and environment  interact at each of a sequence of discrete time steps $t = 0, 1, \dots, T$, where $T$ is the **terminal state**. At each time step $t$, the agent recieves some representation of the environment's **state**, $S_t \in \mathcal{S}$, and on that basis selects an **action**, $A_t \in \mathcal{A}$. Here, $\mathcal{S}$ is the set of all possible states and $\mathcal{A}$ is the set of all possible/valid actions. One time step later, and in part as a consequence of action $A_t$, the agents recieves a numerical **reward**, $R_{t+1} \in \mathbb{R}$, and finds itself in a new state, $S_{t+1}\in \mathcal{S}$. The MDP and agent together give rise to a sequence, or **trajectory** typically denoted by $\tau$:

$$
\tau = S_0, A_0, R_1, S_1, A_1, R_2, S_2, A_2, R_3, \dots 
$$


The goal of the agent is to maximize its rewards over a given trajectory starting from state $S_t$. This is called the **return** and is given with the following equation:

$$
G_{t} = R_{t+1} + \gamma R_{t+2} + \gamma^{2} R_{t+3} \dots, 
$$

where $\gamma \in [0, 1]$ is the **discount rate**. The discount rate determines the present value of the future rewards. This formula can be written recursively as:

$$
G_{t} = R_{t+1} + \gamma G_{t+1}. 
$$



## Policies and the Q-Function

A **policy** is a mapping from states to probabilities of selecting each possible action. 

$$
q_{\pi}(s, a) = \mathbb{E}_{\pi}\Big[ G_t | S_t = s, A_t = a\Big] = \mathbb{E}_{\pi}\Big[ G_t + \gamma G_{t+1}| S_t = s, A_t = a\Big]
$$

Let $Q(S_t, A_t)$ denote the current q-value of the state action pair $(S_t, A_t)$. Through experience, the agent can learn how well our current estimate is (just like we compare predicted labels to true labels in supervised learning). The agent can then update the value of $Q(S_t, A_t)$ after experiencing its future rewards. The following update rule illustrates this updating:

$$
Q(S, A) \leftarrow Q(S, A) + \alpha \Big[R + \gamma \max_{a}Q(S', a) - Q(S, A) \Big]
$$


https://www.youtube.com/watch?v=wVXXLLT6srY
https://www.youtube.com/watch?v=__t2XRxXGxI&t=19s

The notebooks in this folder will specifically be executing

https://arxiv.org/pdf/2012.00583.pdf
https://medium.com/geekculture/reinforcement-machine-learning-the-next-big-step-for-hr-ccc3ea908bd7


