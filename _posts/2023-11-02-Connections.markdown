---
layout: post
title: "A note about connections"
date: 2023-11-02 
categories: jekyll update
---

## Introduction

In multivariable calculus, one often takes the directional derivative of a vector field with respect to another vector field. How can this be generalized to vector fields on manifolds, or even sections of vector bundles? How does one naturally arrive at the notion of a connection?

### Differentiation on bundles

In this section, $\pi\colon E \to M$ is a vector bundle. We already have one notion of a derivative of a section, the ordinary differential of maps of manifolds. That is, if $s$ is a section, and $m$ is a point of $M$, then we can consider the tangent map $T_ms\colon T_mM \to T_{s(m)}E$. This is perfectly legitimate, but, since we were trying to generalize the directional derivative, we need a map to the fibre $E_m$. 

How do we map from $T_{s(m)}E$ to $E_m$? We can naturally identify $E_m$ with a <em>subspace</em> of $T_{s(m)}E$, namely $T_{s(m)}(E_m)$, so the question is now one of linear algebra. We need to project $T_{s(m)}E$ onto $T_{s(m)}(E_m)$, and we must do so in a consistent matter at every point of $M$. 

Let us formalize the notion in the previous paragraph. We denote by $VE$ the vertical subbundle of $TE$. That is, the bundle over $E$ given by $V_eE = \ker(T_e\pi)$. It's easy to see that $V_eE = T_e(E_{\pi(e)})$: one inclusion is trivial, and the other follows from a dimension count. With this established, we make the following definition. A <strong> connection in </strong> $E$ is a projection $TE \to VE$. That is, it is a $VE$-valued one-form $\Phi$ on $E$ such that $\Phi \circ \Phi = \Phi$ and $\mathrm{im}(\Phi) = VE$.

Let us now use the above notion of a connection to give the promised definition. Let $\Phi$ be a connection in $E$, let $s$ be a section of $E$, and let $v$ be a tangent vector to $M$ at some point $m$. We take the ordinary differential and get an element $T_ms(v)$ of $T_{s(m)}E$. Using the connection, we project, and get an element $\Phi(T_ms(v))$ of $V_{s(m)}E$. Identifying this space with $E_m$ finally gives us an element of $E_m$, which we denote by $\nabla_v s$.

### Alternate definitions

A projection in a vector space onto a vector subspace is the same thing as a choice of a complement to the subspace, so we could have just as well defined a connection as the choice of a complementary subbundle to $VE$. That is, a connection is a subbunble $HE$ of $TE$ such that $TE = VE \oplus HE$. This way of defining a connection gives us what is called a <strong>Ehresmann connection</strong>.

We defined a connection as a projection above, but this definition of a connection actually seems to be uncommon in textbooks. A connection in a vector bundle $E \to M$ is typically defined to be a map $\nabla\colon\mathfrak{X}(M) \times \Gamma(E) \to \Gamma(E)$ such that 
<ul>
  <li> $\nabla_{fX + gY}s = f\nabla_X s + g\nabla_Y s$ whenever $f,g\in C^\infty(M)$, $X,Y\in\mathfrak{X}(M)$, and $s\in\Gamma(E)$; </li>
  <li> $\nabla_X(as + bt) = a\nabla_Xs + b\nabla_Xt$ whenever $a,b\in\mathbb{R}$ and $s,t\in\Gamma(E)$; </li>
  <li> $\nabla_X(fs) = f\nabla_Xs + X(f)s$ whenever $X \in \mathfrak{X}(M)$, $f\in C^\infty(M)$, and $s\in \Gamma(E)$. </li>
</ul>
That is, a connection is defined by the algebraic properties such a differentiation operator we were looking for before <em>should</em> satisfy. This kind of connection is typically called a <strong> Koszul connection </strong>, or merely a "linear connection."

<!-- Need to use double backslash square bracket. Setting displayMath: [['\[', '\]']] in default.html 
correctly made it so that \[ and \] would delimit displayed math, but then it would read any square
brackets inside the delimiters as a delimiter itself. Of course, escaping didn't work.
-->


