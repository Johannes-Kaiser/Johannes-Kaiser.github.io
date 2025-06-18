---
title: "Reconstruction attacks on Genetic Data"
collection: teaching
type: "WS23/24 Practical: Applied Deep Learning in Medicine"
layout: teaching
permalink: /teaching/ADLM_WS_23_24
venue: "TUM"
date: 2024-04-01
location: "Munich, Germany"
image: /images/Teaching/Thumbnail_Gene_Rec.png   # path to slide/poster image
pdf: /files/Teaching/Gene_Reconstuction.pdf    # path to PDF file
---

This work shows that training data with higher spatial correlation, such as medical images, is more vulnerable to gray-box model inversion attacks than unstructured data like genetic profiles.

With growing concerns over data privacy in machine learning, this study explores how spatial correlation in training data affects the success of gray-box model inversion attacks—where an attacker attempts to reconstruct training samples using only a model’s weights. The researchers compared two data types: medical images with inherent spatial structure and genetic (tabular) data without.

Using a reconstruction pipeline based on Haim et al., we found that medical images, especially those with high inter-class variance, could be reconstructed with notable accuracy. In contrast, gene expression data—even after dimensionality reduction—resulted in poor reconstructions, despite high classifier accuracy in some cases.

To explain this gap, we ran controlled experiments with synthetic images containing varying levels of spatial correlation. Results showed a clear link: greater spatial correlation led to lower reconstruction error.

The study concludes that data with strong spatial patterns is more vulnerable to inversion attacks, whereas tabular data like genetic information offers greater resistance, highlighting an important factor in assessing model privacy risks.