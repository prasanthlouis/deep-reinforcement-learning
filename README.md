Title: Exploring the Depths of Deep Reinforcement Learning

Tools Utilized: We're leveraging Baselines3 from stable-baselines3.readthedocs.io.

Reinforcement learning, at its essence, provides a framework for addressing control tasks, wherein agents learn to navigate environments through interaction, learning from trial and error while receiving feedback in the form of rewards or penalties.

Reward Hypothesis: Central to RL is the concept of maximizing expected cumulative rewards. This means that agents aim to make decisions that lead to the best possible outcomes over time, based on the rewards they expect to receive.

Markov Property: RL agents rely on the Markov Property, which states that the future depends only on the current state, not on the entire history of states and actions. This simplifies decision-making, as agents only need to consider their current situation.

Differentiating State from Observation: Environments can be fully observed, where agents have access to complete information about the state (e.g., chess), or partially observed, where agents only receive partial information (e.g., Super Mario Bros.).

Discrete vs. Continuous Actions: Actions in RL can be discrete, with a finite number of options (e.g., moving in a grid-based game like Super Mario Bros.), or continuous, with an infinite range of possibilities (e.g., controlling a vehicle).

Understanding Cumulative Reward with Gamma: The cumulative reward is the sum of rewards obtained over time. Gamma is introduced as a discount factor to balance immediate rewards against future rewards, allowing agents to prioritize short-term gains or long-term objectives.

Episodic vs. Continuing Tasks: Tasks in RL can be episodic, with clear start and end points (e.g., completing a level in a game), or continuing, where there is no defined endpoint (e.g., ongoing financial trading).

Exploration/Exploitation Trade-off: Agents face the challenge of balancing exploration (trying new actions to discover potentially better strategies) and exploitation (leveraging known strategies to maximize immediate rewards) to achieve optimal performance.

Downside of Just Exploiting: Focusing solely on exploiting known strategies may lead agents to miss out on potentially higher rewards that could be obtained through exploration. Striking the right balance between exploration and exploitation is crucial for achieving success in RL tasks.

The Policy π
The Policy π is like the brain of our Agent. It's the function that guides the Agent's actions based on its current situation. In simpler terms, it's what determines what the Agent does at any given moment.

Think of the Policy as the decision-maker for our Agent. It's the function that tells us which action to take when we're in a certain situation.

Our aim is to learn this Policy, which means finding the best possible way for the Agent to behave. We call this best Policy π*. We achieve this through training.

We can train our agent to find the optimal policy π* using two methods:
Policy vs Value Based
Directly instructing the agent to learn the best action to take based on the current state. This is known as Policy-Based Methods.
Indirectly teaching the agent to recognize the value of different states and then choosing actions that lead to the most valuable states. These are called Value-Based Methods.

Policy-Based Methods
Deterministic: a policy at a given state will always return the same action.
Stochastic: outputs a probability distribution over actions.

Let's illustrate this with an example related to a stochastic policy in reinforcement learning:

Suppose we have a simple environment where an agent can choose between three actions: "Move left," "Move right," and "Stay still." Given the current state of the environment, our stochastic policy needs to decide the probabilities of each action.

Let's say our stochastic policy for this scenario outputs the following probability distribution:

Probability of "Move left" = 0.4
Probability of "Move right" = 0.3
Probability of "Stay still" = 0.3
This distribution indicates that, given the current state, there's a 40% chance that the agent will choose to "Move left," a 30% chance it will "Move right," and a 30% chance it will "Stay still."

So, when the agent observes this state, it consults the stochastic policy and samples an action based on these probabilities. For example, it might randomly select "Move left" 40% of the time, "Move right" 30% of the time, and "Stay still" 30% of the time, ensuring that over many trials, the agent's actions reflect the probabilities specified by the policy.