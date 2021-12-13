# Q-Learning

Q-learning is a relatively simple reinforcement learning algorithm, which attempts to assess the value of being in a given state and take a specific action from that state. Observe the following example:

![image](https://cdn-media-1.freecodecamp.org/images/3JXI06jyHegMS1Yx8rhIq64gkYwSTM7ZhD25)

Let's say there is a robot that wants to get from where it is now to the square marked "End". It can move up, down, left, or right as long as it stays within the environment. However, there are also bombs to avoid and and power that will ensure it has energy to make it to the end. The robot's rewards are as follows:
- the robot loses 1 point ("energy") at each step (this ensures the robot takes the shortest path/reaches the goal as fast as possible)
- if the robot steps on a mine, it loses 100 points and the game ends
- if the robot lands on power, it gains 1 point
- if the robot reaches the End, it gets 100 points

![image](https://cdn-media-1.freecodecamp.org/images/CcNuUwGnpHhRKkERqJJ6xl7N2W8jcl1yVdE8)

To assess this situation, we create a Q-table, with columns for each action and rows for each state. Each score will be the maximum expected future reward if the robot chooses that action at that state. Thus, the Q-table will need to be updated with teach iteration. At the beginning, all the values in the table are 0.

![image](https://cdn-media-1.freecodecamp.org/images/AjVvggEquHgsnMN8i4N35AMfx53vZtELEL-l)

The values of the cells in the Q-table can be calculated using the Bellman Equation. It takes two inputs: state (s) and action (a)

![image](https://cdn-media-1.freecodecamp.org/images/s39aVodqNAKMTcwuMFlyPSy76kzAmU5idMzk)

There are different strategies for how the robot can select an action, but let's say it chooses to go right. We can then update the table using this equation as many times as we want (or until the robot dies or reaches the end).

![image](https://cdn-media-1.freecodecamp.org/images/TnN7ys7VGKoDszzv3WDnr5H8txOj3KKQ0G8o)

This explanation was based on [this article](https://www.freecodecamp.org/news/an-introduction-to-q-learning-reinforcement-learning-14ac0b4493cc/). For more information, [this video](https://www.youtube.com/watch?v=__t2XRxXGxI&t=19s) provides a more detailed explantion.
