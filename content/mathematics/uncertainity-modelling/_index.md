---
weight: 1
title: Uncertainity Modelling
---

<div style="text-align: justify;">

# Introduction

This notes gives a overview of Probability and Statistics and its applications in modelling uncertainities and randomness. Some topics will be dealt deeper mathematically, but the overall idea is to provide intuition about the various concepts and touch upon the applications.

# Expected Outcomes

The following are the expected outcomes:

- Define a random variable and probability distribution / density functions
- Define expectation, mean and variance
- Calculate the theoretical expectations of random variables and their functions
- Numerically compute the expectation of a random variable (or its function)
- Role of probability and statistics in estimation
- Define joint, marginal and conditional probability density functions
- Define and explain conditional expectation
- Define and compute theoretical covariance / correlation

# Prerequisites

A basic course in Calculus and Set Theory.

# Why Probability and Statistics are studied together?

Probability and Statistics are related areas of mathematics which concern themselves with analyzing the relative frequency of events. Still, there are fundamental differences in the way they see the world:

- Probability deals with predicting the likelihood of future events, while statistics involves the analysis of the frequency of past events.

- Probability is primarily a theoretical branch of mathematics, which studies the consequences of mathematical definitions. Statistics is primarily an applied branch of mathematics, which tries to make sense of observations in the real world.

Both subjects are important, relevant, and useful. But they are different, and understanding the distinction is crucial in properly interpreting the relevance of mathematical evidence. Many a gambler has gone to a cold and lonely grave for failing to make the proper distinction between probability and statistics.

This distinction will perhaps become clearer if we trace the thought process of a mathematician encountering her first craps game:

- If this mathematician were a probabilist, she would see the dice and think six-sided dice? Presumably each face of the dice is equally likely to land face up. Now assuming that each face comes up with probability 1/6, I can figure out what my chances of crapping out are.

- If instead a statistician wandered by, she would see the dice and think ``Those dice may look OK, but how do I know that they are not loaded? I'll watch a while, and keep track of how often each number comes up. Then I can decide if my observations are consistent with the assumption of equal-probability faces. Once I'm confident enough that the dice are fair, I'll call a probabilist to tell me how to play.

`In summary, probability theory enables us to find the consequences of a given ideal world, while statistical theory enables us to to measure the extent to which our world is ideal.`

> Probability is top-down (going from pure distributions to predictions about events) and statistics is bottom-up (going from specific events to predicting pure distributions)

The probabilist can tell you what to infer about the data, given the model; the statistician can tell you what to infer about the model, given the data. `Probability theory is the study of theoretical random processes in which everything is known in principle.` Problems in probability theory involve being given some of the attributes of a theoretical random process and being asked to solve for others that are related.

Statistics is two completely different subjects.

- Descriptive statistics is the study of the descriptions and properties of probability distributions themselves, theoretical or empirical.

- Inferential statistics is the study of what can be told about a random process of which all or part is unknown, by examining one or more samples.

# Notation

# References

# Contents

- [Review of Set Theory and Calculus](shared/Prerequisite.md)
- [Probability](probability/Probability.md)
  - [Experiment or Trail](probability/Probability.md#experiment-or-trail)
  - [Random variables](probability/Probability.md#random-variable)
  - [Sample space vs Event Space](probability/Probability.md#sample-space-vs-event-space)
  - [Probability Approach](probability/Probability.md#probability-approach)
  - [Population vs Sample](probability/Probability.md#population-vs-sample)
  - [Emprical estimation](probability/Probability.md#emprical-estimation)
- [Laws of Probability](probability/Laws%20of%20Probability.md)
  - [Axioms](probability/Laws%20of%20Probability.md#axioms)
  - [Conditional Probability](probability/Laws%20of%20Probability.md#conditional-probability)
  - [Independence](probability/Laws%20of%20Probability.md#independence)
  - [Improbable vs Impossible](probability/Laws%20of%20Probability.md#improbable-vs-impossible)
- [Distribution and Density functions](probability/Distribution%20and%20Density%20functions.md)
- [Moments of a distributions](Co-variance.md)
- [General functions of a Random variable](Co-variance.md)
- [MMSE](Co-variance.md)
- [Conditional probability](Co-variance.md)
- [Joint probability](Co-variance.md)
- [CoVariance](Co-variance.md)
- [$\sigma$-algebra and Measurable spaces](probability/Sigma%20algebra%20and%20Measurable%20spaces.md)
</div>
