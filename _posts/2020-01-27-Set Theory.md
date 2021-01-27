---
layout: post
title: My notes on Set Theory
subtitle: Axiomatic set up of sets as structures
tags: [set-theory, sets]
comments: true
---

# Set Theory

---

## Foundation of Mathematics (?)

So far, I'm of the opinion that it was considered to be the foundations of mathematics but there are questions that arise when we talk about set theory which can
describe everything there is to mathematics. However, this optimism has faded away for reasons we will discuss later. 

<details>
    <summary> Reasons why it is considered to be the Foundation of mathematics </summary>
<p>
    The following are the reasons for Set theory to be considered the foundation of mathematics (in some sense):

    <ol>
    <li> <strong> Ontological: </strong> First reason is that set theory can be used to construct other complicated structures such as completely ordered fields etc. </li>
    <li><strong> Epistemological: </strong> We can reduce the questions in mathematics to that of questions in Set theory. For example, is it the that case that product of compact spaces is compact? Yes, if the Axiom of choice is taken to be true. Or, can lebesgue measure be extended to a countably additive measure on all subsets of the real line? Yes, if there is a real-valued measurable cardinal. (the second example is not in syllabus) </li>
    </ol>
</p>
</details>

---
## Naive Collection Axiom

<details> <summary> Naive collection axiom </summary>
    <p>
    If $\phi(x)$ is any property of sets, then the set $\{ x : \phi(x) \}$ exists.
    </p>

    <p>
        A few questions can be raised about what we mean by the "property of a set". This can be made precise in a rigorous way so "property" will not be an issue
        but rather this axiom creates inconsistencies that we can't really get around unless we tweak this definition is some way. A well known paradox, known as "Russell's paradox" is a proof of this inconsistency.
    </p>
</details>

---

## Russell's Paradox

<details> <summary> Russell's Paradox </summary>
    <p>
    <strong> Theorem: </strong> The naive collection axiom is inconsitent.
    </p>
    <p>
        <details> <summary> <strong> Proof: </strong> </summary>
            <p> 
                Assume the naive collection axiom. Let
                $$
                    D = \{ x : x \not\in \}.
                $$
                This exists, by the naive collection axiom.
            </p>
            <p>
                But $D \in D \iff D \not\in D$ contradiction! So the naive collection axiom is inconsistent.
            </p>
        </details>
    </p>
</details>

---


## Definitions needed for writing axioms formally

<details> <summary> State the definition of Empty Set </summary>
    <p>
        <strong> Definition: </strong> The empty set, denoted by $\emptyset$, is the set with no elements.
    </p>
</details>

<details> <summary> State the definition of union of a set</summary>
<p>
    <strong> Definition: </strong> Suppose $A$ is a set. Then $\bigcup A$ is defined to be 
    $$
        \{x : \exists a \in A \ x \in A \}.
    $$
</p>
<p>
    Suppose $a$ and $b$ are sets. Then we define $a \cup b$ to be $\bigcup \{a,b\}$. Suppose $A = \{ a_i: i\in I\}$ is a set of sets. Then we define
    $ \bigcup_{i\in I} a_i $ to be $\bigcup A$.
</p>
<p>
    <strong> NOTE: </strong> The reason for defining it this way is because we can easily deal with infinite elements.
</p>
</details>

<details> <summary> Informal definition of Class </summary>
    <p>
        A class is anything of the form 
        $$
            \{x : \phi(x) \}
        $$
        where $\phi(x)$ is a property of sets. Example: $\{x : x = x \}$ is a class of all sets.
    </p>
</details>


---

## Basic Axioms
<details> 
    <summary> 
        State the ZFC Axioms
    </summary>
    <p>
        <details> <summary> <strong> Axiom of extensionality </strong> </summary> 
        <p>
            Two sets are equal if and only if they have the same elements.
        </p>
        </details>
    </p>
    <p>
        <details> <summary> <strong> Empty set axiom </strong> </summary>
        <p>
            The empty set $\emptyset$ exists.
        </p>
        </details>
    </p>
    <p>
        <details> <summary> <strong> Axiom of pairs </strong> </summary> 
        <p>
            If a and b are sets, then so is $\{ a, b \}$.
        </p>
        </details>
    </p>
    <p>
        <details> <summary> <strong> Axiom of Unions </strong> </summary> 
        <p>
            Suppose $A$ is a set. Then so is the union $\bigcup A$ of its elements.
        </p>
        </details>
    </p>
    <p>
        <details> <summary> <strong> Subset axiom scheme </strong> </summary> 
        <p>
            Suppose $A$ is a set and $\phi(x)$ is a statement in the language of set theory. Then
            $$
                \{x\in A: \phi(x)\}
            $$
            is a set.
            <p>
            <strong> NOTE: </strong> we are allowing the statement $\phi(x)$ to mention sets other than $x$.
            </p>
            <p>
            <strong> NOTE: </strong> Also known as Separation Scheme and the Comprehension Scheme.
            </p>
        </p>
        </details>
    </p>
    <p>
        <details> <summary> <strong> Axiom of Foundation </strong> </summary>
        <p>
            Suppose $A$ is a non-empty set. Then $A$ has an $\in$-minimal element; that is, there exists $m \in A$ such that $m \cap A = \emptyset$
        </p>
        </details>
    </p>
