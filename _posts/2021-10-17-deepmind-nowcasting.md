---
layout: post
description: An overview of DeepMind's paper Skilful precipitation nowcasting using deep generative models of radar.
categories: [ml, climate]
title: Skillful precipitation nowcasting using deep generative models of radar 🌨️ [Paper Summary]
---

# Skilful precipitation nowcasting using deep generative models of radar

## What
DeepMind trained Deep Generative Models on radar observations in the hopes of creating a model that can accurately model & predict precipitation events within the immediate future (1-2 hours).


## Why
Nowcasting (the act of predicting the weather in the next hour or so) is an extremely important task for a variety of fields.(Sports, transportation, news) Accurate weather predictions can improve safety, increase quality of life, and optimize logistical decisions. Current weather prediction systems have a long compute times & struggle with accurate predictions within 2-hours from a given point in time. Machine Learning methods can fill in this gap and provide quick weather forecasts for the immediate future.

## How
- The GAN approach is used for their Deep Generative Models.
    - The generator context is fed four consectuve radar observations 
    - Two loss functions are used.
        - The first loss function/spatial discriminator is a CNN that attempts to distinguish real radar observations from generated ones.
        - The second loss/temporal discriminator is a 3D CNN that attempts to distinguish real & generated radar observations, but enforces a temporal consistency & penalizes predictions that skip or jump forward in time. 

- The precipitation events are 256 x 256 crops extracted from the radar stream.
    - The stream length is 110 minutes which results in 22 frames.
    - Trained on radar observations from 2016-2018
    - Radar observations from 2019 are used as a test set. 

## Key Findings
- DeepMind's Deep Generative Models achieved high ratings from meterologists surveyed. Over 89% ranked it as their preferred choice compared to existing methods.
- More work is needed to improve accuracy on rare & intense weather events
- The model can generate predictions within seconds on just a NIVIDIA V100 GPU.
- DeepMind's work shows you do not need to encode physical assumptions about the weather to achive promising results. This is not news to ML practioners but more proof of a networks ability to model complex phenomena. 

## Open Questions
- Would a models performance improve *if* some assumptions/meterological knowledge was encoded?
- If trained on radar observations from a variety of regions, would a models ability to predict improve?

## My perspective

This is my first time attempting to summarize a paper in this field. So I'll save you my opinion until its informed by more papers & model building experience. A lot of the information I gleaned from this paper is all new to me. You can load the model & make predictions using [this](https://github.com/deepmind/deepmind-research/tree/master/nowcasting) notebook provided by DeepMind. If you find the methodology interesting go ahead & give the paper a read for details I did not include!

# Sources:
- [Nowcasting the Next Hour of Rain](https://deepmind.com/blog/article/nowcasting)
- [Skilful precipitation nowcasting using deep generative models of radar](https://www.nature.com/articles/s41586-021-03854-z)