# 2 Changement de Réferentiel Physique MPI

## Référentiel

Un référentiel est défini par (horloge sous-entendue) :

- trois axes formant un trièdre orthogonal et fixes les uns par rapport aux autres,
- un point fixe par rapport au trièdre (appelé origine)

| Mouvement   | Description                                                            | Grandeur                  |
| ----------- | ---------------------------------------------------------------------- | ------------------------- |
| Translation | Déplacement de $O'$ dans $\mathcal{R}$                                 | $\vec{v}(O')_\mathcal{R}$ |
| Rotation    | Changement d'orientation des axes de $\mathcal{R}'$ dans $\mathcal{R}$ | $\vec{\Omega}$            |

$\vec{\Omega} = \vec{0}$ : translation pure
$\vec{v}(O')_\mathcal{R} = \vec{0}$ et $\vec{\Omega} = \text{cst}$ : rotation pure uniforme

## Lois de composition

$$\vec{v}(M)_\mathcal{R} = \vec{v}(M)_{\mathcal{R}'} + \vec{v_e}$$
$$\vec{a}(M)_\mathcal{R} = \vec{a}(M)_{\mathcal{R}'} + \vec{a_e} + \vec{a_c}$$

Accélération de Coriolis : $\vec{a_c} = 2\vec{\Omega} \wedge \vec{v}(M)_{\mathcal{R}'}$

## Vitesse et accélération d'entraînement

|                        | $\vec{v_e}$                     | $\vec{a_e}$               | Remarques                                                         |
| ---------------------- | ------------------------------- | ------------------------- | ----------------------------------------------------------------- |
| Translation pure       | $\vec{v}(O')_\mathcal{R}$       | $\vec{a}(O')_\mathcal{R}$ |                                                                   |
| Rotation pure uniforme | $\vec{\Omega} \wedge \vec{O'M}$ | $-\omega^2\vec{HM}$       | $H$ projeté de $M$ sur l'axe, $\omega = \lVert\vec{\Omega}\rVert$ |
