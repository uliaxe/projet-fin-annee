# Projet de Fin d'Année - Analyse des Données de Sécurité Routière

## 🎯 Vue d'Ensemble

Ce projet de fin d'année présente une analyse complète des données de sécurité routière en France, avec un focus particulier sur les zones urbaines et leurs spécificités en matière d'accidents de la route.

## 🗺️ Analyses Régionales

### 🏙️ Bordeaux Métropole

**[📖 Voir l'analyse détaillée](./Bordeaux/Readme_BDX.md)**

Analyse approfondie des dangers routiers à Bordeaux avec :

- Croisement des données de trafic et d'accidents 2023
- Création d'un score de dangerosité pondéré
- Identification des rues les plus à risque
- Analyse des facteurs temporels et météorologiques

**Fichiers :** `danger_bordeaux.ipynb` | [Requirements](./Bordeaux/requirements.txt)

### 🇫🇷 France Nationale

**[📖 Voir l'analyse nationale](./France/Readme_FR.md)**

Analyse des tendances nationales de sécurité routière en France :

- Évolution des accidents sur le territoire français
- Comparaisons inter-régionales
- Facteurs de risque à l'échelle nationale

## 🚀 Démarrage Rapide

### Prérequis

- Python 3.8+
- Jupyter Notebook ou Jupyter Lab

### Installation

1. **Cloner le projet**

   ```bash
   git clone <url-du-repo>
   cd projet-fin-annee
   ```

2. **Installer les dépendances pour Bordeaux**

   ```bash
   cd Bordeaux
   pip install -r requirements.txt
   ```

3. **Lancer l'analyse**

   ```bash
   jupyter notebook danger_bordeaux.ipynb
   ```

## 📊 Données Utilisées

- **Sources officielles** : Open Data Bordeaux Métropole, données nationales
- **Période** : Année 2023 principalement
- **Types** : Données d'accidents, comptages de trafic, conditions météorologiques

## 🔍 Méthodologies

### Approche Bordeaux

- Score de dangerosité : `α × Trafic + β × Taux_Accidents`
- Analyse multifactorielle (temporelle, météo, infrastructure)
- Visualisations interactives et heatmaps

### Approche France

- Analyse de tendances nationales
- Comparaisons géographiques
- Études statistiques macro

## 📈 Résultats Clés

### 🎯 Bordeaux

- **Facteurs critiques** : Intersections, heures de pointe (7h-9h, 17h-20h)
- **Recommandations** : Amélioration signalisation et éclairage
- **Top 10** des rues les plus dangereuses identifiées

### 🌍 France

- **Évolution longitudinale** : Accidents par type de route (2005-2023)
- **Analyse démographique** : Répartition victimes par sexe et gravité
- **Impact de l'âge** : Vulnérabilité selon les tranches d'âge (0-17, 18-25, 26-40, 41-60, 61-80, 80+)
- **Contexte des déplacements** : Gravité selon les motifs de trajet
- **Données nationales** : Plus d'1 million de lignes analysées sur 18 ans

## Sources

[https://www.data.gouv.fr/datasets/base-de-donnees-accidents-corporels-de-la-circulation/](https://www.data.gouv.fr/datasets/base-de-donnees-accidents-corporels-de-la-circulation/)
[https://datahub.bordeaux-metropole.fr/explore/dataset/comptage-du-trafic-2023-bordeaux-metropole/information/](https://datahub.bordeaux-metropole.fr/explore/dataset/comptage-du-trafic-2023-bordeaux-metropole/information/)
