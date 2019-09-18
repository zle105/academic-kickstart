---
title: "Multiscale simulations of material with heterogeneous structures based on representative volume element techniques"
date: 2018-06-01
publishDate: 2019-09-14T20:01:46.125703Z
authors: ["Zeliang Liu*", "C.T. Wu", "Bo Ren", "Wing Kam Liu", "Roger Grimes"]
publication_types: ["1"]
abstract: "This paper presents a concurrent multiscale simulation framework for materials with heterogeneous structures (e.g. composite). This avoids the burdens of finding the macroscale phenomenological models and tedious calibration processes by directly establishing the connection between the microstructure and macro-response through computational homogenization. In the homogenization process, the model links every macroscopic integration point to a Representative Volume Element (RVE) of the microstructure, and macroscopic response is obtained by solving the RVE boundary value problem. Direct numerical simulation (DNS) techniques (e.g. FEM) for RVE analysis are capable of providing accurate high-fidelity material response data for complex phase morphology and behavior. Meanwhile, it is necessary to accelerate the RVE analysis using advanced model reduction techniques to enable efficient concurrent simulations.\n

RVE analysis package based on the FEM implicit analysis has been developed for 2D and 3D problems. Both smp and mpp are enabled. Instead of using separated pre- and post-processing packages for other FEA software, we have integrated the whole RVE analysis processes into LS-DYNA®, including preparing boundary conditions, FE analysis of the boundary value problem and RVE homogenization. Some key features of the RVE analysis package are 1) automatically assign boundary conditions to a given RVE mesh, such as periodic BC and uniform BC; 2) non-matching meshes on the faces can be considered; 3) arbitrary loading directions, such as uniaxial and shear; 4) output the RVE homogenization results to LS-DYNA® database, for both small-strain and finite-strain problem.\n

All the above functions are now covered by two new keywords in LS-DYNA®, *RVE_ANALYSIS_FEM and *DATABASE_RVE. Some numerical benchmarks will be utilized to demonstrate the capability of the RVE package. The linkage of the RVE package and the development of data-driven model reduction techniques will also be discussed.
"

links:
  - name: Preprint
    url: preprint.pdf

projects: ["4-rve"]

featured: false
publication: "*15th International LS-DYNA Users Conference*"
---

