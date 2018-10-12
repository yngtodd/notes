======================
Structure of the Paper
======================

Prototype for the narrative structure of the paper.

Introduction
------------

Questions to be answered:

* Are RL algorithms sensitive to model hyperparameters?
* How do we do model comparison in this field; what is 
  the evidence that one model outperforms another?

**References:**

* Deep RL that Matters - Henderson et al
* Where did my Gradient go? Henderson et al

Related Work
------------

**References:**

* Population Based Training
* Hyperparameter optimization for tracking with DQN


Methods
-------

Use HyperSpace for 2-3 recent RL algorithms on the ALE or
another Open AI baseline. Compare with original baselines with
known hyperparameters, plus random search, Bayesian optimization,
and HyperBand.

* Bootstrap over different initial conditions?
* Compare using performance profiles (Dolan and More)

**References:**

* Benchmarking Optimization Software with Performance Profiles - Dolan and More
* Revisiting Arcade Learning Environment - Machado et al

Experiments
-----------

1. Starter Example: Linear Quadratic Regulator
 
   * Make a connection with Ben Recht's *Tour of RL* paper. 
   * Mention the connection between RL and control?
