# 3 Séries Vectorielles Maths MPI

## Définition d'une série convergente. Montrer que le reste tend vers 0

### Déf

$\sum u_n$ CV si $\left( S_n = \sum_{n=0}^N u_n \right) _{N \in \mathbb{N}}$ CV

### Prop

$\sum u_n$ CV $\Rightarrow R_n = \sum_{n=N+1}^{\infty} u_n \longrightarrow 0$

### Démo

$\displaystyle S =\sum _{n=0}^{N} u_n = S_N + R_N$ et $S_N \longrightarrow S$ donc $R_N \longrightarrow 0$

## Séries de Riemann

### Prop

$\sum \frac{1}{n^\alpha}$ CV $\Leftrightarrow \alpha > 1$

### Démo

Comparaison avec une intégrale

## Une série absolument convergente est convergente

### Prop

$\sum |u_n|$ CV $\Rightarrow \sum u_n$ CV

### Démo

Poser $u_n^+ = \max(u_n,0)$ et $u_n^- = \min(u_n,0)$
$S_N = S_N^+ - S_N^-$

## Critère de convergence des séries alternées

### Prop

Si

- $\forall n, u_n$ est du signe de $(-1)^n$
- $(\vert u_n \vert)_{n}$ est décroissante
- $\vert u_n \vert \longrightarrow 0$

Alors

- $\sum u_n$ CV
- $R_n$ est du signe de $u_{n-1}$ et $\vert R_n \vert \leq \vert u_{n-1} \vert$

## Règle de D'Alembert

Soit $u_n$, on suppose que $\frac{u_{n+1}}{u_n} \longrightarrow l \in \mathbb{R}_+ \cup \{+\infty\}$

- Si $l < 1$, $\sum u_n$ CV
- Si $l > 1$, $\sum u_n$ DV
- Si $l = 1$, on ne peut rien dire

## Théorèmes de sommation des relations de comparaison

### Cas CV

- Si $u_n = \mathcal O(v_n)$ et $\sum v_n$ CV alors $\begin{cases} \sum u_n \text{ CV} \\ R_n(u) = \mathcal O(R_n(v)) \end{cases}$
- Si $u_n = \mathcal o(v_n)$ et $\sum v_n$ CV alors $\begin{cases} \sum u_n \text{ CV} \\ R_n(u) = \mathcal o(R_n(v)) \end{cases}$
- Si $u_n \sim v_n$ et $\sum v_n$ CV alors $\begin{cases} \sum u_n \text{ CV} \\ R_n(u) \sim R_n(v) \end{cases}$

### Cas DV

- Si $u_n = \mathcal O(v_n)$ et $\sum v_n$ DV alors $\begin{cases} \sum u_n \text{ DV} \\ S_n(u) = \mathcal O(S_n(v)) \end{cases}$
- Si $u_n = \mathcal o(v_n)$ et $\sum v_n$ DV alors $\begin{cases} \sum u_n \text{ DV} \\ S_n(u) = \mathcal o(S_n(v)) \end{cases}$
- Si $u_n \sim v_n$ et $\sum v_n$ DV alors $\begin{cases} \sum u_n \text{ DV} \\ S_n(u) \sim S_n(v) \end{cases}$

## Critères de convergence

### Prop

1. Si $u_n \leq v_n$ et $\sum v_n$ CV alors $\sum u_n$ CV
2. Si $u_n = \mathcal O(v_n)$ et $\sum v_n$ CV alors $\sum u_n$ CV
3. Si $u_n = \mathcal o(v_n)$ et $\sum v_n$ CV alors $\sum u_n$ CV
4. Si $u_n \sim v_n$ et $\sum v_n$ alors $\sum u_n$ et $\sum v_n$ ont même nature

### Démo

1. $S_n(u) \leq S_n(v)$ ie $S_n(u)$ est majorée
	 $S_{N+1} - S_N = u_{N+1} \geq 0$ donc $S_n(u)$ est croissante
	 Donc $S_n(u)$ est convergente

## Principe de transformation suite-série

### Prop

$u_n$ CV $\Leftrightarrow \sum u_{n+1} - u_n$ CV

### Démo

#### $\Rightarrow$

$\displaystyle S_N = \sum _{n=0}^{N} u_{n+1} - u_n = u_{N+1} - u_0 \longrightarrow l - u_0$ donc $\sum u_{n+1} - u_n$ CV

#### $\Leftarrow$

$S_N$ CV vers $\tilde l$ or $S_N = u_{N+1} - u_0 \Rightarrow u_{N+1} - u_0 \longrightarrow \tilde l \Rightarrow lim u_N = \tilde l - u_0 = l$

## Définition d'une famille sommable, de réels positifs, puis de complexes

Soit $I$ fini ou dénombrable, $(u_i)_{i \in I} \in \mathbb{R}_+^I$
On pose $\displaystyle \sum u_i = \sup _{J \subset I, J \text{ fini}} \left( \sum _{i \in J} u_i \right) \in \mathbb{R}_+ \cup \{+\infty\}$
On dit que la famille $(u_i)_{i \in I}$ est sommable si $\sum u_i < +\infty$
Avec $(u_i)_{i \in I} \in \mathbb{R}^I \text{ ou } \mathbb{C}^I$, $\sum u_i$ est sommable si $(\vert u_i \vert)$ est sommable.
Soit $(v_n)_{n \in \mathbb{N}} \in \mathbb{R}^{\mathbb{N}}$, alors $(v_n)$ est sommable $\Leftrightarrow \sum v_n$ CVA

## Théorème de sommation par paquets

Soit $I = \displaystyle \bigcup_{j \in J} I_j$ avec $J$ fini ou dénombrable et $\forall j \in J, I_j$ fini ou dénombrable.

1. Soit $(u_i)_{i \in I} \in \mathbb{R}_+^I$ alors $\sum u_i = \displaystyle \sum _{j \in J} \left( \sum _{i \in I_j} u_i \right)$
2. Soit $(u_i)_{i \in I} \in \mathbb{R}^I$ ou $\mathbb{C}^I$. Si $(u_i)_{i \in I}$ est sommable alors $\sum u_i = \displaystyle \sum _{j \in J} \left( \sum _{i \in I_j} u_i \right)$

## Produit de Cauchy de deux séries absolument convergentes

Soit $\sum u_n$ et $\sum v_n$ deux séries absolument convergentes.

$$\left( \sum _{n=0}^{+\infty} u_n \right) \left( \sum _{n=0}^{+\infty} v_n \right) = \sum _{n=0}^{+\infty} \left( \sum _{k=0}^{n} u_k v_{n-k} \right) = \sum _{n=0}^{+\infty} \sum _{k=0}^{n} u_{n-k} v_k$$

## Formule de Stirling

$$n! \sim \sqrt{2\pi}n^{n +\frac {1} {2}}e^{-n}$$

### Démo

1. $\exists \alpha  \frac { n!}{\sqrt n n^n e-n}\longrightarrow \alpha$ (transformation suite-série)
2. Mq $\alpha = \sqrt{2\pi}$ (Intégrale de Wallis)

## Résultats sur les séries de Bertrand (HP)

$$\alpha ,\beta \in R, \sum \frac 1 {n^\alpha (\ln n)^\beta} \text{ CV} \Leftrightarrow \begin{cases}\alpha > 1 \\ \alpha = 1 \text { et } \beta > 1 \end{cases}$$
