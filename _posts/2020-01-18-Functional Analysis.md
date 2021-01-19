---
layout: post
title: Functional Analysis
subtitle: Everything that I learnt in Functional Analysis (revision)
tags: [functional-analysis]
comments: true
---

# Banach Spaces

---

## Norm

<details>
<summary> Define Norm </summary>
<p> Let $X$ be a vector space over a field $\mathbb{F}$. A norm $\norm{\cdot} : X \to \mathbb{R}$ is a function such that $\forall x,y \in X$ and $\forall \lambda \in \mathbb{F}$:</p>
<p> (N1) $\| x \| \geq 0 $ with $\| x \| = 0 \iff x = 0 $ </p>
<p> (N2) $\| \lambda x \| = | \lambda | \| x \| $ </p>
<p> (N3) $\| x + y \| \leq \| x \| + \| y \| $ (Triangle inequality) </p>
</details>

Note: Norms are continuous maps

---

## Continuity

<details> 
<summary> State the theorem about continuity of a function in terms of Sequences  </summary>
<b>Proposition:</b> A function $ f : (X, \| . \|_X) \to (Y, \| . \|_Y) $ is <b>continuous</b> if and only if $\forall x \in X $ and <b>every sequence</b> $ (x_n) $ in $ X $
\[ x_n \to x \implies f(x_n) \to f(x) \]
</details>

---

## Banach Spaces

<details>
<summary> Define Banach Space</summary>
<p> A <b>Normed space</b> $ (X, \| . \|) $ is a <b> Banach Space</b> if it is <b>Complete</b>, i.e every Cauchy Sequence in $X$ converges in X. </p>

</details>

<details> <summary>What is an equivalent definition of a subspace of Banach space being complete</summary>
    <p><b>Proposition: </b> Let $(X, \| . \|) $ be a Banach space, $ Y \subseteq X $ is a subspace of $X$. Then $ (Y, \| . \| ) $ is <b>Complete</b> iff $ Y \subseteq X $ is <b>closed</b> in $X$. </p>

    <p><b>Proof:</b> $\Rightarrow $ Let $ (y_n) $ be a sequence in $Y$ such that $y_n \to x \in X $. Then $(y_n)$ is Cauchy in $Y$ and by <b>uniqueness of limits</b> $y = x \in Y $. Thus $Y$ is <b>complete</b> </p>

    <p>$\Leftarrow$ If $(y_n)$ is a cauchy sequence in $(Y, \| . \|)$, then it is also a cauchy sequence in $(X, \| .\| ) $ and since $X$ is complete therefore $y_n \to x \in X $. But as $Y$ is closed (by assumption), it must be that $x \in Y$. Hence $(Y, \| . \|)$ is <b>complete</b> </p>

</details>

---

## Hilbert Spaces

<details> <summary> Define Hilbert Space</summary>
<p> A <b>Hilbert Space</b> is an <b>inner product space</b> $(X, \langle \cdot , \cdot \rangle)$ which is <b>complete</b> with respect to the <b>induced norm</b> $\| x \| = {\langle x, x \rangle}^\frac{1}{2} $ 

</p>

</details>

---

