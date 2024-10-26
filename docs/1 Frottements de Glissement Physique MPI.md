# 1 Frottements de Glissement Physique MPI

## Actions de contact

Réaction du support : $\vec{R} = \vec{N} + \vec{T}$
Composante normale : $\vec{N}$ (direction fixe)
Composante tangentielle : $\vec{T}$ (dans le plan)

## Lois de Coulomb

Vitesse de glissement : $\vec{v_g} = \vec{v}(I \in \text{solide}) - \vec{v}(I \in \text{support})$

| | Régime de glissement | Régime de non-glissement / adhérence |
|------|----------------|-------------------------------------|
| **Caractérisation** | $\vec{v_g} \neq \vec{0}$ | $\vec{v_g} = \vec{0}$ |
| **Force de frottement**| $\begin{cases} \vec T \propto \vec{v_g} \\ \vec T \cdot \vec{v_g} < 0 \\ \lVert \vec T\rVert = f\lVert\vec{N}\rVert \end{cases}$ | $\lVert \vec T \lVert < f\lVert\vec{N}\rVert$ |

Puissance de la force de frottement :
$$\mathcal{P} = \vec T \cdot \vec{v_g} \Rightarrow \begin{cases} < 0 \text{ si glissement (dissipatif)} \\ 0 \text{ si non-glissement} \end{cases}$$

## Méthodologie

| |Régime de glissement | Régime de non-glissement / adhérence |
|--|--------------------|-------------------------------------|
| **Pour le calcul** (égalité) |$\lVert \vec T\rVert = f\lVert\vec{N}\rVert$ | $\vec{v_g} = \vec{0}$ |
| **Valable tant que** (inégalité) |$\vec{v_g} \neq \vec{0}$ | $\lVert \vec T\rVert < f\lVert\vec{N}\rVert$ |

1. Identifier ou postuler le régime (glissement ou non-glissement).
2. Faire l'étude mécanique avec la ligne " Pour le calcul ".
3. Formuler la condition de validité avec la ligne " Valable tant que ".
4. Discuter un éventuel changement de régime.
