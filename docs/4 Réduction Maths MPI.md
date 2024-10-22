# 4 Réduction Maths MPI

## Définitions de matrices semblables

- $\exists P \in GL_n(\mathbb{K})$ telle que $B = P^{-1}AP$.
- $\exists u \in \mathcal{L}(\mathbb{K}^n), \exists B_1,B_2$ 2 bases de $\mathbb{K}^n$ telles que $A = Mat_{B_1}(u)$ et $B = Mat_{B_2}(u)$.

## Deux matrices semblables ont même rang, même trace, même déterminant et même polynôme caractéristique

### Prop

Soit A et B semblables

1. $rg(A) = rg(B)$.
2. $Tr(A) = Tr(B)$.
3. $Det(A) = Det(B)$.
4. $\chi_A = \chi_B$.

### Démonstration

1. $rg(A) = rg(u) = rg(B)$.
2. $Tr(A) = Tr(P^{-1}BP) = Tr(BP^{-1}P) = Tr(B)$.
3. $Det(A) = Det(P^{-1}BP) = Det(P^{-1})Det(B)Det(P) = Det(B)$.
4. $\chi_A = Det(X I_n - A) = Det(X I_n - P^{-1}BP) = Det(P^{-1}(X I_n - B)P) = Det(X I_n - B) = \chi_B$.

## Définition d'une valeur propre et d'un vecteur propre

- $x$ est un vecteur propre de $u$ si $\begin{cases} x \neq 0 \\ \exists \lambda \in \mathbb{k} \quad u(x) = \lambda x \end{cases}$.
- $\lambda$ est une valeur propre de $u$ si $\exists x \neq 0 , u(x) = \lambda x$.

## Une droite est stable si et seulement si elle est dirigée par un vecteur propre

### Démonstration

Soit $x \neq 0$, notons $\Delta = Vect(x)$.

- Stable $\Rightarrow$ $u(x) = \lambda x$. ie $x$ est un vecteur propre.
- $u(x) = \lambda x$, $y = \mu x\in \Delta$, $u(y) = \mu u(x) = \mu \lambda x \in \Delta$ donc stable.

## Des sous-espaces propres associés à des valeurs propres distinctes sont en somme directe

### Prop

Soit $E$ un $\mathbb{K}$-ev de dimension finie, $u \in \mathcal{L}(E)$, $\lambda_1,…\lambda_n$ valeurs propres distinctes de $u$, alors :
$$\displaystyle \sum_{1 \leq i \leq n} E_{\lambda_i}(u) = \bigoplus_{i = 1} ^n E_{\lambda_i}(u)$$

### Démonstration

Soit $x_i$ vecteur propre associé à $\lambda_i$ avec $1 \leq i \leq n$ tel que $\sum x_i = 0$
Composer par $(u-\lambda_1 Id)$, …, $(u-\lambda_{n-1} Id)$ : on a $x_n = … = x_1 = 0$.

## Si deux endos commutent, le noyau, l'image et les s.e.p de l'un sont stables par l'autre

### Prop

Soit $u, v \in \mathcal{L}(E)$ tels que $u\circ v = v \circ u$, alors:
$$\begin{cases} Ker(u) \text{ stable par } v \\ Im(u) \text{ stable par } v \\ E_{\lambda}(u) \text{ stable par } v \end{cases}$$
et
$$\begin{cases} Ker(v) \text{ stable par } u \\ Im(v) \text{ stable par } u \\ E_{\lambda}(v) \text{ stable par } u \end{cases}$$

### Démonstration

- $x \in Ker(u) \Rightarrow u(v(x)) = v(u(x)) = 0 \Rightarrow v(x) \in Ker(u)$.
- $y \in Im(u) \Rightarrow \exists x, y = u(x) \Rightarrow v(y) = v(u(x)) = u(v(x)) \in Im(u)$.
- $\lambda \in Sp(u)$, $x \in E_{\lambda}(u) \Rightarrow u(x) = \lambda x \Rightarrow v(u(x)) = u(v(x)) = \lambda v(x) \Rightarrow v(x) \in E_{\lambda}(u)$.

## Le polynôme caractéristique est un polynôme, unitaire, de degré n, dont on connait les coefficients de degré n-1 et 0

### Prop

$$\chi_u = X^n - Tr(A)X^{n-1} + … + (-1)^n Det(A)$$

