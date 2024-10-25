# 2 Espaces Vectoriels Maths MPI

## Définition d'une norme

- Forme : $\vert \vert . \vert \vert : \begin{array}{c} E \rightarrow \mathbb{R} \\ x \mapsto \vert \vert x \vert \vert \end{array}$
- Absolue homogénéité : $\forall x \in E, \forall \lambda \in \mathbb{R}, \vert \vert \lambda x \vert \vert = \vert \lambda \vert \vert \vert x \vert \vert$
- Définie positive : $\forall x \in E, \vert \vert x \vert \vert \geq 0$ et $\vert \vert x \vert \vert = 0 \Leftrightarrow x = 0$
- Inégalité triangulaire : $\forall x, y \in E, \vert \vert x + y \vert \vert \leq \vert \vert x \vert \vert + \vert \vert y \vert \vert$

## Normes usuelles

### $\mathbb{R}^n$

- $$\vert \vert x \vert \vert_1 = \sum_{i=1}^{n} \vert x_i \vert$$
- $$\vert \vert x \vert \vert_2 = \sqrt{\sum_{i=1}^{n} x_i^2}$$
- $$\vert \vert x \vert \vert_{\infty} = \max_{1 \leq i \leq n} \vert x_i \vert$$

### $\mathcal{C}([a, b], \mathbb{R})$

- $$\vert \vert f \vert \vert_1 = \int_{a}^{b} \vert f(t) \vert dt$$
- $$\vert \vert f \vert \vert_2 = \sqrt{\int_{a}^{b} f(t)^2 dt}$$
- $$\vert \vert f \vert \vert_{p} = \left( \int_{a}^{b} \vert f(t) \vert^p dt \right)^{\frac{1}{p}}$$

### $\mathcal{M}_{n, p}(\mathbb{K})$

- $$\vert \vert A \vert \vert_1 = \max_{1 \leq j \leq p} \sum_{i=1}^{n} \vert a_{ij} \vert$$
- $$\vert \vert A \vert \vert_2 = \sqrt{Tr(A^T A)}$$
- $$\vert \vert A \vert \vert_{\infty} = \max_{i,j} \vert a_{ij} \vert$$

### $\mathbb{R}[X]$

- $$\vert \vert P \vert \vert_1 = \sum_{i=0}^{n} \vert a_i \vert$$
- $$\vert \vert P \vert \vert_{\infty} = \max_{0 \leq i \leq n} \vert a_i \vert$$

## Deuxième inégalité triangulaire

### Prop

$$\forall x, y \in E, \vert \lVert x \rVert - \lVert y \rVert \vert \leq \lVert x + y \rVert$$

### Démo

I.T avec $ x + y - y$ puis symmétrie des roles.

## Montrer qu'une boule est convexe

### Déf boule

$$B_f(a,r) = \{ x \in E \vert \lVert x - a \rVert \leq r \}$$

### Prop

$$\forall x, y \in B_f(a,r), \forall \lambda \in [0,1], \lambda x + (1 - \lambda) y \in B_f(a,r)$$

### Démo

I.T, définition de la boule.

## Unicité de la limite d'une suite si elle existe

Soient $l, l'$ tq $x_n \longrightarrow l$ et $x_n \longrightarrow l'$
$\lVert l-l'\rVert \leq \lVert l-x_n+ x_n-l'\rVert \leq \lVert l-x_n\rVert + \lVert x_n-l'\rVert \longrightarrow 0$

## Deux normes équivalentes définissent les mêmes suites convergentes

### Prop

Soit $\lVert . \rVert_a$ et $\lVert . \rVert_b$ equivalentes. Alors $x_n \longrightarrow l$ pour $\lVert . \rVert_a \Leftrightarrow x_n \longrightarrow l$ pour $\lVert . \rVert_b$

### Démo

$a \lVert x \rVert_a \leq \lVert x \rVert_b \leq b \lVert x \rVert_a$
$0 \leq \lVert x_n - l \rVert_b \leq \beta \lVert x_n - l \rVert_a \longrightarrow 0$
donc $\lVert x_n - l \rVert_b \longrightarrow 0 \Rightarrow x_n \longrightarrow l$ pour $\lVert . \rVert_b$

## Deux définitions équivalentes d'une valeur d'adhérence d'une suite

- $a$ est une valeur d'adhérence de $(x_n)_n$ si $\exists$ une sous-suite $(x_{\varphi(n)})_n$ telle que $x_{\varphi(n)} \longrightarrow a$
- $a$ est une valeur d'adhérence de $(x_n)_n$ ssi $\forall r > 0, B_f(a,r)$ contient une infinité de termes de $(x_n)_n$
