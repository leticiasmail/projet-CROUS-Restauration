# Projet CROUS – Analyse des services de restauration

Projet d'analyse des services de restauration du CROUS de Lille.

## Objectifs du projet

- Explorer l’offre de restauration CROUS dans la région de Lille
- Analyser la répartition géographique des établissements
- Étudier les types de structures (restaurants, cafétérias)
- Identifier des pistes d’amélioration pour les étudiants

## Outils

- Python
- Pandas
- Matplotlib
- Jupyter Notebook
  
## Données
- Source : [data.enseignementsup-recherche.gouv.fr](https://data.enseignementsup-recherche.gouv.fr)  
- Format : fichier Excel (.xlsx)  
- Colonnes principales utilisées :  
  - `title` : nom du service  
  - `zone` : localisation / campus  
  - `type` : type de service (restaurant, cafétéria)  
  - `opening` / `closing` : horaires d’ouverture et fermeture (simplifiés pour l’analyse)  
  - `lat` / `lon` : coordonnées géographiques  

## Introduction

J’ai décidé de réaliser ce projet par curiosité personnelle, mais aussi par expérience vécue.
En tant qu’étudiante étrangère, le CROUS me paraissait au départ assez abstrait : je pensais qu’il se limitait principalement au logement étudiant.

En arrivant en France, et notamment en étant moi-même logée dans une résidence CROUS, j’ai progressivement découvert que cette organisation publique jouait un rôle bien plus large dans la vie étudiante. Au-delà du logement, le CROUS propose de nombreux services essentiels, notamment dans le domaine de la restauration universitaire.

Étant étudiante à l’Université de Lille, et ayant régulièrement fréquenté les restaurants et cafétérias du CROUS, il m’a semblé pertinent d’étudier plus en profondeur l’offre de restauration étudiante dans cette zone. Ce sujet m’a particulièrement intéressée car il touche directement au quotidien des étudiants, en termes d’accessibilité, de localisation et de services proposés.

À travers ce projet, j’ai analysé les données de la restauration CROUS afin de mieux comprendre la répartition des établissements, leurs types et certaines de leurs caractéristiques. Cette étude m’a permis de mettre en évidence plusieurs éléments pertinents, mais aussi d’identifier des axes d’amélioration et d’optimisation possibles pour renforcer l’utilité de ces services auprès des étudiants.

## Analyse realiser avec pandas

1. Chargement et exploration des données :  
   - Lecture du fichier Excel avec Pandas  
   - Visualisation des premières lignes (`df.head()`) et des colonnes disponibles (`df.columns`)  
2. Sélection des colonnes pertinentes pour l’analyse : `title`, `zone`, `type`, `opening`, `closing`, `lat`, `lon`  
3. Filtrage pour ne garder que les zones de Lille et Valenciennes  
4. Analyse descriptive :  
   - Répartition des services par zone  
   - Types de services disponibles (restaurants et cafétérias)  
   - Vérification des colonnes vides et des doublons  
   - Étude des horaires d’ouverture (simplifiés)  
   - Exploration des coordonnées géographiques  
  
## Visualisation avec Matplotlib

- Répartition des services par type (restaurant vs cafétéria) – **pie chart**  
- Répartition des services par zone – **pie chart**  
- Nombre de services par zone – **bar chart**  
- Localisation des services CROUS à Lille – **scatter plot**

## Observations

- Les données de description des services (`short_desc`) sont vides  
- Les horaires étaient initialement codés en binaire, ce qui a compliqué la réalisation de graphiques  
- Il n’y a que deux types de services dans les données : restaurants et cafétérias  
- Cette analyse met en évidence la répartition géographique et le nombre de services disponibles pour les étudiants  

## Perspectives d’amélioration

- Ajouter les services manquants ou les food trucks pour compléter la base de données, ce qui permettrait d’avoir une meilleure vue d’ensemble sur tous les services proposés  
- Créer un outil interactif pour que les étudiants puissent trouver rapidement un service CROUS près d’eux  
- Visualiser les services sur une carte interactive pour mieux comprendre leur répartition

## Conclusion

Ce projet m’a permis de mieux comprendre l’offre de restauration du CROUS dans la région de Lille et Valenciennes. Grâce à l’exploration des données et à la visualisation, j’ai pu :

- Identifier les zones et types de services disponibles pour les étudiants
- Analyser la répartition géographique des établissements
- Observer les horaires d’ouverture et constater certaines limites des données (absence de descriptions, codage binaire des horaires, types limités)

Au-delà des résultats, ce projet a surtout été un **exercice d’apprentissage concret** :  

- Comprendre comment manipuler des fichiers Excel avec **Pandas**
- Filtrer et nettoyer les données pour ne garder que ce qui est pertinent
- Visualiser les informations avec **Matplotlib** pour rendre les données compréhensibles

Même si je ne maîtrise pas encore parfaitement le code, j’ai appris à **penser comme un data analyst** : réfléchir aux données dont on a besoin, savoir les représenter, et tirer des conclusions utiles. Ce projet m’a aussi donné des idées pour aller plus loin, comme créer un outil interactif pour les étudiants ou enrichir la base de données avec des services manquants.

En résumé, l’expérience acquise et la compréhension des données sont bien plus précieuses que le simple fait de savoir générer du code de A à Z. L’essentiel est d’avoir appris à **observer, analyser et interpréter les données** pour en tirer un enseignement concret.
