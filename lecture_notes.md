# Lecture Notes

## Introduction to RL

sequential decision making under uncertainty
- optimization
- delayed consequences, but temporal credit assignment is hard
- exploration, but there would be no info about path not taken (censoring)
- generalization

ai planning:
- https://en.wikipedia.org/wiki/Automated_planning_and_scheduling
- e.g. alpha go, doesn't need exploration since the model of the world is given

imitatition learning:
- https://drive.google.com/file/d/12QdNmMll-bGlSWnm8pmD_TawuRN7xagX/view
- assumes input of good policies e.g. Ng's helicopter learning
- reduces RL to supervised learning
- benefits: avoids exploration problem, lots of data, supervised learning has good tools
- limitation: expensive, limited by data collected
- imiation learning + RL can be good

seq learning under uncertainty
- maximizing **expected** future reward

assumptions
1. state is just a function of the history (action, observation, reward), but this might omit certain information
2. agent might not have access to world state, but it has its own state space
3. markov assumption: agent's state info is a sufficent statistic of history
4. assume you can make the system markov by including enough history

- **full observability** / mdp : world state = observation
- **partial observatbility** / POMDP : uses prior beliefs to aggregate / cluster info and make decisions
- **bandits**: actions have no influence of next observations, no delayed rewards
- mdp, pomdp: actions affect future observations
- finite vs infinite horizon vs indefinite horizon

agents
- model-based agents - explicit model butt may or may not have policy or value function
- model free: explicit value function and policy function
fundamental differences in model based/free approaches by MSR

how the world changes: deterministic, stochastic (representing hard to model processes)

components
1. **model**: next state given statet and action; prediction of immediate reward
2. **policy**: mapping from state to action (can be deterministic or stochastic)
3. **value**: expected discounted sum of future rewards under particular policy

reward function:
r(s), r(s, a), r(s, a, s')

evaluation and control:
- evaluation: est & pred expected rewards from given policy
- control: find the best policy





