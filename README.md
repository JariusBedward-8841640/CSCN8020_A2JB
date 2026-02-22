
The Taxi environment contains:
- 500 discrete states
- 6 discrete actions
- Reward structure:
  - -1 per step
  - +20 for correct passenger drop-off
  - -10 for illegal pickup or drop-off

The objective is to learn an optimal policy that maximizes cumulative reward by efficiently transporting passengers.

---

## Reinforcement Learning Formulation

- Agent: Taxi
- Environment: Taxi-v3 grid world
- State Space: 500 discrete states
- Action Space: 6 discrete actions
- Policy: ε-greedy
- Value Function: Q(s,a)
- Learning Type: Model-Free, Off-policy, Temporal Difference Learning

We use the Q-Learning update rule:

Q(s,a) ← Q(s,a) + α [r + γ max_a' Q(s',a') − Q(s,a)]

Where:
- α = learning rate
- γ = discount factor
- ε = exploration factor