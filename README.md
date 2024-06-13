# deep-reinforcement-learning
Deep Reinforcement Learning

Tools Used:
This uses: Baselines3 https://stable-baselines3.readthedocs.io/en/master/


Reinforcement learning is a framework for solving control tasks (also called decision problems) by building agents that learn from the environment by interacting with it through trial and error and receiving rewards (positive or negative) as unique feedback.

RL is based on the reward hypothesis, which is that all goals can be described as the maximization of the expected return (expected cumulative reward).
Markov Property implies that our agent needs only the current state to decide what action to take and not the history of all the states and actions they took before.

State vs Observation
State s: is a complete description of the state of the world (there is no hidden information). In a fully observed environment. Eg Chess
Observation o: is a partial description of the state. In a partially observed environment. Eg Super mario bros

Discrete Space vs Continuous Space
Discrete space: the number of possible actions is finite. Eg super mario bros you can go up, down, left and right
Continuous space: the number of possible actions is infinite. Eg driving a car has infinite actions. You can turn the car 10 degrees, 11, honk, etc

How Cumulative Reward works with Gamma
The cumulative reward = rt+1 (rt+k+1 = rt+0+1 = rt+1)+ rt+2 (rt+k+1 = rt+1+1 = rt+2) + ... where t is time
However, in reality, we can’t just add them like that. The rewards that come sooner (at the beginning of the game) are more likely to happen since they are more predictable than the long-term future reward.

To discount the rewards, we proceed like this:

We define a discount rate called gamma. It must be between 0 and 1. Most of the time between 0.95 and 0.99.
The larger the gamma, the smaller the discount. This means our agent cares more about the long-term reward.
On the other hand, the smaller the gamma, the bigger the discount. This means our agent cares more about the short term reward (the nearest cheese).
Then, each reward will be discounted by gamma to the exponent of the time step. As the time step increases, the cat gets closer to us, so the future reward is less and less likely to happen.

Episodic vs continuing tasks
Episodic: In this case, we have a starting point and an ending point. Eg super mario bros -> beginning of level -> ends when you die or completes the level
Continuing: These are tasks that continue forever (no terminal state). In this case, the agent must learn how to choose the best actions and simultaneously interact with the environment. Eg automatic stock trading. You must decide when to end it  