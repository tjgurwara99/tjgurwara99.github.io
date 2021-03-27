---
layout: post
title: Functional Analysis II Notes
subtitle: Everything that I learnt in Functional Analysis II (revision)
tags: [functional-analysis, hilbert-spaces]
comments: true
---

# Hilbert Spaces

---
## Inner Product and Norm it generates
<ol>
<li>
    <details> <summary> State the definition of Inner Product </summary> 
        <p>
            <strong> Definition: </strong>
            An inner (scalar) product in a linear vector space $X$ over $\mathbb{R}$ is a real-valued function on $X \times X$, denoted as $\langle x, y \rangle$, 
            having the following properties:
            <ol>
                <li>
                    <strong> Bilinearity: </strong> For a fixed $y$, $\langle x, y \rangle$ is a linear function of $x$, and for a fixed $x$,
                    $\langle x, y \rangle$ is a linear function of $y$.
                </li>
                <li>
                    <strong> Symmetry: </strong> $\langle x, y \rangle = \langle y, x \rangle$ for all $x, y \in X$.
                </li>
                <li>
                    <strong> Positivity: </strong> $\langle x, x \rangle > 0 $ for $x \neq 0$.
                </li>
            </ol>
        </p>
        <p>
        If we have that $X$ is a linear vector space over $\mathbb{C}$ then 1. and 2. of the above defintion are replaced by:
        <ol>
            <li>
                <strong> Sesquilinearity: </strong> For a fixed $y$, $\langle x, y \rangle$ is a linear function of $x$, and for a fixed $x$, $\langle x, y \rangle$
                is a skewlinear function of $y$, i.e for all $x, y \in X$,
                $$
                    \langle ax, y \rangle = a \langle x y \rangle \ \text{and} \ \langle x, ay \rangle = \bar{a} \langle x, y \rangle
                $$
            </li>
            <li>
                <strong> Skew symmetry: </strong> $\langle x, y \rangle = \overline{\langle y, x \rangle }$ for all $x, y \in X$.
            </li>
        </ol>
        </p>
        <p>
            <strong> REMARK: </strong> We know that the inner product can generate a norm on the space, as follows:
            $$
                \| x \| = \langle x, x \rangle^{1/2}.
            $$ 
        </p>
    </details>
</li>
<li>
    <details> <summary> State the necessary theorem needed to prove that the norm generated by inner product is indeed a norm. </summary>
        <p>
            <strong> Theorem: </strong> (Cauchy-Schwarz Inequality).
            For $x, y \in X$,
            $$
                | \langle x, y \rangle | \leq \| x \| \| y \|.
            $$
            Equality holds if and only if $x$ and $y$ are linearly dependent.
        </p>
        <details> <summary> <strong> Proof: </strong> </summary>
            <p>
                If $y = 0$, then the statement is trivially true.
            </p>
            <p>
                Therefore, we assume that $y \neq 0$. Replacing $x$ by $ax$ with $|a| = 1$ so that $a \langle x, y \rangle$ is real, we may assume WLOG that
                $\langle x, y \rangle$ is real.
            </p>
            <p> 
                For $t \in \mathbb{R}$, we compute using sesquilinearity and skew symmetry:
                $$
                    \|x + ty \|^2 = \langle x + ty, x + ty \rangle = \| x \|^2 + 2t \mathrm{Re}\langle x, y \rangle + t^2 \| y \|^2.
                $$
            </p>
            <p>
                By positivity, this quadratic polynomial in $t$ is non-negative for all $t$. This implies that
                $$
                    (Re \langle x, y \rangle)^2 - \| x \|^2 \| y \|^2 \leq 0,
                $$
                which gives the desired inequality. If equality holds, then there is some $t_0$ such that $x + t_0y = 0$. Then the result follows.
            </p>
        </details>
    </details>
</li>
<li>
    <details> <summary> Prove the norm that we define using the inner product indeed has the triangle inequality property. </summary>
        <p> <strong> Proof: </strong>
            Easy to prove but try it later.
        </p>
    </details>
