---
layout: post
title: Gait Identification based on Local Graphical Feature
image:
  path: /assets/img/researches/nga-feature.jpg
description: >
  Using **ST-GCN** network to classify the **human gaits** according to **skeletons**
sitemap: false
hide_last_modified: true
---

Supervised by **Ke Xu**

## General

In this work, we propose a gait recognition algorithm based on geometric features of human skeletons. We extract the skeletons from videos using a skeleton extraction algorithm, and obtain the geometric features of the skeleton network using geometric operators. Geometric operators are used to provide local features of the graph network structure, which can be used to extract features from the human skeleton. We then use a clustering network to classify the obtained geometric features and construct a histogram feature of each gait sequence. Finally, the histogram features are fed into a convolutional neural network for training and comparison to achieve gait recognition.

The main contributions of this work are: 1) we construct a new geometric operator and complete feature ablation experiments to verify the effectiveness of each operator, and design a divergence distribution statistical feature to enhance the representation ability of the histogram; 2) we optimize and integrate the existing code to build an end-to-end model system, explore the influence of hyperparameters and network structure on the model; 3) the algorithm achieves performance improvement on the CASIA-B database, and we design performance metrics for clustering algorithms, obtaining a method for quickly judging clustering results without inputting the deep learning network; 4) we expand the applicable range of the geometric operator to 3D, and build and test a 3D version of the model network based on 3D skeleton data.

## Local Operators

Position, Angle, Track, Swing, View Local Operators

<div style="display: flex">
  <img src="/assets/img/researches/op1.png" style="flex: 1;width: 35%;">
  <img src="/assets/img/researches/op2.png" style="flex: 1;width: 35%;">
</div>
<div style="display: flex">
  <img src="/assets/img/researches/op3.png" style="flex: 1;width: 35%;">
  <img src="/assets/img/researches/op4.png" style="flex: 1;width: 35%;">
</div>
<div style="display: flex">
  <img src="/assets/img/researches/op5.png" style="flex: 1;width: 35%;">
</div>

## more information

you can find the source code on github <a href="https://github.com/jdxccz/Gait-Identification-based-on-Local-Graphical-Feature">@here</a>.
