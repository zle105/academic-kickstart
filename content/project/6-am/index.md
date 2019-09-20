---
title: Process-Structure-Property relationship in additive manufacturing
summary: Challenging multiscale and multiphysics problems at the intersection of computational physics, material science and data science.
tags:
- Applications
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: 
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
Additive manufacturing (AM) processes have the ability to build complex geometries from a wide variety of materials. In particular, **AM for metallic components** has risen to be one of the major research thrusts in material science and engineering in the past decades. For example, powder-bed metal AM uses a high-power laser or electron beam to melt powder and deposit the material layer-by-layer at arbitrary local spot.

However, due to the intense and repeated localized energy input, the microstructures in additively manufactured materials always contain complex material compositions and morphologies, which dominate **the material’s failure and damage behaviors**. On the part level, the local material microstructure varies significantly and depends on the input processing and design parameters. While there is a vast array of process and design variables, scientific understanding of the process and product is still insufficient to fully utilize this capacity.

The research goal here is to accelerate the quantification of additively manufactured materials by developing multiscale mechanistic theories to understand the process-structure-property relationship with complex microstructures produced from AM fabrication processes. My current effort has been focused on the structure-property part - **modeling of polycrytalline materials with crystal plasticity**.

[3D deep material network]({{< ref "/publication/liu-2019-exploring/index.md" >}}) has been applied to evaluate the effective properties of polycrystalline materials. Other than the online predictions for crystal plasticity, an interesting finding is that DMN can recover the hidden grain orientation information in the mechanical data, shown in the figure below.

{{< figure src="figure1.jpg" title="" lightbox="true" >}}

Future works will target process simulations and growth models. Meanwhile, it is also important to validate multiscale analysis with **uncertainty quantification (UQ)** through experimental testing data. 