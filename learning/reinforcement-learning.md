This is the scenario in which multiple decisions need to be taken by an agent prior to reaching the target and it provides a reward, either +1 or -1, rather than notifying how well or how badly the agent performed across the path:

Reinforcement learning is the problem of getting an agent to act in the world so as to  
 maximize its rewards. It is about what to do and how to map situations to actions so as to  
 maximize a numerical reward signal. The learner is not told which actions to take, as in

most forms of machine learning, but instead must discover which actions yield the most

reward by trying them. The two most important distinguishing features of reinforcement

learning are trial and error and search and delayed reward.

Some examples of reinforcement learning are as follows:

* A chess player making a move, the choice is informed both by planning anticipating possible replies and counter replies.
* An adaptive controller adjusts parameters of a petroleum refinery's operation in real time. The controller optimizes the yield/cost/quality trade-off on the basis of specified marginal costs without sticking strictly to the set points originally suggested by engineers.
* A gazelle calf struggles to its feet minutes after being born. Half an hour later it is running at 20 miles per hour.
* Teaching a dog a new trick--one cannot tell it what to do, but one can reward/punish it if it does the right/wrong thing. It has to figure out what it did that made it get the reward/punishment, which is known as the credit assignment problem.

Reinforcement learning is like trial and error learning. The agent should discover a good policy from its experiences of the environment without losing too much reward along the way. Exploration is about finding more information about the environment while Exploitation exploits known information to maximize reward. For example: Restaurant selection: Exploitation; go to your favorite restaurant. **Exploration**; try a new restaurant. Oil drilling: **Exploitation**; drill at the best-known location. Exploration; drill at a new location.
