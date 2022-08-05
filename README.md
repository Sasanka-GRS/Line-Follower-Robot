# Line tracer bot

# Introduction

The Line Follower Robot is one that follows a specific path indicated by a line (usually a black line on a light colored surface) with a particular width.

The robot will be able to detect a particular line and keep following it.

For special situations such as crossovers, the robot can have more than one path which can be followed, so we restrain from having crossovers in the lines.

# Overview

Our objective is to design robot that finds application in situations where transportation is essential with no human allowance. This robot is designed to be used in transportations in harsh conditions. 

We aim at achieving smooth trajectories using different combinations of P, I, D controllers. We see that the most optimal set of controllers is obtained to be P, D because  we are concerned about the present and upcoming values of the line sensors  and not interested in remembering the past positions of the bot. 

From a general ON-OFF circuitry, we obtain sharp changes in the trajectory of the bot which may lead to jerks and instability of the line tracking. This is solved by using PID controller. 

# Proposed Controller Design 

The proposed controller is a Proportional-plus-Integral -plus-Derivative (PID) digital controller. The PID controller would control the position of the robot with quick response time and minimize the overshoot. 

# The optimal controller design

## Finalising Kp, Kd, Ki values
Starting with Kp, we set Kp to a value of 1 and observe the robot. The goal is to get the robot to follow the line even if it is very wobbly. If the robot overshoots and loses the line, we reduce the Kp value. 

On the other hand, if the robot cannot navigate a turn or seems sluggish, increase the Kp value. Here the robot lost the line and hence we reduced the value to get a final Kp = 0.01

After the robot is able to somewhat follow the line, we decide a value for Kd (skip Ki for the moment). Upon setting a high value the speed was too low and on decreasing the value, the robot started wobbling. Hence we managed to get an intermediate value with a considerable speed and no wobble i.e. Kd = 10^(-5)

# Gains

This robot can be employed in many industrial situations harmful for human activities. In such places, these robots help create a working environment from a safe distance, and transport goods from one place to another. This can be the basis for many complicated robot transporters, which follow a line to accomplish not only transportation, but many more activites which can be eased out of man's stress and labour.
