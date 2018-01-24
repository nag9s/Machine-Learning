This is the scenario in which multiple decisions need to be taken by an agent prior to reaching the target and it provides a reward, either +1 or -1, rather than notifying how well or how badly the agent performed across the path:

**From Practical Machine Learning Cookbook**

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

From [https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/551f9654-1fbf-41fd-8088-a7dbd1dc3ab1.xhtml](https://www.safaribooksonline.com/library/view/statistics-for-machine/9781788295758/551f9654-1fbf-41fd-8088-a7dbd1dc3ab1.xhtml)

Reinforcement learning mimics how humans learn: by interacting with environment, repeating actions for which the reward that is received is higher, and avoiding risky moves for which there is a low or negative reward as an outcome of their actions.

Reinforcement learning Models

* Markov chains - the stocks regime switching model
* Markov chains - the multi-channel attribution model
* Markov chains - the car rental agency service
* Continuous Markov chains - vehicle service at the gas station
* Monte Carlo simulations - calibrated hull and white short-rates
* Bellman equations
* Dynamic programming
* Temporal difference learning

> [https://www.quora.com/What-are-some-practical-applications-of-reinforcement-learning](https://www.quora.com/What-are-some-practical-applications-of-reinforcement-learning)
>
> Nice Example from quora

Suppose you have a dog that is not so well trained, every time the dog messes up the living room you reduce the amount of tasty foods you give it \(punishment\) and every time it behaves well you double the tasty snacks \(reward\). What will the dog eventually learn? Well, that messing up the living room is bad.

This simple concept is powerful. **The dog is the agent, the living room the environment**, you are the source of the reward signal \(tasty snacks\). You are giving feedback to the dog, but this feedback is vague it doesn't mean anything without the context. So eventually the dog's neural networks figure out the relationship between the tasty snacks and good behavior.

So in order for the dog to maximize the goal of eating more tasty snacks, it will simply behave well, never to mess with the living room again. So you can apply RL to non-computer related problems, such as this dog-living room example. Every biological entity has reinforcement learning \(RL\) built in, humans, cats and many more use it. That is why RL, if solved, can be a very powerful tool for artificial intelligence \(AI\) applications in fields like self-driving cars.

It is pretty "heavily" used in robotics





From https://www.safaribooksonline.com/library/view/apache-spark-2x/9781787126497/74757d2e-dd20-4d7a-8531-2d31716f091e.xhtml



 **Reinforced learning is used in artificial intelligence and its related fields. It allows machines and software agents to automatically determine the ideal behavior within a specific context, in order to maximize its performance.**