## Hölder's Inequality
<details> <summary> State Hölder's Inequality </summary>
<p> <b>Lemma:</b> 
Let $ 1 \leq p \lneq q \leq \infty $ be <b> conjugates exponents </b> i.e $ \frac{1}{p} + \frac{1}{q} = 1 $ (note: $\frac{1}{\infty} = 0 $). Then:
</p>
    <details> <summary> Euclidean Space form </summary>
        <p>
        1. $\forall x, y \in \mathbb{R}^n $ we have $ \abs{\sum_{i=1}^n x_i y_i } \leq \norm{x}{}_p \norm{y}{}_q $
        </p>
        <details> <summary> <b>Proof:</b></summary>
        <p>

        </p>
        </details>
    </details>
    <details> <summary> Sequence Space form </summary>
        <p>
        2. $\forall (x_n) $ in $ \ell^p $ and $ \forall (y_n)$ in $\ell^q$ the series $\sum_{i=1}^\infty x_i y_i $ converges absolutely and furthermore $\abs{\sum_{i=1}^\infty x_i y_i} \leq \norm{(x_n)}{}_{\ell^p} \cdot \norm{(y_n)}{}_{\ell^q}$
        </p>
        <details> <summary> <b>Proof:</b></summary>
        <p>

        </p>
        </details>
    </details>
    <details> <summary> Function Space form </summary>
    <p>
    3. If $ f \in L^p(\Omega)$ and $g \in L^q(\Omega)$ then $f \cdot g$ is integrable and $\abs{\int_{\Omega} f \cdot g } \leq \norm{f}{}_{L^p} \cdot \norm{g}{}_{L^q}$
    </p>
    </details>
    <details> <summary> <b>Proof:</b></summary>
    <p>

    </p>
    </details>
</details>

---

## Completeness

<details> 
    <summary> State the equivalent condition that a normed space is complete </summary>

    <b>Lemma:</b> Let $(x_n)$ be a <b>cauchy sequence</b> in a <b>normed space</b> $(X, \norm{\cdot}{})$. Then the following statements are equivalent:


    1. $(x_n)$ <b>converges</b>

    2. $(x_n)$ has a <b>convergent subsequence</b>.

        <details>
            <summary> <b>Proof:</b></summary>
            <p>
            $\Rightarrow$: (i) $ \implies $ (ii) is trivial.
            </p>
            <p>
            $\Leftarrow$: Suppose that <b>there exists</b> a <b>convergent subsequence</b> $ ( x_{n_k} ) $ such that $(x_{n_k}) \to x \in X$.
            Given any $\epsilon > 0$, $ \exists N \in \mathbb{N} $ such that $\forall n,m \geq N$ then $\norm{x_n - x_m}{} < \frac{\epsilon}{2}$ <br/>
            Furthermore, we can choose $ K \in \mathbb{N} $ such that $ \forall k \geq K $, $\norm{x_{n_k} - x}{} < \frac{\epsilon}{2}$. Then for 
            $n \geq N$, we can choose $k \geq K$ such that $n_k \geq N$ which gives:
            $$
                \norm{x_n - x}{} \leq \norm{x - x_{n_k}} + \norm{x_n - x_{n_k}} < 2 \frac{\epsilon}{2} = \epsilon

            $$
            </p>
        </details>

</details>

---

## Equivalent definition of Banach spaces
<details> <summary> What is the equivalent definition of a Banach Space in terms of Absolute convergence </summary>
<p> <b>Proposition:</b> 
Let $(X, \norm{\cdot})$ is a normed vector space. Then the following statements are equivalent:
</p>
<ol>
<li>$(X, \norm{\cdot})$ is a Banach Space.</li>
<li>Absolute convergence of series implies convergence in the space, i.e. for sequence $(x_n)$ in $X$ and corresponding partial sums $ s_n := \sum_{k=1}^n x_k $
we have that 
$$
\sum_{k=1}^\infty \norm{x_k} < \infty \implies s_n \to s \in X
$$
</li>
</ol>
    <details> <summary> <b>Proof:</b></summary>
    <p>
        $\Rightarrow$: If $\sum_{n=1}^\infty \norm{x_n} < \infty $ then $s_n$ is Cauchy because 
        $$
        \norm{s_n - s_m} = \norm{\sum_{k=n+1}^m x_k} \leq \sum_{k=n+1}^m \norm{x_k}
        $$
        and finally $ \exists N \in \mathbb{N} $ such that $\forall n,m \geq N$, $\sum_{k=N+1}^\infty \norm{x_k} \to 0$ as $N \to \infty$
        and so $\sum_{k=n+1}^m \norm{x_k} \leq \sum_{k=N+1}^\infty \norm{x_k} \to 0$.
        Finally since $X$ is a banach space therefore $s_n \to s \in X$
    </p>
    <p>
        $\Leftarrow$: Let $(x_n)$ be a Cauchy sequeunce in $X$. Choose a subsequence $(x_{n_k})$ such that $\norm{x_{n_k} - x_{n_{k+1}}} \leq 2^{-k}$.
        This is possible because $(x_n)$ is cauchy. Then $\sum_{k=1}^\infty \norm{x_{n_{k+1}} - x_{n_k}} \leq 1 < \infty$. So by our assumption,
        $\sum_{k=1}^\infty x_{n_{k+1}} - x_{n_k}$ converges. Thus, $x_{n_k} = x_{n_1} + \sum{i=1}^{k-1} x_{n_{i+1}} - x_{n_i}$ converges.
        Therefore, by proposition above describing equivalent definition of Banach spaces, we have that $(x_n)$ converges thus $X$ is a Banach space.
    </p>
    </details>
