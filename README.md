# Étude dynamique du couple moteur de l’essuie-glace  
*Nissan Qashqai – Analyse du système amorti*  

**Auteurs :** Loubna Taleb, Zélie Besancenet  
**Date :** Mars 2025  

---

##  Contexte du projet
Ce projet s’inscrit dans le cadre d’une étude de modélisation et d’analyse dynamique appliquée à un système automobile : le mécanisme d’essuie-glace du **Nissan Qashqai**.  
L’objectif est de comprendre et de modéliser le comportement du couple moteur en tenant compte des effets d’inertie, d’élasticité et d’amortissement.

---

## Modélisation dynamique
Le système est modélisé à partir de la **deuxième loi de Newton pour la rotation** :



\[
J \ddot{\theta}(t) = C(t) - c \dot{\theta}(t) - k \theta(t)
\]



où :  
- \( J \) : moment d’inertie (kg·m²)  
- \( C(t) \) : couple moteur appliqué  
- \( c \) : coefficient d’amortissement visqueux  
- \( k \) : raideur équivalente des liaisons mécaniques  
- \( \theta(t) \) : angle de rotation  

L’équation normalisée devient :  



\[
\ddot{\theta}(t) + 2 \zeta \omega_0 \dot{\theta}(t) + \omega_0^2 \theta(t) = \frac{C(t)}{J}
\]



avec :  
- \( \omega_0 = \sqrt{\frac{k}{J}} \) : pulsation propre  
- \( \zeta = \frac{c}{2\sqrt{kJ}} \) : coefficient d’amortissement réduit  

---

##  Étude du système libre
Trois régimes sont possibles selon la valeur de \(\zeta\) :  

- **Sous-amorti (0 < ζ < 1)** : oscillations décroissantes  
- **Amortissement critique (ζ = 1)** : retour rapide sans oscillation  
- **Sur-amorti (ζ > 1)** : retour lent sans oscillation  

Les mesures expérimentales montrent des **oscillations amorties**, correspondant au cas **sous-amorti**.

---

##  Résultats et interprétation
- Le couple mesuré présente des oscillations décroissantes dans le temps.  
- Ces oscillations sont dues à :  
  - l’inertie au démarrage,  
  - la souplesse des liaisons mécaniques (tiges, bielles, paliers),  
  - les frottements et pertes mécaniques.  

Le modèle masse-ressort-amortisseur rend compte fidèlement du comportement observé.

---

##  Perspectives
- Validation expérimentale plus poussée avec différents profils de vitesse.  
- Optimisation des paramètres \(c\) et \(k\) pour améliorer la durée de vie et réduire le bruit du système.  
- Extension de l’étude à d’autres composants automobiles soumis à des sollicitations dynamiques.  

---
##  Technologies et outils
- **Python / Matlab** : résolution d’équations différentielles, simulation  
- **LaTeX / Markdown** : rédaction et documentation  
- **Capteurs de contrainte** : acquisition des signaux expérimentaux  


