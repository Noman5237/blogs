---
title: Understanding Closures in Set Theory
date: 2024-01-13 05:30:00 +0630
categories: [Mathematics, Set Theory, Closures]
tags: [mathematics, set theory, closures]
math: true
author: noman
---

To understand closure, we need to understand the composition of relations.

## Composition of Relations
Let $R$ and $S$ be two relations where <br>
$R$ = {$(a, 0), (b, 1), (c, 2)$} and <br>
$S$ = {$(0, x), (1, y), (2, z)$}

The composition of $R$ and $S$ is defined as $R \circ S$ = {$(a, x), (b, y), (c, z)$}.

Let's understand this with diagrams.
![Set Composition of R and S](/assets/img/UnderstandingClosuresInSetTheory/set-composition.png){: .light }
![Set Composition of R and S](/assets/img/UnderstandingClosuresInSetTheory/set-composition-dark.png){: .dark }

The composition is also called the product of relations.
It's ironically similar to matrix multiplication if you think about the elements of the relations as matrices.

### Composition of Relations as Matrices
Lets take another example to understand the composition of relations by representing them as matrices.

Relation $R$ = {$(a, 0), (b, 1), (c, 2)$} can be represented as a matrix

$$
\begin{array}{c c} 
& \begin{array}{c c c} 0 & 1 &2 \\ \end{array} \\
\begin{array}{c c c}a\\b\\c \end{array} &
\left[
\begin{array}{c c c}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{array}
\right]
\end{array}
$$

Relation $S$ = {$(0, x), (1, y), (2, z)$} can be represented as a matrix

$$
\begin{array}{c c} 
& \begin{array}{c c c} x & y &z \\ \end{array} \\
\begin{array}{c c c}0\\1\\2 \end{array} &
\left[
\begin{array}{c c c}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{array}
\right]
\end{array}
$$

And the composition of $R$ and $S$ is basically the matrix multiplication of $R$ and $S$.

$$
\left[
\begin{matrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{matrix}
\right]
\cdot
\left[
\begin{matrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{matrix}
\right]
=
\left[
\begin{matrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{matrix}
\right]
$$

Now you can see why the composition of relations is also called the product of relations or written as $R \circ S$.

## Closure of Relations
There are three types of closures of relations.
1. Reflexive Closure
2. Symmetric Closure
3. Transitive Closure

We will particularly focus on the transitive closure of relations.

### Transitive Closure
Let's try to understand this by using a simple logic.
Say, $R$ = {$(a, b), (b, c), (c, d)$}.

where, $R(x, y)$ means $x > y$.

Simply by looking at the relation we can say that $a > b$, $b > c$, and $c > d$.

Now we can also infer that 
1. $a > c$ because $a > b$ and $b > c$.
2. $b > d$ because $b > c$ and $c > d$.

How can we induce and represent this in terms of relation composition?

If we try to compose the relation $R$ with itself, i.e. $R \circ R$, then,
![Set Composition of R and R](/assets/img/UnderstandingClosuresInSetTheory/r1composition.png){: .light }
![Set Composition of R and R](/assets/img/UnderstandingClosuresInSetTheory/r1composition-dark.png){: .dark }

We can see that $R \circ R$ = {$(a, c), (b, d)$}.

<!-- Say, if A is larger than B, and B is larger than C, then A is larger than C.

Now, if we represent this in terms of relations, we can say that
$R$ = {$(A, B)$}
$S$ = {$(B, C)$}
then by composition of relations, we can say that
$R \circ S$ = {$(A, C)$}

If we try to capture the whole logic in one relation, we can say that
$T$ = {$(A, B), (B, C), (A, C)$}
This relation is transitive because it contains compositions of all the relations within itself. -->

<!-- Let's try to visualize similar relationship like the one above with a directed graph. -->

