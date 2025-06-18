---
title: "Cascade Learning for Group-Specific Medicine: A Multi-Stage Approach"
collection: teaching
type: "WS24/25 Practical: Applied Deep Learning in Medicine"
layout: teaching
permalink: /teaching/ADLM_WS_24_25
venue: "TUM"
date: 2025-04-01
location: "Munich, Germany"
image: /images/Teaching/Thumbnail_Cascade.png   # path to slide/poster image
pdf: /files/Teaching/Cascade.pdf    # path to PDF file
---

Computer-aided diagnosis systems are a powerful tool for
physicians to support the identification of diseases in medical images.

However, the ’one-model-fits-all’ approach is not optimal for highly het-
erogeneous data, as it is common in medical imaging. This work proposes
a cascading model for the group-specific classification of chest radio-
graphs. The model consists of a classification stage, predicting the group,
and multiple group-specific models, predicting the observations. 

The model is evaluated on the CheXpert dataset, split by view (FR/LAT) and
the frontal view direction (AP/PA). The results show that the cascading
models achieve comparable or slightly superior multi-label performance
to ’one-model-fits-all’ approaches while offering additional advantages,
such as efficiency gains and selective retraining of specific modules. The
single-label performance of the multi-stage models was slightly better
than the baseline models in most conditions. 

The modular nature of these models allows for selective retraining of only specific modules after
new data acquisition and faster training times. Future models could in-
corporate domain knowledge more explicitly into the model architecture
and develop specialized architectures optimized for each view type.