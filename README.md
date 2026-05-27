# Cartographie-arbovirus

# Modélisation de niche écologique et cartographie de risque d'un arbovirus en Europe

Ce projet présente une analyse de distribution spatiale pour un arbovirus émergent (type virus du Nil occidental) récemment établi sur le continent européen, basée sur 150 enregistrements de présence simulés.

## Contenu du dépôt
* **data/** : occurrences de l'arbovirus (WGS84), variables environnementales raster (ISIMIP) et masque d'étude européen [4].
* **scripts/** : script R principal incluant la préparation des données, l'entraînement des modèles BRT et la validation croisée [6].
* **results/** : cartographies d'adéquation écologique (moyenne et écart-type), analyse de l'importance relative (RI) et courbes de réponse [5].

## Méthodes utilisées
* **Modélisation de niche (ENM)** : Algorithme de Machine Learning "Boosted Regression Trees" (BRT) avec 30 réplicats pour gérer la stochasticité [4].
* **Validation croisée spatiale** : Utilisation du package `blockCV` avec des blocs hexagonaux de 1 250 km pour neutraliser l'autocorrélation spatiale [5].
* **Métriques de performance** : Évaluation via l'AUC (Area Under the Curve) et l'indice de Sørensen (SIppc) [5].
* **Environnement** : Analyses réalisées sous R version 4.4.2 avec les packages `dismo`, `gbm` et `blockCV`.

## Auteurs
* **Kindi BALDÉ** (Matricule : XXXXXX) [7]
* **Elise GEERTS** (Matricule : 000617159)
* Université Libre de Bruxelles - Cours BING-F432
