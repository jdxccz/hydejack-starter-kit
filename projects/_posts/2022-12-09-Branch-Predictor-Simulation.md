---
layout: post
title: Branch Predictor Simulation
description: >
  I created branch predictors to emulate the hardware branch actions of an operating system, and experimented with developing a custom branch predictor with improved accuracy. (Computer Architecture Course Project)
sitemap: false
hide_last_modified: true
---

Language: **C**

## General

In this work, I build a branch predictor used to predict the execution result (whether to jump or not) of branch instructions and improve program performance based on it. Intotal, I built Gshare, Tournament, Perceptron, and Custom branch predictors.

**Simulation**:
* The Gshare predictor calculates an index by performing an XOR operation between the current instruction address and the global history state, and updates the global history state based on the prediction result for prediction.
* The Tournament predictor includes a selector that chooses between two predictors (Gshare and Local History) based on their prediction results.
* The perceptron algorithm is a binary linear classification algorithm that learns to classify input data into two classes by iteratively adjusting a set of weights. with this ideas, I built a Preceptron branch predictor.
* The Custom predictor is based on the following branch predictors and properly select the predictor in different scenarios by selectors. 

I did experiment on 3 different kinds of program files. And here is the  <a href="https://github.com/jdxccz/Branch-Predictor-Simulation/blob/main/Branch_Predictor.pdf"> report </a>.. Besides you can find source code on Github  <a href="https://github.com/jdxccz/Branch-Predictor-Simulation">@here</a>.