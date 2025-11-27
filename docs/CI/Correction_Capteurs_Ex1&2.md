
## Capteurs de la chaine d'acquisition

Lire le cours et faire les exercices concernant [Les capteurs et la chaîne d'acquisition](./Acquisition_Capteurs-Cours-Exercices.pdf){target="_blank"} ressource [Capteur_US-HC-SR04.pdf](./Capteur_US-HC-SR04.pdf){target="_blank"} ;

### Exercice 1

1. Le **mesurande** m (la grandeur à mesurer) est ici la **présence ou pas d'un aimant** à proximité du capteur ILS obtenue lorsque la pédale droite est en position basse.
La grandeur de sortie s est un **signal électrique** (de tension nulle si le circuit est ouvert, ou de tension maximale si le circuit est fermé).
2. C'est un capteur **logique** (TOR, Tout Ou Rien).
3. Ce capteur en **passif** (c'est un récepteur, il n'est pas générateur)


### Exercice 2

1. La loi des noeuds permet d'écrire : $i_e = i_s + i_2$
or ici $i_s = 0$ donc $i_e = i_2$

2. La loi d'Ohm permet d'écrire : $v_s = R_2 \times i_2$
or ici $i_e = i_2$ donc $v_s = R_2 \times i_e$

3. La loi des mailles permet d'écrire : $v_e = R_1 \times i_e +  R_2 \times i_2$
or ici $i_e = i_2$ donc $v_e = R_1 \times i_e +  R_2 \times i_e= (R_1 +  R_2) \times i_e$

4. On a donc $i_e = {v_s \over R_2} = {v_e \over R_1 + R_2}$
soit donc la relation d'un pont diviseur de tension : $v_s = {R_2 \over R_1 +  R_2} \times v_e $

5. La relation devient pour ce potentiomètre $v_s = {R_{AB} \over R_{AB} +  R_{BC}} \times v_e = {R_{AB} \over R_{AC}} \times v_e$

Pour $v_e = 3,3\;\mathrm{V}$ et $R_{AC} = 10\;\mathrm{k\Omega}$, on obtient les valeurs de tension en sortie :

| $R_{AB}$ | $100\;\mathrm{\Omega}$ | $4,5\;\mathrm{k\Omega}$ | $10\;\mathrm{k\Omega}$ |
| :---: | :---: | :---: | :---: |
| $v_s$         |      $0,033 \;\mathrm{V}$         |   $1,485 \;\mathrm{V}$             |   $3,3 \;\mathrm{V}$            |

6. Après une conversion analogique numérique (CAN) de résolution $n = 10 \;\mathrm{bits}$

$N_{\mathrm{décimal}} = v_s \times {1 \over q} = v_s \times {2^n -1 \over v_e} = v_s \times {1023 \over 3,3} $

Avec le quantum, la plus petite tension discriminable, $q = {v_e \over 2^n -1}$

On obtient les valeurs numériques N image de la tension de sortie :

| $R_{AB}$               | $100\;\mathrm{\Omega}$ | $4,5\;\mathrm{k\Omega}$ | $10\;\mathrm{k\Omega}$ |
| :---: | :---: | :---: | :---: |
| $N_{\mathrm{décimal}}$ | $1$                    | $461$                   | $1023$                 |
| $N_{\mathrm{binaire}}$ | `00 0000 0001`         | `01 1100 1101`          | `11 1111 1111`         |

***


