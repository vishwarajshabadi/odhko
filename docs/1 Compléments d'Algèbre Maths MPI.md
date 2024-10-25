# 1 Compléments d'Algèbre Maths MPI

## Définition d'une projection

### Définition

$p$ est une projection si $p^2=p$.

## Décomposition de l'espace associé à une projection

### Prop

Soit $p$ une projection. Alors $E=\text{Im}(p)\oplus\text{Ker}(p)$.

### Démo

$y\in Im(p) \cap Ker(p) \Rightarrow \exists x\in E, y=p(x) \text{ et } p(y)=0 \Rightarrow p^2(x)=0 \Rightarrow p(x)=0 \Rightarrow y=0$.

$x \in E \Rightarrow x=p(x)+(x-p(x)) \text{ avec } p(x)\in Im(p) \text{ et } x-p(x)\in Ker(p)$.

## Caractérisation de l'injectivité d'une application linéaire

### Prop

$u$ est injective $\Leftrightarrow \text{Ker}(u)=\{0\}$.

### Démo

$\Rightarrow$ : u est injective et $u(0) = 0$

$\Leftarrow$ : $u(x)=u(y) \Rightarrow u(x)-u(y)=0 \Rightarrow u(x-y)=0 \Rightarrow x-y=0 \Rightarrow x=y$.

## Théorème du rang

### Th

$dim(E)=dim(Im(u))+dim(Ker(u))$.

### Démo

$S$ supplémentaire de $Ker(u)$ dans $E$ ie. $E=Ker(u)\oplus S$ donc $dim(E)=dim(Ker(u))+dim(S)$.

$\tilde u : \begin{array}{ccc} Ker(u)\oplus S & \longrightarrow & Im(u) \\ x & \longmapsto & u_{\vert S}(x) \end{array}$

inj: $x \in Ker(\tilde u) \Rightarrow x \in Ker(u) \cap S = \{0\} \Rightarrow Ker(\tilde u)=\{0\}$

surj: $y \in Im(u) \Rightarrow \exists x \in E, u(x)=y$ or $E = Ker(u) \oplus S \Rightarrow \exists !(x_k, x_s) \in Ker(u) \times S, x=x_k+x_s \Rightarrow y = u(x) = u(x_k) + u(x_s) = u_{\vert S}(x_s) \Rightarrow y \in Im(\tilde u)$

## Si une application linéaire est bijective, sa réciproque est linéaire

### Prop

$u \in GL(E,F) \Rightarrow u^{-1} \in GL(F,E)$.

### Démo

- $u(0_E)=0_F \Rightarrow u^{-1}(0_F)=0_E$
- Mq $u^{-1}(\lambda x +\mu y)=\lambda u^{-1}(x)+\mu u^{-1}(y)$

## Si une somme de n sous-espaces est directe, la décomposition d'un vecteur est unique

### Prop

Si $\displaystyle E = \bigoplus_{i=1}^n E_i$, alors $\forall x \in E, \exists ! (x_1, \ldots, x_n) \in E_1 \times \ldots \times E_n, x = x_1 + \ldots + x_n$.

### Démo

Supposons que $\exists (x_1, \ldots, x_n) \in E_1 \times \ldots \times E_n, x = \sum x_i = \sum y_i$.

$\sum x_i - y_i = 0$ or la somme est directe donc $\forall i, x_i - y_i = 0 \Rightarrow x_i = y_i$.

## Une application linéaire est entièrement déterminée par l'image d'une base

### Prop

$B$ base de $E$, $F =(f_1,\ldots,f_n)$ famille de $F$. Alors
$\exists! u \in L(E,F), \forall i, u(e_i)=f_i$.

### Démo

#### Existence

$u : x = \sum x_i e_i \mapsto \sum x_i f_i$.
Mq linéaire et convient.

#### Unicité

Soient $u,v$ qui envoyent $B$ sur $F$.
Posons $x = \sum x_i e_i \in E$
$u(x) = u(\sum x_i e_i) = \sum x_i u(e_i) = \sum x_i f_i = \sum x_i v(e_i) = v(\sum x_i e_i) = v(x)$.

## Le noyau d'une forme linéaire non-nulle est un hyperplan

### Prop

Soit $\varphi \in E^*$ non nulle. Alors $Ker(\varphi)$ est un hyperplan.

### Démo

#### En dim finie

$\varphi \neq 0 \Rightarrow Im(\varphi) \neq \{0\} \Rightarrow rg(\varphi) = 1 \Rightarrow dim(Ker(\varphi)) = dim(E) - rg(\varphi) = dim(E) - 1$. Donc $Ker(\varphi)$ est un hyperplan.

#### Cas général

$\varphi \neq 0 \Rightarrow \exists x_0 \in E, \varphi(x_0) \neq 0$
Posons $\Delta = Vect(x_0)$

