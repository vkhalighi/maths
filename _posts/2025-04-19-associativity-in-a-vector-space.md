---
classes: wide
last_modified_at: 2025-04-19
math: true
title: "Associativity in a vector space"
permalink: /2025/04/19/associativity-in-a-vector-space
categories: [Linear Algebra]
tags: [addition, associativity, vector space, vectors]
author_profile: true
sidebar:
  - title: "Posts"
    nav: sidebar-posts
---
Since a vector space satisfies associativity under addition, one does 
not need to care about the order in which vectors in a vector space are
added together. The aim of this post is to justify this fact.

Suppose that $V$ is a vector space and that $\mathbf{u}$, 
$\mathbf{v}$, and $\mathbf{w}$ are arbitrary vectors in $V$. Then the
associativity under addition states that

$$\mathbf{u}+(\mathbf{v}+\mathbf{w})=(\mathbf{u}+\mathbf{v})+\mathbf{w}.$$

Since these two sums are equal, it does not really matter in which 
order these vectors are added together. As a result, we can drop
the parentheses and simply talk about $\mathbf{u}+\mathbf{v}+
\mathbf{w}$. We can then extend this and talk about the sum of 
arbitrary $n$ vectors $\mathbf{v}_1,\ldots,\mathbf{v}_n$ in a vector
space. Our goal is justify that $\mathbf{v}_1+\cdots+\mathbf{v}_n$
makes sense.

We first need to define what we mean by the sum
$\mathbf{v}_1+\cdots+\mathbf{v}_n$.

{% capture notice-2 %}
**Definition (The sum of $\boldsymbol{n}$ vectors in a vector space).**
The sum $\mathbf{v}_1+\cdots+\mathbf{v}_n$ denotes the sum

$$\mathbf{v}_1+(\mathbf{v}_2+(\mathbf{v}_3+\cdots+(\mathbf{v}_{n-2}+(\mathbf{v}_{n-1}+\mathbf{v}_n))\ldots).$$
{% endcapture %}

<div class="notice--success">{{ notice-2 | markdownify }}</div>

**Example.** $\mathbf{v}_1+\mathbf{v}_2+\mathbf{v}_3$ denotes $\mathbf{v}_1+(\mathbf{v}_2+\mathbf{v}_3)$ and
$\mathbf{v}_1+\mathbf{v}_2+\mathbf{v}_3+\mathbf{v}_4$ denotes $\mathbf{v}_1+(\mathbf{v}_2+(\mathbf{v}_3+\mathbf{v}_4))$.
{: .notice--warning}

Let us first prove the following Claim.

{% capture notice-2 %}
**Claim 1.** We have

$$
(\mathbf{v}_1+\cdots+\mathbf{v}_k)+\mathbf{v}_{k+1}=\mathbf{v}_1+\cdots+\mathbf{v}_{k+1}$$
{% endcapture %}

<div class="notice--info">{{ notice-2 | markdownify }}</div>

We use induction on $k$. For $k=1$, Claim 1 reads $\mathbf{v}_1+\mathbf{v}_2=\mathbf{v}_1+\mathbf{v}_2$ which is clearly true.
Let's assume that Claim 1 is true for $k$ and then prove it for
$k+1$.

$$\begin{align*}
(\mathbf{v}_1+\cdots+\mathbf{v}_{k+1})+\mathbf{v}_{k+2}&=((\mathbf{v}_1+\cdots+\mathbf{v}_k)+\mathbf{v}_{k+1})+\mathbf{v}_{k+2}
\\
&=(\mathbf{v}_1+\cdots+\mathbf{v}_k)+(\mathbf{v}_{k+1}+\mathbf{v}_{k+2})\\
&=\mathbf{v}_1+\cdots+\mathbf{v}_k+(\mathbf{v}_{k+1}+\mathbf{v}_{k+2})\\
&=\mathbf{v}_1+\cdots+\mathbf{v}_{k+2}.
\end{align*}$$

We will use Claim 1 to justify the following Claim.

{% capture notice-2 %}
**Claim 2.**
If $n\geq k$, then

$$(\mathbf{v}_1+\cdots+\mathbf{v}_k)+(\mathbf{v}_{k+1}+\cdots+\mathbf{v}_n)=\mathbf{v}_1+\cdots+\mathbf{v}_n.$$
{% endcapture %}

<div class="notice--info">{{ notice-2 | markdownify }}</div>

We use induction on $k$. For $k=1$, Claim 2 reads $\mathbf{v}_1+(\mathbf{v}_2+\cdots+\mathbf{v}_n)=\mathbf{v}_1+\cdots+\mathbf{v}_n$
which is true by Definition. Let's assume that Claim 2 is true for $k$ and then prove it for
$k+1$.

$$\begin{align*}
(\mathbf{v}_1+\cdots+\mathbf{v}_{k+1})+(\mathbf{v}_{k+2}+\cdots+\mathbf{v}_n)&=
((\mathbf{v}_1+\cdots+\mathbf{v}_k)+\mathbf{v}_{k+1})+(\mathbf{v}_{k+2}+\cdots+\mathbf{v}_n)\\
&=(\mathbf{v}_1+\cdots+\mathbf{v}_k)+(\mathbf{v}_{k+1}+(\mathbf{v}_{k+2}+\cdots+\mathbf{v}_n))\\
&=(\mathbf{v}_1+\cdots+\mathbf{v}_k)+(\mathbf{v}_{k+1}+\cdots+\mathbf{v}_n)\\
&=\mathbf{v}_1+\cdots+\mathbf{v}_n.
\end{align*}$$

Finally, we will use Claim 2 to justify our desired result.

{% capture notice-2 %}
**Lemma.** 
Let $\mathbf{f}(\mathbf{v}_1,\ldots,\mathbf{v}_k)$ be some sum formed from the vectors
$\mathbf{v}_1,\ldots,\mathbf{v}_k$. Then

$$\mathbf{f}(\mathbf{v}_1,\ldots,\mathbf{v}_k)=\mathbf{v}_1+\cdots+\mathbf{v}_k.$$
{% endcapture %}

<div class="notice--info">{{ notice-2 | markdownify }}</div>

We use complete induction on $k$ here. For $k=1$, Lemma reads $\mathbf{f}(\mathbf{v}_1)=\mathbf{v}_1$ which is true. Let's assume that
Lemma is true for all numbers $l< k$. Then

$$\begin{align*}
\mathbf{f}(\mathbf{v}_1,\ldots,\mathbf{v}_k)&=\mathbf{g}(\mathbf{v}_1,\ldots,\mathbf{v}_l)+\mathbf{h}(\mathbf{v}_{l+1},\ldots,\mathbf{v}_k)\\
&=(\mathbf{v}_1+\cdots+\mathbf{v}_l)+(\mathbf{v}_{l+1}+\cdots+\mathbf{v}_k)\\
&=\mathbf{v}_1+\cdots+\mathbf{v}_k.
\end{align*}$$
