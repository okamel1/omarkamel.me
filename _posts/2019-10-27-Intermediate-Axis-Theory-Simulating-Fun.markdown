---
title: "Intermediate Axis Theory: Simulating Fun"
layout: post
date: 2019-10-27 22:00
tag:
- engineering
- simulation
- multibody
- dynamics
- simpack
- mechanics
- dynamics
category: project
author: omarkamel
description: Engineering
---

While wandering around youtube, I ran into this video: 
[![Physics](http://img.youtube.com/vi/lXb3ic10ENc/0.jpg)](http://www.youtube.com/watch?v=lXb3ic10ENc "The Bizarre Behavior of Rotating Bodies, Explained")

So I asked myself a lot of questions, one of those was: ***can we capture this phenomenon in simulation?***. To answer this question, I had to understand more about the physics of the problem, to know whether it is due to imperfections, or it occurs because of a mathematical error in nature :nerd_face:

After reading some articles and papers, starting with [Wikipedia](https://en.wikipedia.org/wiki/Tennis_racket_theorem), I understood that when a body has 3 different moments of inertia, the rotation about the intermediate inertia axis is always unstable und causes reversal in rotation axes as seen in the video.
I will not write an article explaining the theorem, available literature is enough, I will not add anything valuable. I am only concerned with simulating the phenomenon.
Further resources:
- [Tennis Racket Theorem](https://medium.com/engineer-quant/tennis-racket-theorem-8fb391098e34)
- [Van Damme, et al., The tennis racket effect in a three-dimensional rigid body](https://arxiv.org/pdf/1606.08237.pdf)

After that, I went to my favorite dynamics simulation software, built a very simple model with a body with looking like letter **T**, with 3 different moments of inertia. The body is driven with a pulse moment around the intermediate axis (the trunk of **T**), then left free to rotate, without any external effects, i.e. no gravity, friction, other excitations, etc.


[![Simulation](http://img.youtube.com/vi/lXb3ic10ENc/0.jpg)](http://www.youtube.com/watch?v=lXb3ic10ENc "Here is the simulation")