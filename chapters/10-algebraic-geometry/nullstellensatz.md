# Hilbert's Nullstellensatz

## The theorem

Let $k$ be an algebraically closed field and let $I\subseteq k[x_1,\dots,x_n]$ be an ideal. Define

$$
V(I)=\{a\in k^n : f(a)=0\text{ for every }f\in I\},
$$

and for a subset $X\subseteq k^n$, define

$$
I(X)=\{f\in k[x_1,\dots,x_n] : f(a)=0\text{ for every }a\in X\}.
$$

Hilbert's Nullstellensatz says

$$
I(V(I))=\sqrt I.
$$

Equivalently, if a polynomial $g$ vanishes at every common zero of $I$, then some power $g^N$ lies in $I$.

A closely related weak form says that every maximal ideal of $k[x_1,\dots,x_n]$ is of the form

$$
(x_1-a_1,\dots,x_n-a_n)
$$

for some point $a=(a_1,\dots,a_n)\in k^n$.

## Before the theorem

Polynomial equations have two apparently different lives.

They are algebraic objects inside the polynomial ring

$$
k[x_1,\dots,x_n],
$$

but they also cut out geometric objects: points, curves, surfaces, and higher-dimensional sets.

Before the Nullstellensatz, one can move informally between these two viewpoints, but there is no theorem guaranteeing that the geometric zero set retains exactly the algebraic information one hopes it does.

The central problem is therefore:

> If two systems of polynomial equations define the same geometric locus, what precisely is the algebraic relation between those systems?

The Nullstellensatz gives the exact answer.

## The central idea

Start with an ideal $I$. Pass to its geometric zero set $V(I)$. Then forget the original equations and ask for **all** polynomials that vanish on that set.

This produces $I(V(I))$.

The theorem says:

$$
I(V(I))=\sqrt I.
$$

Thus geometry loses only nilpotent/multiplicity information. Apart from that, the ideal is recoverable from its set of zeros.

For example,

$$
(x)\qquad\text{and}\qquad(x^2)
$$

have the same zero set:

$$
V(x)=V(x^2)=\{0\}.
$$

And indeed

$$
\sqrt{(x^2)}=(x).
$$

So the passage from ideals to ordinary algebraic sets naturally identifies ideals with the same radical.

This is why **radical ideals**, rather than arbitrary ideals, are the algebraic objects corresponding exactly to classical affine algebraic sets.

## Why it matters

The theorem creates the basic algebra–geometry dictionary:

$$
\boxed{
\text{affine algebraic sets}
\longleftrightarrow
\text{radical ideals of }k[x_1,\dots,x_n]
}
$$

with inclusion reversed.

If

$$
I\subseteq J,
$$

then

$$
V(J)\subseteq V(I).
$$

Likewise,

$$
V(I+J)=V(I)\cap V(J).
$$

and

$$
I(X\cup Y)=I(X)\cap I(Y).
$$

This contravariance is not accidental. It becomes one of the organizing principles of algebraic geometry.

The theorem also turns geometric implication into algebraic membership.

Suppose

$$
f_1(a)=\cdots=f_m(a)=0
$$

always implies

$$
g(a)=0.
$$

Then

$$
g\in\sqrt{(f_1,\dots,f_m)}.
$$

Equivalently, for some $N\ge1$,

$$
g^N=h_1f_1+\cdots+h_mf_m
$$

for suitable polynomials $h_i$.

Thus a statement quantified over every point of a variety becomes a concrete algebraic certificate.

## Points become ideals

The weak Nullstellensatz gives an even more striking interpretation.

For a point

$$
a=(a_1,\dots,a_n),
$$

the set of all polynomials vanishing there is

$$
\mathfrak m_a=(x_1-a_1,\dots,x_n-a_n).
$$

This is maximal, and every maximal ideal is obtained this way.

Hence

$$
\operatorname{MaxSpec}k[x_1,\dots,x_n]\cong k^n.
$$

So ordinary geometric points can be recovered purely algebraically as maximal ideals.

That observation is one of the conceptual ancestors of scheme theory. Grothendieck's decisive move was to keep not only maximal ideals but **all prime ideals**, producing

$$
\operatorname{Spec}A.
$$

The resulting generalized points encode far more algebraic structure than classical point sets alone.

## A closure operator hidden inside the theorem

The pair of maps

$$
I\mapsto V(I),
\qquad
X\mapsto I(X)
$$

forms an inclusion-reversing correspondence.

Composing them gives

$$
I\mapsto I(V(I))=\sqrt I.
$$

Thus taking the radical is precisely the algebraic closure operation induced by passage to geometric zero sets.

This is structurally similar to many Galois correspondences throughout mathematics: two worlds are linked by order-reversing maps, and fixed points of the resulting closure operation identify the objects that genuinely belong to the correspondence.

Here the fixed points are radical ideals.

## Canonical example

Let

$$
I=(x^2,xy)\subseteq k[x,y].
$$

The common zero set is

$$
V(I)=\{(0,y):y\in k\},
$$

the $y$-axis.

Every polynomial vanishing on that axis lies in $(x)$, and

$$
\sqrt{(x^2,xy)}=(x).
$$

Therefore

$$
I(V(I))=(x)=\sqrt I.
$$

The original ideal remembers extra scheme-theoretic structure along the axis; the classical zero set does not.

## Proof architecture

The standard proof of the strong theorem is built from the weak theorem using the **Rabinowitsch trick**.

Suppose $g$ vanishes on $V(I)$. Introduce a new variable $t$ and consider

$$
J=(I,1-tg)\subseteq k[x_1,\dots,x_n,t].
$$

If $J$ were proper, the weak Nullstellensatz would give a common zero of $J$. But at such a point the equations from $I$ vanish, hence $g=0$, while $1-tg=0$ would force $1=0$, impossible.

Therefore $J$ is the whole polynomial ring, so

$$
1=\sum_i h_i f_i+h(1-tg).
$$

After substituting $t=1/g$ in a suitable localization and clearing denominators, one obtains

$$
g^N\in I
$$

for some $N$.

The proof therefore converts geometric nonexistence of common zeros into an algebraic identity.

## Dependencies

A mature understanding of the Nullstellensatz depends on:

- polynomial rings in several variables
- ideals and quotient rings
- prime and maximal ideals
- field extensions
- algebraic closure
- finitely generated algebras
- the Hilbert basis theorem / Noetherianity

The weak theorem is also closely tied to the fact that a field finitely generated as an algebra over an algebraically closed field must equal that field.

## What it unlocks

The Nullstellensatz makes possible the systematic translation between:

- irreducible algebraic sets and prime ideals
- points and maximal ideals
- coordinate geometry and quotient rings
- geometric inclusion and ideal containment
- polynomial consequences and radical membership

From there one can develop:

- coordinate rings
- dimension theory
- morphisms of varieties
- projective algebraic geometry
- localization and local rings
- schemes
- sheaves
- algebraic geometry over arbitrary base rings

Its conceptual lineage is roughly

$$
\text{Nullstellensatz}
\longrightarrow
\text{varieties as algebra}
\longrightarrow
\operatorname{Spec}
\longrightarrow
\text{schemes}.
$$

## What to remember

If every technical detail is forgotten, retain this:

$$
\boxed{
I(V(I))=\sqrt I
}
$$

and interpret it as:

> Over an algebraically closed field, polynomial geometry and radical ideal theory contain the same classical information.

That is why the Nullstellensatz is reasonably viewed as one of the foundational theorems of classical algebraic geometry.
