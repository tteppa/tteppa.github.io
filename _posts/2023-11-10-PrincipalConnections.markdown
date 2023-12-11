---
layout: post
title: "Connection forms"
date: 2023-11-03 
categories: vector_bundles principal_bundles
published: false
---

## Introduction

This note is to explain how to go between (local) connection forms for vector bundles and connection forms for their frame bundles. I'll assume everything in section 29 of Tu's book.

### Frame bundles, trivial case

We start from the simplest possible case. Consider the trivial vector bundle $E = \mathbb{R}^k \times M \to M$. The frame bundle $\mathrm{Fr}(E)$ is also trivial, given by $\pi = \mathrm{pr}_1\colon M \times GL(k, \mathbb{R}) \to M$. The constant frame $e_1, \dots, e_k$ of $E$ gives us the section $s\colon x \mapsto (x, I)$ of $\mathrm{Fr}(E)$. 

Suppose we have a connection in $E$, described in terms of the connection form with respect to the local frame $s$: 
\\[
\omega_s \in \Omega^1(M; \mathfrak{gl}(k, \mathbb{R})).  
\\]
The goal is to use this to describe the connection in the frame bundle. For later, note that these transform via the following rule: $\omega_{sA} = A^{-1} \omega_s A$ whenever $A \in GL(k, \mathbb{R})$. 

Now let $(x, A)$ be in $\mathrm{Fr}(E)$ and $(v, X)$ be in $T_{(x, A)}(\mathrm{Fr}(E))$. We have that 
\\[
\omega_{(x, A)}(v, x) = (v, X) - h(v, X),
\\]
where $h(v, X)$ is the horizontal part of $(v, X)$. What is this? It's given by the horizontal lift $\tilde{w}$ of some $w$ in $T_xM$, which by Lemma 29.7 in Tu we know is given by 
\\[
\tilde{w} = d(sA)\_x(w) - \underline{\omega_{sA}(w)}|\_{(x, A)}.
\\]
Let us compute each term in the above. The first is easy: $sA$ is given by $y \mapsto (y, A)$, so $d(sA)\_x(w) = (w, 0)$. For the second, we use the definition of a fundamental vector field: 
\\[
\underline{\omega\_{sA}(w)}|\_{(x, A)} = \left.\frac{d}{dt}\right|\_{t=0} (x, A\exp(t\omega\_{sA}(w))) = (0, A\omega\_{sA}(w)) = (0, \omega\_s(w)A).
\\]
So $\tilde{w} = (w, -\omega_s(w)A)$. Moreover, $w = v$, so it follows that 
\\[
\omega\_{(x, A)}(v, X) = (0, X + \omega_s(w)A).    
\\]
Now we need to get something $\mathfrak{gl}(k, \mathbb{R})$-valued. There exists a $Y$ in $\mathfrak{gl}(k, \mathbb{R})$ for which $\underline{Y}|\_{(x, A)} = \omega\_{(x, A)}(v, X)$. Since 
\\[
\underline{Y}|\_{(x, A)} = (0, AY),    
\\]
we make the idenfication of the vertical bundle of $\mathrm{Fr}(E)$ with $\mathrm{Fr}(E) \times \mathfrak{gl}(k, \mathbb{R})$ to arrive at 
\\[
\omega_{(x, A)}(v, X) = A^{-1}X + \mathrm{Ad}(A^{-1})\omega_s(v).    
\\] 
