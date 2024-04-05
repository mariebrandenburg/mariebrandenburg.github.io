---
layout: page
title: Lattice Points and Lattice Polytopes
description: M-convex sets, Ehrhart-polynomials and the Integer Decomposition Property.
img: /assets/img/lattice-polytopes.webp
importance: 4
category: research
# mathrepo: https://mathrepo.mis.mpg.de/intersection-bodies
# arxiv: https://arxiv.org/abs/2110.05996
---

This site collects projects concerning lattice polytopes, i.e., polytopes with vertices contained in the lattice $$\mathbb Z^d$$, and properties of the lattice points inside such polytopes.

* [Quotients of M-convex sets and M-convex functions](#quotients-of-m-convex-sets-and-m-convex-functions)
* [Multivariate Polynomials of Polytropes](#multivariate-polynomials-of-polytropes)
* [Competitive Equilibrium in Economics](#competitive-equilibrium-in-economics)

&nbsp;

### Quotients of M-convex sets and M-convex functions

Two linear spaces $$L,K$$ form a *flag* if $$L \subseteq K$$. , and the containment of two spaces is modeled by two matroids forming a *quotient*.  

A *matroid* is the combinatorial abstraction of an arrangement of 1-dimensional linear spaces spanning a common subspace. A succint way to define matroids is through its *matroid polytope*, which is a lattice polytope with edges in directions $$e_i - e_j$$ contained inside the unit cube $$[0,1]^d$$. Relaxing the condition on the cube to be $$[0,k]^d$$ for $$k \in \mathbb Z_{\geq 0}$$ yields the definition of a *k-polymatroid:* The lattice points in a polytope with edge directions $$e_i-e_j$$ can be interpreted as arrangements of $$d$$ subspaces of dimension at most $$k$$. An even more genaral class is given by *M-conex sets*, which is the sets of lattice points in any lattice polytope with edges in directions $$e_i - e_j$$. Such a polytope is called a lattice *generalized permotohedra*. This class of polytopes and the lattice points therein can be described in many different ways, and we focus on 2 main points of view:

- a lattice generalized permutohedron is a polytope whose support function is a submodular set function $$p: 2^{[n]} \to \mathbb Z$$, i.e., a function such that for all $$A, B \subseteq [n]$$ holds $$p(A) + p(B) \geq p(A \cup B) + p (A \cap B)$$
- the set of lattice points $$P \subset \mathbb Z^n$$ in a lattice generalized permutohedron satisfy the following exchange property: for any $$x, y \in P$$ and any $$i \in [n]$$ such that $$x_i > y_i$$ there exists a $$j \in [n]$$ such that $$x_j < y_j$$ and $$x - e_i + e_j \in P, y + e_i - e_j \in P$$.

For the case of matroids, the submodular set function is the rank function of the matroid, while the exange property is preciely the basis exchange axiom for matroids.

The notion of *matroid quotients* is the combinatorial model of projections. In terms of linear spaces, it can be thought of as two linear subspaces where one is contained in the other.
As usually in matroid theory, there are many ways to define a matroid quotients, and one way is in terms of compliant rank functions:
If $$M, N$$ are matroids on the ground set $$[n]$$, then to matroids form a quotient if for all $$X \subseteq Y \subseteq [n]$$ the inequality
$$\operatorname{rk}_N(Y) -  \operatorname{rk}_N(X) \leq \operatorname{rk}_M(Y) -  \operatorname{rk}_M(X)$$.


In [[BLS24]](#bls24) we a generalize this notion to M-convex sets, and give a list of 10 equivalent characterizations of M-convex set quotiens. The first key equivalences are

*Let $$p,q: 2^{[n]} \to \mathbb Z$$ be two submodular set functions, and $$P,Q$$ be the assiciated M-convex sets. Then the following are equivalent.*
- *the two functions are compliant: $$q(Y) - q(X) \leq p(Y) - p(X)$$*
- *$$P$$ and $$Q$$ satisfy the exchange property: for any $$x \in Q, y \in P$$ and any $$i \in [n]$$ such that $$x_i > y_i$$ there exists a $$j \in [n]$$ such that $$x_j < y_j$$ and $$x - e_i + e_j \in Q, y + e_i - e_j \in P$$.*
- *$$P$$ and $$Q$$ are the top and bottom layers of an* M$$^\natural$$*-convex set, the lattice points in a* generalized polymatroid

The full list includes many more characterizations, including a novel construction of a monoid of linking sets, which vastly generalizes the classical construction of linking systems. Furthermore, we present the first attempt for a extension of this theory for M-convex functions. An M-convex function can be seen as a lifting function on an M-convex set, which subdivides the associated generalized permuohedron into generalized permutohedra. It can also be expressed in terms of an exchange property, however, there is no (straightforward) characterization which resembles the characterization via submodular functions as in the case of M-convex sets. Instead of a list of equivalences, we thus present a hierachy of properties. Two of them can be stated in analogy to the ones above:

*Let $$f,g: \mathbb Z^{[n]} \to \mathbb R \cup \{ \infty \}$$. Then 2. implies 1. with the following statements:*

1. *$$f$$ and $$g$$ satisfy the exchange property: for any $$x \in Q, y \in P$$ and any $$i \in [n]$$ such that $$x_i > y_i$$ there exists a $$j \in [n]$$ such that $$x_j < y_j$$ and $$g(x) + f(y) \geq g(x - e_i + e_j) + f(y + e_i - e_j)$$.*
2. *$$f$$ and $$g$$ are the top and bottom layers of an* M$$^\natural$$*-convex set*



&nbsp;  


##### References #####
<div class="publications">
  {% bibliography -f preprint --query @*[abbr=BLS24] %}
</div>


&nbsp;  
&nbsp;

### Multivariate Polynomials of Polytropes ###

We compute volume, Ehrhart $$h^\ast$$-polynomials of alcoved polytopes of type A.  
This is listed under [&rarr; Tropical Geometry and Positivity](../tropical/#multivariate-polynomials-of-polytropes).

&nbsp;  
&nbsp;


### Competitive Equilibrium in Economics ###

We consider properties of lattice points of the correlation polytope, which are weaker versions of the Integer Decomposition Property.  
This is listed under [&rarr; Economics and Game Theory](../equilibria/#competitive-equilibrium-in-economics).

&nbsp;  
&nbsp;

