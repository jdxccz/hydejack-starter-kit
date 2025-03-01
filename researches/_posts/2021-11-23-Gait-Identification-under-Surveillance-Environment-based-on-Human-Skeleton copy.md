---
layout: post
title: Gait Identification under Surveillance Environment based on Human Skeleton
image:
  path: /assets/img/researches/gait-cycle.jpg
description: >
  Using **ST-GCN** network to classify the **human gaits** according to **skeletons**
sitemap: false
hide_last_modified: true
---

Co-contributor github **@lixirui142**, Supervised by **Ke Xu**

## Leading

In real-world scenarios, identifying specific individuals through surveillance can be a challenging task. Facial recognition can be disrupted by masks or other factors, and even without those disruptions, it can be difficult to obtain sufficient facial information from cameras at a distance. Therefore, we may consider gait recognition as an alternative method for identifying people. By analyzing the unique patterns in a person's walking style, we can build a database of gait signatures to compare against individuals captured on surveillance footage. 

## General

In our study, we utilized OpenPose to extract skeleton data from videos and reconstructed and adjusted Spatio-Temporal Graph Convolutional Networks to identify gaits. To evaluate the effectiveness of our model, we conducted experiments using the CASIC-B gait database. If you would like to learn more about our approach and findings, please refer to our paper, which is available on Arxiv at the following link: <a href="https://arxiv.org/ftp/arxiv/papers/2111/2111.11720.pdf">https://arxiv.org/ftp/arxiv/papers/2111/2111.11720.pdf</a>.

## Structure

![767x279](/assets/img/researches/1.png "structure image")
