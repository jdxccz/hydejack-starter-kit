---
layout: post
title: TLE-Elimination
description: >
  Caught by the idea "Yanged", a kind of elimination game, we build a similar game called TLE elimination. (Functional Programming Course Project)
sitemap: false
hide_last_modified: true
---

Teammates github **@huiz97m @20000607-lxc @chenhs1641**   Language: **haskell**

## General

This is a casual game with simple rules that are easy to learn. Players need to clear the board by eliminating tiles of the same type and using various props to achieve a high score. This project is designed for learning functional programming. Github <a href="https://github.com/jdxccz/TLE-Elimination">@here</a>.

## Basic Rules:
* When the setup is completed, the player can pick a picture from the board and put it into the empty container.
* The player can only select the picture on the top layer.
* After the player picks the picture from the board, he could not put it back on the board.
* After the picture is removed from the board, the picture below it will be exposed if there is one.
* If there are more than three same pictures in the container, they will be eliminated, and the space of the container will be freed. (The order of the pictures added to the container does not matter. They don’t have to be added continuously to be eliminated.)
* The player should repeat the process until there are no pictures on the board.
* If the container is full sometime during the game and the board is not yet cleared, the player will lose the game.

## Window

![1332x752](/assets/img/projects/tle.png "window image")