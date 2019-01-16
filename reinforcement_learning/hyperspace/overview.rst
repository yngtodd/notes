========
Overview
========

General notes to guide the HyperSpace journal paper.

Model Comparison
----------------

I see this as a major contribution of the paper.

**General questions:**

* When are RL algorithms equivalent? 
* What if the performance of the algorithms swap if we switch to
  a new environment?
* What are our baselines across tasks?

**Proposals:**

* Baselines could consist of random search for for policy methods and
  the Linear Quadratic Regulator (LQR)

  * Important distinction: random search in the space of policies here,
    not in the space of hyperparameters.
  * LQR was the driver for Ben Recht's *Tour of RL* paper

* Performance profiles, proposed by Dolan and More. Noted by Ben Recht.

Questions:

* What would happen if we ran the performance profiles across the top k
  models found by HyperSpace? How would they compare with the baselines?

Reproducibility
---------------

* How do we account for the stochastic nature of RL experiments?
 
  * The interaction between the RL algorithm and the environment 
    could change between runs without controlling initialization of 
    weights, and all random seeds.
