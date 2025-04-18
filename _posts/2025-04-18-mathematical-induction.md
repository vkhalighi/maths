---
last_modified_at: 2025-04-18
math: true
title: "Mathematical Induction"
permalink: /2025/04/18/mathematical-induction
categories: [Proof Techniques]
tags: [mathematical induction, proofs, well-ordering]
author_profile: true
sidebar:
  - title: "Posts"
    nav: sidebar-posts
---
We will look at various forms of mathematical induction here.

{% capture notice-2 %}
**Mathematical Induction (First Formulation).**
Suppose $P(n)$ means that the property $P$ holds for the number 
$n$. Then the principle of mathematical induction states that $P(n)$
is true for all natural numbers $n$ provided that

1. $P(1)$ is true.
2. If $P(k)$ is true, then $P(k+1)$ is also true.
{% endcapture %}

<div class="notice--info">{{ notice-2 | markdownify }}</div>

{% capture notice-2 %}
**Mathematical Induction (Second Formulation).**
If $A$ is any set of natural numbers and

1. $1$ is in $A$,
2. If $k\in A$, then $k+1\in A$,

then $A$ is the set of all natural numbers.
{% endcapture %}

<div class="notice--info">{{ notice-2 | markdownify }}</div>

The first and second formulations of mathematical induction are equivalent. To see this, define the set $A$ by

$$A=\{\,n\in\mathbb{N}:P(n) \text{ is true}\,\}.$$

The general principle of mathematical induction follows from the
principle of mathematical induction.

{% capture notice-2 %}
**The General Principle Of Mathematical Induction.**
If $A$ is any set of natural numbers and

1. $n_0$ is in $A$,
2. If $k\in A$, then $k+1\in A$,

then $A$ is the set of all natural numbers $n\geq n_0$.
{% endcapture %}

<div class="notice--info">{{ notice-2 | markdownify }}</div>

Define the set $B$ by

$$B=\{\,m\in\mathbb{N}:n_0-1+m\in A\,\}.$$

Then $1$ is in $B$ and if $k\in B$, then $k+1\in B$. It follows by the 
second formulation of mathematical induction that $B$ is
the set of all natural numbers and consequently, $A$ is the set of all
natural numbers $n\geq n_0$.

**The Well-ordering Principle.** If $A$ is a nonempty set of natural 
numbers, then $A$ has a least element.
{: .notice--info}

The principle of mathematical induction and the well-ordering principle
are equivalent. 

We first justify the well-ordering principle assuming the principle of
mathematical induction.

Suppose that $A$ has no least element. Define the set $B$ by

$$B=\{\,n\in\mathbb{N}:1,\ldots,n\not\in A\,\}.$$

Clearly, $1\in B$ because if $1\in A$, then $A$ would have $1$ as its 
least element. Now assume that $1,\ldots,k\not\in A$. Then
$k+1\not\in A$ since if $k+1\in A$, then it would be the least element of 
$A$. Hence, $1,\ldots,k+1\not\in A$. This means that if $k\in B$, then
$k+1\in B$. It follows by the principle of mathematical induction that all 
natural numbers $n$ are in $B$; that is, $A$ is the empty set.

We can also justify the principle of mathematical induction by using the
well-ordering principle.

Define the set $B$ by

$$B=\{\,n\in\mathbb{N}:n\not\in A\,\}.$$

If $A$ is not the set of all natural numbers, then $B$ is nonempty.
It follows by the well-ordering principle that $B$ has a smallest element $n_0=(n_0-1)+1$. Since $1\in A$, it can not be in $B$ and so $n_0\ne1$; that is, $n_0\geq2$. Since $n_0$ is a smallest element of $B$, the natural number $n_0-1$ can not be in $B$ so it must be in 
$A$. Since $n_0-1\in A$, then $n_0\in A$ and so it can not be in $B$.
This is a contradiction and thus, $A$ must be the set of all natural 
numbers.

There is another form of the principle of mathematical induction
which looks much stronger but actually follows from the principle of
mathematical induction.

{% capture notice-2 %}
**The Principle Of Complete (or Strong) Mathematical Induction.**
If $A$ is any set of natural numbers and

1. $1$ is in $A$,
2. If $1,\ldots,k\in A$, then $k+1\in A$,

then $A$ is the set of all natural numbers.
{% endcapture %}

<div class="notice--info">{{ notice-2 | markdownify }}</div>

Define the set $B$ by

$$B=\{\,n\in\mathbb{N}:1,\ldots,n\in A\,\}.$$

Then $1\in B$ and if $k\in B$, then $k+1\in B$. It follows by the 
principle of mathematical induction that $B$ is the set of all natural 
numbers and consequently, $A$ is the set of all natural numbers.