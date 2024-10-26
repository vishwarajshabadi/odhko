# 5 Champ Gravitationnel Physique MPI

$\vec{G}(M)$ : champ gravitationnel rayonné en un point $M$. Par construction, ne dépend que de sa source et non de l'objet situé en $M$.

C'est un champ de gradient $\Rightarrow$ existence d'un champ scalaire, le potentiel gravitationnel $V$

Pour une masse ponctuelle $m$ située en $M$ où règne un champ gravitationnel :

$$\begin{cases} 
\vec{F} = m\vec{G} \\
E_p = mV
\end{cases} \Leftrightarrow \begin{cases}
\vec{F} = -\vec{\text{grad}}(E_p) \\
\vec{G} = -\vec{\text{grad}}(V)
\end{cases}$$

### Théorème de Gauss

Soit $S$ une surface fermée quelconque et $M_{int}$ la masse totale contenue dedans :

$$\oiint_S \vec{G}\cdot\text{d}\vec{S} = -4\pi\mathcal{G}M_{int}$$

Universellement vrai, quelle que soit la forme de $S$. Mais réellement pratique pour calculer $\vec{G}$ seulement dans les cas « riches en symétries », typiquement quand on peut ramener $\vec{G}(M)$ à un vecteur à une seule composante et ne dépendant que d'une seule variable.

1. Analyse des invariances et des symétries pour simplifier l'expression de $\vec{G}(M)$.
2. Choix de la surface de Gauss pour que $\vec{G}\cdot\text{d}\vec{S}$ soit trivial à calculer ($\vec{G}$ et $\text{d}\vec{S}$ colinéaires ou perpendiculaires entre eux).
3. Calcul du flux de $\vec{G}$ à travers $S$.
4. Calcul de la masse intérieure, contenue dans $S$.
5. Application du théorème de Gauss pour en déduire $\vec{G}$.

### Potentiel gravitationnel

Une fois $\vec{G}$ calculé, on en déduit $V$ en inversant le gradient. Les constantes apparaissant lors des primitivations sont fixées si possible par :
* annulation du potentiel à grande distance de la source,
* raccordement par continuité du potentiel
