# 7 Suites et Séries de fonctions Maths MPI

## Définition de la convergence simple, uniforme et normale d'une suite de fonctions

### Déf - CVS

$(f_n)_n$ CVS vers $f$ si $$\forall x \in I, \lim _{n \rightarrow +\infty} \lVert f_n(x) - f(x) \rVert _E = 0$$

### Déf - CVU

$(f_n)_n$ CVU vers $f$ si $$\lim _{n \rightarrow +\infty} \lVert f_n - f \rVert _{\infty} = 0$$

### Déf - CVN

$(f_n)_n$ CVN vers $f$ si $$\lim _{n \rightarrow +\infty} \lVert f_n - f \rVert _1 = 0$$

## La convergence uniforme d'une suite de fonctions implique la convergence simple

$$(f_n)_n \text{ CVU vers } f \Rightarrow (f_n)_n \text{ CVS vers } f$$

## Théorème de continuité pour les suites de fonctions

Si

- $\forall n, f_n$ est continue sur $I$
- $(f_n)_n$ CVU vers $f$ sur $I$

Alors

- $f$ est continue sur $I$

## Théorème de la double limite pour les suites de fonctions

Si

- $\forall n, f_n$ admet une limite en $a$ notée $l_n$
- $(f_n)_n$ CVU vers $f$ sur $I$

Alors

- $(l_n)_n$ converge vers l \in \mathbb{R}
- $\displaystyle \lim _{x \rightarrow a} f(x) = \lim _{n \rightarrow +\infty} l_n = l$ ie $\displaystyle \lim _{x \rightarrow a} \left( \lim _{n \rightarrow +\infty} f_n(x) \right) = \lim _{n \rightarrow +\infty} \left( \lim _{x \rightarrow a} f_n(x) \right)$

## Théorème d'intégration sur un segment des suites de fonctions

Si

- $\forall n, f_n$ est continue sur $I$
- $(f_n)_n$ CVU vers $f$ sur $I$

Alors

- $f$ est continue sur $I$
- $\displaystyle \lim _{n \rightarrow +\infty} \int _a ^b f_n(t) \, dt = \int _a ^b f(t) \, dt$

## Théorème de " dérivation " des suites de fonctions

Si

