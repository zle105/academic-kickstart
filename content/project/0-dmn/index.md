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

markup: mmark
---

In the past decade, a plethora of data-driven material modeling methods have been proposed based on existing machine learning techniques, such as deep neural network (DNN), recurrent neural network (RNN), Kriging methods, clustering analysis and proper orthogonal decomposition. Enabled by recent progresses in computer hardware systems (e.g. GPU) and open-source libraries (e.g. Tensorflow and PyTorch), neural network-based methods become the most popular ones due to its large model generalities (see the [universal approximation theorem](https://en.wikipedia.org/wiki/Universal_approximation_theorem)). 

However, a issue that lots of us have encountered is "the danger of extrapolation" of neural network. It means the learned model is credible only in the range defined by the training data. In material modeling, this issue become more significant since the data is usually limited, for instance, due to the high cost of conducting experiments. Below are two situations that typically appear in practice,

{{< figure src="figure1.jpg" title="" lightbox="true" >}}

Deep material network is proposed to address this problem by embedding mechanics/physics into the machine learning model. The key ingredients of DMN are a network structure for capturing the complexity of microstructural interactions, and a simple two-layer building block for reproducing the material physics. 

{{< figure src="figure2.jpg" title="" lightbox="true" >}}

The basic formulation for a two-phase material with linear elasticity can be written as
$$
\underbrace{\bar{\textbf{C}}^{rve}}_\text{Output}=\textbf{f}\:( \overbrace{z^{j=1,2,...,2^{N-1}},\alpha_{i=1,2,...,N}^{k=1,2,...,2^{i-1}},\beta_i^k,\gamma_i^k}^\text{Fitting parameters};\: \underbrace{\textbf{C}^{p1},\textbf{C}^{p2}}_\text{Inputs})
$$
The fitting parameters in the model are activation $z$ and rotation angles $\alpha$, $\beta$, $\gamma$.  Since the two-layer building block is designed to have analytical solution, one can derive the derivatives of the output $\bar{\textbf{C}}^{rve}$ with respect to any fitting parameter and input. With linear elastic data obtained from direct numerical simulation or experiement, DMN can be effectively trained via stochastic gradient descent and model compression algorithms.