</details>

---

## Some propositions related to the axioms

<details> <summary> State the proposition describing the uniqueness of empty set. </summary>
    <p>
        There is at most one empty set.
    </p>
    <details> <summary> <strong> Proof: </strong> </summary>
        Suppose $a$ and $b$ are both empty sets. Then $a$ and $b$ have the same elements, for every element of $a$ is (vacuously) an element of $b$, and 
        every element of $b$ is an element of $a$. Hence by the axiom of extensionality $a = b$.
    </details>
</details>

<details>
    <summary> State a proposition about a set in a set (application of axiom of pairs) </summary>
    <p>
        If $a$ is a set, then so is $\{a\}$.
    </p>
    <p>
    <details> <summary> <strong> Proof: </strong> </summary>
    <p>
        Apply Axiom of Pairs to $a$ and $a$; then $\{a,a\}$ is a set, and this is equal to $\{a\}$ by Axiom of Extensionality.
    </p>
    </details>
    </p>
</details>

<details>
    <summary> State the proposition about empty set and set containing empty set. </summary>
    <p>
        $\emptyset$ and $\{\emptyset\}$ are not equal.
    </p>
    <p>
        <details> <summary> <strong> Proof: </strong> </summary>
            <p>
                $\emptyset \in \{\emptyset\}$, so $\{\emptyset\}$ is not empty.
            </p>
        </details>
    </p>
</details>

<details>
    <summary> State the proposition explaining the structure of $\bigcup$ of sets </summary>
    <p>
        If $a$ and $b$ are sets, then $a \cup b$ is a set.
    </p>
    <p>
        <details> <summary> <strong> Proof: </strong> </summary>
        <p>
            $\{a,b\}$ exists by the Axiom of Pairs. $a \cup b = \bigcup \{a,b\}$ then exists by Axiom of Unions.
        </p>
        </details>
    </p>
</details>

<details> <summary> State the proposition which describes the structure of set difference. </summary>
    <p>
        If $a$ and $b$ are sets, then so it their difference $a \setminus b$.
    </p>
    <details> <summary> <strong> Proof: </strong> </summary>
    <p>
        $a \setminus b = \{ x \in a: x \not\in b \}$, which exists by the Subset Axiom Scheme.
    </p>
    </details>
</details>

<details> <summary> State the proposition explaining the structure of intersection of a set. </summary>
    <p>
        Let $a$ be a non-empty set. Then $\bigcap a$, the intersection of all elements of $a$, is a set.
    </p>
    <details> <summary> <strong> Proof: </strong> </summary>
    <p> 
        $\bigcap a = \{ x \in \bigcup a : \forall y \in a \ x \in y \} $, which exists by the Union Axiom and the Subset Axiom Scheme.
    </p>
    </details>
</details>

<details> <summary> State the main consequence of the Subset Axiom Scheme. </summary>
    <p> <strong> Theorem: </strong>
        There is no set of all sets.
    </p>
    <p>
        <details> <summary> <strong> Proof: </strong> </summary>
            <p>
                Let $V$  be a set of all containing all sets.
            </p>
            <p>
                Let $D = \{x \in V: x \not\in x \}$. This is a set by subset axiom scheme.
            </p>
            <p>
                But since $V$ contains all sets as elements, then $D \in V$.
            </p>
            <p>
                Hence $D \in D \iff D \not\in D$ contradiction!.
            </p>
        </details>
    </p>
</details>

<details> <summary> State the consequence of Foundation Axiom </summary>
    <p> <strong> Proposition: </strong>
        Let $a$ be any set. Then $a \not\in a$.
    </p>
    <p>
        <details> <summary> <strong> Proof: </strong> </summary> 
            <p>
                Suppose $a \in a$. Let $A = \{a \}$. If $m$ is any element of $A$, then $m=a$, but then $a \in m \cap A$. This contradicts the Axiom of Foundation.
            </p>
        </details>
    </p>
</details>

<details> <summary> State the equavalent condition of Axiom of Foundation in the presence of all other axioms </summary>
    <p>
        <strong> Proposition: </strong> Let $a$ be any set. Then there does not exist a set $\{a_0, a_1, a_2, \cdots \}$ such that $a = a_0 \ni a_1 \ni a_2 \ni \cdots$
    </p>
    <p>
        <details> <summary> <strong> Proof: </strong> </summary>

        </details>
    </p>
</details>

---

