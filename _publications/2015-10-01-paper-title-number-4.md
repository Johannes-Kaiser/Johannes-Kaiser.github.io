---
title: "Visual Privacy Auditing with Diffusion Models"
collection: publications
permalink: /publication/VisualPrivacy
excerpt: 'This paper explores a threat model, where the attacker has knowledge about the underlying data distribution'
date: 2025-04-10
venue: 'TMLR'
paperurl: 'https://arxiv.org/pdf/2403.07588'
citation: 'Schwethelm, K., Kaiser, J., Knolle, M., Lockfisch, S., Rueckert, D., & Ziller, A. (2024). Visual Privacy Auditing with Diffusion Models. arXiv preprint arXiv:2403.07588.'
---
Data reconstruction attacks on machine learning models pose a substantial threat to pri-
vacy, potentially leaking sensitive information. Although defending against such attacks
using differential privacy (DP) provides theoretical guarantees, determining appropriate DP
parameters remains challenging. Current formal guarantees on the success of data recon-
struction suffer from overly stringent assumptions regarding adversary knowledge about
the target data, particularly in the image domain, raising questions about their real-world
applicability. In this work, we empirically investigate this discrepancy by introducing a re-
construction attack based on diffusion models (DMs) that only assumes adversary access to
real-world image priors and specifically targets the DP defense. We find that (1) real-world
data priors significantly influence reconstruction success, (2) current reconstruction bounds
do not model the risk posed by data priors well, and (3) DMs can serve as heuristic auditing
tools for visualizing privacy leakage.

[Download paper here](https://arxiv.org/pdf/2403.07588)

Recommended citation: 
Schwethelm, K., Kaiser, J., Knolle, M., Lockfisch, S., Rueckert, D., & Ziller, A. (2024). 
Visual Privacy Auditing with Diffusion Models. 
arXiv preprint arXiv:2403.07588.