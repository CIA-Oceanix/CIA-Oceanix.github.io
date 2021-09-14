---
title: "Annual Assembly"
layout: gridlay
excerpt: "AI Chair OceaniX - Annual Assembly"
sitemap: false
permalink: /assembly
---

# First OceaniX Annual Assembly on Sept. 15 2021, PNBI, Brest

We are glad to announce the **first annual assembly of AI Chair OceaniX to be held on Sept. 15 2021**.
The assembly will combine an **in-person meeting at the PNBI on the "Technopôle Brest Iroise, Brest"** and **remote participations on zoom** (link to be posted ni due time).

**Zoom conference:** [link](https://imt-atlantique.zoom.us/j/92787843434?pwd=UjRwMG5raHVyOHhLeHB1WHFEZXovQT09)

## Program
- **Welcome coffee and tea** 09.30am
- **Assembly opening** by Prof. R. Fablet (PI of AI Chair OceaniX), 10.00am
- **Session on data-driven simulation and emulation at OceaniX** 10.15am ([details](#session-on-data-driven-simulation-and-emulation))
- Coffee break, 11.15am
- **Keynote by Prof. S. Gratton**, Prof. INPT, [webpage](http://gratton.perso.enseeiht.fr/), 11.30am ([details](#keynote-by-prof-serge-gratton))
- Lunch 12.30pm
- **Poster session**, 1.30pm 
- **Tutorial session on pytorch lighning** 2.30pm [details](#tutorial-on-pytorch-lighning)
- Coffee break, 3.45pm
- **Tutorial session on transformer networks** 4.00pm [details](#tutorial-on-transformer-networks)
- **Keynote by Prof. P. Heimbach**, Prof. Univ. of Texas, [webpage](https://www.jsg.utexas.edu/researcher/patrick_heimbach/), 5.00pm ([details](#keynote-by-prof-patrick-heinbach))

The detailed program with the list of posters and co-working session themes will be announced early September.

**Registration**: The registration is not mandatory but will help for the organization of the lunch and of  coffee breaks for those attending in-person.
You can use the following registration link [link](https://forms.gle/FfoSbN4KAejGfVY66). 
Please use this registration form to present a poster as well as to propose a co-working theme session.

**Where to meet**: The meeting will take place at the PNBI on Brest campus (technopôle Brest-Iroise) (see [here](https://www.google.com/maps/place/P%C3%B4le+Num%C3%A9rique+Brest+Iroise+(PNBI)/@48.3595771,-4.5646672,15z/data=!4m2!3m1!1s0x0:0xe713edbc83a1d6d4?sa=X&ved=2ahUKEwj8mPyoyNvyAhUExIUKHWO4BH8Q_BIwCnoECEEQBQ) for the direction information), in the conference room (third floor). 
It will also be possible to joint us online through a zoom link which will be posted on this page just before the meeting.

## Detailed Program

### Keynote by Prof. Serge Gratton
- *Title*: **Data Assimilation networks beats Ensemble Kalman filters.**
- *Abstract*: Data assimilation algorithms aim at forecasting the state of a dynami- cal system by combining a mathematical representation of the system with observations thereof. Exploring connections between typical data assimilation algorithms with recurrent Elman networks, we propose a fully data driven deep learning architecture that provably reaches the same prediction goals as Data assimilation algorithms. On numerical experiments based on the well-known Lorenz system, and when suitably trained using snapshots of the system trajectory (i.e., batches of state trajectories) and observations, our architecture successfully reconstructs both the system dynamics and the observation operator. It also outperforms a state-of-the-art data assimilation system on a prediction exercise.
- *Short bio*: Prof. Serge Garront received my engineering degree at ENSEEIHT, a french engineering high school in mathematics and computer science. I got my PhD at Cerfacs (European Center in Scientific Computing)  in 1999 in numerical analysis.  Before joining ENSEEIHT as a full university professor in 2008, he held a research position in the French Space Agency and a senior research position at Cerfacs. He is leading now the APO research team at IRIT (Research Institute in Computer Science), where I develop activities in filtering (Data Assimilation), optimization and high performance computing. I am member of the editorial boards of two international journals: SIAM journal on Optimization and OMS (Optimization Methods and  Software). I am also in the editorial board of the MOS/SIAM Series on Optimization. He is owner of the AI chair for "Machine Learning under physical constraints" at Artificial and Natural Intelligence Toulouse Institute ([ANITI](https://aniti.univ-toulouse.fr/en/)). He works in the areas of Optimization and Data Assimilation. In optimization, he is concerned with the  development of  algorithms for non-convex problems encountered in machine learning and in inverse problems. I am also involved in machine learning techniques to handle for evolution problems, bridging the gap between Data Assimilation and Variational Bayes approaches based on deep learning.

### Keynote by Prof. Patrick Heinbach
- *Title*: **Learning from data through the lens of (ocean) models, surrogates, and their derivatives.**
- *Abstract*: Because of the formidable challenge of observing the full-depth global ocean circulation in its spatial detail and the many time scales of oceanic motions, numerical simulations play an essential role in quantifying patterns of climate variability and change. For the same reason, predictive capabilities are confounded by the high-dimensional space of uncertain inputs required to perform such simulations (initial conditions, model parameters and external forcings). Inverse methods optimally extract and blend information from observations and models. They enable formally calibrated and initialized predictive models to optimally learn from sparse, heterogeneous data while satisfying fundamental equations of motion. A key enabling computational approach is the use of derivative information (adjoints and Hessians) for solving nonlinear least-squares optimization problems with quantified uncertainties. Derivative information enables property-conserving data assimilation for reconstruction, adjoint-based dynamical attribution, and the use of Hessian information for uncertainty quantification and observing system design.  A close correspondence exists to neural network training via backpropagation to learn from big data. Other correspondences exist between layer-wise relevance propagation for explainable AI and the interpretation of the time-evolving dual state of physical models and their use as sensitivity kernels for dynamical attribution. After highlighting these correspondences, we discuss a path forward to merge these perspectives via the concept of universal differential programming encapsulated in general-purpose automatic differentiation, such as being developed in the Julia programming language. 
- *Short bio*: Prof. Patrick Heinbach is a Professor at the University of Texas at Austin in the Department of Geological Sciences (DGS) and joint appointments in the Jackson School of Geosciences (JSG) and the Institute for Geophysics (UTIG). He is a member of the core faculty in the Oden Institute for Computational Engineering and Sciences and hold the W. A. Tex Moncrief, Jr., endowed chair III in Simulation-Based Engineering and Sciences. At the Oden Institute, he directs the Computational Research in Ice and Ocean Systems (CRIOS) group. Patrick's main research interest is understanding the general circulation of the ocean, the dynamics of the marine (and marine-terminating) cryosphere, and their role in the global climate system.

### Session on data-driven simulation and emulation
This session will 
- Session Chairs: R. Fablet
- Hugo Frezat. **End-to-end learning of subgrid scale parameterizations**. 
- Said Ouala. **Approximating Koopman operator using trainable linear aungmented dynamics**.
- Duong Nguyen. **TrAISformer: a generative transformer for AIS trajectory prediction**.
- Amédée Roy. **GANs for the simulation of seabird foraging trajectories**.

### Tutorial on pytorch lighning
- *Tutorial chair*: Quentin Febvre
- *Content*: This tutorial session will provide a short tutorial to the use of Pytorch lighning package and associated coding tools. 

### Tutorial on transformer networks
- *Tutorial chair*: Duong Nguyen
- *Content*: Recently, transformer networks have replaced Recurrent Neural Networks (RNNs) to become the state-of-the-art approach for time series modelling (Vaswani et al., 2017; Radford et al., 2018). Unlike RNNs, which have to process data sequentially and may have difficulty remembering information in several time steps in the past, transformer architectures are highly parallel and can capture long-term dependencies in data. This tutorial gives a quick introduction to Transformer, including the key concepts, current applications, and a discussion on the extent of Transformer to the context of OceaniX.
- *References*:
  - Vaswani, A., Shazeer, N., Parmar, N., Uszkoreit, J., Jones, L., Gomez, A.N., Kaiser, Ł. and Polosukhin, I., 2017. Attention is all you need. In Advances in neural information processing systems (pp. 5998-6008). [link](https://arxiv.org/abs/1706.03762) 
  - Radford, A., Narasimhan, K., Salimans, T. and Sutskever, I., 2018. Improving language understanding by generative pre-training. [link](https://paperswithcode.com/paper/improving-language-understanding-by)
  - Blog post: https://medium.com/inside-machine-learning/what-is-a-transformer-d07dd1fbec04