- $\forall n, f_n$ est $\mathcal{C}^1$ sur $I$
- $(f_n)_n$ CVS vers $f$ sur $I$
- $(f_n')_n$ CVU vers $g$ sur $I$

Alors

- $f$ est $\mathcal{C}^1$ sur $I$
- $f' = g$
- $\forall [a, b] \subset I, (f_n)_n$ CVU vers $f$ sur $[a, b]$

## Définition de la convergence simple, uniforme et normale d'une série de fonctions

### Déf - CVS

$\sum f_n$ CVS si $\forall x \in I, \sum f_n(x)$ CVS

### Déf - CVU

Notons $\displaystyle S: x \mapsto \sum f_n(x)$ et $S_N: x \mapsto \sum _{n=0} ^N f_n(x)$
$\sum f_n$ CVU si : $(S_N)_N$ CVU vers $S$ sur $I$
ssi $(R_N)_N$ CVU vers 0 sur $I$

### Déf - CVN

$\sum f_n$ CVN si

- $\forall n, f_n$ est bornée sur $I$
- $\sum \lVert f_n \rVert _{\infty}$ CV

## Théorème de continuité pour les séries de fonctions

Si

- $\forall n, f_n$ est continue sur $I$
- $\sum f_n$ CVU sur $I$

Alors

- $S$ est continue sur $I$

## Théorème de la double limite pour les séries de fonctions

Si

- $\forall n, f_n$ admet une limite en $a$ notée $l_n \in E$
- $\sum f_n$ CVU sur $I$

Alors

- $\sum l_n$ converge
- $\displaystyle \lim _{x \rightarrow a} S(x) = \sum l_n$ ie $\displaystyle \lim _{x \rightarrow a} \left( \sum_{n=0} ^{+\infty} f_n(x) \right) = \sum_{n=0} ^{+\infty} \left( \lim _{x \rightarrow a} f_n(x) \right)$

## Théorème d'intégration sur un segment pour les séries de fonctions

Si

- $\forall n, f_n$ est continue sur $I$
- $\sum f_n$ CVU sur $I$

Alors

- $S$ est continue sur $I$
- $\displaystyle \int _a ^b S(x) \, dx = \sum \int _a ^b f_n(x) \, dx$

## Théorème de " dérivation " pour les séries de fonctions

Si

- $\forall n, f_n$ est $\mathcal{C}^1$ sur $I$
- $\sum f_n$ CVS sur $I$
- $\sum f_n'$ CVU sur $I$

Alors

- $S$ est $\mathcal{C}^1$ sur $I$
- $\forall x \in I, S'(x) = \sum f_n'(x)$

## Théorème d'approximation uniforme des fonctions continues par des fonctions en escalier sur un segment

Toute fonction continue sur un segment peut être approximée uniformément par des fonctions en escalier
ie (séquentiellement)
$$\forall f \in \mathcal{C}^0(I, \mathbb{K}), \exists (g_n)_n \in \mathcal{E}(I, \mathbb{K})^{(\mathbb{N})}, (f_n)_n \text{ CVU vers } f \text{ sur } I$$
ou
$$\forall f \in \mathcal{C}^0(I, \mathbb{K}), \forall \varepsilon > 0, \exists g \in \mathcal{E}(I, \mathbb{K}), \lVert f - g \rVert _{\infty} \leq \varepsilon$$

## Théorème de Weierstrass

Toute fonction continue sur un segment peut être approximée uniformément par des fonctions polynomiales.

ie (séquentiellement)
$$\forall f \in \mathcal{C}^0(I, \mathbb{K}), \exists (P_n)_n \in \mathbb{K}[X]^{(\mathbb{N})}, (P_n)_n \text{ CVU vers } f \text{ sur } I$$
ou
$$\forall f \in \mathcal{C}^0(I, \mathbb{K}), \exists P _\varepsilon \in \mathbb{K}[X], \lVert f - P _\varepsilon \rVert _{\infty} \leq \varepsilon$$

## Théorème de " primitivation " des suites de fonctions sur un segment

Si

- $\forall n, f_n$ est continue sur $I$
- $(f_n)_n$ CVU vers $f$ sur $I$

Alors

- $f$ est continue sur $I$
- $(F_n)_n$ CVU vers $F$ sur $I$ où $F_n:x\mapsto \int _a ^x f_n(t) \, dt$ et $F:x\mapsto \int _a ^x f(t) \, dt$

## Pour une série de fonctions, CVN $\Rightarrow$ CVU $\Rightarrow$ CVS

$$\sum f_n \text{ CVN} \Rightarrow \sum f_n \text{ CVU} \Rightarrow \sum f_n \text{ CVS}$$

## Extension $C^k$ du théorème de " dérivation "(séries de fonctions)

Si

- $\forall n, f_n$ est $\mathcal{C}^k$ sur $I$
- $\forall p \in \llbracket 0, k-1 \rrbracket , \sum f_n^{(p)}$ CVS sur $I$
- $\sum f_n^{(k)}$ CVU sur $I$

Alors

- $S$ est $\mathcal{C}^k$ sur $I$
- $\forall p \in \llbracket 0, k \rrbracket, S^{(p)}(x)= \sum f_n^{(p)}(x)$

## Équivalent de zêta au voisinage de 1+ à l'aide d'une comparaison intégrale

### Déf - Zêta

$$\zeta(s) = \sum _{n=1} ^{+\infty} \frac 1 {n^s}$$

### Prop

$$\zeta(s) \sim _{1^+} \frac 1 {s-1}$$

## Limite de zêta en 1+

$$\lim _{s \rightarrow 1^+} \zeta(s) = +\infty$$

## La fonction zêta est log-convexe

$\log \circ \zeta$ est convexe
