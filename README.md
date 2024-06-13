# deep-reinforcement-learning
Deep Reinforcement Learning

This uses: Baselines3 https://stable-baselines3.readthedocs.io/en/master/

Reinforcement learning is a framework for solving control tasks (also called decision problems) by building agents that learn from the environment by interacting with it through trial and error and receiving rewards (positive or negative) as unique feedback.

RL is based on the reward hypothesis, which is that all goals can be described as the maximization of the expected return (expected cumulative reward).
Markov Property implies that our agent needs only the current state to decide what action to take and not the history of all the states and actions they took before.

State s: is a complete description of the state of the world (there is no hidden information). In a fully observed environment. Eg Chess
Observation o: is a partial description of the state. In a partially observed environment. Eg Super mario bros

Discrete space: the number of possible actions is finite. Eg super mario bros you can go up, down, left and right
Continuous space: the number of possible actions is infinite. Eg driving a car has infinite actions. You can turn the car 10 degrees, 11, honk, etc
