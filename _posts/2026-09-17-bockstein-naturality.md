---
layout: post
title: "Naturality and some neat relations between Bocksteins"
date: 2026-09-17 00:00:00 +0200
categories: math
---

Yesterday, while doing some computations, I stumbled upon the following basic fact: the Bockstein $\beta: H^n(-, \Z_2) \to H^{n+1}(-, \Z)$ associated to the short exact sequence (SES) 

$$ 1 \to \Z \xrightarrow{\cdot 2} \Z \xrightarrow{\text{mod 2}} \Z_2 \to 1, $$

once reduced mod 2, yields the same result as the Bockstein associated to the SES

$$ 1 \to \Z_2 \xrightarrow{\cdot 2} \Z_4 \xrightarrow{\text{mod 2}} \Z_2 \to 1, $$

which is also known as the first Steenrod square $\mathrm{Sq}^1: H^n(-, \Z_2) \to H^{n+1}(-, \Z_2)$. One can convince oneself about this by spelling out the details of how the Bockstein is defined in each case.

<br>

---  

<br>

It turns out that relations between Bocksteins like the above follow more generally from the **naturality of the Bockstein homomorphisms**, a theorem in homological algebra. Namely, if one has a morphism between SESs of chain complexes, i.e. a commutative diagram

$$
\begin{CD}
    0 @>>> A_\bullet @>>> B_\bullet @>>> C_\bullet @>>> 0 \\
      @. @VVV @VVV @VVV \\
    0 @>>> A'_\bullet @>>> B'_\bullet @>>> C'_\bullet @>>> 0,
\end{CD}
$$

then the following induced diagram between long exact sequences (LESs) is commutative:

$$
\begin{CD}
    \cdots @>>> H_n(A_\bullet) @>>> H_n(B_\bullet) @>>> H_n(C_\bullet) @>\beta>> H_{n-1}(A_\bullet) @>>> \cdots \\
    @. @VVV @VVV @VVV @VVV @. \\
    \cdots @>>> H_n(A'_\bullet) @>>> H_n(B'_\bullet) @>>> H_n(C'_\bullet) @>\beta'>> H_{n-1}(A'_\bullet) @>>>\cdots.
\end{CD}
$$

Of course, the theorem works for cohomology of cochain complexes as well. For the example at the start of the post, one can check that the two SESs indeed fit in a commutative diagram, which one can use to construct a morphism between SESs of cochain complexes, so the relation between Bocksteins follows immediately from this theorem.

<br>

---  

<br>

Although unsurprising if you know the result above, I found interesting that there is also a relation between $\beta$ and the Bockstein $\mathrm{Bock}$ associated to the SES

$$ 1 \to \Z \xrightarrow{\iota} \R \xrightarrow{\scriptsize{e^{2\pi i \bullet}}} U(1) \to 1, $$

since one has the following commutative diagram:

$$
\begin{CD}
    1 @>>> \Z @>\cdot 2>> \Z @>\text{mod 2}>> \Z_2 @>>> 1 \\
      @. @| @V\cdot\frac{1}{2}VV @V{(-1)^{\bullet}}VV \\
    1 @>>> \Z @>\iota>> \R @>{\scriptsize{\exp(2\pi i\bullet)}}>> U(1) @>>> 1.
\end{CD}
$$

In particular — and to apply this to the problem I was interested in — I have the following commutative diagram of cohomology groups:

$$
\begin{CD}
    H^n(-, \ \Z_2) @>\beta>> H^{n+1}(-, \ \Z) \\
    @V{(-1)^\bullet}VV @| \\
    H^n(-, \ U(1)) @>{\scriptsize{\text{Bock}}}>> H^{n+1}(-, \ \Z),
\end{CD}
$$

so that $\beta = \text{Bock} \circ (-1)^\bullet$. Quite neat!




