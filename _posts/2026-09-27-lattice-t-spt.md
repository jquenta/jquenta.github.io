---
layout: post
title: "The (only) 2d time-reversal SPT, but on a lattice"
date: 2026-09-26 00:00:00 +0200
categories: physics
---

Let me start this post by stating a fact: in 1+1 dimensions, symmetry-protected topological (SPT) phases with time-reversal ($T$) symmetry are classified by, 

$$
\mathrm{Hom}(\Omega^{\mathrm{O}}_2, U(1)) \cong \Z_2.
$$

The corresponding cobordism invariant is $w_1^2$, where $w_1 \in H^1(X, \Z_2)$ is the first Stiefel-Whitney class of $X$ (remember that a manifold $X$ is orientable iff $w_1 = 0$). The single non-trivial $T$-SPT is therefore 

$$
Z(X) = (-1)^{\int_X w_1^2},
$$

where the integral really means evaluation of $w_1^2$ on the $\Z_2$ fundamental class of $X$. Since the generator of $\Omega^{\mathrm{O}}_2$ is $\RP^2$, it follows that $Z(\RP^2) = -1$. 

<br>

---

<br>

At some point, I wanted to know how to compute the partition function $Z(X)$ from a triangulation of $X$. This is easy to do if we interpret $w_1$ as a background gauge field — indeed, this class defines a $\Z_2$-principal bundle on $X$: its *orientation bundle*. Remember that $\Z_2$-principal bundles are classified by homotopy classes of maps $X \to B\Z_2$, and $w_1$ fixes such a map via the isomorphism $[X, B\Z_2] \cong H^1(X,\Z_2)$.

This tells us that, just as when one defines a discrete gauge theory on a triangulated manifold, we can think of the edges $\ell_{ij}$ of our triangulation as being colored by elements $g_{ij}$ of $\Z_2$ obeying Gauss' law on triangles $\Delta_{ijk}$: 

$$
g_{ij} + g_{jk} = g_{ik}.
$$

In our case, we have a fixed assignment of colors given by $w_1$ (contrary to the case of a gauge theory, where one sums over all possible assignments). How do we know how to color the edges? The following statement comes to the rescue: 

<div class="centered-box" markdown="1">

A codimension 1-submanifold $Y$ of $X$ is Poincaré dual to $w_1(X)$ if and only if $X-Y$ is orientable. 

</div>

In terms of the triangulation, this means we should color the 1-cycle corresponding to $\mathrm{PD}[w_1]$ by $1 \in \Z_2$, and everything else by $0$. As an example, let's take $X = \RP^2$ with the following triangulation, which I need for my purposes: 

<div style="text-align: center;">

<img src="{{ '/assets/images/lattice-t-spt/rp2triang.png' | relative_url }}"
     alt="RP2"
     width="270">

</div>

In this case, the cycle $\mathrm{PD}[w_1]$ is also the only non-trivial cycle of $\RP^2$, $a - b$. So we can color, for example, $a$ by 1, $b$ by 0, and take appropriate colors for all other edges so as to satisfy Gauss' law. 

The last step is to evaluate the partition function. In our simplicial formulation, we can rewrite it as

$$
(-1)^{\int_X w_1^2} = \prod_{\Delta[012]} (-1)^{g_{01}g_{12}},
$$

where the product runs over all (ordered) triangles $\Delta$ of our triangulation.[^1] If we do the work, we find 

$$
Z(\RP^2) = (-1)^{1 \cdot 0} (-1)^{0 \cdot 0} (-1)^{1 \cdot 1} (-1)^{0 \cdot 1} = -1,
$$

just as we expected.

<br>

---

<br>


Let's also, just for fun, do the same computation for the Klein bottle $K$. Even though this manifold is non-orientable, $w_1^2$ evaluates to zero because $K$ is in the same cobordism class as the empty manifold. The Klein bottle has 2 non-trivial cycles: one of infinite order, and another one of order 2. The Poincaré dual of $w_1$ happens to be the latter. So that said, using a similar triangulation as for $\RP^2$ but with the correct edge identifications,

<div style="text-align: center;">

<img src="{{ '/assets/images/lattice-t-spt/kleintriang.png' | relative_url }}"
     alt="Klein Bottle"
     width="270">

</div>

we happily find that

$$
Z(K) = (-1)^{0 \cdot 0}(-1)^{0 \cdot 1}(-1)^{1 \cdot 0}(-1)^{0 \cdot 1} = +1.
$$

<br>

### Footnotes

[^1]: In general there's also a dependence on the orientation of the triangle, which in our case is irrelevant as we're using $\Z_2$ coefficients.










