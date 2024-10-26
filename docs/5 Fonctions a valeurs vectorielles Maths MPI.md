# 5 Fonctions a valeurs vectorielles Maths MPI

## Définition et caractérisation séquentielle de la continuité et des limites

### Déf - Limite

$\displaystyle \lim _{x \rightarrow a} f(x) = l$ si
$$\forall \varepsilon > 0, \begin{cases} \exists r > 0, \forall x \in B_f(a, r) \cap A, \lVert f(x) - l \rVert _F \leq \varepsilon \\ \exists \eta > 0, \forall x \in A, \lVert x - a \rVert _E < \eta \Rightarrow \lVert f(x) - l \rVert _F \leq \varepsilon \end{cases}$$

### Prop - Caractérisation séquentielle de la limite

$$\lim _{x \rightarrow a} f(x) = l \Leftrightarrow \forall (x_n)_n \in A^{\mathbb{N}}, x_n \rightarrow a, \lim _{n \rightarrow +\infty} f(x_n) = l$$

### Déf - Continuité

1. $f$ est continue en $a$ si $\lim _{x \rightarrow a} f(x) = f(a)$
2. $f$ est continue sur $A$ si elle est continue en tout point $a \in A$

### Prop - Caractérisation séquentielle de la continuité

$f$ est continue en $a \Leftrightarrow \forall (x_n)_n \in A^{\mathbb{N}}, x_n \rightarrow a \Rightarrow f(x_n) \rightarrow f(a)$

## Une fonction Lipschitzienne est continue

### Déf - Lipschitzienne

1. $f$ est $k$-Lipschitzienne si $\forall x, y \in A, \lVert f(x) - f(y) \rVert_F \leq k \lVert x - y \rVert_E$
2. $f$ est lipschitzienne si $\exists k \in \mathbb{R}_+$ tel que $f$ est $k$-Lipschitzienne

### Prop

$f$ lipschitzienne $\Rightarrow f\space \mathcal{C}^0$ sur $A$

## Équivalence entre la dérivabilité et l'existence d'un DL à l'ordre 1

### Déf - Application dérivable

1. $f$ est dérivable en $a$ si $\displaystyle \lim _{h \rightarrow 0, h\neq 0} \frac{f(a + h) - f(a)}{h}$ existe.
2. $f$ est dérivable sur $A$ si elle est dérivable en tout point $a \in A$

### Prop

$f$ dérivable en $a \Leftrightarrow f$ admet un DL à l'ordre 1 en $a$

$f(a + h) = f(a) + hf'(a) + \mathcal o(h)$

## Somme de Riemann et théorème associé

### Déf

$f$ continue ou continue par morceaux sur $[a, b]$

1. Somme de Riemann à gauche : $\displaystyle S_n(f) = \frac{b - a}{n} \sum _{k = 0}^{n - 1} f\left( a + \frac{k(b - a)}{n} \right)$
2. Si $a = 0, b = 1$, $\displaystyle S_n(f) = \frac 1 n \sum _{k = 0}^{n - 1} f\left( \frac k n \right)$

### Théorème

$$\lim _{n \rightarrow +\infty} S_n(f) = \int _a ^b f(t) \, dt$$

## Théorème de Rolle

Soit $f$ continue sur $[a, b]$ et dérivable sur $]a, b[$ et $f(a) = f(b)$ alors $\exists c \in ]a, b[, f'(c) = 0$

## EAF

$$\exists c \in ]a, b[, f'(c) = \frac{f(b) - f(a)}{b - a}$$

## IAF

Soient $m,M \in \mathbb{R} _+, m \leq f' \leq M$
$$\forall(x, y) \in I^2, m(x - y) \leq f(x) - f(y) \leq M(x - y)$$

## Formule de Taylor Young

$f \, \mathcal C ^n$, alors
$$\forall a,b \in I, f(b) = \displaystyle \sum _{k = 0} ^n \frac{(b-a)^k}{k!} f^{(k)}(a) + \mathcal o(\lvert b - a \rvert ^n)$$

## Formule de Taylor reste intégral

$f \, \mathcal C ^{n+1}$, alors
$$\forall a,b \in I, f(b) = \displaystyle \sum _{k = 0} ^n \frac{(b-a)^k}{k!} f^{(k)}(a) + \int _a ^b \frac{(b-t)^n}{n!} f^{(n+1)}(t) \, dt$$

## Définition d'un point adhérent à une partie. Caractérisation séquentielle

### Déf - Point adhérent à une partie

$a\in E$ est adhérent à $A$ si $\forall r > 0, B_f(a, r) \cap A \neq \emptyset$

### Prop - Caractérisation séquentielle

$a$ est adhérent à $A$ si $\exists (x_n)_n \in A^{\mathbb{N}}, x_n \rightarrow a$

## Dérivée de $L( f )$ où $L$ est une application linéaire continue

$$L(f)'(a) = L(f'(a))$$

## Dérivée de $B( f , g )$ où B est une application bilinéaire continue

$$B(f, g)'(a) = B(f'(a), g) + B(f, g'(a))$$

## Continuité de la fonction "distance à une partie $A$"

### Déf - Distance à une partie

$$d : \begin{cases} E \rightarrow \mathbb{R}_+ \\\displaystyle x \mapsto \inf _{a \in A} \lVert x - a \rVert \end{cases} $$

### Prop

$d$ est continue

### Démo

Mq $d$ est $1$-lip

## Inégalité arithmético-géométrique

Soient $(x_1, \ldots, x_n) \in \mathbb{R}^*_+$, alors:
$$(x_1 \times \ldots \times x_n)^{\frac 1 n} \leq \frac{x_1 + \ldots + x_n}{n}$$

### Démo

Inégalité de Jensen pour la fonction $\ln$

## Théorème de convergence des sommes de Riemann

$$\lim _{n \rightarrow +\infty} S_n(f) = \int _a ^b f(t) \, dt$$

## Majoration de l'erreur des sommes de Riemann en $\mathcal O( \frac 1 n )$

Soit $f \, \mathcal C ^1, (a_k)_k$ une subdivision regulière de $I$ d'ordre $n$. Alors, en notant $R_n(f) = \displaystyle \sum _{k = 0} ^{n-1} \frac {b-a}{n} f(a_k)$, on a:
$$R_n - \int _a ^b f(t) \, dt = \mathcal O \left( \frac 1 n \right)$$

## Majoration de l'erreur de la méthode des trapèzes en $\mathcal O( \frac 1 {n^2} )$ (avec la bonne hypothèse)

$T_n = \displaystyle \frac {b-a}{n} \sum _{k = 0} ^{n-1} \frac {f(a_k) + f(a_{k+1})}{2}$, alors:
$$T_n - \int _a ^b f(t) \, dt = \mathcal O \left( \frac 1 {n^2} \right)$$

## Adhérence de GLn (R) dans Mn (R)

$$\overline{GL_n(\mathbb{R})} = M_n(\mathbb{R})$$

## Inégalité de Jensen pour les fonctions convexes

Soit $f$ convexe, $(\lambda_1, \ldots, \lambda_n) \in [0, 1]^n, \sum \lambda_i = 1$ alors:
$$f\left( \sum_{i=1}^n \lambda_i x_i \right) \leq \sum_{i=1}^n \lambda_i f(x_i)$$

## Caractérisation des fonctions convexes par l'inégalité des pentes

$f$ est convexe $\Leftrightarrow \forall (x, y,z) \in I^3, x < y < z \Rightarrow \frac{f(y) - f(x)}{y - x} \leq \frac{f(z) - f(x)}{z - x} \leq \frac{f(z) - f(y)}{z - y}$
