========================================
Deep Reinforcement Learning that Matters
========================================

**Authors:** Peter Henderson1, Riashat Islam, Philip Bachman, 
Joelle Pineau, Doina Precup, David Meger

**Date:** 2017

Abstract
--------

In recent years, significant progress has been made in solving challenging 
problems across various domains using deep re- inforcement learning (RL). 
Reproducing existing work and accurately judging the improvements offered by 
novel methods is vital to sustaining this progress. Unfortunately, reproducing 
results for state-of-the-art deep RL methods is seldom straightforward. In 
particular, non-determinism in standard benchmark environments, combined with 
variance intrinsic to the methods, can make reported results tough to interpret. 
Without significance metrics and tighter standardization of experimental reporting, 
it is difficult to determine whether im- provements over the prior state-of-the-art 
are meaningful. In this paper, we investigate challenges posed by reproducibility, 
proper experimental techniques, and reporting procedures. We illustrate the 
variability in reported metrics and results when comparing against common baselines 
and suggest guidelines to make future results in deep RL more reproducible. We 
aim to spur discussion about how to ensure continued progress in the field by 
minimizing wasted effort stemming from results that are non-reproducible and 
easily misinterpreted.

Introduction
------------

* "To maintain rapid progress in RL research, it is important that existing works 
  can be easily reproduced and compared to accurately judge improvements offered 
  by novel methods. However, reproducing deep RL results is seldom straightforward, 
  and the literature reports a wide range of results for the same baseline algorithms
  (Islam et al. 2017)."

* Reproducibility can be affected by extrinsic factors (hyperparameters) and intrinsic
  factors (random seeds and environment properties).

* Paper focuses on *policy gradient methods*.

* "We note that the diversity of metrics and lack of significance testing in the 
  RL literature creates the potential for misleading reporting of results. We 
  demonstrate possible benefits of significance testing using techniques common 
  in machine learning and statistics."

  * How does this line up with the performance profiles of Dolan and More?

Experimental Analysis
---------------------

* "For most of our experiments1, except for those com- paring codebases, we generally 
  use the OpenAI Baselines2 implementations of the following algorithms: 
  ACKTR (Wu et al. 2017), PPO (Schulman et al. 2017), DDPG (Plappert et al. 2017), 
  TRPO (Schulman et al. 2017). We use the Hopper- v1 and 
  HalfCheetah-v1 MuJoCo (Todorov, Erez, and Tassa 2012) environments from 
  OpenAI Gym (Brockman et al."

**Hyperparameters**

* Hyperparameters are varied one at a time.

Discussion and Conclusion
-------------------------

* "Based on our experimental results and investigations, we can provide some general 
  recommendations. Hyperparameters can have significantly different effects across 
  algorithms and environments. Thus it is important to find the working set which at 
  least matches the original reported perfor- mance of baseline algorithms through 
  standard hyperparame- ter searches."

Supplemental Material
---------------------

This section is a gold mine for details on baselines, hyperparameter configurations, and
their literature review. Following their lead here would be a good idea. 


