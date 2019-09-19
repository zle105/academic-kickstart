---
title: Self-consistent clustering analysis
summary: Model reduction by grouping material points with similar responses.
tags:
- Methods
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
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
### Motivations

Self-consistent clustering analysis (SCA) is a novel reduced order model (ROM) technique [[Liu et al. CMAME 2016](https://www.sciencedirect.com/science/article/pii/S0045782516301499)]. It enables a powerful tradeoff between efficiency and accuracy through synergistic exploitation of high-fidelity analysis and efficient mean field homogenization using a **data-clustering technique**. 

SCA starts with an offline stage, in which a database is created by high-fidelity RVE analysis.  A data compression algorithm is then used to establish clustering groups with similar mechanistic features such as the local strain concentration factor. Material responses are assumed to be uniform in each cluster, and the interaction tensors between each pair of clusters are computed based on the Green’s function method. In the online stage, the discretized **Lippmann-Schwinger integral equation** is solved using a self-consistent scheme.