# Adaptive Memory for Online Reinforcement Learning under Sparse Model Changes
<p align="center">
  <img src="https://github.com/sreejeetm1729/Adaptive-Memory-for-Online-RL-under-Sparse-Model-Changes-/blob/main/Deploy-1.png"
       alt="Figure 2" width="1400">
</p>

We study the discounted reinforcement learning
(RL) problem in a setting where the underlying environment
changes between deployments. Each deployment provides H
observations from a fixed MDP. The reward function and
transition kernel are fixed within each deployment. Across
deployments, at most an ϵ > 0 fraction of the reward and
transition kernel entries may change. In this setting, learning
each model to deploy from scratch may discard useful
observations from past deployments, whereas pooling all past
observations can bias the estimates of entries that have already
changed. We then propose an algorithm that for each state
and action pair, selects how much history to reuse to estimate
the reward and probabilities of the next state. We start with
observations from the current deployment and add earlier
deployment observations one at a time, the most recent first.
After each addition, we check whether a single average reward
agrees with the estimates from all histories considered until
that point. We apply the same check to the distribution of next
states. For each estimate, we leverage the last history that passes
these aforementioned checks. The optimal control policy is then
computed on top of the fitted MDP. We characterize the average
gap between the optimal return and the return of the learner’s
policies over a finite number of deployments.

<p align="center">
  <img src="https://github.com/sreejeetm1729/Adaptive-Memory-for-Online-RL-under-Sparse-Model-Changes-/blob/main/Deploy-2.png"
       alt="Figure 2" width="400">
  <img src="https://github.com/sreejeetm1729/Adaptive-Memory-for-Online-RL-under-Sparse-Model-Changes-/blob/main/Deploy-3.png"
       alt="Figure 1" width="400">
</p>
