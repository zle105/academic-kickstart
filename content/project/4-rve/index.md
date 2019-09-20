---
title: LS-DYNA RVE package
summary: Integration of the whole RVE analysis processes, including microstructural reconstruction, preparation of boundary conditions, FE analysis of the boundary value problem and RVE homogenization.
tags:
- Software
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Roadmap to virtual material library
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
Materials are hierarchical in nature. The macroscopic material properties are strongly affected by the morphology and evolution of the microstructures, especially under extreme events with large material deformations and geometric nonlinearities. The **representative volume element (RVE)** techniques based on homogenization theory are a type of hierarchical multi-scale simulation methods offering the numerical constitutive relationship at the macroscopic point.

LS-DYNA® RVE package integrates the whole RVE analysis processes, including preparation of boundary conditions, FE analysis of the boundary value problem and RVE homogenization. **Some key features are** 

- Arbitrary RVE meshes in 2D and 3D
- Various types of boundary conditions (e.g. periodic and displacement BCs)
- Treatment of no-matching 2D & 3D meshes
- Arbitrary loading conditions through control-node technique
- SMP and MPP enabled

**All these functions are covered by two keywords:**

- *RVE_ANALYSIS_FEM
- *DATABASE_RVE

Virtual material testing data can be generated using RVE analysis, and it will further serve as the offline/training data in **machine learning of multiscale material models**. More details can be found on [LSTC CMMG group website](https://www.lstc-cmmg.org/).