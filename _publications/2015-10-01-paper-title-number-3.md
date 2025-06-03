---
title: "Differentially Private Active Learning: Balancing Effective Data Selection and Privacy"
collection: publications
permalink: /publication/DPAL
excerpt: 'This paper explores and compares different approaches for active learning in differential privacy'
date: 2025-04-10
venue: 'SatML'
paperurl: 'https://arxiv.org/pdf/2410.00542'
citation: 'Schwethelm, K., Kaiser, J., Kuntzer, J., Yiğitsoy, M., Rückert, D., & Kaissis, G. (2025, April). Differentially Private Active Learning: Balancing Effective Data Selection and Privacy. In 2025 IEEE Conference on Secure and Trustworthy Machine Learning (SaTML) (pp. 858-878). IEEE.'
---
Active learning (AL) is a widely used technique
for optimizing data labeling in machine learning by iteratively
selecting, labeling, and training on the most informative data.
However, its integration with formal privacy-preserving methods,
particularly differential privacy (DP), remains largely underex-
plored. While some works have explored differentially private
AL for specialized scenarios like online learning, the fundamental
challenge of combining AL with DP in standard learning settings
has remained unaddressed, severely limiting AL’s applicability
in privacy-sensitive domains. This work addresses this gap by
introducing differentially private active learning (DP-AL) for
standard learning settings. We demonstrate that naively inte-
grating DP-SGD training into AL presents substantial challenges
in privacy budget allocation and data utilization. To overcome
these challenges, we propose step amplification, which leverages
individual sampling probabilities in batch creation to maximize
data point participation in training steps, thus optimizing data
utilization. Additionally, we investigate the effectiveness of var-
ious acquisition functions for data selection under privacy con-
straints, revealing that many commonly used functions become
impractical. Our experiments on vision and natural language
processing tasks show that DP-AL can improve performance for
specific datasets and model architectures. However, our findings
also highlight the limitations of AL in privacy-constrained en-
vironments, emphasizing the trade-offs between privacy, model
accuracy, and data selection accuracy.

[Download paper here](https://arxiv.org/pdf/2410.00542)

Recommended citation: 
Schwethelm, K., Kaiser, J., Kuntzer, J., Yiğitsoy, M., Rückert, D., & Kaissis, G. (2025, April). 
Differentially Private Active Learning: Balancing Effective Data Selection and Privacy. 
In 2025 IEEE Conference on Secure and Trustworthy Machine Learning (SaTML) (pp. 858-878). IEEE.