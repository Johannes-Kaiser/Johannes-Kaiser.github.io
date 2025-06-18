---
title: "Addressing Accuracy-Fairness Trade-off via Laplace Approximation Methods"
collection: teaching
type: "Master Thesis"
layout: teaching
permalink: /teaching/ADLM_MA_MM
venue: "TUM"
date: 2025-04-01
location: "Munich, Germany"
image: /images/Teaching/Thumbnail_MA_MM.png   # path to slide/poster image
pdf:     # path to PDF file
---

The increasing deployment of machine learning models in critical domains such as finance, criminal justice, and healthcare has raised concerns about the ethical implications
of these systems. 

One of the primary ethical challenges is to ensure that these models
are fair and unbiased. Training multiple models and choosing the best one based on
fairness metrics is one of the traditional approaches for achieving fairness, which can
be computationally expensive and time-consuming. 

This thesis introduces a novel
approach called the Laplace Approximation-Based Model Selection Framework. The
framework leverages Laplace Approximation-based (LA) methods, which are employed
to approximate Bayesian Neural Networks (BNNs), and its extension of Riemannian
Laplace Approximation (RLA) in the context of Machine Learning model selection
to address accuracy-fairness trade-off. 

Leveraging LA and RLA allows us to sample
multiple models from a distribution generated using a pre-trained model. Therefore,
with minimal overhead, we have the option to select an optimum model from a set of
models that have similar predictive accuracy scores but various fairness characteristics.
We evaluated the effectiveness of the proposed framework through a series of experiments. 

The results demonstrated that, to some extent, it can produce models with
improved fairness scores without compromising accuracy. The experiments showed
that LA and RLA approaches require 173.46 and 8.08 times less time to generate 500
models compared to the Retraining method, respectively. This thesis contributes to the
development of ethical AI by exploring and offering a practical and efficient solution
to the problem of model fairness with the potential of extending it to a wide range of
applications.