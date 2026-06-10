---
layout: page
title: Machine Learning
description: The geometry of neural networks with piecewise linear activation functions.
img: /assets/img/neural-networks.webp
importance: 4
category: research
# mathrepo: https://mathrepo.mis.mpg.de/intersection-bodies
# arxiv: https://arxiv.org/abs/2110.05996
---


A *ReLU neural network* is an alternating composition of an affine linear function and the ReLU activation $$max(0,x)$$, where this function is applied to a vector coordinate-wise. Any such network is thus a piecewise-linear function, and, in fact, also the converse holds true: Any piecewise linear function can be expressed as a ReLU neural network.
Tropial geometry may be thought of as the geomtry of piecewise-linear functions, and allows a new perspective to study such network representing piecewise-linear functions. Inherently, this draws close connections to polyhedral geometry and oriented matroids.

<!--
&nbsp;  

##### Slides of Talks #####

|  | | |
|  --:  | :-- | :-- |
|  19 March 2024  &nbsp; | [Combinatorial Coworkspace](https://www.combinatorial-cowork.space/)  | [[Slides]](../../assets/pdf/slides/ml-tropical/24-03-coworkspace.pdf) | 
| 20 Febraury 2024 &nbsp; | [Applied Combinatorics, Algebra, Topology and Statistics Seminar &nbsp;&nbsp;](https://www.kth.se/math/kalender/applied-cats/marie-charlotte-brandenburg-separating-points-by-piecewise-linear-functions-the-real-tropical-geometry-of-neural-networks-1.1317579?date=2024-02-20&orgdate=2024-02-01&length=1&orglength=29)    | [[Slides]](../../assets/pdf/slides/ml-tropical/24-02-kth.pdf)    | 
|  23 January 2023  &nbsp; | [MFO Workshop Discrete Geometry](https://www.mfo.de/occasion/2404/www_view) &nbsp;&nbsp; | [[Slides]](../../assets/pdf/slides/ml-tropical/24-01-mfo.pdf) | 
|  6 November 2023 &nbsp;  | [Theoretical Foundations of Deep Learning](https://www.foundationsofdl.de) | [[Slides]](../../assets/pdf/slides/ml-tropical/23-11-spp.pdf) | 
-->

&nbsp;  


##### References #####
<div class="publications">
  {% bibliography -f published --query @*[abbr=BLM24 || abbr=BJ25 || abbr=BGH25] %}
</div>

&nbsp;  
&nbsp;