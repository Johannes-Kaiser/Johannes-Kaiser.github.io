---
title: 'On the Hypothesis Testing Perspective of DP'
date: 2025-07-02
permalink: /posts/2025/07/Bayesian_DP_1/
tags:
  - DP
  - Hypothesis Testing
---
Differential privacy in essence tries to protect an adversary of distinguishing weather a datapoint was present in an the output of the randomized mechanism underlying data.
Therefore it naturally alligns with an Hypothesis testing interpretation with given the outputs of the either $M(S)$ or $M(S')$:
    <p align="center">
    $H_0$: the underlying data set is $S$  
    $H_1$: the underlying data set is $S'$
    </p>
Differential privacy can be measured in terms of the advantage in predicitive performance in this hypothesis testing problem.

The goal of the adversary can also be framed in finding a rejection rule $\phi$ which **optimally** trades of type I (FNR; the underlying data set does not include the sample of interest ($S$) hower the adversary assumes, that it does ($S'$)) and type II errors (FPR; the underlying data set does include the sample of interest ($S'$) hower the adversary assumes, that it does not ($S$)) in an optimal way.

For a fixed type I error finding the optimal (i.e., lowest) type II error (finding the optimal $\phi$) corresponds to **finding the strategy that for a given FNR yields the lowest FPR and thus the hightes TPR**.

## Trade-off Functions

The best possible rejection rule $\phi$ accessible to the adversary is bounded by a tradeoff function:
<!-- Assuming the information on which the adversary bases their rejection rule is gaussian (which is often the case due to the central limit theorem and domination of distributions): -->
> **Definition 3.2 (Trade-off Function).**  
> For any two probability distributions $P$ and $Q$ on the same space, the trade-off function is defined as:
>
> $$
> T(P, Q) : [0, 1] \to [0, 1], \quad T(P, Q)(\alpha) = \inf\{\beta_\phi : \alpha_\phi \leq \alpha\}
> $$
>
> where the infimum is taken over all (measurable) rejection rules, and $\alpha_\phi$ and $\beta_\phi$ are the type I and type II errors for the rejection rule $\phi$.


## Relating Trade-off Functions to differential Privacy
DP bounds these trade-off function and consequently limits the best rejection rule available to the adversary.

> **Definition 3.3 ($f$-Differential Privacy).**  
> Let $f$ be a trade-off function. A mechanism $M$ is $f$-differentially private if for all neighbouring data sets $S$ and $S'$:
>
> $$
> T(M(S), M(S')) \geq f
> $$
>
> That is, the trade-off function between the outputs of $M$ on any pair of neighbouring data sets is lower bounded by $f$.

This definition can be interpreted, that if an aglorithm is $f$-DP,  $f$ bounds all potential tradeoff functions existant on the dataset. 
With the tradeoff function bounding the performance of the rejection rule of an adversary (they are the optimal rejection rule an adversary can choose), this entails, that $f$ also bounds these and consequently the advantage of an adversary.

For a specific $\varepsilon$, $\delta$ pair as used to describe DP, the *trade-off function* i.e., the lowest type II error at given type I error can be described as:

> **Lemma 3.4 (Wasserman and Zhou [2010], Kairouz et al. [2017]).**  
> Suppose $M$ is an $(\varepsilon, \delta)$-differentially private algorithm. Then, for a false positive rate of $\alpha$, the trade-off function is:
>
> $$
> f_{\varepsilon, \delta}(\alpha) = \max\left\{0,\ 1 - \delta - e^{\varepsilon} \alpha,\ e^{-\varepsilon}(1 - \delta - \alpha)\right\}
> $$

However, this is miseading.
The $(\varepsilon, \delta)$-DP framework constrains the adversary's inference about privacy to a fixed $\delta$. However, $\delta$ is not a tunable parameter; for any mechanism, there is a corresponding $\varepsilon$ for each $\delta$. In contrast, the $f$-DP formulation does not depend on calibrating to a particular $\delta$. Instead, the true trade-off function of a mechanism is given by the lower envelope of all $(\varepsilon, \delta)$-based trade-off functions across all possible $\delta$ values.

<!-- Often, it is assumed, that the adversary has a balanced prior between these two hypothesis i.e., the prior porbability of a datapoint being and not being in the dataset is assumed to be the same.
However, this potentially diverges from the real setting in which an adversary querries large amounts of data knowing, that only few will be contained in the data set the attacked mechanism bases its output on.



## Priors in DP
- Often DP assumes a balanced Prior i.e., TODO
- However the prior of an adversary can be skewed
    - The adversary values true positives much more highly than false positives or similar
    - The adversary has their own data distribution on which he performs MIA
 -->