</li>
<li>
    <details> <summary> State the definition of an inner product space. </summary>
        <p>
            <strong> Definition: </strong> A linear vector space with an inner product is called an inner product space.
        </p>
    </details>
</li>
<li>
    <details> <summary> State the definition of Hilbert spaces. </summary>
        <p>
            <strong> Definition: </strong> An inner product space which is complete with the induced norm is called a Hilbert space.
        </p>
        <p>
            <strong> NOTE: </strong> Given an inner product space, one can complete it with respect to the induced norm. Since the inner product is a continuous function on its factors, it can be extended to a completed space. Hence the extended space is a Hilbert space.
        </p>
    </details>
</li>
</ol>

---

## Examples of Hilber spaces

1. $\mathbb{R}^n$ and $\mathbb{C}^n$ with the usual dot product are Hilbert spaces called real and complex $n$-dimensional Euclidean space.
2. $l^2$ is a Hilbert space. For $ x = \{ x_n \} $, $ y = \{ y_n \} \in l^2 $ put $ \langle x, y \rangle = \sum x_n \bar{y}_n. $ Then 
$ \langle \cdot, \cdot \rangle $ is an inner product which defines a norm on $ l^2 $.
3. $L^2$ is a Hilbert space. The inner product of $f, g \in L^2$ is $ \langle f, g \rangle = \int f \bar{g} $. Note that this space is complete (proven as a
consequence of Riesz-Fisher theorem.)
4. The space $C[0,1]$ of continuous functions on the interval $[0,1]$ is an incomplete inner product space with the inner product taken from $L^2$.
5. **Bergman Space**: Let $\mathbb{D}$ be the open unit disk in $\mathbb{C}$. The space $A^2(\mathbb{D})$ consists of all functions which are square integrable
and holomorphic in $\mathbb{D}$ is a closed subspace of $L^2(\mathbb{D})$ and is thus a Hilbert space. (This is a consequence of being closed in a hilbert space.)
6. **Hardy Space**: The space $H^2(\mathbb{T})$ of all functions $f \in L^2(-\pi, \pi)$ whose Fourier series are of the form $ \sum_{n \geq 0} a_n e^{inx} $ is a
closed subspace of $L^2(-\pi, \pi)$ and is thus a Hilbert space.
7. **Sobolev Space $H^1(a,b)$**: The space $H^1(a,b)$ is a Hilbert space with the inner product $\braket{u,v} = \int_a^b (u\bar{v} + u'\bar{v}' \dx.$ We say that $u \in H^1(a,b)$ if $u\in L^2(a,b)$ and there exists a function $v \in L^2(a,b)$ such that for some constant $A$ and for almost all $x \in (a,b).$

$$
    u(x) = A + \int_a^x v(y) \dx
$$

Note: There could be something going on with **Sobolev spaces** and **Gronwall's inequality/lemma**.

---

## Orthogonality

<ol>
<li>
<details> <summary> Define what is meant by two vectors are orthogonal </summary>
    <p>
        <strong> Definition: </strong>
        Two vectos $x,y \in (X, \ubraket)$ are said to be orthogonal if $\braket{x,y} = 0$.
    </p>

</details>
</li>

<li>
<details> <summary> Define Orthogonal complement of a space </summary>
    <p>
        <strong> Definition: </strong>
        Let $Y$ be a subset of $(X, \ubraket)$. We define (orthagonal complement of $Y$ if $Y$ is a subspace of $X$ to be) $Y^\perp$ as the space of all vectors 
        $v \in X$ such that $\braket{v,y} = 0$ for all $y \in Y$.
    </p>
</details>
</li>

<li>
<details> <summary> State the properties of Orthogonal Complement of a subset of inner product space </summary>
       <ol>
            <li>
                <details>
                    <summary>
                        $Y^\perp$ is a closed subspace of $X$.
                    </summary>
                    <p>
                    <details> <summary> <strong> Proof </strong> </summary>
                    <p>
                        It is clear that $Y^\perp$ is a linear space of $X$. (Hint: take $a \in Y^\perp$, $x,y \in X$, $\alpha, \beta \in \mathbb{F}$ and consider
                        $\braket{\alpha x + \beta y, a}$).
                    </p>
                    <p>
                        Now, to prove that it is a closed subspace, consider a sequence $(x_n)$ in $A^\perp$ such that $x_n \to x$ for some $x \in X$. Then for all
                        $a \in Y$, we have that:
                        $$
                            0 = \braket{0, a} = \lim_{n \to \infty} \braket{x - x_n, a} = \braket{x, a} - \lim{n \to \infty} \braket{x_n, a}
                        $$
                        which implies that $\braket{x, a} = 0$ thus $x \in Y^\perp$
                    </p>
                    </details>
                    </p>
                </details>
            </li>
            <li>
                <details> <summary> $Y^\perp \subset Y^{\perp\perp}.$ </summary>
                    <p>
                        <details> <summary> <strong> Proof: </strong> </summary>
                            <p>
                                We have that $Y \subset X$ and $Y^\perp := \{v \in X: \forall y \in Y \, \braket{v,y} = 0 \}$. Also, we have that
                                $ Y^{\perp\perp} := \{ z \in X : \forall v \in Y^\perp \, \braket{z,v} = 0 \}$. But then if $x \in Y$ then $\braket{x, y} = 0$
                                for all $y \in Y^\perp$. Note that $x \in X$ as $Y \subset X$, therefore $x \in Y^{\perp\perp}.$. Thus $Y \subset Y^{\perp\perp}.$
                            </p>
                        </details>
                    </p>
                </details>
            </li>
            <li>
                <details> <summary> If $Y \subset Z \subset X,$ then $Z^\perp \subset Y^\perp.$</summary>
                    <p>
                        <details> <summary> <strong> Proof: </strong> </summary>
                            <p>
                                Let $x \in Z^\perp$ and $y \in Z$ then $y \in Y \supset Y $, therefore $\braket{x, y} = 0$. This is true for arbitrary $y \in Y$,
                                thus $x \in Y^\perp \implies Z^\perp \subset Y^\perp$.
                            </p>
                        </details>
                    </p>
                </details>
            </li>
            <li>
                <details> <summary> $ \overline{U}^\perp = U^\perp $ </summary>
                    <p>
                        <details> <summary> <strong> Proof: </strong> </summary>
                            <p>
                                $ U \subseteq \overline{U}^\perp $ then $ \overline{U}^\perp \subseteq U^\perp $.
                            </p>
                            <p>
                                We know that $ \forall b \in \overline{U} $, there exists a sequence $ (b_n) \in U $ such that $ \norm{b_n - b} \to 0 $.
                                So for $ x \in U^\perp $, we have:
                                $$
                                    0 = \braket{0, x} = \lim_{n \to \infty} \braket{b_n - b, x} = \lim_{n \to \infty} \braket{b_n, x} - \braket{b, x}.
                                $$
                                Thus $ \braket{b, x} = 0$ by continuity of $\braket{\cdot, \cdot}. $ So $ x \in \overline{U}^\perp \implies U^\perp \subseteq \overline{U}^\perp $
                            </p>
                        </details>
                    </p>
                </details>
            </li>
            <li>
                    <details> <summary> $(\overline{\mathrm{span}Y})^\perp = Y^\perp$ </summary>
                        <p>
                            <details> <summary> <strong> Proof: </strong> </summary>
                                <p>
                                    Let $ U := \mathrm{Span}Y $, and we know that $ U \subseteq \overline{U} \implies \overline{U}^\perp \subseteq U^\perp $.
                                </p>
                                <p>
                                    If $v \in Y^\perp, u \in U$, then we have $ u = \sum_{i=1}^n \alpha_i y_i $ with $ y_i \in Y, \alpha_i \in \mathbb{F} $ &
                                    $ n \in \mathbb{N}. $ So 
                                </p>
                            </details>
                        </p>
                    </details>
            </li>
       </ol>
</details>
</li>

</ol>


<!-- for definitions

<li>
<details> <summary> </summary>
    <p>
        <strong> </strong>
        
    </p>
</details>
</li> -->