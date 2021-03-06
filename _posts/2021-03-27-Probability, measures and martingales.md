---
layout: post
title: Probability, Measure and Martingales
subtitle: Everything that I learnt in this course
tags: [probability, measure-theory, martingales, markov-chains, markov, measures]
comments: true
---

# Measuer Spaces

___

## Relation to Topology

In *Topology*, we care about *open* sets. The main property that we work with in *Topology* is characterised by the use of *continuous function* $f$. Mainly,
inverse image $f^{-1}(X)$ of an *open* set $X$ is *open*.

This is in contrast to the *measure* theory which is the study of *measurable* sets. The main characterisation of *measurable function* $f$ is that the
inverse image $f^{-1}(X)$ of a *measurable* set $X$ is a measurable.

One of the axioms of open sets states that finite union of open sets is open.

In contrast, one of the axioms of measurable sets is that countable union of measurable sets is also measurable.


---

## Algebra of set $\Omega$

<details>
<summary> Define Algebra </summary>
<p>
Let $\Omega$ be a set. <br>
We say that a collection  $\mathcal{F}$ of subsets of $\Omega$ is an <em>Algebra</em> on $\Omega$ if:
<ol>
<li>
$\Omega \in \mathcal{F}$,
</li>
<li>
$A \in \mathcal{F}$, then $A^c := \Omega \setminus A \in \mathcal{F}$,
</li>
<li>
$A,B \in \mathcal{F}$, then $A \cup B \in \mathcal{F}$.
</li>
</ol>
NOTE: $\emptyset = \Omega^c \in \mathcal{F}$ and $A, B \in \mathcal{F} \implies A \cap B = (A^c \cup B^c)^c \in \mathcal{F}$
</p>
</details>

<details>
<summary> Define $\sigma$-algebra </summary>

<p>
    We say tha a collection $\mathcal{F}$ of subsets of $\Omega$ is a <em>$\sigma$-algebra</em> on $\Omega$ if $\mathcal{F}$ is an <em>algebra</em> such that
    whenever $F_n \in \mathcal{F}$ for $n \in \mathbb{N}$ then
    $$
        \bigcup_n F_n \in \mathcal{F}.
    $$
</p>
NOTE: If $\algebra$ is a $\sigma$-algebra on $\Omega$ and $F_n \in \algebra$ for $n \in mathbb{N}$, then
$$
    \bigcap_n F_n = \left( \bigcup_n F_n^c \right)^c \in \algebra
$$

</details>

---

## Measurable Space

<details> <summary> Define Measurable Space </summary>

<p>
    A pair $(\Omega , \algebra )$, where $\Omega$ is a set and $\algebra$ is a $\sigma$-algebra on $\Omega$, is called a <em>measurable space</em>. An element of $\algebra$ is called a $\algebra$-measurable subset of $\Omega$.
</p>

</details>

<details> <summary> What do we mean by $\sigma$-algebra generated by a class $\mathcal{C}$ of subsets of $\Omega$. </summary>

<p>
    Let $\mathcal{C}$ be a class of subsets of $\Omega$. Then $\sigma(\mathcal{C})$, the $\sigma$-algebra generated by $\mathcal{C}$, is the <em>smallest</em>
    $\sigma$-algebra $\algebra$ on $\Omega$ such that $\mathcal{C} \subseteq \algebra$. It is the intersection of all $\sigma$-algebras on $\Omega$ that
    contain $\mathcal{C}$.
</p>

</details>