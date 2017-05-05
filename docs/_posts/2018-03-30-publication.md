---
layout: post
title: "Papers"
published: true
categories: misc
permalink: papers
---

## Curl-noise on the GPU

This project aims to implement _curl-noise_ as presented by [_R. Bridson_](https://www.cs.ubc.ca/~rbridson/docs/bridson-siggraph2007-curlnoise.pdf) using __OpenCL__, __C++__, and __OpenGL__.

[__Paper (in Swedish)__]({{ "/assets/papers/curl-noise.pdf" | absoulte_url}}) [__Source Code__](https://github.com/CaffeineViking/cnpf)
<br>

## Monte Carlo Path Tracing

An implementation of a _Monte Carlo Path Tracer_ in __C++__ and __OpenMP__ that produces physically-based renderings of parametric geometry. A _photon map_ is used to speed-up convergence of indirect diffuse light.

[__Paper__]({{ "/assets/papers/monte-carlo-path-tracer.pdf" | absoulte_url}}) [__Source Code__](https://github.com/CaffeineViking/mcrt)
<br>

## Genetic programming of behavior trees

Modelling of adversarial agents where their behavior model as _Behavior Trees_, where the tree structure is generated using _genetic programming_.

[__Paper__]({{ "/assets/papers/genetic-behaviour-trees.pdf" | absoulte_url}}) [__Source Code__](https://github.com/sci10n/Quake2D)
<br>

## Text generation using a Recurrent Neural Network 

A _Recurrent Neural Network_-based prediction model designed to find generalizable structures in sequences of text characters. The model is evaluated through training and prediction on the Linux kernel source code [Linux kernel-code](https://github.com/torvalds/linux).

[__Paper__]({{ "/assets/papers/rnn-text-generation.pdf" | absoulte_url}})
<br>

## Hierarchical Task Network (HTN) planner for multi-agent domains

Evaluation of a _HTN-planning_ system for a _search and rescue_ scenario with multiple robots. Planner is developed in Python and adapted from [_Pyhop_](https://bitbucket.org/dananau/pyhop) and interfaces with the ROS framework.

[__Paper__]({{ "/assets/papers/htn-planning.pdf" | absoulte_url}})
<br>

## Template Matching of GUI elements 

Evaluation on how different image transformations affects the performance of _Template Matching_ to detect and localize GUI components in screenshots.

[__Paper__]({{ "/assets/papers/lightweight-user-agents.pdf" | absoulte_url}}) [__Source Code__](https://github.com/sci10n/GUI-Agent)

## Deep learning bone segmentation in volumetric CT-Volumes 

Semantic segmentation of specific lumbar vertebrae through a __Convolutional Neural Network__ mode working with volumetric data and user provided hints.

[__Paper__]({{ "/assets/papers/bone-fragment-segmentation.pdf" | absoulte_url}})
