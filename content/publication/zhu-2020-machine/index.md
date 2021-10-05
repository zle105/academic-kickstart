---
title: "Machine learning for metal additive manufacturing: Predicting temperature and melt pool fluid dynamics using physics-informed neural networks"
date: 2021-01-06
publishDate: 2021-01-06T20:01:46.110661Z
authors: ["Qiming Zhu","Zeliang Liu*","Jinhui Yan*"]
publication_types: ["2"]
abstract: "The recent explosion of machine learning (ML) and artificial intelligence (AI) shows great potential in the breakthrough of metal additive manufacturing (AM) process modeling. However, the success of conventional machine learning tools in data science is primarily attributed to the unprecedented large amount of labeled data-sets (big data), which can be either obtained by experiments or first-principle simulations. Unfortunately, these labeled data-sets are expensive to obtain in AM due to the high expense of the AM experiments and prohibitive computational cost of high-fidelity simulations.
We propose a physics-informed neural network (PINN) framework that fuses both data and first physical principles, including conservation laws of momentum, mass, and energy, into the neural network to inform the learning processes. To the best knowledge of the authors, this is the first application of PINN to three dimensional AM processes modeling. Besides, we propose a hard-type approach for Dirichlet boundary conditions (BCs) based on a Heaviside function, which can not only enforce the BCs but also accelerate the learning process. The PINN framework is applied to two representative metal manufacturing problems, including the 2018 NIST AM-Benchmark test series. We carefully assess the performance of the PINN model by comparing the predictions with available experimental data and high-fidelity simulation results. The investigations show that the PINN, owed to the additional physical knowledge, can accurately predict the temperature and melt pool dynamics during metal AM processes with only a moderate amount of labeled data-sets. The foray of PINN to metal AM shows the great potential of physics-informed deep learning for broader applications to advanced manufacturing."

links:
  - name: Preprint
    url: "preprint.pdf"
  - name: URL
    url: "https://link.springer.com/article/10.1007/s00466-020-01952-9"

projects: ["6-am"]

featured: yes
publication: "*Computational Mechanics*"
---

