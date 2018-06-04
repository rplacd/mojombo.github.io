---
published: true
layout: post
title: Discrete metric spaces are complete.
---

**June 3, 2018. Part of a running commentary of Dave Perkinson's notes on real analysis.**.

As an example of a complete metric space, Dave Perkinson claims in his real analysis notes that any discrete metric space is complete:

**Example 8.8:** *Let $$(M, \textrm{disc})$$ be a metric space with the discrete metric. $$(M, \textrm{disc})$$ is complete; that is, every Cauchy sequence contained in $$M$$ converges to a point in $$M$$.*

This follows from the following characterisation of Cauchy sequences in discrete metric spaces:

**Lemma:** *A sequence $${x_n}$$ in $$(M, \textrm{disc})$$ is Cauchy iff it is eventually constant.* (This is straightforward to show, so attempt it yourself!)

*Proof.* The $$\impliedby$$ direction is simple: assume that $${x_n}$$ is constant after an index $$N$$. Then for all $$\epsilon>0$$ and any $$m,n>N$$, we have $$d(x_m,x_n)=0<\epsilon$$.

The $$\implies$$ direction is more substantial. We show the contrapositive. Take any $$\epsilon$$ such that $$0<\epsilon$\leq 1$$. Now assume that $$\{x_n\}$$ is never eventually constant; that is, for all indices $$N$$, there exist $$m,n>N$$ such that $$x_m\neq x_n$$. So $$\textrm{disc}(x_m,x_n)=1\geq \epsilon$$.

This is equivalent to saying that for all $$N$$, it is *not* true that for all $$m,n>N$$, $$\textrm{disc}(x_m,x_n)<\epsilon$$. Hence, $$\{x_n\}$$ not eventually constant implies not Cauchy. $$\square$$

With this very specific characterisation of Cauchy sequences in $$(M, \textrm{disc})$$, showing that $$(M,\textrm{disc})$$ is complete is simple:

*Proof of the claim.* Let $$\{x_n\}$$ be a Cauchy sequence fully contained in $$(M,\textrm{disc})$$. Then $$\{x_n\}$$ is eventually constant; that is, after an index $$N$$, any $$x_{n>N}$$ is equal to a constant $$x$$. So $$\{x_n\}\to x\in \{x_n\}\subseteq M$$, and $$\{x_n\}$$ converges to a point in $$M$$. $$\square$$
