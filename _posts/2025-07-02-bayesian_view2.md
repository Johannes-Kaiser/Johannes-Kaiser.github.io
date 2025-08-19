---
title: 'Bayesian view on DP'
date: 2025-07-02
permalink: /posts/2025/07/Hypo_1/
tags:
  - DP
  - Bayesian
---

Often, it is assumed, that the adversary has a balanced prior between these two hypothesis i.e., the prior porbability of a datapoint being and not being in the dataset is assumed to be the same.
However, this potentially diverges from the real setting in which an adversary querries large amounts of data knowing, that only few will be contained in the data set the attacked mechanism bases its output on.

Consequently a membership inference game taking this prior into consideration can be defined as follows.

The adversary runs this experiment:

1. Sample a training set $S \sim D^n$ and train a model $M_S$ on $S$.
2. Randomly sample $b \in \{0, 1\}$, where $b = 1$ with probability $p$.
3. If $b = 1$, sample $z \sim S$; otherwise, sample $z \sim D$.
4. Output $1$ if $A(z, M_S, n, D) = b$; otherwise, output $0$.

This prior can be very small as often the mechanism operates on a very small subset of data that is available from the data distribution.
To exemplify this: Assume a neural network is trained on data from selected individuals admitted to a hospital -- the non-members are thus constituated from the remaining population of the city/ district/ country etc. making p very small.

## Analysing the Advantage of an Adversary

For any prior, the maximal advantage an adversary can gain by querying the response of a randomized mechanism is defined as:

**Theorem 4.1.**  
Let $M$ be an $(\varepsilon, \delta)$-differentially private algorithm. For any randomly chosen record $z$ and fixed false positive rate $\alpha$, the membership advantage of a membership inference adversary $A$ is bounded by:
$$
\text{Adv}_A(\alpha) \leq 1 - f_{\varepsilon, \delta}(\alpha) - \alpha,
$$
where
$$
f_{\varepsilon, \delta}(\alpha) = \max \left\{ 0, 1 - \delta - e^{\varepsilon} \alpha, e^{-\varepsilon}(1 - \delta - \alpha) \right\}.
$$

In essence, at a predefined $\alpha$ (the defined FNR), an adversary gains an advantage that is proportional to the change in FPR of an optimal reject strategy of the underlying hypothesis test.

While this bound holds for any $\varepsilon$, $\delta$ - calibrated method, mechanisms are defined on all $\delta$ and consequently to reason about a mechanism, the advantage of an adversary is defined as:

**Theorem 4.1.**  
Let $M$ be an $(\varepsilon, \delta)$-differentially private algorithm. For any randomly chosen record $z$ and fixed false positive rate $\alpha$, the membership advantage of a membership inference adversary $A$ is bounded by:
$$
\text{Adv}_A(\alpha) \leq 1 - T(M(S), M(S'))(\alpha) - \alpha,
$$
where $T_{M(S), M(S')}$ denotes the trade-off curve of the mechanism $M$ evaluated on a pair of neighboring datasets $S, S'$ (i.e., datasets differing in a single element) that realize the worst-case privacy loss.

Remark:
Diverging from our prior assumption of fixed (and skewed) prior, this allows to find the highest adversary advantage as the supremum over $\alpha$:
$$
\sup_{\alpha} \left[ 1 - T(M(S), M(S'))(\alpha) - \alpha \right]
$$

The power of an attack can be measured with the positive predictive value of the attack (PPV) indicating on how many of the positive predictions are true positives.
To operationalize this on skewed underlying distributions the more weight is given to false positive predictions (why?).
Consequently the PPV can be describeds as:

**Theorem 4.2.**  
Let $M$ be an $(\varepsilon, \delta)$-differentially private algorithm and $A$ be a membership inference adversary. For any randomly chosen record $z$ and a fixed false positive rate $\alpha$, the positive predictive value of $A$ is bounded by:
$$
\mathrm{PPV}_A(\alpha, \gamma) \leq \frac{1 - f_{\varepsilon, \delta}(\alpha)}{1 - f_{\varepsilon, \delta}(\alpha) + \gamma \alpha},
$$
where $f_{\varepsilon, \delta}(\alpha) = \max \left\{ 0, 1 - \delta - e^{\varepsilon} \alpha, e^{-\varepsilon}(1 - \delta - \alpha) \right\}$, $\gamma = \frac{1-p}{p}$, and $p$ is the prior membership probability defined in Membership Experiment 4.1.

## Comparing Mechanisms




## Priors in DP
- Often DP assumes a balanced Prior i.e., TODO
- However the prior of an adversary can be skewed
    - The adversary values true positives much more highly than false positives or similar
    - The adversary has their own data distribution on which he performs MIA