</details>

---


# Bounded Linear Operators

---

## Bounded Linear Operator
<details> <summary> Define Bounded Linear Operator </summary>
    <p>
    Let $(X, \norm{\cdot}{}_X)$ and $(Y, \norm{\cdot}{}_Y)$ be normed vector spaces (always assumed over the same field \mathbb{F}).
    Then we say that $T : X \to Y$  is a bounded linear operator (aka bounded linear transformation) if $T$ is linear (i.e. $T(x + ay) = T(x) + aT(y)$ $\forall x,y \in X$, $a \in \mathbb{F}$ 
    and $T$ has the property that there exists $M \in \mathbb{R}$ such that $ \forall x \in X$ $\norm{Tx}{}_Y \leq M \norm{x}{}_X$  .
    
    </p>
</details>
<details> <summary> Set of bounded operator notation </summary>
    <p>
    We let $L(X,Y) := \{T: X \to Y \  \text{bounded linear operator} \} $ which we equip with the so called operator norm which is 
    defined to be $\norm{T} := \inf{\{M : \norm{Tx}{}_Y \leq M \norm{x}{}_X \ \forall x \} }$
    </p>
    <p> Remark: $\norm{\cdot}{}_{L(X,Y)}$ is the only norm on $L(X,Y)$ (that we use). </p>
    <p> Remark: $L(X,Y) = L(X)$ notation wise. </p>

</details>

---

## Equivalent definitions of Bounded linear operators
<details> <summary> State 6 equivalend definitions of bounded linear operators</summary>
<p> 
    <b>Proposition:</b> 
    Let $X$ and $Y$ be normed vector spaces and let $T: X \to Y$ be a linear map. Then the following statements are equivalent:
    <ol>
        <li>$T$ is Uniformly continuous</li>
        <li>$T$ is Lipschitz continuous</li>
        <li>$T$ is continuous </li>
        <li>$T$ is  conituous at $x_0 = 0$ </li>
        <li>$\forall x \in X$ there exists $K \in \mathbb{R}^{\geq 0} $ such that $\norm{T(x)} \leq K$ </li>
        <li>$T \in L(X,Y)$ </li>
    </ol>

</p>
<p>
    <details> <summary> <b>Proof:</b></summary>
    <p>
        1 $ \implies $ 2 $ \implies $ 3 $ \implies $ 4, by prelim analysis (trivial to prove using epsilon delta)
    </p>

    <p>
        $4 \Rightarrow 5$:
        As $T$ is continuous at $x_0 = 0$, take $\epsilon = 1$, $\exists \delta > 0$ such that $\norm{T(x)} < 1$ when $x \in X$ and $\norm{x} < \delta$.
        Let $\omega \in X$ with $\norm{\omega} \leq 1$. Now, $\norm{\frac{\delta \omega}{2}} \leq \frac{\delta}{2} \norm{\omega} \leq \frac{\delta}{2} < \delta$.
        Thus $\norm{T\left(\frac{\delta \omega}{2}\right)} < 1$ and as $T$ is linear, therefore $T\left(\frac{\delta \omega}{2}\right) = \frac{\delta}{2} T(\omega)$.
        So take $K = \frac{2}{\delta}$ which gives that $T$ satisfies (5).
    </p> 
    <p>
        $5 \Rightarrow 6$:
        Let $K$ be such that $\norm{T(x)} \leq K$ for $x \in X$ such that $\norm{x} \leq 1$. Since $T(0) = 0$ (as $T$ is linear), therefore 
        $\norm{T(0)} \leq K \norm{0}$. Let $ y \in X$ such that $y \neq 0$ and as $\norm{\frac{y}{\norm{y}}} = 1$, so $\norm{T\left(\frac{y}{\norm{y}}\right)} \leq K $
        and therefore $\norm{T(y)} \leq K \norm{y}$. Thus $T \in L(X,Y)$
    </p>
    <p>
        $6 \Rightarrow 1$:
        $T$ is a bounded linear operator so, $\forall x, y \in X$, $\exits K \in \mathbb{R}$ such that $\norm{T(x) - T(y)} = \norm{T(x-y)} \leq K \norm{x-y}$.
        Fix $\epsilon > 0$ and let $\delta = \frac{\epsilon}{K}$. Then for $x,y \in X$ with $\norm{x-y} < \delta$, $\norm{T(x) - T(y)} \leq K \norm{x - y} < k \cdot \delta = \epsilon $.
        Hence $T$ is uniformly continuous.
    </p>
    </details>

</p>
</details>

---

## Isometric Linear Maps
<details> <summary> Define Isometric Linear Maps </summary>
    <p>
        We call a linear function $T: X \to Y$ isometric if for every $x \in X$ we have that $\norm{Tx} = \norm{x}$.
    </p>
    <p>
        Remark: If $T$ is both isometric and bijective then we also have that $T^{-1}$ is linear and isometric.
        Such maps are called isometric isomorphisms and the spaces $X$ and $Y$ are called isometrically isomorphic.
    </p>

</details>

---

## Space of bounded linear operators is a banach space
<details> <summary> State the theorem that describes that space of bounded linear operators is a banach space. </summary>
    <p> 
        <strong>Theorem</strong>:
        Let $X$ be any normed vector space and let $Y$ be a banach space. Then $L(X,Y)$ equipped with the operator norm is complete
        and thus Banach space.
    </p>
    <details>
        <summary> <strong>Proof:</strong> </summary>
        <p>
        Let $(T_n)$ be a cauchy-sequence in $L(X,Y)$. Then for every $x \in X$ we have that
        $$
            \norm{T_nx - T_mx} \leq \norm{T_n - T_m}\norm{x} \to 0
        $$
        as $n,m \to \infty$. So, $(T_nx)$ is a cauchy sequence in $Y$ and $Y$ is banach (so complete) therefore $T_nx$
        converges to some $Tx \in Y$. Now, we show that $x \mapsto Tx$ is an element of $L(X,Y)$ and $T_n \to T$ in $L(X,Y)$.
        </p>
        <p>
        First note that, by linearity of $T_n$ and AOL impliest that $T$ is linear. Now, fix $\epsilon > 0$, $\exists N\in \mathbb{N}$ such that 
        $\forall n,m \geq N$ we have $\norm{T_n -T_m} < \epsilon$.
        So for any $x \in X$, we have that:
        $$
            \norm{Tx - T_nx} = \norm{\lim_{m\to \infty} T_mx - T_nx} = \lim_{m \to \infty} \norm{T_mx - T_nx} < \epsilon \norm{x}. 
        $$ 
        Therefore, $T$ is bounded and linear thus $T \in L(X,Y)$ and $\norm{T - T_n} < \epsilon$ for all $n \geq N$, and 
        since $\epsilon > 0$ was chosen arbitrarily so $T_n \to T$ as $n \to \infty$. Thus $L(X,Y)$ is complete and hence Banach.
        </p>
</details>




<!-- 
# Template for new Theorem proof block
<details> <summary> Statement </summary>
<p> <b>Proposition:</b> 

</p>
    <details> <summary> <b>Proof:</b></summary>
    <p>

    </p>
    </details>


</details>
 -->
