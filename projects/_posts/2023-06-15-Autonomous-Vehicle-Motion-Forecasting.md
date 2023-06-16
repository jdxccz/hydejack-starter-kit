---
layout: post
title: Autonomous Vehicle Motion Forecasting
description: >
  This is a car trajectory prediction model based on LSTM. It encompasses model construction, data preprocessing, and our outstanding performance in the class Kaggle competition.
image:
  path: /assets/img/projects/LSTM.png
sitemap: false
hide_last_modified: true
---

Language: **Python**

## General

Autonomous Vehicle Motion Forecasting is a crucial task in the field of autonomous vehicles, involving the prediction of future positions of traffic agents. The LSTM model, a type of recurrent neural network, is widely used for this task due to its ability to capture long-term dependencies in sequential data. Three variations of the LSTM model were developed, each with different input and output features:

- Version 1: Input - Position, Output - Position
- Version 2: Input - Position+Velocity, Output - Position+Velocity
- Version 3: Input - Position+Lane, Output - Position

The LSTM pipeline for trajectory prediction can be summarized as follows:

- Data Pre-processing (including normalization and bagging)
- Train: Extract actual car trajectories using mask ID and form batches
- Test: Extract target car trajectories using track ID
- Input the features based on the selected version into the LSTM model
- Obtain predictions and de-normalize them to position
- Merge the output into a file

The LSTM model architecture includes LSTM cells, encoding input data and generating output sequences in an autoregressive manner. Dropout and other regularization techniques were considered but did not significantly improve the model's performance. The Adam optimizer was chosen, and the Mean Squared Error (MSE) loss function was used, aligning with the evaluation metric of Root Mean Square Error (RMSE).

The LSTM model offers an effective solution for autonomous vehicle motion forecasting, capturing complex dynamics and long-term dependencies in car movements.

## Ranking

Here is our model ranking among all the teams. You can see more details on Kaggle Page  <a href="https://www.kaggle.com/competitions/ucsd-cse-251b-class-competition/leaderboard">@here</a>.

![rank](/assets/img/projects/ranking.png)

## Source Code

If you want to know more details, you can check source code <a href="https://github.com/jdxccz/Autonomous-Vehicle-Motion-Forecasting">@here</a>.