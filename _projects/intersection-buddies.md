---
layout: page
title: Intersection bodies of polytopes
description: Leaving the realm of convexity.
img: /assets/img/intersection_cube.png
importance: 4
category: research
toc: true
# mathrepo: https://mathrepo.mis.mpg.de/intersection-bodies
# arxiv: https://arxiv.org/abs/2110.05996
---


Intersection bodies of polytopes are geometric objects, which we can describe by using a variety of combinatorial and algebraic methods. This site describes previous and ongoing work regarding these objects. The first project that is described below focuses on (real) algebro-geometric aspects, where we describe their semialgebraic structure, which is governed by an underlying hyperplane arrangement. The second project below describes an ongoing follow-up work in which we consider the transformation of the intersection body under translation of the polytope, and pose the question of when an intersection body of a polytope is convex.


The intersection body of a geometric object is constructed by measuring the volume of central hyperplane sections. More precisely, let $$P \subseteq \mathbb{R}^d$$ be a star body (for example a convex body or a polytope). Pick a unit direction $$u \in S^{d-1}$$ on the unit sphere, and let $$u^\perp \subseteq \mathbb{R}^d$$ denote the orthogonal hyperplane contiaining the origin. We measure the $$(d-1)$$-dimensional Euclidean volume $$\rho(u)$$ of the section $$P \cap u^\perp$$. The *intersection body* $$IP$$ of $$P$$ is defined to be the unique star body such that $$\rho(u)$$ is the distance from the origin to the boundary of $$IP$$ in direction $$u$$. This video illustrates this construction:

<center>
<video width="100%" height="auto" autoplay loop>
  <source src="../../assets/video/animation.mp4" type="video/mp4">
</video>
(To show this video in full-screen <a href="../../assets/video/animation.mp4">click here</a>)
</center>

&nbsp;  

Historically, intersection bodies arose from questions in convex analysis, and have thus mostly been studied with methods drawn from this area. They are closely related projection bodies and cross-section bodies. Richard Garnder has coined the term *Geometric Tomography* for the study of these objects, which he describes as "*the area of mathematics dealing with the retrieval of information about a geometric object from data about its sections, or projections, or both.*"

&nbsp;  


### Semialgebraic Intersection Bodies ###


In general, intersection bodies are not semialgebraic sets. However, in the case of polytopes, we show that the intersection body of a polytope is always semialgebraic, and we provide an algorithm for its computation. We show that the regions of polynomiality of the boundary of $$IP$$ are defined by a hyperplane arrangement, which allows us to associate a zonotope to an intersection body of a polytope.  
Furthermore, we consider the algebraic boundary of $$IP$$, which is the algebraic variety that is the (complex) Zariski closure of its Euclidean boundary. We compute the irreducible components of the algebraic boundary and provide an upper bound for the degree of these components.

&nbsp;

##### Slides of Talks #####

|  | | |
|  --:  | :-- | :-- |
|  18 November 2021  &nbsp; | [Nonlinear Algebra Seminar at MPI MiS in Leipzig](https://www.mis.mpg.de/calendar/lectures/2021/abstract-33274.html)  | [[Slides]](../../assets/pdf/slides/intersection-bodies/21-11-nlalg.pdf) | 
| 30 November 2021 &nbsp; | [Women in Algebra and Symbolic Computation II](https://www.computeralgebra.de/sfb/our-news/women-in-algebra-and-symbolic-computations-ii/) &nbsp;&nbsp;   | [[Slides]](../../assets/pdf/slides/intersection-bodies/21-11-bad-duerkheim.pdf)    | 
|  14 February 2022  &nbsp; | [Colloquium of Facets of Complexity in Berlin](http://www.facetsofcomplexity.de/monday/20220214-C-Brandenburg.html) | [[Slides]](../../assets/pdf/slides/intersection-bodies/22-02-foc.pdf) | 
|  23 March 2022 &nbsp;  | [Combinatorial Coworkingspace](https://www.combinatorial-cowork.space) | [[Slides]](../../assets/pdf/slides/intersection-bodies/22-03-coworking-space.pdf) | 


&nbsp;  


##### References #####
<div class="publications">
  {% bibliography -f published --query @*[abbr=BBMS22] %}
</div>

&nbsp;


### Convex Intersection Bodies of Polygons ###

Intersection bodies are not always convex. In fact, it is known that every star body has an affine translation such that its intersection body is non-convex. In a current work in progress together with [Chiara Meroni](https://merochia.wixsite.com/chiara-meroni) we consider the behaviour of an intersection body of a polytope when translating the polytope and pose the following question:

> *For a fixed polytope $$P$$, what is the set of translations $$t$$ such that the intersection body $$I(P+t)$$ of $$P+t$$ is convex?*

Our results on the 2-dimensional case can already be found in my PhD Thesis (Chapter 4.6). Surprisingly, it turns out that every polygon has only finitely many transpositions such that its intersection body is convex, and the number of such translations is at most 5. 

We expect the results on the general case to appear on the arXiv soon.

&nbsp;

##### References #####
<div class="publications">
  {% bibliography -f thesis --query @*[abbr=phd] %}
</div>

&nbsp;


### Supplementary Material ###

Our [MathRepo page](https://mathrepo.mis.mpg.de/intersection-bodies/) contains lots of additional supplementary material:
- We implemented an algorithm in `SageMath` to compute interseciton bodies of polytopes of any dimension. We also implemented this algorimth in `OSCAR` for polytopes of dimension at most 3
- We provide a step by step explanation of the algorithm with the example of the cube  
- We created gallery of 3d models that show how different intersection bodies can look like when translating the original polytope

Here are two of the 3d models that you can find in the gallery. The first one shows the intersection body of the centrally symmetric cube $$[-1,-1]^3$$, and the second one shows the intersection body of its translation $$[0,2]^3$$. [Click here so see them all!](https://mathrepo.mis.mpg.de/intersection-bodies/case-study.html)

<div class="row">
    <div class="col-sm mt mt-md">
        <div class="embed-responsive embed-responsive-1by1">
            <iframe class="embed-responsive-item" src="../../assets/html/cube1.html"></iframe>
        </div>
    </div>
    <div class="col-sm mt mt-md">
        <div class="embed-responsive embed-responsive-1by1">
            <iframe class="embed-responsive-item" src="../../assets/html/cube5.html"></iframe>
        </div>
    </div>
</div>
<p style="text-align: center;"> (We are 3d models, you can rotate us) </p>


