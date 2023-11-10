---
layout: post
title: "Connection forms"
date: 2023-11-03 
categories: vector_bundles princiapal_bundles
published: false 
---

## Introduction

This note is to explain how to go between connections in vector bundles (in terms of local connection forms) and connections in their frame bundles (in terms of principal connection forms).

### Frame bundles, trivial case

We start from the simplest possible case. Consider the trivial vector bundle $E = \mathbb{R}^k \times M \to M$. The frame bundle $\mathrm{Fr}(E)$ is also trivial, given by $\pi = \mathrm{pr}_1\colon M \times GL(k, \mathbb{R}) \to M$. The constant frame $e_1, \dots, e_k$ of $E$ gives us the section $s\colon x \mapsto (x, I)$ of $\mathrm{Fr}(E)$. 

Suppose we have a connection in $E$, described in terms of the connection form with respect to the local frame $s$: 
$$
\omega_s \in \Omega^1(M; \mathfrak{gl}(k, \mathbb{R})).  
$$
For later, note that these transform via the following rule: $\omega_sA = A^{-1} \omega_s A$ whenever $A \in GL(k, \mathbb{R})$. <!-- WHY WON'T YOU FORMAT??????? -->




