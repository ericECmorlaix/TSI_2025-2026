
## Codeurs de position

Lire le [cours](./Codeur-Cours.pdf){target=_blank} et faire les [exercices](./Codeur-exercices.pdf){target=_blank} (cf : [document ressource détection mécanique et électronique](./Detection_mecanique_electronique.pdf){target=_blank}) ;

### Exercice 1

La $longueur = 3000 \;\mathrm{mm}$ ;
La $précision_{linéaire} = 1 \;\mathrm{mm}$

On aura donc ici besoin d'un nombre total d'impulsions : $$n_{impulsions_{total}} = {longueur \over précision_{linéaire}} = {3000 \over 1} = 3000$$

La $rayon_{rouleau} = 50 \;\mathrm{mm}$ ;

Alors le nombre de tours réalisés par le rouleau sera : $$n_{tours} = {longueur \over périmètre} = {3000 \over {2\pi \times rayon_{rouleau}}} = {3000 \over {2\pi \times 50}}= 9,55 \;\mathrm{trs} $$

Le nombre d'impulsions par tour est donc :

$$n_{impulsions_{/tour}} = {{n_{impulsions_{total}}} \over {n_{tours}}} = {{{longueur \over précision_{linéaire}}} \over {{longueur \over périmètre}}} = {{périmètre} \over {précision_{linéaire}}} = {{2\pi \times 50} \over 1} $$

Autre approche, selon la relation de transformation d'une rotation en translation :

La $précision_{linéaire} = rayon_{rouleau} \times précision_{angulaire}$

$$n_{impulsions_{/tour}} = {{angle_{/tour}} \over {précision_{angulaire}}} = {{angle_{/tour}} \over {{précision_{linéaire}} \over rayon_{rouleau} }}= {{2\pi} \over {1 \over 50}} = {{2\pi \times 50} \over 1} $$

La fréquence des signaux émis par le codeur est :

$$fréquence = {n_{impulsions/total} \over {durée}} = {n_{impulsions/total} \over {longueur \over vitesse}}= {1 \over période}$$ 