## $Card(Sp(u)) \leq dim(E)$

### Démonstration

$Sp(u) = Rac(\chi_u)$, $\chi_u$ polynôme de degré $dim(E)$ ie $Card(Rac(\chi_u)) \leq dim(E)$.

## Définition du polynôme caractéristique et lien avec les valeurs propres

### Définition

$\chi_u = Det(X Id - (u)$.

### Prop

$Rac(\chi_u) = Sp(u)$.

### Démonstration

$\lambda \in Sp(u) \Leftrightarrow u(x) = \lambda x \Leftrightarrow x \in Ker(\lambda Id - u) \Leftrightarrow Ker \neq 0 \Leftrightarrow Det(\lambda Id - u) = 0 \Leftrightarrow \lambda \in Rac(\chi_u)$.

## Encadrement de la dimension d'un sous-espace propre, majoration avec la multiplicité de la valeur propre

### Prop

$1 \leq dim(E_{\lambda}(u)) \leq m_\lambda$.

### Démonstration

- $\lambda \in Sp(u) \Rightarrow \dim(E_{\lambda}(u)) \geq 1$.
- $F \subset E$ $u$-stable, soit $\tilde u$ induit, $\chi_{\tilde u} \vert \chi_u$ ie $m_{\lambda} \geq dim(E_{\lambda}(u))$ car $\chi_u = \prod_{\lambda \in Sp(u)} (X - \lambda)^{m_{\lambda}}$.

## Lien entre les valeurs propres et la trace et le déterminant pour une matrice trigonalisable

### Prop

Soit $A \in M_n(\mathbb{K})$ trigonalisable, alors:
$$\begin{cases} \displaystyle Tr(A) = \sum_{\lambda \in Sp(A)} \lambda m_\lambda \\ \displaystyle Det(A) = \prod_{\lambda \in Sp(A)} \lambda ^{m_\lambda} \end{cases}$$

### Démonstration

La trace et le déterminant sont invariants par similitude, en considérant une base où $A$ est trigonalisable, les valeurs propres sont sur la diagonale.

## Le nilindice est inférieur ou égal à la dimension de l'espace

### Prop

Soit u nilpotent d'indice $k$, alors $k \leq dim(E)$.

### Démonstration

Montrer que $(a, u(a), …, u^{k-1}(a))$ est libre en composant par $u ^{k-1}, …$.

## Si un s.e.v est u-stable, le polynôme caractéristique de l'endo induit divise celui de u

### Prop

Soit $F \subset E$ $u$-stable, alors $\chi_{u_{\vert F}} \vert \chi_u$.

## Théorème fondamental de diagonalisation à l'aide du polynôme caractéristique

### Théorème

$u$ diagonalisable $\Leftrightarrow \begin{cases} \chi_u \text{ scindé } \\ \forall \lambda \in Sp(u), m_\lambda = dim(E_{\lambda}(u)) \end{cases}$.

## En dimension finie, tout endomorphisme admet un polynôme annulateur non nul

### Prop

$\exists P \in \mathbb{K}[X] \setminus \{0\}$ tel que $P(u) = 0$.

### Démonstration

$(I_n, A,…, Â^{n^2})$ est liée donc $\exists (a_i)_{0\leq i \leq n^2}, \sum a_i A^i = 0$.
$\displaystyle P = \sum_{i=0} ^{n^2} a_i X^i$ convient.\

## Lien entre spectre et polynôme annulateur

### Prop

$Sp(u) \subset Rac(P)$ avec $P(u) = 0$.

### Démonstration

- $P(u) = 0 \Rightarrow \forall x \in E, P(u)(x) = 0 \Rightarrow P(u)(x_o) = 0$
- $P(u)(x_0) = \sum a_i u^i(x_0) = \sum a_i \lambda^i x_0 = x_0P(\lambda) = 0 \Rightarrow P(\lambda) = 0 \Rightarrow \lambda \in Rac(P)$.

## Existence et unicité du polynôme minimal en dimension finie

### Définition

Il existe un unique polynôme annulateur de u, noté $\Pi _u$, de degré minimal, unitaire et non nul.

### Démonstration

#### Existence

$D_u = \{degP\vert P \in \mathbb{K}[X], P(u) = 0\}$ est non vide car $\chi_u \in D_u$.
Il existe un polynôme de degré minimal, notons le $P_0$.
$\Pi_0 = \frac {P_0}{cd(P_0)}$ convient.

#### Unicité

$P=Q\Pi_u + R$ avec $deg(R) < deg(\Pi_u)$ et $P(u) = 0$ donc $R(u) = 0$ ie $R = 0$ donc $\Pi_u \vert P$.
S'il existe un autre polynôme minimal $Q_u$, alors $\Pi_u \vert Q_u$ et $Q_u \vert \Pi_u$ donc $\Pi_u = Q_u$.

## Théorème de Cayley Hamilton

### Théorème

$\chi_u(u) = 0$.

### Démonstration ($n = 2$)

Posons $A = \begin{pmatrix} a & b \\ c & d \end{pmatrix}$, ie $\begin{cases} u(e_1) = a e_1 + c e_2 \\ u(e_2) = b e_1 + d e_2 \end{cases}$.
Donc $\chi_u (u)= u ^2 - (a +d) u + (ad - bc) Id = 0$.

- $\chi_u (e_1) = 0$.
- $\chi_u (e_2) = 0$.
	Donc $\chi_u(u) = 0$ ( l'image d'une base détermine entièrement une A.L).

## Lemme de décomposition des noyaux

Soient $P_1, …, P_k$ premiers entre eux, alors:
$$Ker((P_1 \times…\times P_n)(u)) = \bigoplus_{i=1} ^n Ker(P_i(u))$$

## Si u est diagonalisable, tout endo induit sur un sous-espace stable l'est

### Prop

Soit $F \subset E$ $u$-stable, alors $u_{\vert F}$ diagonalisable.

### Démonstration

$\begin{cases} u \text{ diagonalisable } \Leftrightarrow \chi_u \text{ scindé simple } \\ F \text{ u-stable } \Rightarrow \chi_{u_{\vert F}} \vert \chi_u \end{cases} \Rightarrow \Pi_{\tilde u} \text{ scindé simple } \Rightarrow u_{\vert F} \text{ diagonalisable }$

## Caractérisation des endos trigonalisables par le polynôme minimal ou un polynôme annulateur

$u$ trigonalisable $\Leftrightarrow \begin{cases} \Pi_u \text{ scindé } \\ \text{ il existe un polynôme annulateur scindé } \end{cases}$.

## Le polynôme minimal divise tout polynôme annulateur

### Prop

$\Pi_u \vert P$ avec $P(u) = 0$.

### Démonstration

$P = \Pi_u Q + R$ avec $deg(R) < deg(\Pi_u)$ et $P(u) = 0$ donc $R(u) = 0$ ie $R = 0$.

## Le spectre est égal à l'ensemble des racines du polynôme minimal

### Prop

$Sp(u) = Rac(\Pi_u)$.

### Démonstration

- $Sp(u) \subset Rac(\Pi_u)$ [cf](docs/4%20Réduction%20Maths%20MPI#Définition%20du%20polynôme%20caractéristique%20et%20lien%20avec%20les%20valeurs%20propres)
- Soit $r \in Rac(\Pi_u)$, Si $ r \notin Sp(u)$ alors $(u - r Id) \in GL(E)$ or $r \in Rac(\Pi_u) \Rightarrow (X-r) \vert \Pi_u$ et $\frac {\Pi_u}{X-r} (u) = 0$ Absurde (son degré est strictement inférieur à celui de $\Pi_u$). $\Rightarrow r \in Sp(u)$.

## Un endomorphisme est diagonalisable ssi son polynôme minimal est scindé simple

### Prop

$u$ diagonalisable $\Leftrightarrow \begin{cases} \Pi_u \text{ scindé simple } \\ \text {il existe un polynôme annulateur scindé simple} \end{cases}$.

### Démonstration

#### $\Rightarrow$

$u$ diagonalisable $\Rightarrow \chi_u$ scindé.
$\displaystyle P_0 = \prod_{\lambda \in Sp(u)}( X - \lambda)$
Lemme de décomposition des noyaux $\Rightarrow Ker(P_0(u)) = …= E \Rightarrow P_0(u) = 0 \Rightarrow \Pi_u \vert P_0$ et $P_0$ scindé simple $\Rightarrow \Pi_u$ scindé simple.

#### $\Leftarrow$

Lemme de décomposition des noyaux $\displaystyle \Rightarrow Ker(\Pi_u(u)) = \bigoplus_{\lambda \in Sp(u)} Ker((u - \lambda Id)$ d'où $\displaystyle E = \bigoplus_{\lambda \in Sp(u)} E_{\lambda}(u)$.

## Si F est un sous-espace stable par u, le polynôme minimal de l'endo induit divise celui de u

### Prop

Soit $F \subset E$ $u$-stable, alors $\Pi_{u_{\vert F}} \vert \Pi_u$.

### Démonstration

$\Pi_u$ annule $\tilde u$ donc $\Pi_{\tilde u} \vert \Pi_u$.

## Définition des sous-espaces caractéristiques

$N_\lambda(u) = Ker((u - \lambda Id)^{m_\lambda})$

## Un endo est trigonalisable ssi son polynôme caractéristique est scindé

### Prop

$u$ trigonalisable $\Leftrightarrow \chi_u$ scindé.

## Une matrice $A$ est nilpotente si et seulement si $Tr(A^k) = 0$ pour tout entier $k$ non nul

### Prop

$A$ nilpotente $\Leftrightarrow \forall k \in \mathbb{N}^*, Tr(A^k) = 0$.

## Codiagonalisation de deux endomorphismes qui commutent

### Prop

Soit $u, v \in \mathcal{L}(E)$ tels que $u \circ v = v \circ u$, alors il existe une base de $E$ où $u$ et $v$ sont simultanément diagonaux.

## Toute matrice est limite d'une suite de matrices inversibles

### Prop

$\exists ( M_p)_p \in GL_n(\mathbb{K})^\N$ telle que $M_p \xrightarrow[p \to +\infty]{} A$.

## Si une matrice est inversible, son inverse est un polynôme en cette matric

### Prop

Soit $A \in GL_n(\mathbb{K})$, alors $\exists P \in \mathbb{K}[X]$ tel que $A^{-1} = P(A)$.

## Toute matrice est limite d'une suite de matrices diagonalisables

### Prop

$\exists (A_n)_n \in M_n(\mathbb{C})^\mathbb{N}$ telle que $A_n$ diagonalisable et $A_n \xrightarrow[n \to +\infty]{} A$.

## Décomposition de Dunford

### Théorème

Soit $u$ tel que $\chi_u$ scindé, alors;
$\exists ! (d,n) \in L(E)^2$ tels que:

- $u = d + n$.
- $d$ diagonalisable.
- $n$ nilpotent.
- $d \circ n = n \circ d$.

## Deux matrices réelles semblables dans $\mathcal{M}_n(\mathbb{C})$ sont semblables dans $\mathcal{M}_n(\mathbb{R})$

### Prop

Soit $A, B \in \mathcal{M}_n(\mathbb{R})$ telles que $A$ et $B$ sont semblables dans $\mathcal{M}_n(\mathbb{C})$, alors $A$ et $B$ sont semblables dans $\mathcal{M}_n(\mathbb{R})$.

# Tableau Synthése

|           | $\chi_u$                                                                                                                                                           | $\pi_u$                                                                                           | $P \ \text{tq.} \ P(u) = 0$                                   |
| --------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------------------------- | ------------------------------------------------------------- |
| $Sp(u)$   | $Sp(u) = Rac(\chi_u)$                                                                                                                                              | $Sp(u) = Rac(\pi_u)$                                                                              | $Sp(u) \subseteq Rac(P)$                                      |
| $d^\circ$ | $d^\circ(\chi_u) = n$                                                                                                                                              | $d^\circ(\pi_u) \leq n$                                                                           | $d^\circ(P) \geq d^\circ(\pi_u)$                              |
| **Diag.** | $u \ \text{diag.} \iff \left\{ \begin{array}{l} 1. \ \chi*u \ \text{scindé} \\ 2. \ \forall \lambda \in Sp(u), \ \dim(E*\lambda) = m\_\lambda \end{array} \right.$ | $u \ \text{diag.} \iff \left\{ \begin{array}{l} \pi_u \ \text{scindé simple} \end{array} \right.$ | $u \ \text{diag.} \iff \text{il existe un p.a scindé simple}$ |
| **Trig.** | $u \ \text{trig.} \iff \chi_u \ \text{scindé}$                                                                                                                     | $u \ \text{trig.} \iff \pi_u \ \text{scindé}$                                                     | $u \ \text{trig.} \iff \text{il existe un p.a scindé}$        |
