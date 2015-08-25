
Tree-structured Gaussian Process Approximations
====

Authors: Thang Bui and Richard Turner,
Computational and Biological Learning Lab,
University of Cambridge

Appeared at NIPS 2014

----

Abstract: 
Gaussian process regression can be accelerated by constructing a small pseudo-dataset to summarize the observed data. This idea sits at the heart of many approximation schemes, but such an approach requires the number of pseudo-datapoints to be scaled with the range of the input space if the accuracy of the approximation is to be maintained. This presents problems in time-series settings or in spatial datasets where large numbers of pseudo-datapoints are required since computation typically scales quadratically with the pseudo-dataset size. In this paper we devise an approximation whose complexity grows linearly with the number of pseudo-datapoints. This is achieved by imposing a tree or chain structure on the pseudo-datapoints and calibrating the approximation using a Kullback-Leibler (KL) minimization. Inference and learning can then be performed efficiently using the Gaussian belief propagation algorithm. We demonstrate the validity of our approach on a set of challenging regression tasks including missing data imputation for audio and spatial datasets. We trace out the speed-accuracy trade-off for the new method and show that the frontier dominates those obtained from a large number of existing approximation techniques.

------

Required: GPML package

To get started, check out a toy regression example by running:

run gpmlpath/startup.m

addpath main

addpath exps

addpath util

addpath vfeGP

run_toy

---
Package details:

* main: model + inference/training code
* vfeGP: implementation of Titsias (2009) paper
* exps: experimental set ups to reproduce results in the paper