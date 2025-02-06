---
title: "Adapted-MoE: Mixture of Experts with Test-Time Adaption for Anomaly Detection"
collection: publications
category: conferences
permalink: #/publication/2009-10-01-paper-title-number-1
excerpt: #'This paper is about the number 1. The number 2 is left for future work.'
date: 2024-08-15
venue: 'Arxiv'
slidesurl: #'http://academicpages.github.io/files/slides1.pdf'
paperurl: 'https://arxiv.org/pdf/2409.05611'
citation: 'Lei T, Chen S, Wang B, et al. Adapted-MoE: Mixture of Experts with Test-Time Adaption for Anomaly Detection[J]. arXiv preprint arXiv:2409.05611, 2024.'
---

Most unsupervised anomaly detection methods based on representations of normal samples to distinguish anomalies have
recently made remarkable progress. However, existing methods only learn a single decision boundary for distinguishing
the samples within the training dataset, neglecting the variation in feature distribution for normal samples even in the
same category in the real world. Furthermore, it was not considered that a distribution bias still exists between the test
set and the train set. Therefore, we propose an Adapted-MoE
which contains a routing network and a series of expert models to handle multiple distributions of same-category samples
by divide and conquer. Specifically, we propose a routing network based on representation learning to route same-category
samples into the subclasses feature space. Then, a series of
expert models are utilized to learn the representation of various normal samples and construct several independent decision boundaries. We propose the test-time adaption to eliminate the bias between the unseen test sample representation
and the feature distribution learned by the expert model. Our
experiments are conducted on a dataset that provides multiple
subclasses from three categories, namely Texture AD benchmark. The Adapted-MoE significantly improves the performance of the baseline model, achieving 2.18%-7.20% and
1.57%-16.30% increase in I-AUROC and P-AUROC, which
outperforms the current state-of-the-art methods.