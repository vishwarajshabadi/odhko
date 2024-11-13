# 2 Étude qualitative du champ électrostatique Physique MPI

## 2-3. Champ électrostatique et équation de Maxwell-Gauss

Force électrostatique subie par une charge ponctuelle placée en un point $M$ où règne un champ électrostatique :
$\vec{F} = q\vec{E}(M)$

| Distribution de charges | Caractérisée par                      | Unité      |
| ----------------------- | ------------------------------------- | ---------- |
| Ponctuelle              | charge $q$                            | C          |
| Linéique                | densité linéique de charge $\lambda$  | C m$^{-1}$ |
| Surfacique              | densité surfacique de charge $\sigma$ | C m$^{-2}$ |
| Volumique               | densité volumique de charge $\rho$    | C m$^{-3}$ |

Expression du champ électrostatique rayonné par une distribution de charges :

$\vec{E} = \begin{cases} 
\frac{q}{4\pi\varepsilon_0}\frac{1}{r^2}\vec{u_r} & \text{pour une source ponctuelle de charge }q \\
\text{théorème de Gauss} & \text{sinon}
\end{cases}$

L'équation de Maxwell-Gauss et le théorème de Gauss sont équivalents :

$\text{div}(\vec{E}) = \frac{\rho}{\varepsilon_0} \Leftrightarrow \oiint_S \vec{E}\cdot\text{d}\vec{S} = \frac{Q_{int}}{\varepsilon_0}$

Le théorème de Gauss n'est donc pas la seule méthode possible pour calculer $\vec{E}$, mais c'est souvent la plus pratique.

| En un point où se trouve une distribution... | $\vec{E}$ est...                  |
| -------------------------------------------- | --------------------------------- |
| volumique                                    | continu                           |
| surfacique                                   | discontinu 1$^{\text{re}}$ espèce |
| linéique / ponctuelle                        | discontinu 2$^{\text{e}}$ espèce  |

Dans le cas surfacique, la discontinuité est donnée par la relation de passage :

$\vec{E}(M_2) - \vec{E}(M_1) = \frac{\sigma}{\varepsilon_0}\vec{n}_{1\rightarrow2}$

### Méthodologie du théorème de Gauss pour calculer $\vec{E}$ :

1. Déterminer les invariances et symétries de la source, ce qui amène à introduire un point $M$ par lequel doivent passer les plans de symétrie et d'antisymétrie.
   Parfois cette étape s'accompagne d'une discussion sur la parité ou l'imparité du champ.

2. Choisir une surface de Gauss $S$ fermée, orientée sortante, passant par $M$ et telle que $\vec{E}\cdot\text{d}\vec{S}$ soit simple à exprimer en tout point.

3. Calculer le flux de $\vec{E}$ à travers $S$ et la charge intérieure à $S$.

4. Appliquer le théorème et conclure (graphe, continuité...)
