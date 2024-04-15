---
layout: page
title: Hyperplane Sections of Polytopes
description: Intersection bodies and best slices of polytopes.
img: /assets/img/PermuComb.png #/assets/img/intersection_cube.png
importance: 5
category: research
# mathrepo: https://mathrepo.mis.mpg.de/intersection-bodies
# arxiv: https://arxiv.org/abs/2110.05996
---

* [Affine Sections of Polytopes](#affine-sections-of-polytopes)
* [Intersection Bodies of Polytopes](#intersection-bodies-of-polytopes)
  * [Supplementary Material (including a gallery of 3d models)](#supplementary-material)

&nbsp; 

## Affine Sections of Polytopes ##

Given a 3-dimensional cube, the intersection with an affine hyperplane is always a polygon with 3,4,5, or 6 vertices. But how can one understand the slices of a general polytope? And which slice is "the best," e.g., is the slice of maximal volume?

In [[BDLM23]](#bdlm23) we study the structure of the set of all possible sections of a convex polytope by arbitrary affine hyperplanes. We encounter several subdivisions of the space of hyperplanes into polyhedral cells with the property that all hyperplane sections coming from the same cell form a class of equivalent polytopes. Computing all such classes of hyperplanes allows for the identification of the optimal section according to numerous possible combinatorial criteria.

In each of these polyhedral cells, the volume of the hyperplane section can be expressed as a rational function, a quotient of two polynomials, in the parameters identifying the hyperplane. Finding the section of maximum volume thus turns into a global optimization problem over all polyhedral cells. With analogous strategies, one can extend these results further from hyperplane sections to orthogonal projections onto hyperplanes, and intersections with affine half-spaces. 

In the article, we describe two approaches, which we call the rotational and the translational approach. In the rotational approach, we first choose the position of the origin, which induces the *cocircuit arrangement* $$\mathcal{R}_{\circlearrowleft}$$. Once we have fixed the origin, we consider central sections, i.e. intersections with hyperplane through the origin. This induces a second hyperplane arrangement $$\mathcal{C}_{\circlearrowleft}$$. Here is an animation which illustrates the interaction between these two arrangements for a fixed pentagon (grey polygon on the right side). The left picture shows the space of translation vectors, and black dot in the left picture represents a translation vector $$t$$ of the polytope $$P$$, and thus determines the position of the origin. The right picture shows the polytope (grey pentagon in the left picture), and the black dot in the right picture represents the origin.

<img src="/assets/video/slicing-polytopes-rotation.gif" alt="rotational approach" width="100%"/>

In the translational approach, we first choose a normal direction. These directions are organized by the *sweep arrangement* (or *lineup arrangement*) $$\mathcal{R}_{\uparrow}$$. Once we have fixed the normal direction, we consider intersections of the polytope with affine translates of the hyperplane that is orthogonal to the chosen normal vector. These affine hyperplanes can be organized into chambers of the *parallel arrangement* $$\mathcal {C}_{\uparrow}$$. The following animation shows the interplay between the two arrangement in the translational approach. The left picture shows the space of normal vectors, and the right picture shows the polytope (grey pentagon) and affine hyperplanes which are orthogonal to the normal vector $$u$$ (pink).

<img src="/assets/video/slicing-polytopes-translation.gif" alt="rotational approach" width="100%"/>


&nbsp;  


##### References #####
<div class="publications">
  {% bibliography -f preprint --query @*[abbr=BDLM23] %}
  {% bibliography -f misc --query @*[abbr=nsf] %}
</div>


&nbsp;

##### Slides of Talks #####

|  | | |
|  --:  | :-- | :-- |
|  13 March 2024  &nbsp; | [Combinatorics Seminar at KTH in Stockholm](https://www.kth.se/math/kalender/kombinatorik/marie-brandenburg-how-to-slice-a-polytope-1.1313049?date=2024-03-13&orgdate=2024-03-01&length=1&orglength=31) &nbsp;&nbsp; | [[Slides]](../../assets/pdf/slides/slices/24-03-kth.pdf) | 
|  23 November 2023  &nbsp; | [Discrete Geometry Seminar at FU Berlin](https://www.mi.fu-berlin.de/en/math/groups/discgeom/Seminar/index.html) &nbsp;&nbsp; | [[Slides]](../../assets/pdf/slides/slices/23-11-villa.pdf) | 
|  05 June 2023  &nbsp; | [Nonlinear Algebra Seminar at MPI MiS in Leipzig](https://www.mis.mpg.de/calendar/lectures/2023/abstract-35817.html) &nbsp;&nbsp; | [[Slides]](../../assets/pdf/slides/slices/23-06-nlalg.pdf) | 

&nbsp;

## Intersection Bodies of Polytopes ##


Intersection bodies of polytopes are geometric objects, which we can describe by using a variety of combinatorial and algebraic methods. The intersection body of a geometric object is constructed by measuring the volume of central hyperplane sections. More precisely, let $$P \subseteq \mathbb{R}^d$$ be a star body (for example a convex body or a polytope). Pick a unit direction $$u \in S^{d-1}$$ on the unit sphere, and let $$u^\perp \subseteq \mathbb{R}^d$$ denote the orthogonal hyperplane contiaining the origin. We measure the $$(d-1)$$-dimensional Euclidean volume $$\rho(u)$$ of the section $$P \cap u^\perp$$. The *intersection body* $$IP$$ of $$P$$ is defined to be the unique star body such that $$\rho(u)$$ is the distance from the origin to the boundary of $$IP$$ in direction $$u$$. This video illustrates this construction:

<center>
<video width="100%" height="auto" autoplay loop>
  <source src="../../assets/video/animation.mp4" type="video/mp4">
</video>
(To show this video in full-screen <a href="../../assets/video/animation.mp4">click here</a>)
</center>

&nbsp;  

Historically, intersection bodies arose from questions in convex analysis, and have thus mostly been studied with methods drawn from this area. They are closely related projection bodies and cross-section bodies. Richard Garnder has coined the term *Geometric Tomography* for the study of these objects, which he describes as "*the area of mathematics dealing with the retrieval of information about a geometric object from data about its sections, or projections, or both.*"


In general, intersection bodies are not semialgebraic sets. However, in the case of polytopes, we show that the intersection body of a polytope is always semialgebraic, and we provide an algorithm for its computation [[BBMS22]](#bbms22). We show that the regions of polynomiality of the boundary of $$IP$$ are defined by a hyperplane arrangement, which allows us to associate a zonotope to an intersection body of a polytope.  
Furthermore, we consider the algebraic boundary of $$IP$$, which is the algebraic variety that is the (complex) Zariski closure of its Euclidean boundary. We compute the irreducible components of the algebraic boundary and provide an upper bound for the degree of these components.


Although intersection bodies of polytopes inherit some of the combinatorial structures of the polytopes, they are not always convex sets. In fact, it is known that every star body has an affine translation such that its intersection body is non-convex. In the second article [[BM24]](#bm24), we consider the behaviour of an intersection body of a polytope when translating the polytope and pose the following question:

> *For a fixed polytope $$P$$, what is the set of translations $$t$$ such that the intersection body $$I(P+t)$$ of $$P+t$$ is convex?*

Surprisingly, it turns out that the intersection body of a polygon is convex if and only if the polygon is centrally symmetric and centered at the origin. Whe show that the same statement can be made for cubes of arbitrary dimensions, but not for general polytopes.

&nbsp;  

##### Slides of Talks #####

|  | | |
|  --:  | :-- | :-- |
|  23 March 2022 &nbsp;  | [Combinatorial Coworkingspace](https://www.combinatorial-cowork.space) | [[Slides]](../../assets/pdf/slides/intersection-bodies/22-03-coworking-space.pdf) | 
|  14 February 2022  &nbsp; | [Colloquium of Facets of Complexity in Berlin](http://www.facetsofcomplexity.de/monday/20220214-C-Brandenburg.html) | [[Slides]](../../assets/pdf/slides/intersection-bodies/22-02-foc.pdf) | 
| 30 November 2021 &nbsp; | [Women in Algebra and Symbolic Computation II](https://www.computeralgebra.de/sfb/our-news/women-in-algebra-and-symbolic-computations-ii/) &nbsp;&nbsp;   | [[Slides]](../../assets/pdf/slides/intersection-bodies/21-11-bad-duerkheim.pdf)    | 
|  18 November 2021  &nbsp; | [Nonlinear Algebra Seminar at MPI MiS in Leipzig](https://www.mis.mpg.de/calendar/lectures/2021/abstract-33274.html)  | [[Slides]](../../assets/pdf/slides/intersection-bodies/21-11-nlalg.pdf) | 





&nbsp;  


##### References #####
<div class="publications">
  {% bibliography -f published --query @*[abbr=BBMS22] | @*[abbr=BM24] %}
</div>

&nbsp;  

##### Supplementary Material #####

*Gallery of 3D models*  
[Click here](../intersection-bodies-gallery/) for a gallery of intersection bodies of translates of the 3-dimensional cube.

*MathRepo*  
Our [MathRepo page](https://mathrepo.mis.mpg.de/intersection-bodies/) contains additional supplementary material:
- We implemented an algorithm in `SageMath` to compute interseciton bodies of polytopes of any dimension. We also implemented this algorimth in `OSCAR` for polytopes of dimension at most 3
- We provide a step by step explanation of the algorithm with the example of the cube  