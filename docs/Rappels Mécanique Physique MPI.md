# Rappels Mécanique Physique MPI

## Forces usuelles (expression, W, Ep)

- Force gravitationnelle, poids
- Réaction normale de support
- Rappel élastique
- Couple de torsion
- Force électrostatique de Coulomb
- Tension de fil
- Couple de Laplace d'un champ mag. uniforme sur dipôle
- Frottements fluides linéaires
- Force de Lorentz
- Poussée d'Archimède

## Théorèmes fondamentaux

### PFD

$\frac{d}{dt}(m\vec{v}) = \sum_i \vec{F_i}$

### Moment d'une force

$\vec{M_A}(\vec{F}) = \vec{AP} \wedge \vec{F}$
$\vec{M_\Delta}(\vec{F}) = \vec{M_A}(\vec{F})\cdot\vec{u_\Delta}$

### Moment cinétique

$\vec{L_A} = \vec{AM} \wedge m\vec{v}$
$L_\Delta = J\omega$

### TMC

$\frac{d}{dt}(\vec{L_A}) = \sum_i \vec{M_A}(\vec{F_i})$

## Énergie

### Énergie potentielle

$\vec{F} = -\vec{\text{grad}}(E_p)$

### Puissance

$P(\vec{F}) = \vec{F}\cdot\vec{v} = -\frac{dE_p}{dt}$

### Travail

$W_{t1\rightarrow t2}(\vec{F}) = \int_{t1}^{t2} P(\vec{F})dt = -\Delta_{[t2,t1]}E_p$

### Énergie cinétique

$E_c = \frac{1}{2}m\vec{v}^2 = \frac{1}{2}J\omega^2 = \frac{1}{2}m\vec{v}(G)^2 + \frac{1}{2}J\omega^2$

## Théorèmes énergétiques

### TPC

$\frac{dE_c}{dt} = \sum_i P(\vec{F_i})$

### TEC

$\Delta E_c = \sum_i W(\vec{F_i})$

### TPM

$\frac{dE_m}{dt} = \sum_{i,nc} P(\vec{F_{i,nc}})$

### TEM

$\Delta E_m = \sum_{i,nc} W(\vec{F_{i,nc}})$

## Lois de Kepler

1. La planète décrit une trajectoire elliptique dont l'étoile est un foyer
2. $C = r^2\dot{\theta} = \text{cte}$
3. $\frac{T^2}{a^3} = \frac{4\pi^2}{GMT} = \text{cte}$
