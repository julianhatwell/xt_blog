---
title: My First Shiny App!
author: Julian Hatwell
date: '2016-02-05'
slug: my-first-shiny-app
categories:
  - Statistics
tags:
  - Sample Size
  - Shiny Apps
draft: no
---

I thought I would check out the buzz around Shiny Apps and build myself a little prototype. Nothing fancy - it's just a [sample size calculator](https://julianhatwell.shinyapps.io/SampleSizeCalculator/) for statistical experimental design.

The side panels asks you for the desired effect size $\delta$, signifance level $\alpha$ and power $1 - \beta$. It simply calculates the sample size required to design the appropriate test using the formula:

$$n = \frac{2(Z_{\alpha} + Z_{1-\beta})^{2 \sigma^2}}{\delta^2}$$

and states the Z-score required to reject the null hypothesis assuming the control group score is zero. 

As a little eye candy, I also added a graphical rejection region that updates in real time with any input parameter changes. It helps to visualise App/formula sensitivity to the three input parameters. This was done in base R graphics.

Not bad for a first attempt!