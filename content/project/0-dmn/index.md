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

In the past decade, a plethora of data-driven material modeling methods have been proposed based on existing machine learning techniques, such as deep neural network (DNN), recurrent neural network (RNN), Kriging methods, clustering analysis and proper orthogonal decomposition. Enabled by recent progresses in **computer hardware systems (e.g. GPU) and open-source libraries (e.g. Tensorflow and PyTorch)**, neural network-based methods become the most popular ones due to its large model generalities (see the [universal approximation theorem](https://en.wikipedia.org/wiki/Universal_approximation_theorem)). 

However, an issue that lots of us may have encountered when experimenting on neural networks is **"the danger of extrapolation"**. It means the learned model is credible only in the range defined by the training data. In material modeling, this issue become more significant since the data is usually limited, for instance, due to the high cost of conducting experiments. Below are two situations that typically appear in practice,

{{< figure src="figure1.jpg" title="" lightbox="true" >}}

Deep material network (DMN) is proposed to address these problems by embedding mechanics/physics into the machine learning model. The key ingredients of DMN are a network structure for capturing the complexity of microstructural interactions, and a simple **two-layer building block for reproducing the material physics**. 

{{< figure src="figure2.jpg" title="" lightbox="true" >}}

Several equilibrium condition and kinematic constraints need to be satisfied in the building block. By applying the transformation function of building block iteratively through the network, the microscale information propagates from the bottom layer to the top-layer node, which represents the macroscale material. 

**The basic formulation of the overall stiffness tensor** for a two-phase material with linear elasticity can be written as

$$\underbrace{\bar{\textbf{C}}^{rve}}_\text{Output}=\textbf{f}\:( \overbrace{z^{j=1,2,...,2^{N-1}},\alpha_{i=1,2,...,N}^{k=1,2,...,2^{i-1}},\beta_i^k,\gamma_i^k}^\text{Fitting parameters};\: \underbrace{\textbf{C}^{p1},\textbf{C}^{p2}}_\text{Inputs})$$

The fitting parameters in the model are the activations $z$ and rotation angles $\alpha$, $\beta$, $\gamma$.  Since the two-layer building block is designed to have analytical solutions, one can derive the derivative of the output $\bar{\textbf{C}}^{rve}$ with respect to any fitting parameter or input. With **linear elastic data** obtained from direct numerical simulation or experiment, DMN can be effectively trained via stochastic gradient descent (SGD) and model compression algorithms.

The trained network can be **extrapolated to unknown material and loading spaces** in the prediction stage. For nonlinear materials, the system is solved via Newton’s method. Each Newton iteration contains one forward homogenization process and one backward de-homogenization process, and the mechanical data in the forward and backward propagations are shown as below,

$$\text{layer } N \xrightarrow[\text{homogenization}]{\text{forward } (\textbf{A},\delta\textbf{P})} \text{layer } 1 \text{ (macroscale)} \xrightarrow[\text{de-homogenization}]{\text{backward }(\Delta\textbf{F},\Delta\textbf{P})} \text{layer } N.$$

Comparing to other data-driven methods, DMN has the following intriguing features: 

- Avoiding an extensive offline sampling stage; 
- Eliminating the need for extra calibration and micromechanics assumption;
- Efficient online prediction without the danger of extrapolation

DMN has been applied to addressing various RVE challenges, such as hyperelastic rubber composite under large deformation, polycrystalline materials with rate-dependent crystal plasticity and various carbon fiber reinforced polymer (CFRP) composites. **The network structure with physically based parameters also provides a promising tool for materials design**. 

Recently, the original material network has been enriched with cohesive networks to handle materials with deformable interfaces. Same as before, the new cohesive building blocks has analytical solutions, so that the enriched network can still be optimized via SGD. An important application is on the interfacial failure analysis in CFRP composites, as well as particle-reinforced rubber composites.