Soit $x \in Ker(\varphi) \cap \Delta$ ie $\varphi(x) = 0$ et $x = \lambda x_0 \Rightarrow \varphi(\lambda x_0) = \lambda \varphi(x_0) = 0 \Rightarrow \lambda = 0 \Rightarrow x = 0$.

Soit $x \in E$,

Analyse :
$x = x_k + x_\Delta$
$\lambda = \frac{\varphi(x)}{\varphi(x_0)}$
donc $x_\Delta = \frac{\varphi(x)}{\varphi(x_0)} x_0$ et $x_k = x - x_\Delta$

Synthèse :

- $x_\Delta \in \Delta$
- $x_k \in Ker(\varphi)$
- $x = x_k + x_\Delta$
	$\Delta$ de dim 1

## L'image directe et l'image réciproque de s.e.v par une application linéaire sont des s.e.v

### Prop

$E,F$ e.v, $E_1 \subset E, F_1 \subset F, u \in L(E,F)$
Alors $u(E_1)$ et $u^{-1}(F_1)$ sont des s.e.v de $F$ et $E$ respectivement.

### Démo

- $u(E_1) \subset F$ , $u^{-1}(F_1) \subset E$
- $u(0_E) = 0_F \Rightarrow 0_F \in u(E_1)$, $u^{-1}(0_F) = 0_E \in u^{-1}(F_1)$
- stable par CL

## Déterminant d'une matrice triangulaire par blocs

### Prop

$M = \left(\begin{array}{c|c} A & B \\ \hline 0 & C \end{array}\right)$

$$Det(M) = Det(A)Det(C)$$

### Démo

Si $A$ inversible:
$M = \left(\begin{array}{c|c} A & 0 \\ \hline 0 & I_p \end{array}\right) \times \left(\begin{array}{c|c} I_q & A^{-1}B \\ \hline 0 & C \end{array}\right)$

$\Rightarrow \text{Det}(M) = \left[\begin{array}{c|c} A & (0) \\ \hline (0) & ^1\ddots _1 \end{array}\right] \times \left[\begin{array}{c|c} ^1\ddots _1 & A^{-1}B \\ \hline (0) & C \end{array}\right]$

Sinon:
$Det(A) = 0 \Rightarrow \text{ colonnes de A forment une famille liée}$
$\Rightarrow \text{ colonnes de M forment une famille liée}$
$\Rightarrow \text{Det}(M) = 0$

## Expression du polynôme interpolateur

### Prop

Soient $(a_0, \ldots, a_n)$ et $(b_0, \ldots, b_n) \in \mathbb{R}^{n+1}$.
Alors $\exists! P \in \mathbb{R}_n[X], \forall i, P(a_i) = b_i$.

### Démo

#### Existence

$\displaystyle L_i(X) = \prod_{k=0, k\neq i}^n \frac{X-a_k}{a_i-a_k}$
$L_i(a_k) = \delta_{k,i}$
$P(X) = \sum b_i L_i(a_k)$
$P(a_k) = \sum b_i L_i(a_k) = \sum b_i \delta_{k,i} = b_k$

#### Unicité

$\varphi : P \mapsto (P(a_0), \ldots, P(a_n))$

inj: $P \in Ker(\varphi) \Rightarrow P(a_i) = 0 \Rightarrow P = 0$

bij: $\varphi$ est linéaire et injective entre espaces de même dimension donc bijective.

## Majoration de la dimension d'une somme de sous-espaces vectoriels (en dimension finie) par la somme des dimensions

### Prop

Soient $E_1, \ldots, E_p$ des s.e.v de $E$ de dimension finie.
Alors
$$\displaystyle dim(\sum_{i=1}^p E_i) \leq \sum_{i=1}^p dim(E_i)$$

### Démo

$p = 2$ :
$dim(E_1 + E_2) = dim(E_1) + dim(E_2) - dim(E_1 \cap E_2)$ -> Formule de Grassman
$\leq dim(E_1) + dim(E_2)$

$H_p \Rightarrow H_{p+1}$ :
$\displaystyle dim(E_1 + \ldots + E_{p+1}) = dim((E_1 + \ldots + E_p) + E_{p+1}) - dim((E_1 + \ldots + E_p) \cap E_{p+1}) \leq dim(E_1 + \ldots + E_p) + dim(E_{p+1}) \leq \sum_{i=1}^{p+1} dim(E_i)$

## Deux matrices sont équivalentes si et seulement si elles ont le même rang

### Prop

$A \sim B \Leftrightarrow rg(A) = rg(B)$

## Formule de changement de base

### Prop

$Mat_{C_2,B_2}(u) = P_{C_2,C_1}Mat_{C_1,B_1}(u)P_{B_1,B_2}$
