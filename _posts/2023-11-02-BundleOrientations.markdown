---
layout: post
title: "2-out-of-3 principle and normal bundles"
date: 2023-11-02
categories: jekyll update
---

## Introduction

Recently, somebody online asked whether or not the fact that a Riemannian hypersurface (inside of an oriented Riemannian manifold) is orientable if and only if it admits a global unit normal generalizes to any submanifold. This led to a fun discussion about normal bundles (in general, i.e., away from the Riemannian setting) and orientability. The purpose of this note is to record some of my thoughts on that discussion. 

OOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO

In what follows, all vector spaces are real and finite-dimensional, and all manifolds are smooth, real, and finite-dimensional.

### 2-out-of-3 principle 

This is <em>not</em> the same as the 2-out-of-3 principle of Kähler geometry.

Linear algebra for the appetizer. Suppose that we have a vector space $V$, and that it is the direct sum of $V_1$ and $V_2$. The <em>2-out-of-3</em> principle states that an orientation on any two of $V$, $V_1$, or $V_2$ determines an orientation on the third such that the identity map $V_1 \oplus V_2 \to V_2$ is orientation-preserving. In somewhat more generality, for any short exact sequence of vector spaces 
\\[
  0 \longrightarrow V_2 \longrightarrow V \longrightarrow V_1 \longrightarrow 0,  
\\]
orientations on any two of $V$, $V_1$, or $V_2$ determine orientations on the third in such a way that $V \cong V_1' \oplus V_2$ is an orientation preserving isomorphism, for any complement $V_1'$ of $V_2$ isomorphic to $V_1$.

### Normal bundles

Let $M$ be a manifold and let $N$ be a submanifold. There is a natural short exact sequence of vector bundles over $N$, given by 
\\[
  0 \longrightarrow TN \longrightarrow TM\|\_N \longrightarrow \nu(M, N) \longrightarrow 0,
\\]
where $\nu(M, N) = TM\|\_N / TN$ is the <strong>normal bundle</strong> of $N$ in $M$. With the notion of orientability <em>for vector bundles</em>, the 2-out-of-3 principle carries over to vector bundles, and we can use it to study them. 

We will assume in what follows that $M$ is orientable as a manifold. This is equivalent to the orientability of $TM$, and orientability of $TM\|\_N$ follows from it. The 2-out-of-3 principle implies that $TN$ is an orientable vector bundle (i.e. $N$ is an orientable manifold) if and only if $\nu(M, N)$ is an orientable bundle. 

If $\nu(M, N)$ is trivial, then it's certainly orientable, and orientability of $N$ follows. The converse is not true in general (consider $S^2$ as the zero section in $TS^2$), but it does hold when $N$ is a hypersurface, for then $\nu(M, N)$ is a line bundle over $N$, and the only orientable line bundle is the trivial one (use the orientation to construct a nowhere-vanishing section). This is the "abstract" (metric-free) version of the Riemannian geometry fact originally asked about.



<!-- Need to use double backslash square bracket. Setting displayMath: [['\[', '\]']] in default.html 
correctly made it so that \[ and \] would delimit displayed math, but then it would read any square
brackets inside the delimiters as a delimiter itself. Of course, escaping didn't work.
-->


