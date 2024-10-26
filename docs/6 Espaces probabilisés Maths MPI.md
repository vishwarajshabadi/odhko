# 6 Espaces probabilisés Maths MPI

## Définition d'un ensemble dénombrable

On dit d'un ensemble qu'il est dénombrable si il est fini ou en bijection avec $\mathbb N$.

## Définition d'une tribu

Soit $\Omega$ un ensemble. On appelle tribu sur $\Omega$ un ensemble $T \subset \mathcal P(\Omega)$ tel que :

- $\emptyset \in T$
- $\forall A \in T, \overline A \in T$ (stabilité par complémentaire)
- $\displaystyle \forall (A_n)_n \in T^{\mathbb N}, \bigcup _{n=0} ^{+\infty} A_n \in T$ (stabilité par union dénombrable)

## Compatibilité d'une tribu avec l'intersection finie ou dénombrable

$$\left( \bigcap _{n=0} ^{+\infty} A_n \right) \in T$$

## Définition d'une mesure de probabilité

Soit $(\Omega, T)$ un espace probabilisé. On appelle mesure de probabilité sur $(\Omega, T)$ une application $p : T \rightarrow \mathbb R_+$ telle que :
- $\forall A \in T, p(A) \in [0, 1]$
- $p(\Omega) = 1$
- $\forall I$ ensemble dénombrable, $\forall (A_i)_i \in T^I$ disjoints, $\displaystyle p\left( \bigcup _{i \in I} A_i \right) = \sum _{i \in I} p(A_i)$

## La probabilité d'une union est inférieure à la somme des probabilités

$$p(A \cup B) \leq p(A) + p(B)$$

## Formule des probabilités totales

### Déf - Système quasi-complet d'événements

1. Les $(A_i)_i$ sont deux à deux disjoints : $\forall i \neq j, A_i \cap A_j = \emptyset$
2. $\displaystyle \bigcup _{i\in I} A_i$ est presque sûr: $\displaystyle \bigcup _{i\in I} A_i = 1$

### Prop

Soit $B\in T$,
$$p(B) = \sum _{i\in I} p(B \cap A_i)$$
et si pour tout $i\in I, p(A_i) > 0$ :
$$p(B) = \sum _{i\in I} p(A_i) \times p_{A_i}(B)$$

## Formule de Bayes

### Déf - Probabilité conditionnelle

$$p(A \cap B) = p_B(A) \times p(B)$$

### Prop - Formule de Bayes

$$p_B(A) = p_{A}(B) \times \frac{p(A)}{p(B)}$$

## Si A et B sont indépendants, alors A et B le sont également

### Déf - Évènements indépendants

$A$ et $B$ sont indépendants si $p(A \cap B) = p(A) \times p(B)$

### Déf - Famille d'évènements mutuellement indépendants et 2 à 2 indépendants

- $(A_i)_i$ sont mutuellement indépendants si:
	$$\forall J \subset I \text{ fini, } p\left( \bigcap _{j\in J} A_j \right) = \prod _{j\in J} p(A_j)$$
- $(A_i)_i$ sont 2 à 2 indépendants si:
	$$\forall i \neq j, p(A_i \cap A_j) = p(A_i) \times p(A_j)$$
- On a bien indépendance mutuelle $\Rightarrow$ indépendance 2 à 2 mais la réciproque est fausse.

### Prop

$A$ et $B$ indépendants $\Rightarrow$ $A$ et $\overline B$ indépendants

## Z est dénombrable, Q+ est dénombrable

### Prop

- $\mathbb Z$ est dénombrable

### Démo

On pose $\Phi : n \mapsto \begin{cases} -\frac n 2 & \text{ si n est pair} \\ \frac {n+1} 2 & \text{ si n est impair} \end{cases}$ qui est une bijection de $\mathbb N$ dans $\mathbb Z$

### Prop

$\mathbb Q_+$ est dénombrable

### Démo

Mq $\mathbb N \times \mathbb N ^*$ est dénombrable

## $\mathbb R$ N'est pas dénombrable

### Prop

$\mathbb R$ n'est pas dénombrable

### Démo

Procédé diagonal de Cantor

## Théorèmes de continuité croissante et décroissante

### Théorème de continuité croissante

Soit $(A_n)_n$ une suite croissante par l'inclusion, alors $\forall n \in \mathbb N, A_n \subset A_{n+1}$. Alors,
$$\lim _{n \rightarrow +\infty} p(A_n) = p\left( \bigcup _{n=0} ^{+\infty} A_n \right)$$

### Théorème de continuité décroissante

Soit $(A_n)_n$ une suite décroissante par l'inclusion, alors $\forall n \in \mathbb N, A_{n+1} \subset A_n$. Alors,
$$\lim _{n \rightarrow +\infty} p(A_n) = p\left( \bigcap _{n=0} ^{+\infty} A_n \right)$$

## Une tribu infinie n'est pas dénombrable

### Prop

Une tribu infinie n'est pas dénombrable
