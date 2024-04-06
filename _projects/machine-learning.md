---
layout: page
title: Machine Learning
description: The geometry of neural networks with piecewise linear activation functions.
img: /assets/img/neural-networks.webp
importance: 2
category: research
# mathrepo: https://mathrepo.mis.mpg.de/intersection-bodies
# arxiv: https://arxiv.org/abs/2110.05996
---

### The Real Tropical Geometry of Neural Networks

A *ReLU neural network* is an alternating composition of an affine linear function and the *ReLU activation function* $$max(0,x)$$, where this function is applied to a vector coordinate-wise. Any such network is thus a piecewise-linear function, and, in fact, also the converse holds true: Any piecewise linear function can be expressed as a ReLU neural network.
Tropial geometry may be thought of as the geomtry of piecewise-linear functions, and so it is natural to study such networks through the lense of tropical geometry. We focus on binary classification tasks: given a finite data set, we seek separate the data into two classes, depening on the sign of the value of the function which is reoresented by the network. 

A special case of this setup is the classification by hyperplanes defined by a linear function, where points are classified depending on the side of the hyperplane they lie on. Ranging over all possible classifications of a fixed set of datapoints yields three equivalent combinatorial constructions:
- The parameters of linear functions which induce the same classification form a chamber in a hyperplane arrangement
- the hyperplane arrangement induces the normal fan of a zonotope, i.e., a Minkowski sum of 1-dimensional simplices
- the possible classificatoins correspond to the maximal covectors of a realizable oriented matroid

In [[BLM24]](#blm24) we characterize the analogues of these constructions when extending from linear to piecewise linear functions. This yields the following:
- The  parameters of piecewise linear functions form a polyhedral fan in an arrangement of "bent hyperplanes" (which are, in fact, positive tropicalizations of certain hypersurfaces)
- the arrangement induces a normal fan of the *activation polytope*, which is a Minkowski sum of simplices
- the possible classifications correspond to *activation patterns*, which are bipartite graphs resembling the covectors of oriented matroids and tropical oriented matroids.


&nbsp;  

##### Slides of Talks #####

|  | | |
|  --:  | :-- | :-- |
|  19 March 2024  &nbsp; | [Combinatorial Coworkspace](https://www.combinatorial-cowork.space/)  | [[Slides]](../../assets/pdf/slides/ml-tropical/24-03-coworkspace.pdf) | 
| 20 Febraury 2024 &nbsp; | [Applied Combinatorics, Algebra, Topology and Statistics Seminar &nbsp;&nbsp;](https://www.kth.se/math/kalender/applied-cats/marie-charlotte-brandenburg-separating-points-by-piecewise-linear-functions-the-real-tropical-geometry-of-neural-networks-1.1317579?date=2024-02-20&orgdate=2024-02-01&length=1&orglength=29)    | [[Slides]](../../assets/pdf/slides/ml-tropical/24-02-kth.pdf)    | 
|  23 January 2023  &nbsp; | [MFO Workshop Discrete Geometry](https://www.mfo.de/occasion/2404/www_view) &nbsp;&nbsp; | [[Slides]](../../assets/pdf/slides/ml-tropical/24-01-mfo.pdf) | 
|  6 November 2023 &nbsp;  | [Theoretical Foundations of Deep Learning](https://www.foundationsofdl.de) | [[Slides]](../../assets/pdf/slides/ml-tropical/23-11-spp.pdf) | 


&nbsp;  


##### References #####
<div class="publications">
  {% bibliography -f preprint --query @*[abbr=BLM24] %}
</div>

&nbsp;  
&nbsp;