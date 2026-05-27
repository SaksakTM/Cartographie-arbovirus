# Cartographie-arbovirus

# Modélisation de niche écologique et cartographie de risque d'un arbovirus en Europe

Ce projet présente une analyse de distribution spatiale pour un arbovirus émergent récemment établi sur le continent européen, basée sur 150 enregistrements géocodés de présence simulés.

## Contenu du dépôt
* **data/** : occurrences de l'arbovirus (WGS84), variables environnementales raster (ISIMIP) et masque d'étude européen.
* **scripts/** : script R principal incluant la préparation des données, l'entraînement des modèles BRT et la validation croisée.
* **results/** : cartographies d'adéquation écologique (moyenne et écart-type), analyse de l'importance relative (RI) et courbes de réponse.

## Méthodes utilisées
* **Modélisation de niche (ENM)** : Algorithme de machine-learning "Boosted Regression Trees" (BRT) avec 30 réplicats pour gérer la stochasticité.
* **Validation croisée spatiale** : Utilisation du package `blockCV` avec des blocs hexagonaux de 1 250 km pour neutraliser l'autocorrélation spatiale.
* **Métriques de performance** : Évaluation via l'AUC (Area Under the Curve) et l'indice de Sørensen (SIppc).

## Installation et Dépendances
Pour exécuter les analyses de ce dépôt, vous devez disposer de **R (version 4.4.2 ou supérieure)**. 
Les bibliothèques suivantes ont été utilisées et peuvent être installées via le script principal :

### Manipulation de données spatiales (SIG)
* **raster** : Gestion des couches environnementales (grilles).
* **sp** & **sf** : Manipulation des objets vectoriels et des coordonnées (WGS84).

### Modélisation et Statistiques
* **dismo** & **gbm** : Implémentation des Boosted Regression Trees (BRT).
* **blockCV** : Génération des plis (folds) pour la cross-validation spatiale.
* **ncf** : Analyse de l'autocorrélation spatiale (corrélogrammes).

### Visualisation
* **RColorBrewer** : Échelles de couleurs divergentes pour les cartes de risque.

## Autrices
* **Kindi BALDÉ** (Matricule : XXXXXX)
* **Elise GEERTS** (Matricule : 000617159)


Université Libre de Bruxelles - Cours BING-F432 - "Introduction à l'épidémiologie spatiale et moléculaire"
