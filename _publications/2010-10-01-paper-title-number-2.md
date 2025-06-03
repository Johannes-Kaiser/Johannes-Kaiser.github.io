---
title: "Laplace Sample Information: Data Informativeness Through a Bayesian Lens"
collection: publications
permalink: /publication/LSI
excerpt: 'This paper introduces LSI a novel measure of data informativeness founded in information theory.'
date: 2025-05-02
venue: 'ICLR'
paperurl: 'https://arxiv.org/pdf/2505.15303?'
citation: 'Kaiser, J., Schwethelm, K., Rueckert, D., & Kaissis, G. Laplace Sample Information: Data Informativeness Through a Bayesian Lens. In The Thirteenth International Conference on Learning Representations.'
---
Accurately estimating the informativeness of individual samples in a dataset is
an important objective in deep learning, as it can guide sample selection, which
can improve model efficiency and accuracy by removing redundant or potentially
harmful samples. We propose Laplace Sample Information (LSI) measure of sample
informativeness grounded in information theory widely applicable across model
architectures and learning settings. LSI leverages a Bayesian approximation to the
weight posterior and the KL divergence to measure the change in the parameter
distribution induced by a sample of interest from the dataset. We experimentally
show that LSI is effective in ordering the data with respect to typicality, detecting
mislabeled samples, measuring class-wise informativeness, and assessing dataset
difficulty. We demonstrate these capabilities of LSI on image and text data in
supervised and unsupervised settings. Moreover, we show that LSI can be computed
efficiently through probes and transfers well to the training of large models

[Download paper here](https://arxiv.org/pdf/2505.15303?)

Recommended citation: 
Kaiser, J., Schwethelm, K., Rueckert, D., & Kaissis, G. 
Laplace Sample Information: Data Informativeness Through a Bayesian Lens. 
In The Thirteenth International Conference on Learning Representations.