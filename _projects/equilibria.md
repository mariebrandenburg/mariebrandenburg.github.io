---
layout: page
title: Equilibria in Economics and Game Theory
description: The mathematics of making everybody happy. <br/>
img: /assets/img/hammer.png
importance: 3
#arxiv: https://arxiv.org/abs/2107.08813
---

I have worked on two different projects involving concepts of equilibria. In general, an equilibrium in a game (game theory) or auction (economics) is reached, if each participating player or bidder conciders the outcome as most beneficial for their own (selfish) good. Mathematically, this can take various forms depending on the mathematical formulation of the problem, as well as the assumptions and variables that are taken into account.


### Competitive Equilibrium in Economics ###

A combinatorial auction is an auction, in which the price and allocation of multiple goods are decided simultatiously within an instant. In the setting of *graphical valuations*, each bidder tells the auctioneer beforehands how much they would be willing to pay for each subset of goods. This valuation is controlled by a graph \\(G\\), for which weights on the vertices and edges define the valuation for each subset of goods. Given these valuations, the auctioneer decides a price per item and a distribution of the goods among the bidders.

 A bidder is happy with the outcome of an aution, if they receive a subset of goods at a price, which maximizes their surplus. We pose the question of the existence of a price and an allocation, at which all bidders are happy; this is a competitive equilibrium. 

We translate the question of the existence of a competitive equilibrium to a condition on lattice points in the Minkowski sum of faces of a certain polytope \\(P(G)\\). This condition can be viewed as a generalization of the *Integer Decomposition Property* of lattice polytopes. In the case of the complete graph, the polytope turns out to be the *correlation polytope*, a polytope which is isomorphic to the cut polytope.

##### Slides of Talks #####
4  March 2022. [Mini-Symposium on Lattice Polytopes.](../../assets/pdf/auctions-slides.pdf)


##### References #####
<div class="publications">
  {% bibliography -f preprint --query @*[abbr=BHT21] %}
</div>

&nbsp;

### Correlated Equilibrium in Game Theory ###



 The most famous equilibrium concept in game theory is the notion of *Nash Equilbrium*. This has been extensively studied since the 1950's, and it is known that the set of Nash equilibria of a fixed game can be arbitrarily complicated: in fact, a universality statement holds, saying that every (arbitrarily complicated) semialgebraic set can appear as the set of Nash equilibria of some game. At the same time, Nash equilibria assume that the choices of all players are made independenlty -- a feature which is arguably only the case in very special instances.

 A more general concept is the notion of *Correlated Equilibrium*, a notion which assumes that there exists some external device which gives a recommendation to all players, modelling a relation between their choices. The set of correlated equilibria of a fixed game is described by a linear program. That is, the set of such equilibria is given as the set of solutions of finitely many linear inequalities, and the set of solutions thus forms the *Correlated Equilibrium Polytope* of the game. 

We study the *Region of full-dimensionality*, a semialgebriac set which describes the conditions for the polytope to be of maximal dimension. By a use of oriented matroid strata we investigate the possible combinatorial types of such polytopes that can appear for small games.

<div class="publications">
  {% bibliography -f preprint --query @*[abbr=BHP22] %}
</div>

<!--
<div class="row justify-content-sm-center">
    <div class="col-sm-3 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="" alt="" title=""/>
    </div>
    <div class="col-sm-5 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="/assets/img/hammer.png" alt="" title="Making autions a happier place since 2007"/>
    </div>
    <div class="col-sm-3 mt-3 mt-md-0">
        <img class="img-fluid rounded z-depth-1" src="" alt="" title=""/>
    </div>
</div>

<div class="caption">
	Special thanks for this gavel to my favorite comic artist <a href="https://www.youtube.com/c/lolnein">LOLNEIN</a> 
</div>
-->