# Rappels Électronique Physique MPI

## Caractéristiques d'un dipôle

En convention récepteur
$u = Ri$
$u = C \frac{du}{dt}$
$u = L \frac{di}{dt}$

$\mathcal{P} = ui$

$i = \frac{dq}{dt}$
$i = C \frac{du}{dt}$

### Loi d'Ohm

$\underline u = \underline Z \underline i$ avec $\underline Z = \begin{cases} R \text{ résistance } \\ \frac{1}{i \omega C} \text{ condensateur } \\ i \omega L \text{ bobine} \end{cases}$

### Équivalences à très basse ou très haute fréquence

| Dipôle       | BF                  | HF                  |
| ------------ | ------------------- | ------------------- |
| Bobine       | fil                 | interrupteur ouvert |
| Condensateur | interrupteur ouvert | fil                 |

## Théorèmes généraux

### Ponts diviseurs

| Pont diviseur de … | Tension                         | Courant                         |
| ------------------ | ------------------------------- | ------------------------------- |
| Validité           | Montage série                   | Montage parallèle               |
| Formule            | $u_1 = \frac{Z_1}{Z_1 + Z_2} u$ | $i_1 = \frac{Z_2}{Z_1 + Z_2} i$ |

## Filtrage en régime harmonique

### Pulsation de coupure

$$\vert H(\omega_c) \vert = \frac{H_{\text{max}}}{\sqrt{2}}$$

### Bande passante à −3 dB

$$\vert H \vert \geq \frac{H_{\text{max}}}{\sqrt{2}}$$

### Comportement intégrateur ou dérivateur

$i\omega$ : dérivateur
$\frac{1}{i\omega}$ : intégrateur
