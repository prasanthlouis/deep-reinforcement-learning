Title: Exploring Deep Reinforcement Learning

Tools: We're using Baselines3 from stable-baselines3.readthedocs.io.

Reinforcement learning helps us solve control tasks, where agents learn by interacting with the environment, getting rewards for their actions.

At its core, RL is about maximizing future rewards. Agents use the current state to decide what to do next, without needing to remember everything.

State vs. Observation: In some cases, we see the full state (like in chess), while in others, we only get part of it (like in Super Mario Bros.).

Discrete vs. Continuous Actions: Some actions are finite (like in Super Mario Bros.), while others have infinite possibilities (like driving a car).

Understanding Cumulative Reward with Gamma: We add up rewards over time, adjusting for how predictable they are. Gamma lets us balance short-term and long-term rewards.

Episodic vs. Continuing Tasks: Some tasks have clear start and end points (like levels in Super Mario Bros.), while others keep going (like stock trading).

Exploration/Exploitation Trade-off: We balance trying new things and sticking with what works to maximize rewards.

Downside of Just Exploiting: Sometimes, focusing only on what we know means missing out on big rewards. Balancing exploration and exploitation helps us find the best outcomes.