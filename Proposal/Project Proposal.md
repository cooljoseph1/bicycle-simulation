---
title:  Backflipping Bicycles (Project Proposal)
author: Joseph Camacho
date: March 22, 2023
geometry: margin=1in
---

## Main Idea
I want to simulate a bicyclist doing backflips off a ramp. A "success" is a robot that manages to do a complete backflip and land on its wheels without crashing.

I plan to start with a basic model that models the bicycle as two wheels, a seat, and handlebars and the bicyclist as a torso with two arms:
![[Project Proposal 2023-03-22 22.35.41.excalidraw.png]]
and add more details later (if I can successfully simulate this first).

The bicycist will have two controls:
1. He can use the pedals, accelerating the bicycle forwards.
1. He can pull up on the handlebar, leading to an equal and opposite push down on the seat.
These are the only controls he will have--it's a very underactuated system. This is an interesting problem because at first glance it might seem impossible to do a back flip with only these controls, but humans have been able to successfully do so anyways.

## Topics Related to Class
1. Underactuated robotics
2. Stability theory, probably using Lyapunov analysis (can I prove that the robot will be able to balance, for example?)
3. Trajectory optimization

## Method
I plan to use Drake to do the simulation. I'm not yet sure which trajectory optimization methods I'll use, though I plan to use something simple like an iterative linear quadratic regulator (as done in the homework exercise 10.3) if possible.


## Related Papers
I found a couple papers on bicycle simulation and learning stunts, but none that did backflipping in particular, and they mostly used reinforcement learning. Two of the more relevant papers I found were https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8571685 and https://dl.acm.org/doi/pdf/10.1145/2601097.2601121.