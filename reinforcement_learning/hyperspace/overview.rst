========
Overview
========

General notes to guide the HyperSpace journal paper.

Model Comparison
----------------

**General questions:**

* When is a DQN equivalent to SARSA?
* What if the performance of the algorithms swap if we switch to
  a new environment?

**Proposals:**

* Performance profiles, proposed by Dolan and More. Noted by Ben Recht.

Questions:

* What would happen if we ran the performance profiles across the top k
  models found by HyperSpace? How would they compare with the baselines?

Reporducibility
---------------

* How do we account for the stochastic nature of RL experiments?
  
    The interaction between the RL algorithm and the environment 
    could change between runs without controlling initialization of 
    weights, and all random seeds.
