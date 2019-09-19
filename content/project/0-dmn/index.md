---
title: Deep material network
summary: Network-based machine-learning model with physics-based building blocks and interpretable fitting parameters.
tags:
- Methods
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Framework of deep material network
  placement: 1
  focal_point: Smart

#links:
#- icon: twitter
#  icon_pack: fab
#  name: Follow
#  url: https://twitter.com/georgecushen
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---
### Motivation

In the past decade, a plethora of data-driven material modeling methods have been proposed based on existing machine learning techniques, such as deep neural network (DNN), recurrent neural network (RNN), Kriging methods, clustering analysis and proper orthogonal decomposition. Enabled by recent progresses in computer hardware systems (e.g. GPU) and open-source libraries (e.g. Tensorflow and PyTorch), neural network-based methods become the most popular ones due to its large model generalities (see the [universal approximation theorem](https://en.wikipedia.org/wiki/Universal_approximation_theorem)). 

However, one issue lots of us have encountered "the danger of extrapolation" of neural network. It means the learned model is credible only in the range defined by the training data. In material modeling, this issue become more significant since the data is usually limited, for instance, due to the high cost of conducting experiments. Below are two situations that typical appears in practice,

{{< figure src="figure1.jpg" title="" lightbox="true" >}}





