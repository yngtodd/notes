==================================================================
A Tour of Reinforcement Learning: The View from Continuous Control
==================================================================

**Author:** Ben Recht
**Date:** 2018

Abstract
--------

This manuscript surveys reinforcement learning from the perspective of optimization 
and control with a focus on continuous control applications. It surveys the general 
formulation, terminology, and typical experimental implementations of reinforcement 
learning and reviews competing solution paradigms.



4. Simplifying theme: The Linear Quadratic Regulator
----------------------------------------------------

"I’d argue that in controls, the simplest non-trivial class of instances of optimal 
control is those with convex quadratic rewards and linear dynamics. That is, the 
problem of the Linear Quadratic Regulator (LQR):"

#ToDo: add maths.

**Cross-reference with blog:** http://www.argmin.net/2018/02/08/lqr/


6 Beyond the Linear Quadratic Regulator
---------------------------------------

- Studying simple baselines such as LQR often give us insights into how to approach 
  more challenging problems. In this section, we explore some directions inspired by 
  our analysis of LQR.

**6.1 Derivative Free Methods for Optimal Control**

* "Random search works well on simple linear problems and appears better than more complex 
  methods like policy gradient. Does simple random search work less well on more difficult problems?
  The answer, it turns out, is yes. The deep RL community has recently been using a suite of 
  benchmarks to compare methods, maintained by OpenAI2 and based on the MuJoCo simulator [80]."

* Recht, Guy, and Mania showed that random search, supplemented by whitened statistics of 
  the MuJoCo simulation states, was able to get state of the results on all MuJoCo benchmarks.

  * "There are a few of important takeaways from their study. On the one hand, the results suggest 
    that these MuJoCo demos are easy, or at least considerably easier than they were believed to be. 
    Benchmarking is difficult, and having only a few simulation benchmarks encourages overfitting 
    to these benchmarks."
  * "All model-free methods exhibit alarmingly high variance on these benchmarks. For instance, 
    on the humanoid task, the the model is slow to train almost a quarter of the time even when 
    supplied with what we thought were good parameters (see Figure 4 (middle))."

    * "Henderson et al and Islam et al observed this phenomenon with deep reinforcement learning methods, 
      but our results on linear controllers suggest that such high variability will be a symptom of all 
      model-free methods [35, 36]. Though direct policy search methods are easy to code up, their 
      reliability on any reasonable control task remains in question."


